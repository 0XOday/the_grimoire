The `bootstap-servers command` can be used to prepare the new hosts that are being added to the system. This adds an entry to `/etc/hosts` for new hosts, and some services, such as RabbitMQ, requires entries to exist for all controllers on every controller. if using a `--limit` argument, ensure that all controllers are included

`kolla-ansible bootstrap-servers -i <inventory> [ --limit <limit> ]`

Note : Server instances are not automatically balanced onto the new compute nodes. So we need to live migrate server instances onto new hosts.  

`openstack server migrate <server> --live-migration --host <target host> --os-compute-api-version 2.30`

Note : The Watcher module can do live migration automatically  

## removing existing compute nodes 
When removing compute nodes from a system we have to consider the capacity to host the currently running workload, including overhead. 
It's recommended to migrate or destroy any instances they are hosting. 
For each host, disable the compute service to ensure that no new instances are scheduled to it

`openstack compute service set <host> nova-compute --disable`

live migration 
```
openstack server list --all-projects --host <host> -f value -c ID | while read server; do openstack server migrate --live-migration $server
done 
```

stop all services running on the hosts being removed:
```

```



#openstack
