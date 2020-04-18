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

