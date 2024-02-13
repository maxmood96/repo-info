<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `spiped`

-	[`spiped:1`](#spiped1)
-	[`spiped:1-alpine`](#spiped1-alpine)
-	[`spiped:1.6`](#spiped16)
-	[`spiped:1.6-alpine`](#spiped16-alpine)
-	[`spiped:1.6.2`](#spiped162)
-	[`spiped:1.6.2-alpine`](#spiped162-alpine)
-	[`spiped:alpine`](#spipedalpine)
-	[`spiped:latest`](#spipedlatest)

## `spiped:1`

```console
$ docker pull spiped@sha256:a938dfc05bd0ae364481f50cf15ffa46a834192176e695415c6ddc3dbe042378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `spiped:1` - linux; amd64

```console
$ docker pull spiped@sha256:4ccadbc769537bc07b35d853a30b35c6bcfcfbb14b5afa1e39603961c9a1c504
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38218644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:719ab71cf6a39481230305e3f871866993446bf78b83793b6ad21eb9342a4ac1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:18 GMT
ADD file:af0f4e41d68b67ca88a1ce6297326159e18e27670d7bfc0bf5804a4e2b268cc8 in / 
# Wed, 31 Jan 2024 22:35:18 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:33:07 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 01 Feb 2024 06:33:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 06:33:11 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 01 Feb 2024 06:33:32 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 01 Feb 2024 06:33:32 GMT
VOLUME [/spiped]
# Thu, 01 Feb 2024 06:33:32 GMT
WORKDIR /spiped
# Thu, 01 Feb 2024 06:33:32 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 01 Feb 2024 06:33:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Feb 2024 06:33:33 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c57ee5000d61345aa3ee6684794a8110328e2274d9a5ae7855969d1a26394463`  
		Last Modified: Wed, 31 Jan 2024 22:39:55 GMT  
		Size: 29.2 MB (29150465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44203c61795ceb5aa717874cc1c355a9febb762aa26db4d54762e140810bbd54`  
		Last Modified: Thu, 01 Feb 2024 06:33:44 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e96bb7906b0259f589b790f2a964e471097a06ff9c7074ee37939bf8874705a`  
		Last Modified: Thu, 01 Feb 2024 06:33:45 GMT  
		Size: 2.6 MB (2591920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350c478c0a9093fe3fbcdc25bd19f449229047c45bea61c39d68fd3dcc1cc7bf`  
		Last Modified: Thu, 01 Feb 2024 06:33:46 GMT  
		Size: 6.5 MB (6474660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb52b2c13591cae666bda1051270553763a9a0bb3d7ad942ae5375fcc54a2c4`  
		Last Modified: Thu, 01 Feb 2024 06:33:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7250b86daa96d08375a28325fd62af52cdebd4a8df190afab8e656cce4e34dc`  
		Last Modified: Thu, 01 Feb 2024 06:33:44 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; arm variant v5

```console
$ docker pull spiped@sha256:b67e57b88e008cf9495661ee2ac582e540d884d7703cac52bdd25796ce7b070e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34209394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3ba318184d148d492ca1c33bce26da95c059a01ae51ada227bc61f97a0a8bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 13 Feb 2024 01:08:21 GMT
ADD file:468c16fc087244db1784e8f07bec3a1a417cd85172afa7dc960c2d1ecd1f37bc in / 
# Tue, 13 Feb 2024 01:08:21 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 03:19:26 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 13 Feb 2024 03:19:34 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 03:19:34 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 13 Feb 2024 03:20:18 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Feb 2024 03:20:18 GMT
VOLUME [/spiped]
# Tue, 13 Feb 2024 03:20:19 GMT
WORKDIR /spiped
# Tue, 13 Feb 2024 03:20:19 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 13 Feb 2024 03:20:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 03:20:19 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:e0d489e60efeee042d73afc4d45ad77014188c0ac8941f9ba5f15760d2288c3a`  
		Last Modified: Tue, 13 Feb 2024 01:13:30 GMT  
		Size: 26.9 MB (26883902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2938e571c4babe989613853227d886d5928626333e4c093c6df91b19aec5fb0a`  
		Last Modified: Tue, 13 Feb 2024 03:20:29 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81838218c39638dc1e94dcc33057179085a406b579d8a1c5373b5f346060a63`  
		Last Modified: Tue, 13 Feb 2024 03:20:30 GMT  
		Size: 2.2 MB (2185998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c82383d90854f15f62cb55494b6901cdb81348474b581d9348f9f1f8a34a3b51`  
		Last Modified: Tue, 13 Feb 2024 03:20:31 GMT  
		Size: 5.1 MB (5137895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47e2773e38f75c046da3e84e7a7b0090923df1fe1cc1dbbd8f93ce8225dc010`  
		Last Modified: Tue, 13 Feb 2024 03:20:29 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a409bade7427266fd4c9e2c0562dbc0dcc2d9ae1633f9076dda77d58995ca396`  
		Last Modified: Tue, 13 Feb 2024 03:20:29 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; arm variant v7

```console
$ docker pull spiped@sha256:e9aac91d1d18c179c5a51cd537b6f29e9292fde388f587ab78292df4ca4e2a21
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31671961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0401e2242f201e1af1e125c6b52a39ff240bcaed35ddb7ae70db1bd7b9ae2e3d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:20 GMT
ADD file:d6072ced9736ca566086eea2514cf12faccec9859bbd93e83950ad51f6827e8c in / 
# Wed, 31 Jan 2024 22:44:20 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 02:25:32 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 01 Feb 2024 02:25:36 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 02:25:36 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 01 Feb 2024 02:25:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 01 Feb 2024 02:25:56 GMT
VOLUME [/spiped]
# Thu, 01 Feb 2024 02:25:56 GMT
WORKDIR /spiped
# Thu, 01 Feb 2024 02:25:57 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 01 Feb 2024 02:25:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Feb 2024 02:25:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:404006a0fd99beed6ef1a9502692bd5005ae8c3b9d36a9b48654f7dfaacfb2c5`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 24.7 MB (24741565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f0470047587d9d6a62cea3a77a55beb2bbe272c0a66fd7e9c83ea6a19fbd6ed`  
		Last Modified: Thu, 01 Feb 2024 02:26:08 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:789649eb9a8c062d810952062c99f90c9a0a124cef3588670ee6a5fbc94a8935`  
		Last Modified: Thu, 01 Feb 2024 02:26:08 GMT  
		Size: 2.0 MB (2046255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf7678736899447540748561d2c0dba7822c0532da2d937b351ee52d2d3894aa`  
		Last Modified: Thu, 01 Feb 2024 02:26:09 GMT  
		Size: 4.9 MB (4882543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc6cd5c5c4b771dbedf160095e62642c0afaee343572c1bc3ae1d42bc6069cd`  
		Last Modified: Thu, 01 Feb 2024 02:26:08 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55cb396e9adad99fe98f84363e64919fa7e728f6080a762976e88c45e240ea87`  
		Last Modified: Thu, 01 Feb 2024 02:26:08 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:b422fe4000fdc564bc2261e42686183590617716cc42297a2bbf77db6b2ab896
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37101287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c9e8a773970c13d02591938a3ba84ac2a1885ff2df38d811ddf6128247ca799`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:26 GMT
ADD file:ef6f078c1e72fcfafb9bfeeff0c1c771219dc2efe34650963106f63d32183b49 in / 
# Wed, 31 Jan 2024 22:44:27 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 05:56:32 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 01 Feb 2024 05:56:35 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 05:56:35 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 01 Feb 2024 05:56:52 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 01 Feb 2024 05:56:53 GMT
VOLUME [/spiped]
# Thu, 01 Feb 2024 05:56:53 GMT
WORKDIR /spiped
# Thu, 01 Feb 2024 05:56:53 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 01 Feb 2024 05:56:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Feb 2024 05:56:53 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:25d3892798f8b99159e3c1136799bfed560027ce451b50d57d961f4f02577ff5`  
		Last Modified: Wed, 31 Jan 2024 22:48:07 GMT  
		Size: 29.2 MB (29180832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab70de86f0546f613f3351b6316ea1ea9a0c6562cdce9336f24d6552e0cc3b47`  
		Last Modified: Thu, 01 Feb 2024 05:57:04 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed15fb941dfb5e9137761f97b3e344916691cc8473a8d589bee58e24388cd2f7`  
		Last Modified: Thu, 01 Feb 2024 05:57:05 GMT  
		Size: 2.4 MB (2434866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b862a579330ea8f3bc50e0e60057d34b75553a18deccc7bab7a1b331ae5016`  
		Last Modified: Thu, 01 Feb 2024 05:57:05 GMT  
		Size: 5.5 MB (5483992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429251a29a2a0f675bcd3504dd3e855182dd3fbb197347f36c4e1baa6bc8303f`  
		Last Modified: Thu, 01 Feb 2024 05:57:04 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3867deda232b6d0f845d84dfd23666b4965f52bc6177bb9f4f9dd024ebbe6af`  
		Last Modified: Thu, 01 Feb 2024 05:57:04 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; 386

```console
$ docker pull spiped@sha256:af3a94935515497a1ade45fcc72c70ac050cfd1381185b8904a3c6c5c00f612a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38699213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0210fdce54e20cfde76f132661954d813e3b6a0f3993e8d9d04a53fc96fc39e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 31 Jan 2024 22:39:00 GMT
ADD file:540e2de73452bd162dd7f630bf29f60e7d2e4a7a5d32a495bedf8ad390b59d7f in / 
# Wed, 31 Jan 2024 22:39:01 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:28:50 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 31 Jan 2024 23:28:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:28:56 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 31 Jan 2024 23:29:29 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 31 Jan 2024 23:29:30 GMT
VOLUME [/spiped]
# Wed, 31 Jan 2024 23:29:30 GMT
WORKDIR /spiped
# Wed, 31 Jan 2024 23:29:30 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 31 Jan 2024 23:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Jan 2024 23:29:30 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:34ef135b45f33052e8e5bca668f9a45a938944a9cf3fb73a46f54a7bf11f091b`  
		Last Modified: Wed, 31 Jan 2024 22:43:46 GMT  
		Size: 30.2 MB (30165018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751a96ff8957608f7ad889db770d428885c2b206b3f8652b3d06872194295d78`  
		Last Modified: Wed, 31 Jan 2024 23:29:47 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53160d66b23e9b2c4404e8fbb7ddb70966b2fa0ae6fef0fcd290dc733f9866b9`  
		Last Modified: Wed, 31 Jan 2024 23:29:47 GMT  
		Size: 2.6 MB (2588154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c15a42863551b8164cceac5ac558601c2b66a6c81c590cd98e5dfe6af43dbfa4`  
		Last Modified: Wed, 31 Jan 2024 23:29:49 GMT  
		Size: 5.9 MB (5944440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e297082e00314cd0f8763f69ec7001fa8440dbd507fa8975cd5620cd5cc63d6`  
		Last Modified: Wed, 31 Jan 2024 23:29:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba709f2eb9259a79c1eec4292df8fae1b367472b00185af3340f0a963ab390c4`  
		Last Modified: Wed, 31 Jan 2024 23:29:47 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; mips64le

```console
$ docker pull spiped@sha256:6ce4d2d0d50f6e83deb694c99ecdd43098dd3e8d5741391f4299b075b03a043f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36784313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04a7ca6e08978ccba1c67b528ff59cb65d5ffc61df8decfa703a154e5cf0fda1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 31 Jan 2024 22:27:13 GMT
ADD file:c38ae3175b2ea7bff74f0e28558af27158de7697be9142ed9d681c4d37b24e35 in / 
# Wed, 31 Jan 2024 22:27:17 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 11:09:49 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 01 Feb 2024 11:10:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 11:10:12 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 01 Feb 2024 11:11:58 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 01 Feb 2024 11:12:01 GMT
VOLUME [/spiped]
# Thu, 01 Feb 2024 11:12:04 GMT
WORKDIR /spiped
# Thu, 01 Feb 2024 11:12:06 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 01 Feb 2024 11:12:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Feb 2024 11:12:12 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:21bfa6f58b3ab30099793f844be56212a593fddbf3f030cd8c42b38a1dcefcff`  
		Last Modified: Wed, 31 Jan 2024 22:38:21 GMT  
		Size: 29.1 MB (29142437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c86ec7ab62c6acb9250eba5339643c146a5e73365420e68d7acb3e218bdacd57`  
		Last Modified: Thu, 01 Feb 2024 11:12:33 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea4b98fda2b541f972777b687167057487d97a7201574da0b7eebe255d46e1a`  
		Last Modified: Thu, 01 Feb 2024 11:12:35 GMT  
		Size: 1.8 MB (1834351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a784d99cbd8a4388e1a1943324e49b064d6f2dee4c80dafed2855dcc71b1f0`  
		Last Modified: Thu, 01 Feb 2024 11:12:38 GMT  
		Size: 5.8 MB (5806014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b288162c33595db1d26d19277130f65a6dcd72972f3cbd54812c14fb44ffabd8`  
		Last Modified: Thu, 01 Feb 2024 11:12:33 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43ddcf2cc851edfe7424b2bbfecc440922c44231bc57f9a2a827a78a1ffe941`  
		Last Modified: Thu, 01 Feb 2024 11:12:33 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; ppc64le

```console
$ docker pull spiped@sha256:64c5c55b229219480ea25215bdab6b03b1f345286ecbc63dc3f869e1ce330b3e
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42311916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59508d985231a098bed6b2ae23582037f4e79ddfe90b8a2f294822913213b7d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:03 GMT
ADD file:b65bdf3d9277efbf6bbf8bf0121f92bdcd342ed0c4f49f1cee3b91adafacd76c in / 
# Tue, 13 Feb 2024 00:39:05 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 03:44:05 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 13 Feb 2024 03:44:10 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 03:44:10 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 13 Feb 2024 03:45:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Feb 2024 03:45:11 GMT
VOLUME [/spiped]
# Tue, 13 Feb 2024 03:45:12 GMT
WORKDIR /spiped
# Tue, 13 Feb 2024 03:45:12 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 13 Feb 2024 03:45:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 03:45:13 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b1cce6d9947985e4270ac998aa258401bc5deca94d504040a14f9f3c47258d68`  
		Last Modified: Tue, 13 Feb 2024 00:43:56 GMT  
		Size: 33.1 MB (33118908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28eab5449fc59b53e9f2279940a43c6d3a3fd364d96fa2c3d2922cbc5de81e1b`  
		Last Modified: Tue, 13 Feb 2024 03:45:38 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:725f98f5d63a98ff542ad7b2403dd5c368b4ebb1a8856490eecd72bae96151a6`  
		Last Modified: Tue, 13 Feb 2024 03:45:38 GMT  
		Size: 2.8 MB (2769282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d6df2553e038156a19aa44c6722f55beeb50690123dd9f30ced381006e9e7a8`  
		Last Modified: Tue, 13 Feb 2024 03:45:39 GMT  
		Size: 6.4 MB (6422129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:360a23e225035c41d84713834b9665254b25b1888bdbeca5ac335fb5955fdfa6`  
		Last Modified: Tue, 13 Feb 2024 03:45:38 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8256250ad5ac412b1f0b34de7655074aeb8f3347b40f7226af075854090e891a`  
		Last Modified: Tue, 13 Feb 2024 03:45:38 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; s390x

```console
$ docker pull spiped@sha256:237c566ae2695688605457ce444873bacc827c72a5dab859f380f431cf8435fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.2 MB (35165793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab5dc818013c2717f8a89991acd65937b38331f6e81aae94516a765057ed63f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 31 Jan 2024 22:58:51 GMT
ADD file:d543e4bc70d0d1d81c594a97289d7f2b4925d86461644cf881890997abfb6ead in / 
# Wed, 31 Jan 2024 22:58:53 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 05:54:15 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 01 Feb 2024 05:54:19 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 05:54:19 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 01 Feb 2024 05:54:51 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 01 Feb 2024 05:54:52 GMT
VOLUME [/spiped]
# Thu, 01 Feb 2024 05:54:52 GMT
WORKDIR /spiped
# Thu, 01 Feb 2024 05:54:53 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 01 Feb 2024 05:54:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Feb 2024 05:54:53 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:84abfb784f629f520e19ebd281090b7f1b3b78ff96b3be919578a053d2708ad5`  
		Last Modified: Wed, 31 Jan 2024 23:29:10 GMT  
		Size: 27.5 MB (27513479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9096f642a1ac565ee2d5c07e0d0cf6e1bf955b8b0844bfef49d774de9bfcde`  
		Last Modified: Thu, 01 Feb 2024 05:57:44 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d2aef7174c2e6a7a1c9d301f1c42480cfe91e8854437e9401d6d09be37e8b6`  
		Last Modified: Thu, 01 Feb 2024 05:57:45 GMT  
		Size: 2.3 MB (2262471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc72cc5f176534103dfa802d29e26026288813d1b7db888527e71d18a695e3a`  
		Last Modified: Thu, 01 Feb 2024 05:57:45 GMT  
		Size: 5.4 MB (5388243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5820f59a9ec53afbe9859e889d57ec691f07ff8774a6e3d6131dd2f3916ff9`  
		Last Modified: Thu, 01 Feb 2024 05:57:44 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a83e6ca20ca5ee69c588a377a2897bb10e1c3f3d149b3bf42517d7b6fe686e0`  
		Last Modified: Thu, 01 Feb 2024 05:57:44 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1-alpine`

```console
$ docker pull spiped@sha256:f84d8a95e3e950b92f95d85b787be2683a48c95bce66e074dc979bb1fadf87f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `spiped:1-alpine` - linux; amd64

```console
$ docker pull spiped@sha256:0db343ac47d10615e10448e605656eb7d9f8a7355742c16d724da24cf8bc8200
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5058548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c3fac6726c34597dbefe1ed2357ed9a503e3e9fbee4de673c7329536ec6690`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:53:15 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 03:53:16 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 03:53:16 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 03:53:26 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 03:53:26 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 03:53:26 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 03:53:27 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 03:53:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 03:53:27 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233335b905cdbc6ef4fd933dc93fa62f3181b6bd01639a4f13fd5686f1e60d13`  
		Last Modified: Sat, 27 Jan 2024 03:53:39 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd31ddc1313d2d26e7d3bf86684929340ae1c767c9023291012725885f68aed3`  
		Last Modified: Sat, 27 Jan 2024 03:53:39 GMT  
		Size: 1.4 MB (1432997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c381fda201d7dc3075b77745e2944ca6c6ed05b2b4a637483745ef7f435c81`  
		Last Modified: Sat, 27 Jan 2024 03:53:39 GMT  
		Size: 221.3 KB (221268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aeb01bcfc8c133af082c950a536224f400f37222340e8485ecb27f7730763b9`  
		Last Modified: Sat, 27 Jan 2024 03:53:39 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc677c6186bf867e737581c8144ce09e6150804b11cea8b63a5ad1d4c51705a6`  
		Last Modified: Sat, 27 Jan 2024 03:53:39 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:8ce831c9a9bd85aaaaa936078674fee912bcb1ab6a559a10ac05bfeb88205258
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4591419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cab2da111d02d52ac4d4c3108792e47cd3b4483a442f6ad1ec888adcdc0fa0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:29:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 09:29:49 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 09:29:49 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 09:29:56 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 09:29:56 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 09:29:57 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 09:29:57 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 09:29:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 09:29:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b7c245ae48f36f63fc5c01b46647a3f81f0f9c15eed37b8450c4a8f6acf4813`  
		Last Modified: Sat, 27 Jan 2024 09:30:06 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a01e2971f82c2f2015b52374f97e3eaa86424ab24628e5202bc501ff7cc55f`  
		Last Modified: Sat, 27 Jan 2024 09:30:07 GMT  
		Size: 1.2 MB (1236766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3317277e0d843266a95b229df043b700dcd3be7294bf12f7772982cecce35a0a`  
		Last Modified: Sat, 27 Jan 2024 09:30:07 GMT  
		Size: 205.9 KB (205855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe542138d0182af83ab0348a6ad629fd96d9f51a8c11af831827488c66fe9ead`  
		Last Modified: Sat, 27 Jan 2024 09:30:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8730b4279c13c83155000948a3a668ef61f646291e4eb110261402e0306892`  
		Last Modified: Sat, 27 Jan 2024 09:30:06 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:6942a5aad13c9c0357adaa915683aa0841283c335001c09fefec4834207fe8db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4266572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ac9b14691221a3a70d3ce535e8a310dbb261aa500240fb5ff06ec64c51205a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 10:00:45 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 10:00:47 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 10:00:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 10:00:54 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 10:00:54 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 10:00:54 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 10:00:54 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 10:00:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 10:00:54 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b25927e775c6b583d50d82035663da8e070092f5179da4474850e0328ad14bb`  
		Last Modified: Sat, 27 Jan 2024 10:01:06 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:570c06b7a65d23f9b1b3ad7304bb3cfcfe3add9daf5f39922433e6832b4b01c3`  
		Last Modified: Sat, 27 Jan 2024 10:01:06 GMT  
		Size: 1.2 MB (1163906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7ebfc2c419f514f89fb6622c744006a791608d9e5ec7b54919a91d1efc0261`  
		Last Modified: Sat, 27 Jan 2024 10:01:07 GMT  
		Size: 199.5 KB (199536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0f599b0ec5b6d56ec2ba25d5fbaae221270e0e08d87a0e37f50fdc37d74736`  
		Last Modified: Sat, 27 Jan 2024 10:01:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb96c25e72b85a60641b35a0c7b1fff4fe6ddce5ec193d8abd51da0578aa10fd`  
		Last Modified: Sat, 27 Jan 2024 10:01:06 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:1e10f9c4cd5a0e555299d647aee397159cf3cc9c49ebae9d37f43d785efc2384
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4913491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a23f576db03337acb2a717f8e576bcec70c8cf09d4730860e3ba311eaef323`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:09:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 09:09:58 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 09:09:59 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 09:10:06 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 09:10:06 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 09:10:06 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 09:10:06 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 09:10:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 09:10:06 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8856182d07b0c02f8d441ffc00e795edcd647f6c5641b66df213b4f37cce4225`  
		Last Modified: Sat, 27 Jan 2024 09:10:17 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278472923ca4d7acdc0bc5101538bba2be4bc9817efad8bee80b7403ec35a8f4`  
		Last Modified: Sat, 27 Jan 2024 09:10:18 GMT  
		Size: 1.4 MB (1362704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07330ac41b8ac7b1962cf975117db9bb85969a5f9c58c66a15a065b85ccb4900`  
		Last Modified: Sat, 27 Jan 2024 09:10:17 GMT  
		Size: 215.7 KB (215689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5751cd73d323468ab539e9b67218720747135bed806a1395d8518fc12f72ca0`  
		Last Modified: Sat, 27 Jan 2024 09:10:17 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7703ff668a2070168836bbffb2f18084d597d189a2e555d423d14e72f416ef68`  
		Last Modified: Sat, 27 Jan 2024 09:10:17 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; 386

```console
$ docker pull spiped@sha256:d3a824307ae8cc220762e6f2043727e060fa6c3a918513c7d6dc167f588c220c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4826330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:399c596c03762587fa8fb8f210f5fc0ee2e6948e2905a3c8bec2a2ec243123fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:23 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Sat, 27 Jan 2024 00:38:23 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 07:52:17 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 07:52:18 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 07:52:18 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 07:52:31 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 07:52:31 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 07:52:31 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 07:52:31 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 07:52:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 07:52:32 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd471e9831f61183ecc69596284cb73f5ad30faee2d88b9be671b2e4ac9127c`  
		Last Modified: Sat, 27 Jan 2024 07:52:44 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdd3381a2456733e62fd73e208da969fc736e142d3dfc59d9c20574d6a03b20`  
		Last Modified: Sat, 27 Jan 2024 07:52:45 GMT  
		Size: 1.4 MB (1353891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c859820ed9aaf3367c0aef4d952f366e5e3a87cc24b68f63aa90e96ad7c760bf`  
		Last Modified: Sat, 27 Jan 2024 07:52:44 GMT  
		Size: 231.6 KB (231637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8281c045fc7e2e825eaafe157921bfeb141287f288180c08b32aeb520210886`  
		Last Modified: Sat, 27 Jan 2024 07:52:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a217ef75062c5c1546aec015509ac1e9cd1196309bf2416b9cf2946ca8023ed5`  
		Last Modified: Sat, 27 Jan 2024 07:52:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:e1caf5c06d70c575f68a2cfc9d1f28866de40ffc4538386849eab4457b11dd05
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4931986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2b22668c6ed4bd4242ee6b0823d1bb1e89f0cbf12f4f006c8e3c9e5c0bf946c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 06:56:45 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 06:56:49 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 06:56:51 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 06:57:04 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 06:57:06 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 06:57:12 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 06:57:12 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 06:57:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 06:57:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f38342a65739ff156e510b0402148c23bd29070f31cd8094ce9dcb6103c642c`  
		Last Modified: Sat, 27 Jan 2024 06:57:33 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4741e7cfa5277c2b562fbf0c5b2ad4315ce86d9e85b18dbc8048c6f2a59674ce`  
		Last Modified: Sat, 27 Jan 2024 06:57:34 GMT  
		Size: 1.4 MB (1361740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb83ebefffb65a8041304caea5b161380e4bcc9f83e3850a37f1a9215bb48bf`  
		Last Modified: Sat, 27 Jan 2024 06:57:34 GMT  
		Size: 220.0 KB (220022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86d9e19ad5862b1c9e0f209808dbf8b0d955cc8133e5fca9f9abeb2fc72e02e`  
		Last Modified: Sat, 27 Jan 2024 06:57:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3c09da5c10a6e8af149a2d66d3ec1ecd17a20e4ca69b351187d7ae16a6294d`  
		Last Modified: Sat, 27 Jan 2024 06:57:33 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:b3ac08887b93771eb3edc0900f301191ce0b2ab78f5f8bcc083d00e7ed4ef614
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4649400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d791c997a460e956f270fae0568846bc53b6326c809afe52f6f29185fa563c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:29:04 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 04:29:06 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 04:29:06 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 04:29:11 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 04:29:11 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 04:29:11 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 04:29:11 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 04:29:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 04:29:11 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94fd1e7053a9e79fdc6fb18948ee8438abdb6a673501fd245ba7199ef24334ae`  
		Last Modified: Sat, 27 Jan 2024 04:30:28 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e84b87b749a1bd8e548de258d2c03726b157ce7543a7e3c4c323484c64f3df4`  
		Last Modified: Sat, 27 Jan 2024 04:30:28 GMT  
		Size: 1.2 MB (1221487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db717c8240748de34eac9be8f3893bc45ad2632d5ab62765073e77c0dc964dce`  
		Last Modified: Sat, 27 Jan 2024 04:30:28 GMT  
		Size: 208.6 KB (208642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e6522b6475f44c3e255370c7cf9721b28c96fdcba8371cde2d371502dea270`  
		Last Modified: Sat, 27 Jan 2024 04:30:28 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d007dcbb3f6219ef0c2534135ee1816650af5ec516db978bd44eac8bb6a94027`  
		Last Modified: Sat, 27 Jan 2024 04:30:28 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6`

```console
$ docker pull spiped@sha256:a938dfc05bd0ae364481f50cf15ffa46a834192176e695415c6ddc3dbe042378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `spiped:1.6` - linux; amd64

```console
$ docker pull spiped@sha256:4ccadbc769537bc07b35d853a30b35c6bcfcfbb14b5afa1e39603961c9a1c504
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38218644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:719ab71cf6a39481230305e3f871866993446bf78b83793b6ad21eb9342a4ac1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:18 GMT
ADD file:af0f4e41d68b67ca88a1ce6297326159e18e27670d7bfc0bf5804a4e2b268cc8 in / 
# Wed, 31 Jan 2024 22:35:18 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:33:07 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 01 Feb 2024 06:33:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 06:33:11 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 01 Feb 2024 06:33:32 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 01 Feb 2024 06:33:32 GMT
VOLUME [/spiped]
# Thu, 01 Feb 2024 06:33:32 GMT
WORKDIR /spiped
# Thu, 01 Feb 2024 06:33:32 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 01 Feb 2024 06:33:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Feb 2024 06:33:33 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c57ee5000d61345aa3ee6684794a8110328e2274d9a5ae7855969d1a26394463`  
		Last Modified: Wed, 31 Jan 2024 22:39:55 GMT  
		Size: 29.2 MB (29150465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44203c61795ceb5aa717874cc1c355a9febb762aa26db4d54762e140810bbd54`  
		Last Modified: Thu, 01 Feb 2024 06:33:44 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e96bb7906b0259f589b790f2a964e471097a06ff9c7074ee37939bf8874705a`  
		Last Modified: Thu, 01 Feb 2024 06:33:45 GMT  
		Size: 2.6 MB (2591920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350c478c0a9093fe3fbcdc25bd19f449229047c45bea61c39d68fd3dcc1cc7bf`  
		Last Modified: Thu, 01 Feb 2024 06:33:46 GMT  
		Size: 6.5 MB (6474660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb52b2c13591cae666bda1051270553763a9a0bb3d7ad942ae5375fcc54a2c4`  
		Last Modified: Thu, 01 Feb 2024 06:33:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7250b86daa96d08375a28325fd62af52cdebd4a8df190afab8e656cce4e34dc`  
		Last Modified: Thu, 01 Feb 2024 06:33:44 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; arm variant v5

```console
$ docker pull spiped@sha256:b67e57b88e008cf9495661ee2ac582e540d884d7703cac52bdd25796ce7b070e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34209394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3ba318184d148d492ca1c33bce26da95c059a01ae51ada227bc61f97a0a8bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 13 Feb 2024 01:08:21 GMT
ADD file:468c16fc087244db1784e8f07bec3a1a417cd85172afa7dc960c2d1ecd1f37bc in / 
# Tue, 13 Feb 2024 01:08:21 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 03:19:26 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 13 Feb 2024 03:19:34 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 03:19:34 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 13 Feb 2024 03:20:18 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Feb 2024 03:20:18 GMT
VOLUME [/spiped]
# Tue, 13 Feb 2024 03:20:19 GMT
WORKDIR /spiped
# Tue, 13 Feb 2024 03:20:19 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 13 Feb 2024 03:20:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 03:20:19 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:e0d489e60efeee042d73afc4d45ad77014188c0ac8941f9ba5f15760d2288c3a`  
		Last Modified: Tue, 13 Feb 2024 01:13:30 GMT  
		Size: 26.9 MB (26883902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2938e571c4babe989613853227d886d5928626333e4c093c6df91b19aec5fb0a`  
		Last Modified: Tue, 13 Feb 2024 03:20:29 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81838218c39638dc1e94dcc33057179085a406b579d8a1c5373b5f346060a63`  
		Last Modified: Tue, 13 Feb 2024 03:20:30 GMT  
		Size: 2.2 MB (2185998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c82383d90854f15f62cb55494b6901cdb81348474b581d9348f9f1f8a34a3b51`  
		Last Modified: Tue, 13 Feb 2024 03:20:31 GMT  
		Size: 5.1 MB (5137895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47e2773e38f75c046da3e84e7a7b0090923df1fe1cc1dbbd8f93ce8225dc010`  
		Last Modified: Tue, 13 Feb 2024 03:20:29 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a409bade7427266fd4c9e2c0562dbc0dcc2d9ae1633f9076dda77d58995ca396`  
		Last Modified: Tue, 13 Feb 2024 03:20:29 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; arm variant v7

```console
$ docker pull spiped@sha256:e9aac91d1d18c179c5a51cd537b6f29e9292fde388f587ab78292df4ca4e2a21
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31671961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0401e2242f201e1af1e125c6b52a39ff240bcaed35ddb7ae70db1bd7b9ae2e3d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:20 GMT
ADD file:d6072ced9736ca566086eea2514cf12faccec9859bbd93e83950ad51f6827e8c in / 
# Wed, 31 Jan 2024 22:44:20 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 02:25:32 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 01 Feb 2024 02:25:36 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 02:25:36 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 01 Feb 2024 02:25:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 01 Feb 2024 02:25:56 GMT
VOLUME [/spiped]
# Thu, 01 Feb 2024 02:25:56 GMT
WORKDIR /spiped
# Thu, 01 Feb 2024 02:25:57 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 01 Feb 2024 02:25:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Feb 2024 02:25:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:404006a0fd99beed6ef1a9502692bd5005ae8c3b9d36a9b48654f7dfaacfb2c5`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 24.7 MB (24741565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f0470047587d9d6a62cea3a77a55beb2bbe272c0a66fd7e9c83ea6a19fbd6ed`  
		Last Modified: Thu, 01 Feb 2024 02:26:08 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:789649eb9a8c062d810952062c99f90c9a0a124cef3588670ee6a5fbc94a8935`  
		Last Modified: Thu, 01 Feb 2024 02:26:08 GMT  
		Size: 2.0 MB (2046255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf7678736899447540748561d2c0dba7822c0532da2d937b351ee52d2d3894aa`  
		Last Modified: Thu, 01 Feb 2024 02:26:09 GMT  
		Size: 4.9 MB (4882543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc6cd5c5c4b771dbedf160095e62642c0afaee343572c1bc3ae1d42bc6069cd`  
		Last Modified: Thu, 01 Feb 2024 02:26:08 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55cb396e9adad99fe98f84363e64919fa7e728f6080a762976e88c45e240ea87`  
		Last Modified: Thu, 01 Feb 2024 02:26:08 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:b422fe4000fdc564bc2261e42686183590617716cc42297a2bbf77db6b2ab896
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37101287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c9e8a773970c13d02591938a3ba84ac2a1885ff2df38d811ddf6128247ca799`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:26 GMT
ADD file:ef6f078c1e72fcfafb9bfeeff0c1c771219dc2efe34650963106f63d32183b49 in / 
# Wed, 31 Jan 2024 22:44:27 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 05:56:32 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 01 Feb 2024 05:56:35 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 05:56:35 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 01 Feb 2024 05:56:52 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 01 Feb 2024 05:56:53 GMT
VOLUME [/spiped]
# Thu, 01 Feb 2024 05:56:53 GMT
WORKDIR /spiped
# Thu, 01 Feb 2024 05:56:53 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 01 Feb 2024 05:56:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Feb 2024 05:56:53 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:25d3892798f8b99159e3c1136799bfed560027ce451b50d57d961f4f02577ff5`  
		Last Modified: Wed, 31 Jan 2024 22:48:07 GMT  
		Size: 29.2 MB (29180832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab70de86f0546f613f3351b6316ea1ea9a0c6562cdce9336f24d6552e0cc3b47`  
		Last Modified: Thu, 01 Feb 2024 05:57:04 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed15fb941dfb5e9137761f97b3e344916691cc8473a8d589bee58e24388cd2f7`  
		Last Modified: Thu, 01 Feb 2024 05:57:05 GMT  
		Size: 2.4 MB (2434866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b862a579330ea8f3bc50e0e60057d34b75553a18deccc7bab7a1b331ae5016`  
		Last Modified: Thu, 01 Feb 2024 05:57:05 GMT  
		Size: 5.5 MB (5483992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429251a29a2a0f675bcd3504dd3e855182dd3fbb197347f36c4e1baa6bc8303f`  
		Last Modified: Thu, 01 Feb 2024 05:57:04 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3867deda232b6d0f845d84dfd23666b4965f52bc6177bb9f4f9dd024ebbe6af`  
		Last Modified: Thu, 01 Feb 2024 05:57:04 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; 386

```console
$ docker pull spiped@sha256:af3a94935515497a1ade45fcc72c70ac050cfd1381185b8904a3c6c5c00f612a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38699213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0210fdce54e20cfde76f132661954d813e3b6a0f3993e8d9d04a53fc96fc39e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 31 Jan 2024 22:39:00 GMT
ADD file:540e2de73452bd162dd7f630bf29f60e7d2e4a7a5d32a495bedf8ad390b59d7f in / 
# Wed, 31 Jan 2024 22:39:01 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:28:50 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 31 Jan 2024 23:28:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:28:56 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 31 Jan 2024 23:29:29 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 31 Jan 2024 23:29:30 GMT
VOLUME [/spiped]
# Wed, 31 Jan 2024 23:29:30 GMT
WORKDIR /spiped
# Wed, 31 Jan 2024 23:29:30 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 31 Jan 2024 23:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Jan 2024 23:29:30 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:34ef135b45f33052e8e5bca668f9a45a938944a9cf3fb73a46f54a7bf11f091b`  
		Last Modified: Wed, 31 Jan 2024 22:43:46 GMT  
		Size: 30.2 MB (30165018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751a96ff8957608f7ad889db770d428885c2b206b3f8652b3d06872194295d78`  
		Last Modified: Wed, 31 Jan 2024 23:29:47 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53160d66b23e9b2c4404e8fbb7ddb70966b2fa0ae6fef0fcd290dc733f9866b9`  
		Last Modified: Wed, 31 Jan 2024 23:29:47 GMT  
		Size: 2.6 MB (2588154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c15a42863551b8164cceac5ac558601c2b66a6c81c590cd98e5dfe6af43dbfa4`  
		Last Modified: Wed, 31 Jan 2024 23:29:49 GMT  
		Size: 5.9 MB (5944440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e297082e00314cd0f8763f69ec7001fa8440dbd507fa8975cd5620cd5cc63d6`  
		Last Modified: Wed, 31 Jan 2024 23:29:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba709f2eb9259a79c1eec4292df8fae1b367472b00185af3340f0a963ab390c4`  
		Last Modified: Wed, 31 Jan 2024 23:29:47 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; mips64le

```console
$ docker pull spiped@sha256:6ce4d2d0d50f6e83deb694c99ecdd43098dd3e8d5741391f4299b075b03a043f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36784313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04a7ca6e08978ccba1c67b528ff59cb65d5ffc61df8decfa703a154e5cf0fda1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 31 Jan 2024 22:27:13 GMT
ADD file:c38ae3175b2ea7bff74f0e28558af27158de7697be9142ed9d681c4d37b24e35 in / 
# Wed, 31 Jan 2024 22:27:17 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 11:09:49 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 01 Feb 2024 11:10:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 11:10:12 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 01 Feb 2024 11:11:58 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 01 Feb 2024 11:12:01 GMT
VOLUME [/spiped]
# Thu, 01 Feb 2024 11:12:04 GMT
WORKDIR /spiped
# Thu, 01 Feb 2024 11:12:06 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 01 Feb 2024 11:12:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Feb 2024 11:12:12 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:21bfa6f58b3ab30099793f844be56212a593fddbf3f030cd8c42b38a1dcefcff`  
		Last Modified: Wed, 31 Jan 2024 22:38:21 GMT  
		Size: 29.1 MB (29142437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c86ec7ab62c6acb9250eba5339643c146a5e73365420e68d7acb3e218bdacd57`  
		Last Modified: Thu, 01 Feb 2024 11:12:33 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea4b98fda2b541f972777b687167057487d97a7201574da0b7eebe255d46e1a`  
		Last Modified: Thu, 01 Feb 2024 11:12:35 GMT  
		Size: 1.8 MB (1834351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a784d99cbd8a4388e1a1943324e49b064d6f2dee4c80dafed2855dcc71b1f0`  
		Last Modified: Thu, 01 Feb 2024 11:12:38 GMT  
		Size: 5.8 MB (5806014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b288162c33595db1d26d19277130f65a6dcd72972f3cbd54812c14fb44ffabd8`  
		Last Modified: Thu, 01 Feb 2024 11:12:33 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43ddcf2cc851edfe7424b2bbfecc440922c44231bc57f9a2a827a78a1ffe941`  
		Last Modified: Thu, 01 Feb 2024 11:12:33 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; ppc64le

```console
$ docker pull spiped@sha256:64c5c55b229219480ea25215bdab6b03b1f345286ecbc63dc3f869e1ce330b3e
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42311916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59508d985231a098bed6b2ae23582037f4e79ddfe90b8a2f294822913213b7d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:03 GMT
ADD file:b65bdf3d9277efbf6bbf8bf0121f92bdcd342ed0c4f49f1cee3b91adafacd76c in / 
# Tue, 13 Feb 2024 00:39:05 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 03:44:05 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 13 Feb 2024 03:44:10 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 03:44:10 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 13 Feb 2024 03:45:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Feb 2024 03:45:11 GMT
VOLUME [/spiped]
# Tue, 13 Feb 2024 03:45:12 GMT
WORKDIR /spiped
# Tue, 13 Feb 2024 03:45:12 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 13 Feb 2024 03:45:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 03:45:13 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b1cce6d9947985e4270ac998aa258401bc5deca94d504040a14f9f3c47258d68`  
		Last Modified: Tue, 13 Feb 2024 00:43:56 GMT  
		Size: 33.1 MB (33118908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28eab5449fc59b53e9f2279940a43c6d3a3fd364d96fa2c3d2922cbc5de81e1b`  
		Last Modified: Tue, 13 Feb 2024 03:45:38 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:725f98f5d63a98ff542ad7b2403dd5c368b4ebb1a8856490eecd72bae96151a6`  
		Last Modified: Tue, 13 Feb 2024 03:45:38 GMT  
		Size: 2.8 MB (2769282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d6df2553e038156a19aa44c6722f55beeb50690123dd9f30ced381006e9e7a8`  
		Last Modified: Tue, 13 Feb 2024 03:45:39 GMT  
		Size: 6.4 MB (6422129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:360a23e225035c41d84713834b9665254b25b1888bdbeca5ac335fb5955fdfa6`  
		Last Modified: Tue, 13 Feb 2024 03:45:38 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8256250ad5ac412b1f0b34de7655074aeb8f3347b40f7226af075854090e891a`  
		Last Modified: Tue, 13 Feb 2024 03:45:38 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; s390x

```console
$ docker pull spiped@sha256:237c566ae2695688605457ce444873bacc827c72a5dab859f380f431cf8435fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.2 MB (35165793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab5dc818013c2717f8a89991acd65937b38331f6e81aae94516a765057ed63f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 31 Jan 2024 22:58:51 GMT
ADD file:d543e4bc70d0d1d81c594a97289d7f2b4925d86461644cf881890997abfb6ead in / 
# Wed, 31 Jan 2024 22:58:53 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 05:54:15 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 01 Feb 2024 05:54:19 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 05:54:19 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 01 Feb 2024 05:54:51 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 01 Feb 2024 05:54:52 GMT
VOLUME [/spiped]
# Thu, 01 Feb 2024 05:54:52 GMT
WORKDIR /spiped
# Thu, 01 Feb 2024 05:54:53 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 01 Feb 2024 05:54:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Feb 2024 05:54:53 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:84abfb784f629f520e19ebd281090b7f1b3b78ff96b3be919578a053d2708ad5`  
		Last Modified: Wed, 31 Jan 2024 23:29:10 GMT  
		Size: 27.5 MB (27513479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9096f642a1ac565ee2d5c07e0d0cf6e1bf955b8b0844bfef49d774de9bfcde`  
		Last Modified: Thu, 01 Feb 2024 05:57:44 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d2aef7174c2e6a7a1c9d301f1c42480cfe91e8854437e9401d6d09be37e8b6`  
		Last Modified: Thu, 01 Feb 2024 05:57:45 GMT  
		Size: 2.3 MB (2262471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc72cc5f176534103dfa802d29e26026288813d1b7db888527e71d18a695e3a`  
		Last Modified: Thu, 01 Feb 2024 05:57:45 GMT  
		Size: 5.4 MB (5388243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5820f59a9ec53afbe9859e889d57ec691f07ff8774a6e3d6131dd2f3916ff9`  
		Last Modified: Thu, 01 Feb 2024 05:57:44 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a83e6ca20ca5ee69c588a377a2897bb10e1c3f3d149b3bf42517d7b6fe686e0`  
		Last Modified: Thu, 01 Feb 2024 05:57:44 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6-alpine`

```console
$ docker pull spiped@sha256:f84d8a95e3e950b92f95d85b787be2683a48c95bce66e074dc979bb1fadf87f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `spiped:1.6-alpine` - linux; amd64

```console
$ docker pull spiped@sha256:0db343ac47d10615e10448e605656eb7d9f8a7355742c16d724da24cf8bc8200
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5058548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c3fac6726c34597dbefe1ed2357ed9a503e3e9fbee4de673c7329536ec6690`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:53:15 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 03:53:16 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 03:53:16 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 03:53:26 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 03:53:26 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 03:53:26 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 03:53:27 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 03:53:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 03:53:27 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233335b905cdbc6ef4fd933dc93fa62f3181b6bd01639a4f13fd5686f1e60d13`  
		Last Modified: Sat, 27 Jan 2024 03:53:39 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd31ddc1313d2d26e7d3bf86684929340ae1c767c9023291012725885f68aed3`  
		Last Modified: Sat, 27 Jan 2024 03:53:39 GMT  
		Size: 1.4 MB (1432997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c381fda201d7dc3075b77745e2944ca6c6ed05b2b4a637483745ef7f435c81`  
		Last Modified: Sat, 27 Jan 2024 03:53:39 GMT  
		Size: 221.3 KB (221268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aeb01bcfc8c133af082c950a536224f400f37222340e8485ecb27f7730763b9`  
		Last Modified: Sat, 27 Jan 2024 03:53:39 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc677c6186bf867e737581c8144ce09e6150804b11cea8b63a5ad1d4c51705a6`  
		Last Modified: Sat, 27 Jan 2024 03:53:39 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:8ce831c9a9bd85aaaaa936078674fee912bcb1ab6a559a10ac05bfeb88205258
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4591419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cab2da111d02d52ac4d4c3108792e47cd3b4483a442f6ad1ec888adcdc0fa0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:29:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 09:29:49 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 09:29:49 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 09:29:56 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 09:29:56 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 09:29:57 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 09:29:57 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 09:29:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 09:29:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b7c245ae48f36f63fc5c01b46647a3f81f0f9c15eed37b8450c4a8f6acf4813`  
		Last Modified: Sat, 27 Jan 2024 09:30:06 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a01e2971f82c2f2015b52374f97e3eaa86424ab24628e5202bc501ff7cc55f`  
		Last Modified: Sat, 27 Jan 2024 09:30:07 GMT  
		Size: 1.2 MB (1236766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3317277e0d843266a95b229df043b700dcd3be7294bf12f7772982cecce35a0a`  
		Last Modified: Sat, 27 Jan 2024 09:30:07 GMT  
		Size: 205.9 KB (205855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe542138d0182af83ab0348a6ad629fd96d9f51a8c11af831827488c66fe9ead`  
		Last Modified: Sat, 27 Jan 2024 09:30:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8730b4279c13c83155000948a3a668ef61f646291e4eb110261402e0306892`  
		Last Modified: Sat, 27 Jan 2024 09:30:06 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:6942a5aad13c9c0357adaa915683aa0841283c335001c09fefec4834207fe8db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4266572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ac9b14691221a3a70d3ce535e8a310dbb261aa500240fb5ff06ec64c51205a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 10:00:45 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 10:00:47 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 10:00:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 10:00:54 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 10:00:54 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 10:00:54 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 10:00:54 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 10:00:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 10:00:54 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b25927e775c6b583d50d82035663da8e070092f5179da4474850e0328ad14bb`  
		Last Modified: Sat, 27 Jan 2024 10:01:06 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:570c06b7a65d23f9b1b3ad7304bb3cfcfe3add9daf5f39922433e6832b4b01c3`  
		Last Modified: Sat, 27 Jan 2024 10:01:06 GMT  
		Size: 1.2 MB (1163906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7ebfc2c419f514f89fb6622c744006a791608d9e5ec7b54919a91d1efc0261`  
		Last Modified: Sat, 27 Jan 2024 10:01:07 GMT  
		Size: 199.5 KB (199536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0f599b0ec5b6d56ec2ba25d5fbaae221270e0e08d87a0e37f50fdc37d74736`  
		Last Modified: Sat, 27 Jan 2024 10:01:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb96c25e72b85a60641b35a0c7b1fff4fe6ddce5ec193d8abd51da0578aa10fd`  
		Last Modified: Sat, 27 Jan 2024 10:01:06 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:1e10f9c4cd5a0e555299d647aee397159cf3cc9c49ebae9d37f43d785efc2384
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4913491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a23f576db03337acb2a717f8e576bcec70c8cf09d4730860e3ba311eaef323`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:09:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 09:09:58 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 09:09:59 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 09:10:06 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 09:10:06 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 09:10:06 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 09:10:06 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 09:10:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 09:10:06 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8856182d07b0c02f8d441ffc00e795edcd647f6c5641b66df213b4f37cce4225`  
		Last Modified: Sat, 27 Jan 2024 09:10:17 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278472923ca4d7acdc0bc5101538bba2be4bc9817efad8bee80b7403ec35a8f4`  
		Last Modified: Sat, 27 Jan 2024 09:10:18 GMT  
		Size: 1.4 MB (1362704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07330ac41b8ac7b1962cf975117db9bb85969a5f9c58c66a15a065b85ccb4900`  
		Last Modified: Sat, 27 Jan 2024 09:10:17 GMT  
		Size: 215.7 KB (215689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5751cd73d323468ab539e9b67218720747135bed806a1395d8518fc12f72ca0`  
		Last Modified: Sat, 27 Jan 2024 09:10:17 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7703ff668a2070168836bbffb2f18084d597d189a2e555d423d14e72f416ef68`  
		Last Modified: Sat, 27 Jan 2024 09:10:17 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; 386

```console
$ docker pull spiped@sha256:d3a824307ae8cc220762e6f2043727e060fa6c3a918513c7d6dc167f588c220c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4826330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:399c596c03762587fa8fb8f210f5fc0ee2e6948e2905a3c8bec2a2ec243123fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:23 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Sat, 27 Jan 2024 00:38:23 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 07:52:17 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 07:52:18 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 07:52:18 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 07:52:31 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 07:52:31 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 07:52:31 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 07:52:31 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 07:52:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 07:52:32 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd471e9831f61183ecc69596284cb73f5ad30faee2d88b9be671b2e4ac9127c`  
		Last Modified: Sat, 27 Jan 2024 07:52:44 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdd3381a2456733e62fd73e208da969fc736e142d3dfc59d9c20574d6a03b20`  
		Last Modified: Sat, 27 Jan 2024 07:52:45 GMT  
		Size: 1.4 MB (1353891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c859820ed9aaf3367c0aef4d952f366e5e3a87cc24b68f63aa90e96ad7c760bf`  
		Last Modified: Sat, 27 Jan 2024 07:52:44 GMT  
		Size: 231.6 KB (231637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8281c045fc7e2e825eaafe157921bfeb141287f288180c08b32aeb520210886`  
		Last Modified: Sat, 27 Jan 2024 07:52:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a217ef75062c5c1546aec015509ac1e9cd1196309bf2416b9cf2946ca8023ed5`  
		Last Modified: Sat, 27 Jan 2024 07:52:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:e1caf5c06d70c575f68a2cfc9d1f28866de40ffc4538386849eab4457b11dd05
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4931986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2b22668c6ed4bd4242ee6b0823d1bb1e89f0cbf12f4f006c8e3c9e5c0bf946c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 06:56:45 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 06:56:49 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 06:56:51 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 06:57:04 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 06:57:06 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 06:57:12 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 06:57:12 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 06:57:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 06:57:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f38342a65739ff156e510b0402148c23bd29070f31cd8094ce9dcb6103c642c`  
		Last Modified: Sat, 27 Jan 2024 06:57:33 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4741e7cfa5277c2b562fbf0c5b2ad4315ce86d9e85b18dbc8048c6f2a59674ce`  
		Last Modified: Sat, 27 Jan 2024 06:57:34 GMT  
		Size: 1.4 MB (1361740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb83ebefffb65a8041304caea5b161380e4bcc9f83e3850a37f1a9215bb48bf`  
		Last Modified: Sat, 27 Jan 2024 06:57:34 GMT  
		Size: 220.0 KB (220022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86d9e19ad5862b1c9e0f209808dbf8b0d955cc8133e5fca9f9abeb2fc72e02e`  
		Last Modified: Sat, 27 Jan 2024 06:57:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3c09da5c10a6e8af149a2d66d3ec1ecd17a20e4ca69b351187d7ae16a6294d`  
		Last Modified: Sat, 27 Jan 2024 06:57:33 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:b3ac08887b93771eb3edc0900f301191ce0b2ab78f5f8bcc083d00e7ed4ef614
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4649400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d791c997a460e956f270fae0568846bc53b6326c809afe52f6f29185fa563c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:29:04 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 04:29:06 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 04:29:06 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 04:29:11 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 04:29:11 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 04:29:11 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 04:29:11 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 04:29:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 04:29:11 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94fd1e7053a9e79fdc6fb18948ee8438abdb6a673501fd245ba7199ef24334ae`  
		Last Modified: Sat, 27 Jan 2024 04:30:28 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e84b87b749a1bd8e548de258d2c03726b157ce7543a7e3c4c323484c64f3df4`  
		Last Modified: Sat, 27 Jan 2024 04:30:28 GMT  
		Size: 1.2 MB (1221487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db717c8240748de34eac9be8f3893bc45ad2632d5ab62765073e77c0dc964dce`  
		Last Modified: Sat, 27 Jan 2024 04:30:28 GMT  
		Size: 208.6 KB (208642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e6522b6475f44c3e255370c7cf9721b28c96fdcba8371cde2d371502dea270`  
		Last Modified: Sat, 27 Jan 2024 04:30:28 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d007dcbb3f6219ef0c2534135ee1816650af5ec516db978bd44eac8bb6a94027`  
		Last Modified: Sat, 27 Jan 2024 04:30:28 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6.2`

```console
$ docker pull spiped@sha256:a938dfc05bd0ae364481f50cf15ffa46a834192176e695415c6ddc3dbe042378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `spiped:1.6.2` - linux; amd64

```console
$ docker pull spiped@sha256:4ccadbc769537bc07b35d853a30b35c6bcfcfbb14b5afa1e39603961c9a1c504
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38218644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:719ab71cf6a39481230305e3f871866993446bf78b83793b6ad21eb9342a4ac1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:18 GMT
ADD file:af0f4e41d68b67ca88a1ce6297326159e18e27670d7bfc0bf5804a4e2b268cc8 in / 
# Wed, 31 Jan 2024 22:35:18 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:33:07 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 01 Feb 2024 06:33:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 06:33:11 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 01 Feb 2024 06:33:32 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 01 Feb 2024 06:33:32 GMT
VOLUME [/spiped]
# Thu, 01 Feb 2024 06:33:32 GMT
WORKDIR /spiped
# Thu, 01 Feb 2024 06:33:32 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 01 Feb 2024 06:33:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Feb 2024 06:33:33 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c57ee5000d61345aa3ee6684794a8110328e2274d9a5ae7855969d1a26394463`  
		Last Modified: Wed, 31 Jan 2024 22:39:55 GMT  
		Size: 29.2 MB (29150465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44203c61795ceb5aa717874cc1c355a9febb762aa26db4d54762e140810bbd54`  
		Last Modified: Thu, 01 Feb 2024 06:33:44 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e96bb7906b0259f589b790f2a964e471097a06ff9c7074ee37939bf8874705a`  
		Last Modified: Thu, 01 Feb 2024 06:33:45 GMT  
		Size: 2.6 MB (2591920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350c478c0a9093fe3fbcdc25bd19f449229047c45bea61c39d68fd3dcc1cc7bf`  
		Last Modified: Thu, 01 Feb 2024 06:33:46 GMT  
		Size: 6.5 MB (6474660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb52b2c13591cae666bda1051270553763a9a0bb3d7ad942ae5375fcc54a2c4`  
		Last Modified: Thu, 01 Feb 2024 06:33:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7250b86daa96d08375a28325fd62af52cdebd4a8df190afab8e656cce4e34dc`  
		Last Modified: Thu, 01 Feb 2024 06:33:44 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; arm variant v5

```console
$ docker pull spiped@sha256:b67e57b88e008cf9495661ee2ac582e540d884d7703cac52bdd25796ce7b070e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34209394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3ba318184d148d492ca1c33bce26da95c059a01ae51ada227bc61f97a0a8bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 13 Feb 2024 01:08:21 GMT
ADD file:468c16fc087244db1784e8f07bec3a1a417cd85172afa7dc960c2d1ecd1f37bc in / 
# Tue, 13 Feb 2024 01:08:21 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 03:19:26 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 13 Feb 2024 03:19:34 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 03:19:34 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 13 Feb 2024 03:20:18 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Feb 2024 03:20:18 GMT
VOLUME [/spiped]
# Tue, 13 Feb 2024 03:20:19 GMT
WORKDIR /spiped
# Tue, 13 Feb 2024 03:20:19 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 13 Feb 2024 03:20:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 03:20:19 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:e0d489e60efeee042d73afc4d45ad77014188c0ac8941f9ba5f15760d2288c3a`  
		Last Modified: Tue, 13 Feb 2024 01:13:30 GMT  
		Size: 26.9 MB (26883902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2938e571c4babe989613853227d886d5928626333e4c093c6df91b19aec5fb0a`  
		Last Modified: Tue, 13 Feb 2024 03:20:29 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81838218c39638dc1e94dcc33057179085a406b579d8a1c5373b5f346060a63`  
		Last Modified: Tue, 13 Feb 2024 03:20:30 GMT  
		Size: 2.2 MB (2185998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c82383d90854f15f62cb55494b6901cdb81348474b581d9348f9f1f8a34a3b51`  
		Last Modified: Tue, 13 Feb 2024 03:20:31 GMT  
		Size: 5.1 MB (5137895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47e2773e38f75c046da3e84e7a7b0090923df1fe1cc1dbbd8f93ce8225dc010`  
		Last Modified: Tue, 13 Feb 2024 03:20:29 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a409bade7427266fd4c9e2c0562dbc0dcc2d9ae1633f9076dda77d58995ca396`  
		Last Modified: Tue, 13 Feb 2024 03:20:29 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; arm variant v7

```console
$ docker pull spiped@sha256:e9aac91d1d18c179c5a51cd537b6f29e9292fde388f587ab78292df4ca4e2a21
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31671961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0401e2242f201e1af1e125c6b52a39ff240bcaed35ddb7ae70db1bd7b9ae2e3d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:20 GMT
ADD file:d6072ced9736ca566086eea2514cf12faccec9859bbd93e83950ad51f6827e8c in / 
# Wed, 31 Jan 2024 22:44:20 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 02:25:32 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 01 Feb 2024 02:25:36 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 02:25:36 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 01 Feb 2024 02:25:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 01 Feb 2024 02:25:56 GMT
VOLUME [/spiped]
# Thu, 01 Feb 2024 02:25:56 GMT
WORKDIR /spiped
# Thu, 01 Feb 2024 02:25:57 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 01 Feb 2024 02:25:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Feb 2024 02:25:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:404006a0fd99beed6ef1a9502692bd5005ae8c3b9d36a9b48654f7dfaacfb2c5`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 24.7 MB (24741565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f0470047587d9d6a62cea3a77a55beb2bbe272c0a66fd7e9c83ea6a19fbd6ed`  
		Last Modified: Thu, 01 Feb 2024 02:26:08 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:789649eb9a8c062d810952062c99f90c9a0a124cef3588670ee6a5fbc94a8935`  
		Last Modified: Thu, 01 Feb 2024 02:26:08 GMT  
		Size: 2.0 MB (2046255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf7678736899447540748561d2c0dba7822c0532da2d937b351ee52d2d3894aa`  
		Last Modified: Thu, 01 Feb 2024 02:26:09 GMT  
		Size: 4.9 MB (4882543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc6cd5c5c4b771dbedf160095e62642c0afaee343572c1bc3ae1d42bc6069cd`  
		Last Modified: Thu, 01 Feb 2024 02:26:08 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55cb396e9adad99fe98f84363e64919fa7e728f6080a762976e88c45e240ea87`  
		Last Modified: Thu, 01 Feb 2024 02:26:08 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:b422fe4000fdc564bc2261e42686183590617716cc42297a2bbf77db6b2ab896
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37101287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c9e8a773970c13d02591938a3ba84ac2a1885ff2df38d811ddf6128247ca799`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:26 GMT
ADD file:ef6f078c1e72fcfafb9bfeeff0c1c771219dc2efe34650963106f63d32183b49 in / 
# Wed, 31 Jan 2024 22:44:27 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 05:56:32 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 01 Feb 2024 05:56:35 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 05:56:35 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 01 Feb 2024 05:56:52 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 01 Feb 2024 05:56:53 GMT
VOLUME [/spiped]
# Thu, 01 Feb 2024 05:56:53 GMT
WORKDIR /spiped
# Thu, 01 Feb 2024 05:56:53 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 01 Feb 2024 05:56:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Feb 2024 05:56:53 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:25d3892798f8b99159e3c1136799bfed560027ce451b50d57d961f4f02577ff5`  
		Last Modified: Wed, 31 Jan 2024 22:48:07 GMT  
		Size: 29.2 MB (29180832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab70de86f0546f613f3351b6316ea1ea9a0c6562cdce9336f24d6552e0cc3b47`  
		Last Modified: Thu, 01 Feb 2024 05:57:04 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed15fb941dfb5e9137761f97b3e344916691cc8473a8d589bee58e24388cd2f7`  
		Last Modified: Thu, 01 Feb 2024 05:57:05 GMT  
		Size: 2.4 MB (2434866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b862a579330ea8f3bc50e0e60057d34b75553a18deccc7bab7a1b331ae5016`  
		Last Modified: Thu, 01 Feb 2024 05:57:05 GMT  
		Size: 5.5 MB (5483992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429251a29a2a0f675bcd3504dd3e855182dd3fbb197347f36c4e1baa6bc8303f`  
		Last Modified: Thu, 01 Feb 2024 05:57:04 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3867deda232b6d0f845d84dfd23666b4965f52bc6177bb9f4f9dd024ebbe6af`  
		Last Modified: Thu, 01 Feb 2024 05:57:04 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; 386

```console
$ docker pull spiped@sha256:af3a94935515497a1ade45fcc72c70ac050cfd1381185b8904a3c6c5c00f612a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38699213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0210fdce54e20cfde76f132661954d813e3b6a0f3993e8d9d04a53fc96fc39e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 31 Jan 2024 22:39:00 GMT
ADD file:540e2de73452bd162dd7f630bf29f60e7d2e4a7a5d32a495bedf8ad390b59d7f in / 
# Wed, 31 Jan 2024 22:39:01 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:28:50 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 31 Jan 2024 23:28:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:28:56 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 31 Jan 2024 23:29:29 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 31 Jan 2024 23:29:30 GMT
VOLUME [/spiped]
# Wed, 31 Jan 2024 23:29:30 GMT
WORKDIR /spiped
# Wed, 31 Jan 2024 23:29:30 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 31 Jan 2024 23:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Jan 2024 23:29:30 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:34ef135b45f33052e8e5bca668f9a45a938944a9cf3fb73a46f54a7bf11f091b`  
		Last Modified: Wed, 31 Jan 2024 22:43:46 GMT  
		Size: 30.2 MB (30165018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751a96ff8957608f7ad889db770d428885c2b206b3f8652b3d06872194295d78`  
		Last Modified: Wed, 31 Jan 2024 23:29:47 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53160d66b23e9b2c4404e8fbb7ddb70966b2fa0ae6fef0fcd290dc733f9866b9`  
		Last Modified: Wed, 31 Jan 2024 23:29:47 GMT  
		Size: 2.6 MB (2588154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c15a42863551b8164cceac5ac558601c2b66a6c81c590cd98e5dfe6af43dbfa4`  
		Last Modified: Wed, 31 Jan 2024 23:29:49 GMT  
		Size: 5.9 MB (5944440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e297082e00314cd0f8763f69ec7001fa8440dbd507fa8975cd5620cd5cc63d6`  
		Last Modified: Wed, 31 Jan 2024 23:29:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba709f2eb9259a79c1eec4292df8fae1b367472b00185af3340f0a963ab390c4`  
		Last Modified: Wed, 31 Jan 2024 23:29:47 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; mips64le

```console
$ docker pull spiped@sha256:6ce4d2d0d50f6e83deb694c99ecdd43098dd3e8d5741391f4299b075b03a043f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36784313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04a7ca6e08978ccba1c67b528ff59cb65d5ffc61df8decfa703a154e5cf0fda1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 31 Jan 2024 22:27:13 GMT
ADD file:c38ae3175b2ea7bff74f0e28558af27158de7697be9142ed9d681c4d37b24e35 in / 
# Wed, 31 Jan 2024 22:27:17 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 11:09:49 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 01 Feb 2024 11:10:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 11:10:12 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 01 Feb 2024 11:11:58 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 01 Feb 2024 11:12:01 GMT
VOLUME [/spiped]
# Thu, 01 Feb 2024 11:12:04 GMT
WORKDIR /spiped
# Thu, 01 Feb 2024 11:12:06 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 01 Feb 2024 11:12:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Feb 2024 11:12:12 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:21bfa6f58b3ab30099793f844be56212a593fddbf3f030cd8c42b38a1dcefcff`  
		Last Modified: Wed, 31 Jan 2024 22:38:21 GMT  
		Size: 29.1 MB (29142437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c86ec7ab62c6acb9250eba5339643c146a5e73365420e68d7acb3e218bdacd57`  
		Last Modified: Thu, 01 Feb 2024 11:12:33 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea4b98fda2b541f972777b687167057487d97a7201574da0b7eebe255d46e1a`  
		Last Modified: Thu, 01 Feb 2024 11:12:35 GMT  
		Size: 1.8 MB (1834351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a784d99cbd8a4388e1a1943324e49b064d6f2dee4c80dafed2855dcc71b1f0`  
		Last Modified: Thu, 01 Feb 2024 11:12:38 GMT  
		Size: 5.8 MB (5806014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b288162c33595db1d26d19277130f65a6dcd72972f3cbd54812c14fb44ffabd8`  
		Last Modified: Thu, 01 Feb 2024 11:12:33 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43ddcf2cc851edfe7424b2bbfecc440922c44231bc57f9a2a827a78a1ffe941`  
		Last Modified: Thu, 01 Feb 2024 11:12:33 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; ppc64le

```console
$ docker pull spiped@sha256:64c5c55b229219480ea25215bdab6b03b1f345286ecbc63dc3f869e1ce330b3e
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42311916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59508d985231a098bed6b2ae23582037f4e79ddfe90b8a2f294822913213b7d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:03 GMT
ADD file:b65bdf3d9277efbf6bbf8bf0121f92bdcd342ed0c4f49f1cee3b91adafacd76c in / 
# Tue, 13 Feb 2024 00:39:05 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 03:44:05 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 13 Feb 2024 03:44:10 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 03:44:10 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 13 Feb 2024 03:45:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Feb 2024 03:45:11 GMT
VOLUME [/spiped]
# Tue, 13 Feb 2024 03:45:12 GMT
WORKDIR /spiped
# Tue, 13 Feb 2024 03:45:12 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 13 Feb 2024 03:45:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 03:45:13 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b1cce6d9947985e4270ac998aa258401bc5deca94d504040a14f9f3c47258d68`  
		Last Modified: Tue, 13 Feb 2024 00:43:56 GMT  
		Size: 33.1 MB (33118908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28eab5449fc59b53e9f2279940a43c6d3a3fd364d96fa2c3d2922cbc5de81e1b`  
		Last Modified: Tue, 13 Feb 2024 03:45:38 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:725f98f5d63a98ff542ad7b2403dd5c368b4ebb1a8856490eecd72bae96151a6`  
		Last Modified: Tue, 13 Feb 2024 03:45:38 GMT  
		Size: 2.8 MB (2769282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d6df2553e038156a19aa44c6722f55beeb50690123dd9f30ced381006e9e7a8`  
		Last Modified: Tue, 13 Feb 2024 03:45:39 GMT  
		Size: 6.4 MB (6422129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:360a23e225035c41d84713834b9665254b25b1888bdbeca5ac335fb5955fdfa6`  
		Last Modified: Tue, 13 Feb 2024 03:45:38 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8256250ad5ac412b1f0b34de7655074aeb8f3347b40f7226af075854090e891a`  
		Last Modified: Tue, 13 Feb 2024 03:45:38 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; s390x

```console
$ docker pull spiped@sha256:237c566ae2695688605457ce444873bacc827c72a5dab859f380f431cf8435fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.2 MB (35165793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab5dc818013c2717f8a89991acd65937b38331f6e81aae94516a765057ed63f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 31 Jan 2024 22:58:51 GMT
ADD file:d543e4bc70d0d1d81c594a97289d7f2b4925d86461644cf881890997abfb6ead in / 
# Wed, 31 Jan 2024 22:58:53 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 05:54:15 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 01 Feb 2024 05:54:19 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 05:54:19 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 01 Feb 2024 05:54:51 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 01 Feb 2024 05:54:52 GMT
VOLUME [/spiped]
# Thu, 01 Feb 2024 05:54:52 GMT
WORKDIR /spiped
# Thu, 01 Feb 2024 05:54:53 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 01 Feb 2024 05:54:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Feb 2024 05:54:53 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:84abfb784f629f520e19ebd281090b7f1b3b78ff96b3be919578a053d2708ad5`  
		Last Modified: Wed, 31 Jan 2024 23:29:10 GMT  
		Size: 27.5 MB (27513479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9096f642a1ac565ee2d5c07e0d0cf6e1bf955b8b0844bfef49d774de9bfcde`  
		Last Modified: Thu, 01 Feb 2024 05:57:44 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d2aef7174c2e6a7a1c9d301f1c42480cfe91e8854437e9401d6d09be37e8b6`  
		Last Modified: Thu, 01 Feb 2024 05:57:45 GMT  
		Size: 2.3 MB (2262471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc72cc5f176534103dfa802d29e26026288813d1b7db888527e71d18a695e3a`  
		Last Modified: Thu, 01 Feb 2024 05:57:45 GMT  
		Size: 5.4 MB (5388243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5820f59a9ec53afbe9859e889d57ec691f07ff8774a6e3d6131dd2f3916ff9`  
		Last Modified: Thu, 01 Feb 2024 05:57:44 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a83e6ca20ca5ee69c588a377a2897bb10e1c3f3d149b3bf42517d7b6fe686e0`  
		Last Modified: Thu, 01 Feb 2024 05:57:44 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6.2-alpine`

```console
$ docker pull spiped@sha256:f84d8a95e3e950b92f95d85b787be2683a48c95bce66e074dc979bb1fadf87f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `spiped:1.6.2-alpine` - linux; amd64

```console
$ docker pull spiped@sha256:0db343ac47d10615e10448e605656eb7d9f8a7355742c16d724da24cf8bc8200
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5058548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c3fac6726c34597dbefe1ed2357ed9a503e3e9fbee4de673c7329536ec6690`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:53:15 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 03:53:16 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 03:53:16 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 03:53:26 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 03:53:26 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 03:53:26 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 03:53:27 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 03:53:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 03:53:27 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233335b905cdbc6ef4fd933dc93fa62f3181b6bd01639a4f13fd5686f1e60d13`  
		Last Modified: Sat, 27 Jan 2024 03:53:39 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd31ddc1313d2d26e7d3bf86684929340ae1c767c9023291012725885f68aed3`  
		Last Modified: Sat, 27 Jan 2024 03:53:39 GMT  
		Size: 1.4 MB (1432997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c381fda201d7dc3075b77745e2944ca6c6ed05b2b4a637483745ef7f435c81`  
		Last Modified: Sat, 27 Jan 2024 03:53:39 GMT  
		Size: 221.3 KB (221268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aeb01bcfc8c133af082c950a536224f400f37222340e8485ecb27f7730763b9`  
		Last Modified: Sat, 27 Jan 2024 03:53:39 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc677c6186bf867e737581c8144ce09e6150804b11cea8b63a5ad1d4c51705a6`  
		Last Modified: Sat, 27 Jan 2024 03:53:39 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:8ce831c9a9bd85aaaaa936078674fee912bcb1ab6a559a10ac05bfeb88205258
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4591419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cab2da111d02d52ac4d4c3108792e47cd3b4483a442f6ad1ec888adcdc0fa0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:29:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 09:29:49 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 09:29:49 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 09:29:56 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 09:29:56 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 09:29:57 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 09:29:57 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 09:29:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 09:29:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b7c245ae48f36f63fc5c01b46647a3f81f0f9c15eed37b8450c4a8f6acf4813`  
		Last Modified: Sat, 27 Jan 2024 09:30:06 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a01e2971f82c2f2015b52374f97e3eaa86424ab24628e5202bc501ff7cc55f`  
		Last Modified: Sat, 27 Jan 2024 09:30:07 GMT  
		Size: 1.2 MB (1236766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3317277e0d843266a95b229df043b700dcd3be7294bf12f7772982cecce35a0a`  
		Last Modified: Sat, 27 Jan 2024 09:30:07 GMT  
		Size: 205.9 KB (205855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe542138d0182af83ab0348a6ad629fd96d9f51a8c11af831827488c66fe9ead`  
		Last Modified: Sat, 27 Jan 2024 09:30:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8730b4279c13c83155000948a3a668ef61f646291e4eb110261402e0306892`  
		Last Modified: Sat, 27 Jan 2024 09:30:06 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:6942a5aad13c9c0357adaa915683aa0841283c335001c09fefec4834207fe8db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4266572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ac9b14691221a3a70d3ce535e8a310dbb261aa500240fb5ff06ec64c51205a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 10:00:45 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 10:00:47 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 10:00:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 10:00:54 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 10:00:54 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 10:00:54 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 10:00:54 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 10:00:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 10:00:54 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b25927e775c6b583d50d82035663da8e070092f5179da4474850e0328ad14bb`  
		Last Modified: Sat, 27 Jan 2024 10:01:06 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:570c06b7a65d23f9b1b3ad7304bb3cfcfe3add9daf5f39922433e6832b4b01c3`  
		Last Modified: Sat, 27 Jan 2024 10:01:06 GMT  
		Size: 1.2 MB (1163906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7ebfc2c419f514f89fb6622c744006a791608d9e5ec7b54919a91d1efc0261`  
		Last Modified: Sat, 27 Jan 2024 10:01:07 GMT  
		Size: 199.5 KB (199536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0f599b0ec5b6d56ec2ba25d5fbaae221270e0e08d87a0e37f50fdc37d74736`  
		Last Modified: Sat, 27 Jan 2024 10:01:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb96c25e72b85a60641b35a0c7b1fff4fe6ddce5ec193d8abd51da0578aa10fd`  
		Last Modified: Sat, 27 Jan 2024 10:01:06 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:1e10f9c4cd5a0e555299d647aee397159cf3cc9c49ebae9d37f43d785efc2384
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4913491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a23f576db03337acb2a717f8e576bcec70c8cf09d4730860e3ba311eaef323`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:09:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 09:09:58 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 09:09:59 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 09:10:06 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 09:10:06 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 09:10:06 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 09:10:06 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 09:10:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 09:10:06 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8856182d07b0c02f8d441ffc00e795edcd647f6c5641b66df213b4f37cce4225`  
		Last Modified: Sat, 27 Jan 2024 09:10:17 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278472923ca4d7acdc0bc5101538bba2be4bc9817efad8bee80b7403ec35a8f4`  
		Last Modified: Sat, 27 Jan 2024 09:10:18 GMT  
		Size: 1.4 MB (1362704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07330ac41b8ac7b1962cf975117db9bb85969a5f9c58c66a15a065b85ccb4900`  
		Last Modified: Sat, 27 Jan 2024 09:10:17 GMT  
		Size: 215.7 KB (215689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5751cd73d323468ab539e9b67218720747135bed806a1395d8518fc12f72ca0`  
		Last Modified: Sat, 27 Jan 2024 09:10:17 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7703ff668a2070168836bbffb2f18084d597d189a2e555d423d14e72f416ef68`  
		Last Modified: Sat, 27 Jan 2024 09:10:17 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; 386

```console
$ docker pull spiped@sha256:d3a824307ae8cc220762e6f2043727e060fa6c3a918513c7d6dc167f588c220c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4826330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:399c596c03762587fa8fb8f210f5fc0ee2e6948e2905a3c8bec2a2ec243123fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:23 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Sat, 27 Jan 2024 00:38:23 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 07:52:17 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 07:52:18 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 07:52:18 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 07:52:31 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 07:52:31 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 07:52:31 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 07:52:31 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 07:52:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 07:52:32 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd471e9831f61183ecc69596284cb73f5ad30faee2d88b9be671b2e4ac9127c`  
		Last Modified: Sat, 27 Jan 2024 07:52:44 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdd3381a2456733e62fd73e208da969fc736e142d3dfc59d9c20574d6a03b20`  
		Last Modified: Sat, 27 Jan 2024 07:52:45 GMT  
		Size: 1.4 MB (1353891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c859820ed9aaf3367c0aef4d952f366e5e3a87cc24b68f63aa90e96ad7c760bf`  
		Last Modified: Sat, 27 Jan 2024 07:52:44 GMT  
		Size: 231.6 KB (231637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8281c045fc7e2e825eaafe157921bfeb141287f288180c08b32aeb520210886`  
		Last Modified: Sat, 27 Jan 2024 07:52:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a217ef75062c5c1546aec015509ac1e9cd1196309bf2416b9cf2946ca8023ed5`  
		Last Modified: Sat, 27 Jan 2024 07:52:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:e1caf5c06d70c575f68a2cfc9d1f28866de40ffc4538386849eab4457b11dd05
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4931986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2b22668c6ed4bd4242ee6b0823d1bb1e89f0cbf12f4f006c8e3c9e5c0bf946c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 06:56:45 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 06:56:49 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 06:56:51 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 06:57:04 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 06:57:06 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 06:57:12 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 06:57:12 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 06:57:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 06:57:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f38342a65739ff156e510b0402148c23bd29070f31cd8094ce9dcb6103c642c`  
		Last Modified: Sat, 27 Jan 2024 06:57:33 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4741e7cfa5277c2b562fbf0c5b2ad4315ce86d9e85b18dbc8048c6f2a59674ce`  
		Last Modified: Sat, 27 Jan 2024 06:57:34 GMT  
		Size: 1.4 MB (1361740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb83ebefffb65a8041304caea5b161380e4bcc9f83e3850a37f1a9215bb48bf`  
		Last Modified: Sat, 27 Jan 2024 06:57:34 GMT  
		Size: 220.0 KB (220022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86d9e19ad5862b1c9e0f209808dbf8b0d955cc8133e5fca9f9abeb2fc72e02e`  
		Last Modified: Sat, 27 Jan 2024 06:57:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3c09da5c10a6e8af149a2d66d3ec1ecd17a20e4ca69b351187d7ae16a6294d`  
		Last Modified: Sat, 27 Jan 2024 06:57:33 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:b3ac08887b93771eb3edc0900f301191ce0b2ab78f5f8bcc083d00e7ed4ef614
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4649400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d791c997a460e956f270fae0568846bc53b6326c809afe52f6f29185fa563c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:29:04 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 04:29:06 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 04:29:06 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 04:29:11 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 04:29:11 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 04:29:11 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 04:29:11 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 04:29:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 04:29:11 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94fd1e7053a9e79fdc6fb18948ee8438abdb6a673501fd245ba7199ef24334ae`  
		Last Modified: Sat, 27 Jan 2024 04:30:28 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e84b87b749a1bd8e548de258d2c03726b157ce7543a7e3c4c323484c64f3df4`  
		Last Modified: Sat, 27 Jan 2024 04:30:28 GMT  
		Size: 1.2 MB (1221487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db717c8240748de34eac9be8f3893bc45ad2632d5ab62765073e77c0dc964dce`  
		Last Modified: Sat, 27 Jan 2024 04:30:28 GMT  
		Size: 208.6 KB (208642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e6522b6475f44c3e255370c7cf9721b28c96fdcba8371cde2d371502dea270`  
		Last Modified: Sat, 27 Jan 2024 04:30:28 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d007dcbb3f6219ef0c2534135ee1816650af5ec516db978bd44eac8bb6a94027`  
		Last Modified: Sat, 27 Jan 2024 04:30:28 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:alpine`

```console
$ docker pull spiped@sha256:f84d8a95e3e950b92f95d85b787be2683a48c95bce66e074dc979bb1fadf87f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `spiped:alpine` - linux; amd64

```console
$ docker pull spiped@sha256:0db343ac47d10615e10448e605656eb7d9f8a7355742c16d724da24cf8bc8200
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5058548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c3fac6726c34597dbefe1ed2357ed9a503e3e9fbee4de673c7329536ec6690`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:53:15 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 03:53:16 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 03:53:16 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 03:53:26 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 03:53:26 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 03:53:26 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 03:53:27 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 03:53:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 03:53:27 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233335b905cdbc6ef4fd933dc93fa62f3181b6bd01639a4f13fd5686f1e60d13`  
		Last Modified: Sat, 27 Jan 2024 03:53:39 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd31ddc1313d2d26e7d3bf86684929340ae1c767c9023291012725885f68aed3`  
		Last Modified: Sat, 27 Jan 2024 03:53:39 GMT  
		Size: 1.4 MB (1432997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c381fda201d7dc3075b77745e2944ca6c6ed05b2b4a637483745ef7f435c81`  
		Last Modified: Sat, 27 Jan 2024 03:53:39 GMT  
		Size: 221.3 KB (221268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aeb01bcfc8c133af082c950a536224f400f37222340e8485ecb27f7730763b9`  
		Last Modified: Sat, 27 Jan 2024 03:53:39 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc677c6186bf867e737581c8144ce09e6150804b11cea8b63a5ad1d4c51705a6`  
		Last Modified: Sat, 27 Jan 2024 03:53:39 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:8ce831c9a9bd85aaaaa936078674fee912bcb1ab6a559a10ac05bfeb88205258
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4591419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cab2da111d02d52ac4d4c3108792e47cd3b4483a442f6ad1ec888adcdc0fa0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:29:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 09:29:49 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 09:29:49 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 09:29:56 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 09:29:56 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 09:29:57 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 09:29:57 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 09:29:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 09:29:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b7c245ae48f36f63fc5c01b46647a3f81f0f9c15eed37b8450c4a8f6acf4813`  
		Last Modified: Sat, 27 Jan 2024 09:30:06 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a01e2971f82c2f2015b52374f97e3eaa86424ab24628e5202bc501ff7cc55f`  
		Last Modified: Sat, 27 Jan 2024 09:30:07 GMT  
		Size: 1.2 MB (1236766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3317277e0d843266a95b229df043b700dcd3be7294bf12f7772982cecce35a0a`  
		Last Modified: Sat, 27 Jan 2024 09:30:07 GMT  
		Size: 205.9 KB (205855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe542138d0182af83ab0348a6ad629fd96d9f51a8c11af831827488c66fe9ead`  
		Last Modified: Sat, 27 Jan 2024 09:30:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8730b4279c13c83155000948a3a668ef61f646291e4eb110261402e0306892`  
		Last Modified: Sat, 27 Jan 2024 09:30:06 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:6942a5aad13c9c0357adaa915683aa0841283c335001c09fefec4834207fe8db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4266572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ac9b14691221a3a70d3ce535e8a310dbb261aa500240fb5ff06ec64c51205a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 10:00:45 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 10:00:47 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 10:00:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 10:00:54 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 10:00:54 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 10:00:54 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 10:00:54 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 10:00:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 10:00:54 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b25927e775c6b583d50d82035663da8e070092f5179da4474850e0328ad14bb`  
		Last Modified: Sat, 27 Jan 2024 10:01:06 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:570c06b7a65d23f9b1b3ad7304bb3cfcfe3add9daf5f39922433e6832b4b01c3`  
		Last Modified: Sat, 27 Jan 2024 10:01:06 GMT  
		Size: 1.2 MB (1163906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7ebfc2c419f514f89fb6622c744006a791608d9e5ec7b54919a91d1efc0261`  
		Last Modified: Sat, 27 Jan 2024 10:01:07 GMT  
		Size: 199.5 KB (199536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0f599b0ec5b6d56ec2ba25d5fbaae221270e0e08d87a0e37f50fdc37d74736`  
		Last Modified: Sat, 27 Jan 2024 10:01:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb96c25e72b85a60641b35a0c7b1fff4fe6ddce5ec193d8abd51da0578aa10fd`  
		Last Modified: Sat, 27 Jan 2024 10:01:06 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:1e10f9c4cd5a0e555299d647aee397159cf3cc9c49ebae9d37f43d785efc2384
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4913491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a23f576db03337acb2a717f8e576bcec70c8cf09d4730860e3ba311eaef323`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:09:57 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 09:09:58 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 09:09:59 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 09:10:06 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 09:10:06 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 09:10:06 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 09:10:06 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 09:10:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 09:10:06 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8856182d07b0c02f8d441ffc00e795edcd647f6c5641b66df213b4f37cce4225`  
		Last Modified: Sat, 27 Jan 2024 09:10:17 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278472923ca4d7acdc0bc5101538bba2be4bc9817efad8bee80b7403ec35a8f4`  
		Last Modified: Sat, 27 Jan 2024 09:10:18 GMT  
		Size: 1.4 MB (1362704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07330ac41b8ac7b1962cf975117db9bb85969a5f9c58c66a15a065b85ccb4900`  
		Last Modified: Sat, 27 Jan 2024 09:10:17 GMT  
		Size: 215.7 KB (215689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5751cd73d323468ab539e9b67218720747135bed806a1395d8518fc12f72ca0`  
		Last Modified: Sat, 27 Jan 2024 09:10:17 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7703ff668a2070168836bbffb2f18084d597d189a2e555d423d14e72f416ef68`  
		Last Modified: Sat, 27 Jan 2024 09:10:17 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; 386

```console
$ docker pull spiped@sha256:d3a824307ae8cc220762e6f2043727e060fa6c3a918513c7d6dc167f588c220c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4826330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:399c596c03762587fa8fb8f210f5fc0ee2e6948e2905a3c8bec2a2ec243123fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:23 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Sat, 27 Jan 2024 00:38:23 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 07:52:17 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 07:52:18 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 07:52:18 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 07:52:31 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 07:52:31 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 07:52:31 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 07:52:31 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 07:52:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 07:52:32 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd471e9831f61183ecc69596284cb73f5ad30faee2d88b9be671b2e4ac9127c`  
		Last Modified: Sat, 27 Jan 2024 07:52:44 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdd3381a2456733e62fd73e208da969fc736e142d3dfc59d9c20574d6a03b20`  
		Last Modified: Sat, 27 Jan 2024 07:52:45 GMT  
		Size: 1.4 MB (1353891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c859820ed9aaf3367c0aef4d952f366e5e3a87cc24b68f63aa90e96ad7c760bf`  
		Last Modified: Sat, 27 Jan 2024 07:52:44 GMT  
		Size: 231.6 KB (231637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8281c045fc7e2e825eaafe157921bfeb141287f288180c08b32aeb520210886`  
		Last Modified: Sat, 27 Jan 2024 07:52:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a217ef75062c5c1546aec015509ac1e9cd1196309bf2416b9cf2946ca8023ed5`  
		Last Modified: Sat, 27 Jan 2024 07:52:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:e1caf5c06d70c575f68a2cfc9d1f28866de40ffc4538386849eab4457b11dd05
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4931986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2b22668c6ed4bd4242ee6b0823d1bb1e89f0cbf12f4f006c8e3c9e5c0bf946c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 06:56:45 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 06:56:49 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 06:56:51 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 06:57:04 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 06:57:06 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 06:57:12 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 06:57:12 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 06:57:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 06:57:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f38342a65739ff156e510b0402148c23bd29070f31cd8094ce9dcb6103c642c`  
		Last Modified: Sat, 27 Jan 2024 06:57:33 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4741e7cfa5277c2b562fbf0c5b2ad4315ce86d9e85b18dbc8048c6f2a59674ce`  
		Last Modified: Sat, 27 Jan 2024 06:57:34 GMT  
		Size: 1.4 MB (1361740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb83ebefffb65a8041304caea5b161380e4bcc9f83e3850a37f1a9215bb48bf`  
		Last Modified: Sat, 27 Jan 2024 06:57:34 GMT  
		Size: 220.0 KB (220022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86d9e19ad5862b1c9e0f209808dbf8b0d955cc8133e5fca9f9abeb2fc72e02e`  
		Last Modified: Sat, 27 Jan 2024 06:57:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3c09da5c10a6e8af149a2d66d3ec1ecd17a20e4ca69b351187d7ae16a6294d`  
		Last Modified: Sat, 27 Jan 2024 06:57:33 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; s390x

```console
$ docker pull spiped@sha256:b3ac08887b93771eb3edc0900f301191ce0b2ab78f5f8bcc083d00e7ed4ef614
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4649400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d791c997a460e956f270fae0568846bc53b6326c809afe52f6f29185fa563c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:29:04 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 27 Jan 2024 04:29:06 GMT
RUN apk add --no-cache libssl1.1
# Sat, 27 Jan 2024 04:29:06 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 27 Jan 2024 04:29:11 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 27 Jan 2024 04:29:11 GMT
VOLUME [/spiped]
# Sat, 27 Jan 2024 04:29:11 GMT
WORKDIR /spiped
# Sat, 27 Jan 2024 04:29:11 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 27 Jan 2024 04:29:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 04:29:11 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94fd1e7053a9e79fdc6fb18948ee8438abdb6a673501fd245ba7199ef24334ae`  
		Last Modified: Sat, 27 Jan 2024 04:30:28 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e84b87b749a1bd8e548de258d2c03726b157ce7543a7e3c4c323484c64f3df4`  
		Last Modified: Sat, 27 Jan 2024 04:30:28 GMT  
		Size: 1.2 MB (1221487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db717c8240748de34eac9be8f3893bc45ad2632d5ab62765073e77c0dc964dce`  
		Last Modified: Sat, 27 Jan 2024 04:30:28 GMT  
		Size: 208.6 KB (208642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e6522b6475f44c3e255370c7cf9721b28c96fdcba8371cde2d371502dea270`  
		Last Modified: Sat, 27 Jan 2024 04:30:28 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d007dcbb3f6219ef0c2534135ee1816650af5ec516db978bd44eac8bb6a94027`  
		Last Modified: Sat, 27 Jan 2024 04:30:28 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:latest`

```console
$ docker pull spiped@sha256:a938dfc05bd0ae364481f50cf15ffa46a834192176e695415c6ddc3dbe042378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `spiped:latest` - linux; amd64

```console
$ docker pull spiped@sha256:4ccadbc769537bc07b35d853a30b35c6bcfcfbb14b5afa1e39603961c9a1c504
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38218644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:719ab71cf6a39481230305e3f871866993446bf78b83793b6ad21eb9342a4ac1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:18 GMT
ADD file:af0f4e41d68b67ca88a1ce6297326159e18e27670d7bfc0bf5804a4e2b268cc8 in / 
# Wed, 31 Jan 2024 22:35:18 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:33:07 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 01 Feb 2024 06:33:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 06:33:11 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 01 Feb 2024 06:33:32 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 01 Feb 2024 06:33:32 GMT
VOLUME [/spiped]
# Thu, 01 Feb 2024 06:33:32 GMT
WORKDIR /spiped
# Thu, 01 Feb 2024 06:33:32 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 01 Feb 2024 06:33:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Feb 2024 06:33:33 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c57ee5000d61345aa3ee6684794a8110328e2274d9a5ae7855969d1a26394463`  
		Last Modified: Wed, 31 Jan 2024 22:39:55 GMT  
		Size: 29.2 MB (29150465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44203c61795ceb5aa717874cc1c355a9febb762aa26db4d54762e140810bbd54`  
		Last Modified: Thu, 01 Feb 2024 06:33:44 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e96bb7906b0259f589b790f2a964e471097a06ff9c7074ee37939bf8874705a`  
		Last Modified: Thu, 01 Feb 2024 06:33:45 GMT  
		Size: 2.6 MB (2591920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350c478c0a9093fe3fbcdc25bd19f449229047c45bea61c39d68fd3dcc1cc7bf`  
		Last Modified: Thu, 01 Feb 2024 06:33:46 GMT  
		Size: 6.5 MB (6474660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb52b2c13591cae666bda1051270553763a9a0bb3d7ad942ae5375fcc54a2c4`  
		Last Modified: Thu, 01 Feb 2024 06:33:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7250b86daa96d08375a28325fd62af52cdebd4a8df190afab8e656cce4e34dc`  
		Last Modified: Thu, 01 Feb 2024 06:33:44 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; arm variant v5

```console
$ docker pull spiped@sha256:b67e57b88e008cf9495661ee2ac582e540d884d7703cac52bdd25796ce7b070e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34209394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3ba318184d148d492ca1c33bce26da95c059a01ae51ada227bc61f97a0a8bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 13 Feb 2024 01:08:21 GMT
ADD file:468c16fc087244db1784e8f07bec3a1a417cd85172afa7dc960c2d1ecd1f37bc in / 
# Tue, 13 Feb 2024 01:08:21 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 03:19:26 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 13 Feb 2024 03:19:34 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 03:19:34 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 13 Feb 2024 03:20:18 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Feb 2024 03:20:18 GMT
VOLUME [/spiped]
# Tue, 13 Feb 2024 03:20:19 GMT
WORKDIR /spiped
# Tue, 13 Feb 2024 03:20:19 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 13 Feb 2024 03:20:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 03:20:19 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:e0d489e60efeee042d73afc4d45ad77014188c0ac8941f9ba5f15760d2288c3a`  
		Last Modified: Tue, 13 Feb 2024 01:13:30 GMT  
		Size: 26.9 MB (26883902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2938e571c4babe989613853227d886d5928626333e4c093c6df91b19aec5fb0a`  
		Last Modified: Tue, 13 Feb 2024 03:20:29 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81838218c39638dc1e94dcc33057179085a406b579d8a1c5373b5f346060a63`  
		Last Modified: Tue, 13 Feb 2024 03:20:30 GMT  
		Size: 2.2 MB (2185998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c82383d90854f15f62cb55494b6901cdb81348474b581d9348f9f1f8a34a3b51`  
		Last Modified: Tue, 13 Feb 2024 03:20:31 GMT  
		Size: 5.1 MB (5137895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47e2773e38f75c046da3e84e7a7b0090923df1fe1cc1dbbd8f93ce8225dc010`  
		Last Modified: Tue, 13 Feb 2024 03:20:29 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a409bade7427266fd4c9e2c0562dbc0dcc2d9ae1633f9076dda77d58995ca396`  
		Last Modified: Tue, 13 Feb 2024 03:20:29 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; arm variant v7

```console
$ docker pull spiped@sha256:e9aac91d1d18c179c5a51cd537b6f29e9292fde388f587ab78292df4ca4e2a21
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.7 MB (31671961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0401e2242f201e1af1e125c6b52a39ff240bcaed35ddb7ae70db1bd7b9ae2e3d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:20 GMT
ADD file:d6072ced9736ca566086eea2514cf12faccec9859bbd93e83950ad51f6827e8c in / 
# Wed, 31 Jan 2024 22:44:20 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 02:25:32 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 01 Feb 2024 02:25:36 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 02:25:36 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 01 Feb 2024 02:25:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 01 Feb 2024 02:25:56 GMT
VOLUME [/spiped]
# Thu, 01 Feb 2024 02:25:56 GMT
WORKDIR /spiped
# Thu, 01 Feb 2024 02:25:57 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 01 Feb 2024 02:25:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Feb 2024 02:25:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:404006a0fd99beed6ef1a9502692bd5005ae8c3b9d36a9b48654f7dfaacfb2c5`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 24.7 MB (24741565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f0470047587d9d6a62cea3a77a55beb2bbe272c0a66fd7e9c83ea6a19fbd6ed`  
		Last Modified: Thu, 01 Feb 2024 02:26:08 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:789649eb9a8c062d810952062c99f90c9a0a124cef3588670ee6a5fbc94a8935`  
		Last Modified: Thu, 01 Feb 2024 02:26:08 GMT  
		Size: 2.0 MB (2046255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf7678736899447540748561d2c0dba7822c0532da2d937b351ee52d2d3894aa`  
		Last Modified: Thu, 01 Feb 2024 02:26:09 GMT  
		Size: 4.9 MB (4882543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc6cd5c5c4b771dbedf160095e62642c0afaee343572c1bc3ae1d42bc6069cd`  
		Last Modified: Thu, 01 Feb 2024 02:26:08 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55cb396e9adad99fe98f84363e64919fa7e728f6080a762976e88c45e240ea87`  
		Last Modified: Thu, 01 Feb 2024 02:26:08 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:b422fe4000fdc564bc2261e42686183590617716cc42297a2bbf77db6b2ab896
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37101287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c9e8a773970c13d02591938a3ba84ac2a1885ff2df38d811ddf6128247ca799`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:26 GMT
ADD file:ef6f078c1e72fcfafb9bfeeff0c1c771219dc2efe34650963106f63d32183b49 in / 
# Wed, 31 Jan 2024 22:44:27 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 05:56:32 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 01 Feb 2024 05:56:35 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 05:56:35 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 01 Feb 2024 05:56:52 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 01 Feb 2024 05:56:53 GMT
VOLUME [/spiped]
# Thu, 01 Feb 2024 05:56:53 GMT
WORKDIR /spiped
# Thu, 01 Feb 2024 05:56:53 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 01 Feb 2024 05:56:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Feb 2024 05:56:53 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:25d3892798f8b99159e3c1136799bfed560027ce451b50d57d961f4f02577ff5`  
		Last Modified: Wed, 31 Jan 2024 22:48:07 GMT  
		Size: 29.2 MB (29180832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab70de86f0546f613f3351b6316ea1ea9a0c6562cdce9336f24d6552e0cc3b47`  
		Last Modified: Thu, 01 Feb 2024 05:57:04 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed15fb941dfb5e9137761f97b3e344916691cc8473a8d589bee58e24388cd2f7`  
		Last Modified: Thu, 01 Feb 2024 05:57:05 GMT  
		Size: 2.4 MB (2434866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b862a579330ea8f3bc50e0e60057d34b75553a18deccc7bab7a1b331ae5016`  
		Last Modified: Thu, 01 Feb 2024 05:57:05 GMT  
		Size: 5.5 MB (5483992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429251a29a2a0f675bcd3504dd3e855182dd3fbb197347f36c4e1baa6bc8303f`  
		Last Modified: Thu, 01 Feb 2024 05:57:04 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3867deda232b6d0f845d84dfd23666b4965f52bc6177bb9f4f9dd024ebbe6af`  
		Last Modified: Thu, 01 Feb 2024 05:57:04 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; 386

```console
$ docker pull spiped@sha256:af3a94935515497a1ade45fcc72c70ac050cfd1381185b8904a3c6c5c00f612a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38699213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0210fdce54e20cfde76f132661954d813e3b6a0f3993e8d9d04a53fc96fc39e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 31 Jan 2024 22:39:00 GMT
ADD file:540e2de73452bd162dd7f630bf29f60e7d2e4a7a5d32a495bedf8ad390b59d7f in / 
# Wed, 31 Jan 2024 22:39:01 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:28:50 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 31 Jan 2024 23:28:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:28:56 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 31 Jan 2024 23:29:29 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 31 Jan 2024 23:29:30 GMT
VOLUME [/spiped]
# Wed, 31 Jan 2024 23:29:30 GMT
WORKDIR /spiped
# Wed, 31 Jan 2024 23:29:30 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 31 Jan 2024 23:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 Jan 2024 23:29:30 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:34ef135b45f33052e8e5bca668f9a45a938944a9cf3fb73a46f54a7bf11f091b`  
		Last Modified: Wed, 31 Jan 2024 22:43:46 GMT  
		Size: 30.2 MB (30165018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751a96ff8957608f7ad889db770d428885c2b206b3f8652b3d06872194295d78`  
		Last Modified: Wed, 31 Jan 2024 23:29:47 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53160d66b23e9b2c4404e8fbb7ddb70966b2fa0ae6fef0fcd290dc733f9866b9`  
		Last Modified: Wed, 31 Jan 2024 23:29:47 GMT  
		Size: 2.6 MB (2588154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c15a42863551b8164cceac5ac558601c2b66a6c81c590cd98e5dfe6af43dbfa4`  
		Last Modified: Wed, 31 Jan 2024 23:29:49 GMT  
		Size: 5.9 MB (5944440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e297082e00314cd0f8763f69ec7001fa8440dbd507fa8975cd5620cd5cc63d6`  
		Last Modified: Wed, 31 Jan 2024 23:29:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba709f2eb9259a79c1eec4292df8fae1b367472b00185af3340f0a963ab390c4`  
		Last Modified: Wed, 31 Jan 2024 23:29:47 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; mips64le

```console
$ docker pull spiped@sha256:6ce4d2d0d50f6e83deb694c99ecdd43098dd3e8d5741391f4299b075b03a043f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36784313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04a7ca6e08978ccba1c67b528ff59cb65d5ffc61df8decfa703a154e5cf0fda1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 31 Jan 2024 22:27:13 GMT
ADD file:c38ae3175b2ea7bff74f0e28558af27158de7697be9142ed9d681c4d37b24e35 in / 
# Wed, 31 Jan 2024 22:27:17 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 11:09:49 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 01 Feb 2024 11:10:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 11:10:12 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 01 Feb 2024 11:11:58 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 01 Feb 2024 11:12:01 GMT
VOLUME [/spiped]
# Thu, 01 Feb 2024 11:12:04 GMT
WORKDIR /spiped
# Thu, 01 Feb 2024 11:12:06 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 01 Feb 2024 11:12:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Feb 2024 11:12:12 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:21bfa6f58b3ab30099793f844be56212a593fddbf3f030cd8c42b38a1dcefcff`  
		Last Modified: Wed, 31 Jan 2024 22:38:21 GMT  
		Size: 29.1 MB (29142437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c86ec7ab62c6acb9250eba5339643c146a5e73365420e68d7acb3e218bdacd57`  
		Last Modified: Thu, 01 Feb 2024 11:12:33 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea4b98fda2b541f972777b687167057487d97a7201574da0b7eebe255d46e1a`  
		Last Modified: Thu, 01 Feb 2024 11:12:35 GMT  
		Size: 1.8 MB (1834351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a784d99cbd8a4388e1a1943324e49b064d6f2dee4c80dafed2855dcc71b1f0`  
		Last Modified: Thu, 01 Feb 2024 11:12:38 GMT  
		Size: 5.8 MB (5806014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b288162c33595db1d26d19277130f65a6dcd72972f3cbd54812c14fb44ffabd8`  
		Last Modified: Thu, 01 Feb 2024 11:12:33 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43ddcf2cc851edfe7424b2bbfecc440922c44231bc57f9a2a827a78a1ffe941`  
		Last Modified: Thu, 01 Feb 2024 11:12:33 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; ppc64le

```console
$ docker pull spiped@sha256:64c5c55b229219480ea25215bdab6b03b1f345286ecbc63dc3f869e1ce330b3e
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42311916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59508d985231a098bed6b2ae23582037f4e79ddfe90b8a2f294822913213b7d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:03 GMT
ADD file:b65bdf3d9277efbf6bbf8bf0121f92bdcd342ed0c4f49f1cee3b91adafacd76c in / 
# Tue, 13 Feb 2024 00:39:05 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 03:44:05 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 13 Feb 2024 03:44:10 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 03:44:10 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 13 Feb 2024 03:45:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Feb 2024 03:45:11 GMT
VOLUME [/spiped]
# Tue, 13 Feb 2024 03:45:12 GMT
WORKDIR /spiped
# Tue, 13 Feb 2024 03:45:12 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 13 Feb 2024 03:45:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 03:45:13 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b1cce6d9947985e4270ac998aa258401bc5deca94d504040a14f9f3c47258d68`  
		Last Modified: Tue, 13 Feb 2024 00:43:56 GMT  
		Size: 33.1 MB (33118908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28eab5449fc59b53e9f2279940a43c6d3a3fd364d96fa2c3d2922cbc5de81e1b`  
		Last Modified: Tue, 13 Feb 2024 03:45:38 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:725f98f5d63a98ff542ad7b2403dd5c368b4ebb1a8856490eecd72bae96151a6`  
		Last Modified: Tue, 13 Feb 2024 03:45:38 GMT  
		Size: 2.8 MB (2769282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d6df2553e038156a19aa44c6722f55beeb50690123dd9f30ced381006e9e7a8`  
		Last Modified: Tue, 13 Feb 2024 03:45:39 GMT  
		Size: 6.4 MB (6422129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:360a23e225035c41d84713834b9665254b25b1888bdbeca5ac335fb5955fdfa6`  
		Last Modified: Tue, 13 Feb 2024 03:45:38 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8256250ad5ac412b1f0b34de7655074aeb8f3347b40f7226af075854090e891a`  
		Last Modified: Tue, 13 Feb 2024 03:45:38 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; s390x

```console
$ docker pull spiped@sha256:237c566ae2695688605457ce444873bacc827c72a5dab859f380f431cf8435fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.2 MB (35165793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab5dc818013c2717f8a89991acd65937b38331f6e81aae94516a765057ed63f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 31 Jan 2024 22:58:51 GMT
ADD file:d543e4bc70d0d1d81c594a97289d7f2b4925d86461644cf881890997abfb6ead in / 
# Wed, 31 Jan 2024 22:58:53 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 05:54:15 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 01 Feb 2024 05:54:19 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 05:54:19 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 01 Feb 2024 05:54:51 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 01 Feb 2024 05:54:52 GMT
VOLUME [/spiped]
# Thu, 01 Feb 2024 05:54:52 GMT
WORKDIR /spiped
# Thu, 01 Feb 2024 05:54:53 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 01 Feb 2024 05:54:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Feb 2024 05:54:53 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:84abfb784f629f520e19ebd281090b7f1b3b78ff96b3be919578a053d2708ad5`  
		Last Modified: Wed, 31 Jan 2024 23:29:10 GMT  
		Size: 27.5 MB (27513479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9096f642a1ac565ee2d5c07e0d0cf6e1bf955b8b0844bfef49d774de9bfcde`  
		Last Modified: Thu, 01 Feb 2024 05:57:44 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d2aef7174c2e6a7a1c9d301f1c42480cfe91e8854437e9401d6d09be37e8b6`  
		Last Modified: Thu, 01 Feb 2024 05:57:45 GMT  
		Size: 2.3 MB (2262471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc72cc5f176534103dfa802d29e26026288813d1b7db888527e71d18a695e3a`  
		Last Modified: Thu, 01 Feb 2024 05:57:45 GMT  
		Size: 5.4 MB (5388243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5820f59a9ec53afbe9859e889d57ec691f07ff8774a6e3d6131dd2f3916ff9`  
		Last Modified: Thu, 01 Feb 2024 05:57:44 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a83e6ca20ca5ee69c588a377a2897bb10e1c3f3d149b3bf42517d7b6fe686e0`  
		Last Modified: Thu, 01 Feb 2024 05:57:44 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
