# How to set ssh-keys for the linux-lab of the HS-Fulda
To access the server in the linux lab with ssh more conviniently and securly. This can be done with ssh-keys.

First of all you need to be connected to the university network.

It is necessary to create a ssh-key on the local pc
```
shh-keygen -t rsa -b 4096
```
This will generate two files in `.ssh`, the private key `id_rsa` and the public key `id_rsa.pub`.

The content of the `id_rsa.pub` file needs to be appended to the `~/.ssh/authorized_keys` file on the `exin.informatik.hs-fulda.de` server. If it doesn't exist create it.

Now you should be able to login in to the exin server without password. To connect without password to a pc you need to do this again on the exin server and add it to the `authorized_keys` file. Now you should have two keys in there (one for your local machine and one for the linux lab).

After this step all ssh connections are secured via ssh-keys.
