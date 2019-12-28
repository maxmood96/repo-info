## `varnish:stable`

```console
$ docker pull varnish@sha256:1a86025e3297b692f1be2308ae82606c717c17265249d93ff2e31afad7f0cf2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:stable` - linux; amd64

```console
$ docker pull varnish@sha256:97b65d85d8423d0b69b18b018f5ce0737eda0e2888551081dbd2bf3540970a75
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67212471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff3dce924eb9db51468c49f4d46d6336b6eb25bb0c3494facef30a331302289f`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `["varnishd","-F","-f","\/etc\/varnish\/default.vcl"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:39:47 GMT
ENV VARNISH_VERSION=6.0.5-1~stretch
# Sat, 28 Dec 2019 08:40:22 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=48D81A24CB0456F5D59431D94CFCFD6BA750EDCD; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver http://ha.pool.sks-keyservers.net/ --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish60lts/debian/ stretch main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 08:40:22 GMT
WORKDIR /etc/varnish
# Sat, 28 Dec 2019 08:40:22 GMT
COPY file:0301ec458d312e5c085462f916888bc85bb94c134ed6116667d225487db56cac in /usr/local/bin/ 
# Sat, 28 Dec 2019 08:40:23 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Sat, 28 Dec 2019 08:40:23 GMT
EXPOSE 80
# Sat, 28 Dec 2019 08:40:23 GMT
CMD ["varnishd" "-F" "-f" "/etc/varnish/default.vcl"]
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d75d3befb2551921acda03c74674a8ab18e802c7c1ad172029b8270d43c9df75`  
		Last Modified: Sat, 28 Dec 2019 08:41:15 GMT  
		Size: 44.7 MB (44687480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6afdeb276efd7cf4b698b42db8557d9c36634bbcb95f22017e9792de5424a8`  
		Last Modified: Sat, 28 Dec 2019 08:40:59 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
