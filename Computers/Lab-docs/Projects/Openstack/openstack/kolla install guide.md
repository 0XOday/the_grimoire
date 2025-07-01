`pip install git+https://opendev.org/openstack/kolla-ansible@stable/2024.1` works get odd depend errors with rocky 9.5 and 9.6 rocky 10 is not supported atm on 2025.2 

have to set up a lvm group for cinder-volumes Note we want to have this name because it is the default name 

`sudo vgcreate cinder-volumes /dev/sda /dev/sdb`

also grab ssh keys for both root and rosepaladin copy them over to both accounts Note we just ssh in ourself

edit the suborders file to disable sudo 


things we enabled in `etc/kolla/gloabls.yaml`


we have to init `source /path/to/venv/bin/activate` the virt environment 

have to install ansible-core via pip


```
enable_central_logging: "yes"

enable_cinder: "yes"

enable_cinder_backend_lvm: "yes"

network_interface: "ens18"

kolla_internal_vip_address: "192.168.129.2"

enable_neutron_provider_networks: "yes"

enable_skyline: "yes"





```