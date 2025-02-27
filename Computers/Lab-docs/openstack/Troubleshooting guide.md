``kolla-ansible destroy -i <<inventory-file>>``
if a failure in a bootstrap task occurs, a further deploy action will not correct the problem. In this scenario, Kolla’s behavior is undefined.

This command is to recover from a deployment failure is to remove the failed deployment