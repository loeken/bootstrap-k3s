###

# test connection to nodes

ansible -i inventory k3s -m ping

# simple way to bootstrap k3s cluster

it expects 3 ( or more ) vms/servers with the user {{ ansible_user }} ( specified in inventory ) configured and sudo permissions for this user to execute commands ( without password )

this does no checking but it ll output the exeuction of k3sup so if something goes wrong you should be able to see and act upon this


# execute playbook:

ansible -i inventory playbook.yml