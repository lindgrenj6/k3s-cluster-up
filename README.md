# k3s-cluster-up

#### Small ansible script to get k3s up and running in a clustered configuration.

### Requirements
- ansible
- some computers (preferably more than one, otherwise this is really boring)

### How to run:

1) edit the `inventory.ini` to set up your master node(s) and slave node(s)
2) `ansible-playbook -i inventory.init deploy.cluster.yml` 

After thinking a bit you'll have a super fresh cluster available! Get the kubeconfig from the master node, it is at `/etc/rancher/k3s/k3s.yaml` on the master node.

Edit the config to point at the master IP and you can then access the cluster from any machine. 
