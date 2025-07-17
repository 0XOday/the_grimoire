`pip install git+https://opendev.org/openstack/kolla-ansible@stable/2024.1` works get odd depend errors with rocky 9.5 and 9.6 rocky 10 is not supported atm on 2025.2 

have to set up a lvm group for cinder-volumes Note we want to have this name because it is the default name 

`sudo vgcreate cinder-volumes /dev/sda /dev/sdb`

also grab ssh keys for both root and rosepaladin copy them over to both accounts Note we just ssh in ourself

edit the suborders file to disable sudo 


things we enabled in `etc/kolla/gloabls.yaml`


we have to init `source /path/to/venv/bin/activate` the virt environment 

have to install ansible-core via pip

we want to also source admin-openrc.sh for our open stack creds 

```
enable_central_logging: "yes"

enable_cinder: "yes"

enable_cinder_backend_lvm: "yes"

network_interface: "ens18"

kolla_internal_vip_address: "192.168.129.2"

enable_neutron_provider_networks: "yes"

enable_skyline: "yes"





```

 TSing Notes : make sure you are using the VIP if you are experiencing image upload fails and or strange daemonic errors .   


`openstack network create --share -external --provider-physical-network physnet1 --provider-network-type flat whatever-you-want-to-call-it`

open search 


neutron_external_interface: "enp1s0f1np.1011"


Fat oneliner

```
 kolla-ansible destroy -i multinode --yes-i-really-really-mean-it; kolla-ansible bootstrap-server -i multinode; kolla-ansible prechecks -i multinode; kolla-ansible deploy -i multinode; kolla-ansible post-deploy -i multinode; source /etc/kolla/admin-openrc.sh; openstack network create --share --external --provider-physical-network physnet1 --provider-network-type flat provider; openstack subnet create  openstack volume type create Nimble-Cinder; openstack volume type set --property volume_backend_name=Nimble-Cinder Nimble-Cinder; cat /etc/kolla/admin-openrc.sh; openstack zone create --email woof@paladin.labs paladin.labs.; openstack network create --dns-domain paladin.labs. internal; openstack subnet create --allocation-pool start=55.0.0.10,end=55.0.0.250 --network internal --subnet-range 55.0.0.0/24 --dns-publish-fixed-ip internal-subnet; openstack router create sdn-router; openstack router add subnet sdn-router internal; openstack router set --external-gateway public sdn-router; openstack flavor create --public m1.tiny --id auto--ram 2048 --disk 0 --vcpus 2 


```

