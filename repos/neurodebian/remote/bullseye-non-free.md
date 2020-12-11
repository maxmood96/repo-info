## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:75ae55657348a156032e0a0ecea5f009b3dcf51d942e02171e420985ab3a882e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:bullseye-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:9bf19a92d933b6fb1f7ac038c684a7f6e317a44386d68aadd6d47a4f90f429d3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64482451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad9bb9e2d7f8d12558afc7e0b79f0d1a0e4128606d9b6d48847ea3611e9e278`
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
# Fri, 11 Dec 2020 17:13:28 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
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
	-	`sha256:ca63a627aa245fcab33f7b58024e3aeeb0ab247a5a7358c5773ed0399cfaa7fc`  
		Last Modified: Fri, 11 Dec 2020 17:15:29 GMT  
		Size: 365.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
