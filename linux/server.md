## Transfer files between servers (`scp`)

- `-P` specifies the port number (uppercase for scp)
- `-r` for directory-level transfers
- Source and target don't have to be your own server, good to keep in mind

``` sh
scp -P <port> [-r] <source> <target>
```

## Access localhost externally (`ngrok`)

- During development, servers typically run on localhost at a specific port (web, Jupyter Notebook)
- Used to expose local ports to external access
- If using VSCode with SSH remote, this step is unnecessary

``` sh
ngrok http <port>
```

## Change server password (`passwd`)

- Running this command will prompt you to change the password, similar to other services

```
passwd
```

## Use remote server ports on localhost (`ssh -L` or `ssh -R`)

- Also known as **SSH tunneling**
- Useful when running services on a remote server (TensorBoard, local web servers, etc.) and need to access them from your local machine
- Originally accessible only on the remote server's localhost, but can be forwarded to your local machine
- `-L` is local forwarding, `-R` is remote forwarding; the choice depends on firewall rules and connection method

```
ssh -L <local port>:localhost:<remote port> username@<remote server>
```

## Use server GUI on local Mac (`ssh -X` or `ssh -Y`)

- To run a server's GUI application locally, use `ssh` with the `-X` or `-Y` flag
- Both use X11 Forwarding
- On Mac, some setup is required:
  - Install XQuartz
  - Modify ssh config
- See [the differences between the two modes](https://askubuntu.com/questions/35512/what-is-the-difference-between-ssh-y-trusted-x11-forwarding-and-ssh-x-u)

```
ssh -X
ssh -Y
```

## SSH key-based passwordless login (`ssh-keygen`)

- Instead of entering a password every time, pre-generate an SSH key
- There are various key types, but RSA 4096 is commonly used
- Send the `.pub` file to the target server using `ssh-copy-id`

```
ssh-keygen -t rsa -b 4096
ssh-copy-id -i ~/.ssh/id_rsa_name.pub username@server -p port_num
```

## Simplify connections with ssh config (`~/.ssh/config`)

- [ssh config](https://www.ssh.com/academy/ssh/config) can be customized in many ways
- Edit the `config` file in `~/.ssh/` to simplify your connections
- Add entries in the following format (multiple servers supported):

```
Host host_name
    HostName xxx.xxx.xxx.xxx
    User username
    Port 1234
    IdentityFile ~/.ssh/id_rsa_name
```

- `host_name` can be anything you want
- Works even better with ssh-keygen (IdentityFile)
- Once configured, connect directly without specifying server, user, port, or password:

```
ssh host_name
```
