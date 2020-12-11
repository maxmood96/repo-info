## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:dca7df967bdd425d17c5ae33dfb5c4b06ef8462cabc0c2f2175395f40abc910e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:bullseye` - linux; amd64

```console
$ docker pull neurodebian@sha256:4822d6aed16d14b3669592a692e8c5b905611b7cce831ac8da2c0b5fe76702fb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64482086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a52c6da805609fb1ce4134b127b4ae23b51bfda1a0bf62959f54be7774254c3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:05:18 GMT
ADD file:ec1a9a704ae13b142c48069368561119760ccdf3d65d854c426d0dc9c39e60fb in / 
# Fri, 11 Dec 2020 02:05:18 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 17:13:15 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 17:13:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 11 Dec 2020 17:13:18 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 11 Dec 2020 17:13:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e4991c356405721fc787980835bdbf5c529ae12379346a771feb34407c522bd6`  
		Last Modified: Fri, 11 Dec 2020 02:11:29 GMT  
		Size: 53.1 MB (53113553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353792b9e936b188911447b02e0aff739e6f0e161b04c62ba4c7f5abc5cb1e38`  
		Last Modified: Fri, 11 Dec 2020 17:15:24 GMT  
		Size: 11.1 MB (11067471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6457673d7b064448a5710fe6f5cd263a5cea3dbfae10351d3c824e52772a8c84`  
		Last Modified: Fri, 11 Dec 2020 17:15:23 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34e7c7dcff96673e9fbe9761465d1e98bcf967fdaa476049f13f5426388d8f4`  
		Last Modified: Fri, 11 Dec 2020 17:15:23 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf620bacf3a0e8bee1c96a446f79206ab8fbbff0a82b9c661afed05a9172e95a`  
		Last Modified: Fri, 11 Dec 2020 17:15:24 GMT  
		Size: 299.1 KB (299057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
