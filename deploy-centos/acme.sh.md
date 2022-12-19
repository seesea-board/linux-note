# Acme.sh

## Install acme.sh

```
yum -y install socat
wget -qO- get.acme.sh | bash 

# run acme.sh anywhere
source ~/.bashrc
```

## Change ssl source

```
# letsencrypt | zerossl| buypass
 acme.sh --set-default-ca --server letsencrypt
```

## Apply SSL

1\. issue domain cert

```
mydomain="*.abc.com"
acme.sh --issue -d $mydomain --dns \
 --yes-I-know-dns-manual-mode-enough-go-ahead-please
```

2\. set TXT records

```
# login to your domain vender
```

3\. renew ssl

```
acme.sh --renew -d $mydomain \
  --yes-I-know-dns-manual-mode-enough-go-ahead-please
```
