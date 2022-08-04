# ceph

working 3 node cluster with 1 osd per node with persistent volumes for storage in ceph

Create `.vaultpassword` file with "sam" in it and `~/secrets/local.password` and use `make decrypt` and `make encrypt` to decrypt ansible vault and encrypt.

# install

```
vagrant plugin install vagrant-persistent-storage
vagrant up
vagrant provision
```

You might get intermittent failures with `Mount cephfs`, I just `vagrant provision` again and it fixes it.

Go to `/srv/ceph` and try create a file, then `vagrant ssh storage02` or `vagrant ssh storage03` and you'll see the file in both places.
