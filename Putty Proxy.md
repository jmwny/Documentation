# Proxy Utilizing Putty / Firefox

### Configure Firefox to utilize the SOCKS Host

* Select 'Manual proxy configuration'
  * SOCKS Host:
    * Textbox: 127.0.0.1
    * Port   : 9898 (or the configured port)
  * Radio Button: SOCKS v5
  * Checkbox: 'Proxy DNS when using SOCKS v5'
  
### Example Putty command line

```
plink -ssh -v -P 8854 -T -D 9898 <hostname>
```

Where:
* -ssh
  * force use of the ssh protocol
* -v
  * verbose messages
* -P
  * remote sshd listening port
* -T
  * disable pty allocation
* -D
  * SOCKS listening port

```
Options:
  -V        print version information and exit
  -pgpfp    print PGP key fingerprints and exit
  -v        show verbose messages
  -load sessname  Load settings from saved session
  -ssh -telnet -rlogin -raw -serial
            force use of a particular protocol
  -P port   connect to specified port
  -l user   connect with specified username
  -batch    disable all interactive prompts
  -proxycmd command
            use 'command' as local proxy
  -sercfg configuration-string (e.g. 19200,8,n,1,X)
            Specify the serial configuration (serial only)
The following options only apply to SSH connections:
  -pw passw login with specified password
  -D [listen-IP:]listen-port
            Dynamic SOCKS-based port forwarding
  -L [listen-IP:]listen-port:host:port
            Forward local port to remote address
  -R [listen-IP:]listen-port:host:port
            Forward remote port to local address
  -X -x     enable / disable X11 forwarding
  -A -a     enable / disable agent forwarding
  -t -T     enable / disable pty allocation
  -1 -2     force use of particular protocol version
  -4 -6     force use of IPv4 or IPv6
  -C        enable compression
  -i key    private key file for user authentication
  -noagent  disable use of Pageant
  -agent    enable use of Pageant
  -hostkey aa:bb:cc:...
            manually specify a host key (may be repeated)
  -m file   read remote command(s) from file
  -s        remote command is an SSH subsystem (SSH-2 only)
  -N        don't start a shell/command (SSH-2 only)
  -nc host:port
            open tunnel in place of session (SSH-2 only)
  -sshlog file
  -sshrawlog file
            log protocol details to a file
  -shareexists
            test whether a connection-sharing upstream exists
```
