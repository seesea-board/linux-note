# Steam Region Check

### Ref From

{% embed url="https://github.com/lmc999/RegionRestrictionCheck" %}

### Check Code

```

mkdir -p /root/docker && cd /root/docker
wget https://github.com/caonimagfw/bbrfast/releases/download/v0.9.1/regioncheck
unar -D regioncheck regioncheck.tar && rm -rf regioncheck
docker import regioncheck.tar regioncheck && rm -rf regioncheck.tar

docker run --rm -ti --net=host regioncheck \
	/bin/bash -l -c /check.sh
	
docker rmi regioncheck

```
