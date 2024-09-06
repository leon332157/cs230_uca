# Setting Up SSH Public/Private Keys

## Generate Public/Private Keys

Open a terminal and run

```bash
ssh-keygen -t ed25519
```

You should see an output like this

```bash
$ ssh-keygen -t ed25519
Generating public/private rsa key pair.
Enter file in which to save the key (/home/YOUR_USER/.ssh/id_ed25519):
```

Just press enter (leave it blank). Next it will ask you for a `passphrase` twice. Again just press enter. You should see an output like this 

```bash
Created directory '/home/YOUR_USER/.ssh'.
Enter passphrase (empty for no passphrase): 
Enter same passphrase again: 
Your identification has been saved in /home/YOUR_USER/.ssh/id_ed25519
Your public key has been saved in /home/YOUR_USER/.ssh/id_ed25519.pub
The key's randomart image is:
+---[RSA 3072]----+
|         o.+.    |
|          B.     |
|        E+..   ..|
|         oo  o oo|
|    . o S o.o.B..|
|   . = * + +.=+o |
|  + ..*.  + +. . |
| . +.o= ...o.    |
|  .  +o+.. ..    |
+----[SHA256]-----+
```

## Copy Your Public Key to Edlab

## Mac users:

From the terminal run

```bash
ssh-copy-id YOUR_EDLAB_USAERNAME@elnux.cs.umass.edu
```

## Windows uses

from the terminal that runs powershell

```pwsh
type C:\Users\YOUR_USER\.ssh\id_ed25519.pub | ssh YOUR_EDLAB_USERNAME@elnux.cs.umass.edu "mkdir -p ~/.ssh;cat >> .ssh/authorized_keys"
```

## Setting Up SSH Config File

Run this LOCALLY on your machine

First go into the `.ssh` directory and run the following commands 

## Mac 

```bash
cd ~/.ssh
touch config
vim config
```

## Windows

#### Run this in powershell!

```pwsh
New-Item -Name $HOME/.ssh/config -ItemType File
notepad $HOME/.ssh/config
```

and paste (make sure the lines are indented) 

```bash
Host edlab 
    HostName elnux.cs.umass.edu
    User YOUR_EDLAB_USERNAME
```

you should now be able to type

```bash
ssh edlab
```

and log into edlab without a username and password.
