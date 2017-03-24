# README

The start of a server on Linode.

## Set up Ansible hosts
On macOs, default is *not* `/etc/ansible/hosts`. It's `/usr/local/etc/ansible/hosts`. Add the IP address to the `hosts` file. Also, if necessary, remove the IP address from `~/.ssh/known_hosts` on the *local* machine.

## Set up SSH access
See [this Linode article](https://www.linode.com/docs/security/use-public-key-authentication-with-ssh#uploading-keys) for reference.

On the *remote* machine, ensure `.ssh` directory exists.
On the *local* machine, `scp ~/.ssh/id_rsa.pub root@xxx.xxx.xxx.xxx:/root/.ssh/uploaded_key.pub`
On the *remote* machine, `cat ~/.ssh/uploaded_key.pub >> ~/.ssh/authorized_keys`

## Using Ansible
If you get an `UNREACHABLE` error with `ansible all -m ping`, use the `-u root` flag: `ansible all -m ping -u root`.

