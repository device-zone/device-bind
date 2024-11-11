# device-bind
Provides an Bind DNS resolver appliance.

The appliance provides a default installation of the bind DNS service, which
is in turn enabled through the use of device-bind-resolver.


# device-bind-resolver
Provides an Bind appliance so the localhost can resolve DNSSEC securely.

This appliance does the following:

- All parameters passed to the device commands are syntax checked and canonicalised, with bash completion.
- Installs a local bind caching nameserver, available on ::1.
- Updates /etc/resolv.conf to use local unbound for DNS queries.
- Enables ability to securely handle DNSSEC without having to trust the network.
- Autostarts on server restart.
- Zero Trust configuration.

## before

- Deploy the device-bind-resolver package.

```
[root@server ~]# dnf install device-bind-resolver
```

## enable

To switch the appliance on, run this.

```
[root@server ~]# device services dns resolver enable 
```

## disable

To switch the appliance off, run this.

```
[root@server ~]# device services dns resolver disable  
```



