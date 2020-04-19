# README.md
Build a single node kubernetes 
  
## Prequisites
[Vagrant Setup](../README.md)

## TODO

## Build the VM 
```sh
vagrant plugin install vagrant-env 
echo "PASSWORD=$(uuidgen)" > .env 
```

### Configure Network
Avoid adding to home network to prevent bridging. 

### Data Folder
1. Create a data folder in the repo root.



## NOTES

### Adding for bionic
Tried to use the apt repository
curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add
https://stackoverflow.com/questions/53068337/unable-to-add-kubernetes-bionic-main-ubuntu-18-04-to-apt-repository
sudo apt-add-repository "deb http://apt.kubernetes.io/ kubernetes-yakkety main"
https://linuxconfig.org/how-to-install-kubernetes-on-ubuntu-18-04-bionic-beaver-linux
https://kubernetes.io/docs/setup/production-environment/tools/kubeadm/install-kubeadm/

sudo apt-get update && sudo apt-get install -y apt-transport-https curl
curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add -
cat <<EOF | sudo tee /etc/apt/sources.list.d/kubernetes.list
deb https://apt.kubernetes.io/ kubernetes-xenial main
EOF
sudo apt-get update
sudo apt-get install -y kubelet kubeadm kubectl

https://kubernetes.io/docs/reference/setup-tools/kubeadm/kubeadm/


kubeadm config images pull
sudo kubeadm init
sudo shutdown -r now  
