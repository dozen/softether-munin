# munin plugin for softether

## usage
### usual case
environment:

```
Host: localhost
vpncmd path: /usr/local/vpnserver/vpncmd
Hub name: defaultHub
Hub password: softetherpassword
```

symlinked to `/etc/munin/plugins_{Hub name}`

```
ln -s /usr/share/munin/plugins/softether_ /etc/munin/plugins/softether_defaultHub
```

add config to `/etc/munin/plugin-conf.d/munin-node`

```
[softether_*]
env.password softetherpassword
```

### different host, vpncmd path case
environment:

```
vpncmd path: /opt/vpnserver/vpncmd
Hub name: 192.168.10.5
Hub password: softetherpassword
```

modify `/etc/munin/plugin-conf.d/munin-node`

```
[softether_*]
env.password softetherpassword
env.host 192.168.10.5
env.vpncmdpath /opt/vpnserver/vpncmd
```
