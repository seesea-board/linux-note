# Haproxy

### Install

```
yum -y install haproxy
systemctl restart haproxy
systemctl enable haproxy

```

### ipv6 forward to ipv4

```
cat /etc/haproxy/haproxy.cfg

echo "
global
    ulimit-n  512000
defaults
    log    global
    mode    tcp
    option    dontlognull
        timeout connect 5000
        timeout client  50000
        timeout server  50000
frontend ss-in
        bind xx:xx:443
        default_backend ss-out
backend ss-out
    server server1 0.0.0.0:443 maxconn 20480
 ">/etc/sysctl.conf

```
