# ceph

working 3 node cluster with 1 osd per node with persistent volumes for storage in ceph

Create `.vaultpassword` file with "sam" in it and `~/secrets/local.password` and use `make decrypt` and `make encrypt` to decrypt ansible vault and encrypt.

# install

```
vagrant plugin install vagrant-persistent-storage
vagrant up
vagrant provision
```
