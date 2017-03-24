# README

The start of a server on Linode.

## Set up SSH access
See [this Linode article](https://www.linode.com/docs/security/use-public-key-authentication-with-ssh#uploading-keys) for reference.

On the *remote* machine, ensure `.ssh` directory exists.
On the *local* machine, `scp ~/.ssh/id_rsa.pub root@xxx.xxx.xxx.xxx:/root/.ssh/uploaded_key.pub`
On the *remote* machine, `cat ~/.ssh/uploaded_key.pub >> ~/.ssh/authorized_keys`

## Using Ansible
With ad hoc commands, use the `-u root` flag in Ubuntu.

