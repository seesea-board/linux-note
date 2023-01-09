# firewall-cmd

### Add port

```
firewall-cmd --permanent --zone=public \
    --add-port=xxxx/tcp \
    --add-port=xxxx/tcp

# remove
firewall-cmd --permanent --zone=public \
    --remove-port=xxxx/tcp \
    --remove-port=xxxx/tcp
```

### Add Rich

```
# add
firewall-cmd --permanent --add-rich-rule="rule family=ipv6 port protocol=tcp port=443 accept" --zone=public

# remove
firewall-cmd --permanent --remove-rich-rule="rule family=ipv6 port protocol=tcp port=443 accept" --zone=public

```

### Add forward

```
firewall-cmd --permanent --zone=public \
                --add-forward-port=port=aaaa:proto=tcp:toport=bbbb \
                --add-forward-port=port=aaaa:proto=tcp:toport=bbbb

# remove forward
firewall-cmd --permanent --zone=public \
                --remove-forward-port=port=aaaa:proto=tcp:toport=bbbb \
                --remove-forward-port=port=aaaa:proto=tcp:toport=bbbb

```
