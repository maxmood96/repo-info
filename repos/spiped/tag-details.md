<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `spiped`

-	[`spiped:1`](#spiped1)
-	[`spiped:1-alpine`](#spiped1-alpine)
-	[`spiped:1.6`](#spiped16)
-	[`spiped:1.6-alpine`](#spiped16-alpine)
-	[`spiped:1.6.1`](#spiped161)
-	[`spiped:1.6.1-alpine`](#spiped161-alpine)
-	[`spiped:alpine`](#spipedalpine)
-	[`spiped:latest`](#spipedlatest)

## `spiped:1`

```console
$ docker pull spiped@sha256:002299301e9b7e3d62ece4463aaf97204581200e1c40a00c6d82aa89506328f4
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
$ docker pull spiped@sha256:a696ea93d50ac968bc64ce5ab01eaf4ff13ae39fa9f099b9cd19a8e7a9d07aee
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37320955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683078eccb0851809c92a9dfdb1dcdd47c187bd8a7a5cc960a8fa55b1ece7e86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 12 Oct 2021 01:20:42 GMT
ADD file:16dc2c6d1932194edec28d730b004fd6deca3d0f0e1a07bc5b8b6e8a1662f7af in / 
# Tue, 12 Oct 2021 01:20:42 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 16:21:25 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 12 Oct 2021 16:21:29 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 16:21:29 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Tue, 12 Oct 2021 16:21:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 16:21:56 GMT
VOLUME [/spiped]
# Tue, 12 Oct 2021 16:21:56 GMT
WORKDIR /spiped
# Tue, 12 Oct 2021 16:21:57 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 12 Oct 2021 16:21:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Oct 2021 16:21:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7d63c13d9b9b6ec5f05a2b07daadacaa9c610d01102a662ae9b1d082105f1ffa`  
		Last Modified: Tue, 12 Oct 2021 01:26:05 GMT  
		Size: 31.4 MB (31357311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c825e91f209a1656f91feea4a2861373b55da8c1c3eb72e742c7f31c3d367918`  
		Last Modified: Tue, 12 Oct 2021 16:22:19 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba3f6cb28bad6f7f95e8be3b815465b3d5585c01a7cde8e6c561a81fd08d8e7`  
		Last Modified: Tue, 12 Oct 2021 16:22:19 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbac5321939b951af500d72dc338b30ccdc61d354b3a466ce698a006ca3f4999`  
		Last Modified: Tue, 12 Oct 2021 16:22:20 GMT  
		Size: 6.0 MB (5960389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e58545b0e832a28e4b2fe9fe327f35158f38ccc204ce2c8fe1597803e860c0c2`  
		Last Modified: Tue, 12 Oct 2021 16:22:19 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c1557262dbc7e84098fd29719562170e4c257f980350cf3e68318ecd07a8956`  
		Last Modified: Tue, 12 Oct 2021 16:22:19 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; arm variant v5

```console
$ docker pull spiped@sha256:470773bf2dac565adf268ce74a10c0ca68c421d0de4192c4f6f29f15e8663e54
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33928107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee42cb8fa181c28acac6a722b80b4ea34b101698e1d8886a77f8323f3dbc1d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 12 Oct 2021 00:50:30 GMT
ADD file:fb1afabdc1f93b4866b4c4d696f272b4888519cb5bf35eb7ed1a4c021d1a04c8 in / 
# Tue, 12 Oct 2021 00:50:30 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 11:33:43 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 12 Oct 2021 11:33:53 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 11:33:53 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Tue, 12 Oct 2021 11:34:54 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 11:34:55 GMT
VOLUME [/spiped]
# Tue, 12 Oct 2021 11:34:55 GMT
WORKDIR /spiped
# Tue, 12 Oct 2021 11:34:56 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 12 Oct 2021 11:34:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Oct 2021 11:34:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:5c9bab66abc5c53391435f6fd66e0ff3571295d568f45ac7d2dc480bcbfd56e8`  
		Last Modified: Tue, 12 Oct 2021 01:06:07 GMT  
		Size: 28.9 MB (28899715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29fa5bfe046f908c4024b12760d6a235703129cf889a6b12fe9cb3c909e50ea`  
		Last Modified: Tue, 12 Oct 2021 11:35:35 GMT  
		Size: 1.7 KB (1725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f15e6ebdfdcc8907dc36ff08f672c463d0fbb6c59b0bb232ff1a229f64e4ea34`  
		Last Modified: Tue, 12 Oct 2021 11:35:35 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0030f062ce13c3eb3f6f0020460e01e4beebed73ca735660e5fe74df98d62119`  
		Last Modified: Tue, 12 Oct 2021 11:35:40 GMT  
		Size: 5.0 MB (5025142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9edc074a3eb9dffdb9440831266c18299dcccc42834d767fc489b92ca7f2a48`  
		Last Modified: Tue, 12 Oct 2021 11:35:35 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef7dd4a1c957efda249f4568cd568c8671c526848a4b9f57ffc9783bf81cef3`  
		Last Modified: Tue, 12 Oct 2021 11:35:35 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; arm variant v7

```console
$ docker pull spiped@sha256:958d2e76bb92a4709c36123b6553d179419227b06b733ec19cf1a4899da20853
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31309843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c0880cb9c6c234ff2fe6a3c163710a28845c22e1207ecd0b31cd8887cb77d26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 12 Oct 2021 01:28:36 GMT
ADD file:89eac94007ac04f9168737686fa0a6c737f2c28fc9e5918d4d512924fe1973be in / 
# Tue, 12 Oct 2021 01:28:37 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 03:43:34 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 12 Oct 2021 03:43:41 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 03:43:42 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Tue, 12 Oct 2021 03:44:37 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 03:44:37 GMT
VOLUME [/spiped]
# Tue, 12 Oct 2021 03:44:38 GMT
WORKDIR /spiped
# Tue, 12 Oct 2021 03:44:39 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 12 Oct 2021 03:44:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Oct 2021 03:44:40 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4e5300249f84466df4dc73ea0ce09938ca00c1718bb12619c4f26bd936162331`  
		Last Modified: Tue, 12 Oct 2021 01:44:28 GMT  
		Size: 26.6 MB (26561058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6ecc7e48d063e5bf0a086847e03c73699a183e8a9129e1b8ee3cab1482dde2d`  
		Last Modified: Tue, 12 Oct 2021 03:45:39 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584009012f86b47c7e4e6d1fd99c2d00976e77d0c5c66f0179ed3c7ea7c54725`  
		Last Modified: Tue, 12 Oct 2021 03:45:39 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aae397080ab7f297afe0c2760bc744f5c6ab5ff8f88b8e0830bc8ae8d97b565f`  
		Last Modified: Tue, 12 Oct 2021 03:45:44 GMT  
		Size: 4.7 MB (4745527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c697bb38b9e3862762d00df70d8a431fd891e25b33a03308c9e1cf59a02c712`  
		Last Modified: Tue, 12 Oct 2021 03:45:39 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c305948d80dae9d7e0b495eba60d890696dba8079d33af0619bb473c03c079`  
		Last Modified: Tue, 12 Oct 2021 03:45:39 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:0e89927947ad9449b0d9919da34674f7fd0095391138d87e11a147544a9a68d5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35310399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9587caa0158c348ca5fe2ca4f04dec822f9902fd9aa85fd89adbb258601bfd9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 12 Oct 2021 01:41:18 GMT
ADD file:d84144ad575672cd6cc8a00c8e5a88ab0545348f040fc249ea5fcf8193b2bce6 in / 
# Tue, 12 Oct 2021 01:41:18 GMT
CMD ["bash"]
# Fri, 12 Nov 2021 18:18:47 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 12 Nov 2021 18:18:51 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 12 Nov 2021 18:18:52 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Fri, 12 Nov 2021 18:19:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 12 Nov 2021 18:19:17 GMT
VOLUME [/spiped]
# Fri, 12 Nov 2021 18:19:18 GMT
WORKDIR /spiped
# Fri, 12 Nov 2021 18:19:20 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 12 Nov 2021 18:19:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 18:19:21 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a9eb63951c1c2ee8efcc12b696928fee3741a2d4eae76f2da3e161a5d90548bf`  
		Last Modified: Tue, 12 Oct 2021 01:48:13 GMT  
		Size: 30.0 MB (30043906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7073e48df5d25256c7c393e704c59a9f201985036d095eb06301c3db8136c68d`  
		Last Modified: Fri, 12 Nov 2021 18:20:24 GMT  
		Size: 1.6 KB (1619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4320355a643d17b982b97870451762d8b863c511b7d751f740c4a9fef0e2912`  
		Last Modified: Fri, 12 Nov 2021 18:20:23 GMT  
		Size: 923.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36f544201620c633914c2a7e3d6a50bffd46317df2cc5156cd6c0453609e14d`  
		Last Modified: Fri, 12 Nov 2021 18:20:25 GMT  
		Size: 5.3 MB (5263513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997c9a99799eb5bf9429e4dd669acfb00da7fc1efc80a08476c2b7f17f5041ca`  
		Last Modified: Fri, 12 Nov 2021 18:20:24 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac3d4565cd75cd143042ec6c135f1225a031c6caf0d66d8bdb4372e6b4a82c06`  
		Last Modified: Fri, 12 Nov 2021 18:20:24 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; 386

```console
$ docker pull spiped@sha256:7e62ad8ce0310713b81cee83e9f2df9a18a94cf41dc99ba28a629f7554aeefa3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40257794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e2bf1ef1d62cb3d5701cdee3834206614fd56059103a424063a602168d47abe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 12 Oct 2021 01:39:47 GMT
ADD file:42196ffa4c70af8d9f1e7b74edb3bb92d47296acf989adf615e8208230f8bd0c in / 
# Tue, 12 Oct 2021 01:39:47 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 22:29:57 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 12 Oct 2021 22:30:05 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 22:30:05 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Tue, 12 Oct 2021 22:31:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 22:31:03 GMT
VOLUME [/spiped]
# Tue, 12 Oct 2021 22:31:03 GMT
WORKDIR /spiped
# Tue, 12 Oct 2021 22:31:04 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 12 Oct 2021 22:31:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Oct 2021 22:31:05 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:87318d165b5c0fdf05c8ccf97d83084f56b4608075a3335b1a46c76295b82753`  
		Last Modified: Tue, 12 Oct 2021 01:47:39 GMT  
		Size: 32.4 MB (32370344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4928a77f1df28f1a46c20db916ae41f9f3331dc5058d03d8298439de44db7b91`  
		Last Modified: Tue, 12 Oct 2021 22:31:47 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb53cf6a9579bfadc1f1fd25438cdfad0ff235db1fe68eb4bb2afd7719b791d`  
		Last Modified: Tue, 12 Oct 2021 22:31:47 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aef6d6c4e04c173d1a0914846ba20d15a2f5f95d88f30069d1eca250898b325`  
		Last Modified: Tue, 12 Oct 2021 22:31:49 GMT  
		Size: 7.9 MB (7884197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b6984d7102b271e3fdc811759f7c556d04efe1259b67fab31e59565516fbed`  
		Last Modified: Tue, 12 Oct 2021 22:31:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e088d6a7c91ad6e879108222fefc2fff6a12de71734608e2b594ae36399c1d29`  
		Last Modified: Tue, 12 Oct 2021 22:31:47 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; mips64le

```console
$ docker pull spiped@sha256:eff58594b3d812760bbc2b4221d61e20cd31ab2ada880341e6e756d55b0e8dfa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35328007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eaccc3d11f7debbf79cd094b33cdae93860e3d40b42f7779edf587b67fc976c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 12 Oct 2021 01:11:15 GMT
ADD file:f90ca8957172106f42a9096c9a21082d51f3201aa78e6f64621a73117e2b7b6a in / 
# Tue, 12 Oct 2021 01:11:16 GMT
CMD ["bash"]
# Wed, 13 Oct 2021 01:30:36 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 13 Oct 2021 01:30:47 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 01:30:47 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Wed, 13 Oct 2021 01:31:57 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 13 Oct 2021 01:31:57 GMT
VOLUME [/spiped]
# Wed, 13 Oct 2021 01:31:58 GMT
WORKDIR /spiped
# Wed, 13 Oct 2021 01:31:58 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 13 Oct 2021 01:31:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Oct 2021 01:31:59 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:59ddca50ce05605e6234c1e7213c39cdedabc48ef11637e12156b7bd69afe161`  
		Last Modified: Tue, 12 Oct 2021 01:20:03 GMT  
		Size: 29.6 MB (29618732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195b13cd10a541ef73f29b46be3ae53a62b047ad5919580c0601496f9a63a3f3`  
		Last Modified: Wed, 13 Oct 2021 01:32:10 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11abea7ddca4b5031aa9fdff9ad5b49b60d36fd5940b7805f93333ca5da482f7`  
		Last Modified: Wed, 13 Oct 2021 01:32:10 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b0c25ac4296890c80ee4f1bea71c20c6a8251252085a00c9f764d7601ac9e7`  
		Last Modified: Wed, 13 Oct 2021 01:32:15 GMT  
		Size: 5.7 MB (5706076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb391de145f2fb5b8ba0dda5a96231a88d0c7e58514503ab861743a74f24c3ea`  
		Last Modified: Wed, 13 Oct 2021 01:32:10 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95bbf8647f8ba425f0ba8506aa7c276231190bb29fb4f34f2306f160f1c3795b`  
		Last Modified: Wed, 13 Oct 2021 01:32:10 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; ppc64le

```console
$ docker pull spiped@sha256:44b13757ab959642c428cd66c8a503318b7916932e88ee0f686aff3c40b6f88e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41263678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aadb76166ced7d8733fac685c49d5b3e6c4e0ca8713e0c26fa2829ab87bb9172`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 12 Oct 2021 01:25:45 GMT
ADD file:d8794fadf16c9948c3574ba28740d08393eca57766340333ad91f9c2a33eb719 in / 
# Tue, 12 Oct 2021 01:25:53 GMT
CMD ["bash"]
# Wed, 13 Oct 2021 08:03:47 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 13 Oct 2021 08:03:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 08:04:02 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Wed, 13 Oct 2021 08:07:07 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 13 Oct 2021 08:07:16 GMT
VOLUME [/spiped]
# Wed, 13 Oct 2021 08:07:24 GMT
WORKDIR /spiped
# Wed, 13 Oct 2021 08:07:26 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 13 Oct 2021 08:07:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Oct 2021 08:07:32 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6c28c1405c677dd809094d06190225b38cee3d24f18da38d287ef5bcc67884d6`  
		Last Modified: Tue, 12 Oct 2021 01:37:00 GMT  
		Size: 35.3 MB (35258729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c02b2acecad78932397dca6224b551528ccaf70fed1c60da8884b1ee077de8`  
		Last Modified: Wed, 13 Oct 2021 08:08:15 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e5dcbe4d07e13aa9f6162d201034eb2b26b9f69987315148425a39102ba3df`  
		Last Modified: Wed, 13 Oct 2021 08:08:15 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d805dc3af7457dd0105eca804e08afa7eed7d23d36613d054713cef0cd7f301a`  
		Last Modified: Wed, 13 Oct 2021 08:08:16 GMT  
		Size: 6.0 MB (6001677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c36c3789c72419dd7c04f766b8ef090133dd4afbffd43366f439be9bdcb7d88`  
		Last Modified: Wed, 13 Oct 2021 08:08:15 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1414313671940f5f943d32775bed04903cb0d2af90ece5729859bf3a6284b292`  
		Last Modified: Wed, 13 Oct 2021 08:08:15 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; s390x

```console
$ docker pull spiped@sha256:0ea844713c5be79b86f0ed403e6d7a38c6b37f92d690035d328f933e7d828d3c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34828428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:224bab1ef5e8e000f26cc5a15fc7f3d3851979e858ee4d475d6f18295d2e5c27`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 12 Oct 2021 00:42:27 GMT
ADD file:6038dd6db57fb05c3d39c02c3379667ccd2989e7667ff773a8020fe6a69a760c in / 
# Tue, 12 Oct 2021 00:42:29 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 04:31:53 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 12 Oct 2021 04:31:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 04:31:56 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Tue, 12 Oct 2021 04:32:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 04:32:12 GMT
VOLUME [/spiped]
# Tue, 12 Oct 2021 04:32:12 GMT
WORKDIR /spiped
# Tue, 12 Oct 2021 04:32:12 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 12 Oct 2021 04:32:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Oct 2021 04:32:12 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ded751c48f72503973be01be2794cc039490f22b039b8ac106e9f17de4980742`  
		Last Modified: Tue, 12 Oct 2021 00:48:05 GMT  
		Size: 29.6 MB (29641215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9339c2f00e96cfd5d66e69eeaec4b0592b4ff1f2798f167750a1ca9f15264c42`  
		Last Modified: Tue, 12 Oct 2021 04:32:43 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd1ae5a6b4870b8387c848046338d1914594cc3738bc5631e96eb22fba322290`  
		Last Modified: Tue, 12 Oct 2021 04:32:42 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61437e76afae45198095fc895e7d4154ce1ca4d68f4a7f7ad160c99b7bb4d341`  
		Last Modified: Tue, 12 Oct 2021 04:32:43 GMT  
		Size: 5.2 MB (5183956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90528d405e1a63caf7013a7715aa3ba6a0d0eabc5ce0955bc7a383eb3dd3cef8`  
		Last Modified: Tue, 12 Oct 2021 04:32:43 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5158295881f8176e354104f90f22e99b9211b9860e03e398f262f8a6b5828a4`  
		Last Modified: Tue, 12 Oct 2021 04:32:43 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1-alpine`

```console
$ docker pull spiped@sha256:94622cc2ebc9d6e307aeff3e1b8a1408af46869fdf4f99c1cfb2c7648ab83012
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
$ docker pull spiped@sha256:44015ddc42ceef8878c9b2bad7a6bcbf2b5d2ca42ab52cca20f9f66b2c15ffd8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3036014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c65d8337530e6b8e116202287d477945c4375886702df4698f8740106658a777`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 28 Aug 2021 00:56:12 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 28 Aug 2021 00:56:13 GMT
RUN apk add --no-cache libssl1.1
# Sat, 28 Aug 2021 00:56:13 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Sat, 28 Aug 2021 00:56:31 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Sat, 28 Aug 2021 00:56:31 GMT
VOLUME [/spiped]
# Sat, 28 Aug 2021 00:56:31 GMT
WORKDIR /spiped
# Sat, 28 Aug 2021 00:56:31 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 28 Aug 2021 00:56:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Aug 2021 00:56:32 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72fe484884c949a7fba8b7d917cbe40b9fa50036f4c10e4b82e3075576fe3fc`  
		Last Modified: Sat, 28 Aug 2021 00:56:49 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06083e8d35a44724cf84de43d971fb5b141e8ce6468a5c267c43c96f79869f23`  
		Last Modified: Sat, 28 Aug 2021 00:56:49 GMT  
		Size: 7.3 KB (7282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46037fda176acae1eef93fa1dde784253576faf4d880c75c8d7df76fdf212dda`  
		Last Modified: Sat, 28 Aug 2021 00:56:49 GMT  
		Size: 212.5 KB (212547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb3cd7f024c8cfa70e1c8e8f282e44395bbaa20cd69851af0552d8041deaea2`  
		Last Modified: Sat, 28 Aug 2021 00:56:49 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64fccea2af66d4ffdbdd93edf485c1e6e17f14ac10329842af6fea7741bd3504`  
		Last Modified: Sat, 28 Aug 2021 00:56:49 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:7e548b9910cf9bcbce660ff537e09660dbd9d84cbc06621e45fb2282f2f52270
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2838978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8539d235dbd2d180f98df622ec1586ed595c7026c53f57b67876cbe0b641be9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Sat, 28 Aug 2021 00:39:21 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 28 Aug 2021 00:39:23 GMT
RUN apk add --no-cache libssl1.1
# Sat, 28 Aug 2021 00:39:23 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Sat, 28 Aug 2021 00:39:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Sat, 28 Aug 2021 00:39:58 GMT
VOLUME [/spiped]
# Sat, 28 Aug 2021 00:39:58 GMT
WORKDIR /spiped
# Sat, 28 Aug 2021 00:39:59 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 28 Aug 2021 00:39:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Aug 2021 00:40:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3ec865614b924d3ebd8faaf1468ff031de3ccb2f178656d907e4a89f8673776`  
		Last Modified: Sat, 28 Aug 2021 00:40:31 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07908dc20812a0124cb96563b08ff2d4ebd32f0ca0cef02511faa0c127496e96`  
		Last Modified: Sat, 28 Aug 2021 00:40:31 GMT  
		Size: 7.3 KB (7290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae2ce7f8303145adfe2a17235c758d30fa18338c417eb73738b591c1dd3d1315`  
		Last Modified: Sat, 28 Aug 2021 00:40:31 GMT  
		Size: 202.5 KB (202499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d07f8ab6ed47190923d1d152d960c5fd80b7d9f27f84a289e8236a1e4f22843c`  
		Last Modified: Sat, 28 Aug 2021 00:40:31 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f17d0a64e682741c70413fc90f0d8a4dac61425dcc5c98ce054909120977e587`  
		Last Modified: Sat, 28 Aug 2021 00:40:31 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:24d05f05df7127b2aa61654a9d29c77a0c2a00f8ba29dbfc127a672700d5f652
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2635217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c197156cacbfdbdb870ce3391ad1bdf7d6c922d18648489e7549033356f432b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 27 Aug 2021 17:57:31 GMT
ADD file:a7da7992ccea54d3295231027614f138aa45c4d4a25ea6ec9bf7b316b9f67d95 in / 
# Fri, 27 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Sat, 28 Aug 2021 03:04:23 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 28 Aug 2021 03:04:26 GMT
RUN apk add --no-cache libssl1.1
# Sat, 28 Aug 2021 03:04:26 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Sat, 28 Aug 2021 03:04:59 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Sat, 28 Aug 2021 03:04:59 GMT
VOLUME [/spiped]
# Sat, 28 Aug 2021 03:05:00 GMT
WORKDIR /spiped
# Sat, 28 Aug 2021 03:05:00 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 28 Aug 2021 03:05:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Aug 2021 03:05:01 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a14774a5a62e0f454febaec7cb603e18a6a8e25ef9da4a4da85b155bdd5e5a7a`  
		Last Modified: Fri, 27 Aug 2021 17:59:00 GMT  
		Size: 2.4 MB (2430419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c187e6961a8f3ae8bf645e1fbec375c4f7c3d8146ab5ee5a09f57cd5615f33cb`  
		Last Modified: Sat, 28 Aug 2021 03:05:54 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e56c389f9017243d26a8fd61b3cc3385e2b4dcf930d608cc682a5ff3b437137`  
		Last Modified: Sat, 28 Aug 2021 03:05:54 GMT  
		Size: 7.3 KB (7298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b0da469457d5465481ffd06dc86cd457daaf02e8b501cbee7b9cb52b675525`  
		Last Modified: Sat, 28 Aug 2021 03:05:54 GMT  
		Size: 195.8 KB (195763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eea4333c9f229866ca36ab2d7e036e1d23031e78c62c3ad0bcbbeacaaf8f8e65`  
		Last Modified: Sat, 28 Aug 2021 03:05:54 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4907440a689992d3e1fbcc2fcef650c5ef7b7abe5b8b3aa9c97d6d697d5050fd`  
		Last Modified: Sat, 28 Aug 2021 03:05:54 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:cbaa0533059fb17c768fe05790c3675b5b5cecf35f0b461e5347d763b1322af8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2932006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49787cc7861893f9d6020342db1639e60d7af6850ca4866d08840d8438a2b0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 18:19:31 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 12 Nov 2021 18:19:33 GMT
RUN apk add --no-cache libssl1.1
# Fri, 12 Nov 2021 18:19:34 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Fri, 12 Nov 2021 18:19:54 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Fri, 12 Nov 2021 18:19:55 GMT
VOLUME [/spiped]
# Fri, 12 Nov 2021 18:19:56 GMT
WORKDIR /spiped
# Fri, 12 Nov 2021 18:19:58 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 12 Nov 2021 18:19:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 18:19:59 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbcce6bf922e4817964b0a9575d547fbb39004874a87c290658dcbb8939209e`  
		Last Modified: Fri, 12 Nov 2021 18:20:41 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b342172a90f6f6a837eeb8f0025e02facad5a97fdd12c0aeac68c2411928d16f`  
		Last Modified: Fri, 12 Nov 2021 18:20:41 GMT  
		Size: 7.8 KB (7751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8a670bc36ab2f74e650d7cb573c4c3542673b9488e2659efbc0d6b9db67529`  
		Last Modified: Fri, 12 Nov 2021 18:20:41 GMT  
		Size: 204.9 KB (204879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698de19c09a4c9763fb04c4946f3bffafe6556fcfe73a3d55bbb4255f65bd458`  
		Last Modified: Fri, 12 Nov 2021 18:20:41 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d1aa9a890181cdc95e60ea01849306cb72c967e13716722baa68c7bca76fdb`  
		Last Modified: Fri, 12 Nov 2021 18:20:42 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; 386

```console
$ docker pull spiped@sha256:da842be683e4aa6e7f0e6581d7d9bd1604d2d140a1b452e47a1ca595261af814
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3055327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c67a7b5670b88fbd238447f1f65531173381d0aff05ec6d63ef2df4dfb7b8c43`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 27 Aug 2021 17:38:29 GMT
ADD file:42a7bc5a08b546b47049dd0f89ae4e7a8c86342f87000f39ade3ff52916a6c2e in / 
# Fri, 27 Aug 2021 17:38:30 GMT
CMD ["/bin/sh"]
# Sat, 28 Aug 2021 00:35:24 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 28 Aug 2021 00:35:25 GMT
RUN apk add --no-cache libssl1.1
# Sat, 28 Aug 2021 00:35:25 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Sat, 28 Aug 2021 00:35:45 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Sat, 28 Aug 2021 00:35:45 GMT
VOLUME [/spiped]
# Sat, 28 Aug 2021 00:35:45 GMT
WORKDIR /spiped
# Sat, 28 Aug 2021 00:35:46 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 28 Aug 2021 00:35:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Aug 2021 00:35:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b11ae9fc5d8a106cfed3a6f6c75e5b5b5797c566fac4411622b4055df6541286`  
		Last Modified: Fri, 27 Aug 2021 17:39:18 GMT  
		Size: 2.8 MB (2822857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95070702ac27305ca355fc2880dec01d9e18d3c8a4a22842a599db59ea5467e0`  
		Last Modified: Sat, 28 Aug 2021 00:36:17 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35be501885b2efd06479a1d05af31f0d06d6b0a5c4dfb3f760af81657d7919ea`  
		Last Modified: Sat, 28 Aug 2021 00:36:17 GMT  
		Size: 7.3 KB (7287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f5e404d9d5a395b15445e0403dfa9a598ab9ecd02814798d33098ac6a8ba9c`  
		Last Modified: Sat, 28 Aug 2021 00:36:17 GMT  
		Size: 223.4 KB (223445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233b8287cb974321164bff4ca80e9a231471fecf0bbab1bbf130172709ae47ae`  
		Last Modified: Sat, 28 Aug 2021 00:36:17 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c88353a13d0403b037e398aa01ea54701b91f2adf180d6ed9df1b155b62c89`  
		Last Modified: Sat, 28 Aug 2021 00:36:17 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:3c83af52715b14ccfd27cc89b7b988ae73b9d05500efd053b99b027c0328f14d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3042554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f59b6df7881927f19f4b2dcab5974d93c4284e7e9ba9c21098a82d888389b26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 27 Aug 2021 19:39:54 GMT
ADD file:d213c56ffc24a5051e8060fd0fec1a0520367c10d88ab16321c36336b6c66098 in / 
# Fri, 27 Aug 2021 19:39:59 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 21:36:44 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 27 Aug 2021 21:36:56 GMT
RUN apk add --no-cache libssl1.1
# Fri, 27 Aug 2021 21:37:02 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Fri, 27 Aug 2021 21:37:39 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Fri, 27 Aug 2021 21:37:41 GMT
VOLUME [/spiped]
# Fri, 27 Aug 2021 21:37:48 GMT
WORKDIR /spiped
# Fri, 27 Aug 2021 21:37:54 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 27 Aug 2021 21:38:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Aug 2021 21:38:21 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:63da8ca98f7b4b94381aed56862a60aecf355d9428b9aeb7c61d5bd017100c18`  
		Last Modified: Fri, 27 Aug 2021 19:41:06 GMT  
		Size: 2.8 MB (2812284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f143c775bd94ef9de49da05aab2353301bc02ceb74a237332f8d9b23e193234b`  
		Last Modified: Fri, 27 Aug 2021 21:38:57 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9067169d42bea9851adf89b67776e5a280513855fb73120a8d2c5f0051a1097b`  
		Last Modified: Fri, 27 Aug 2021 21:38:57 GMT  
		Size: 7.3 KB (7292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe10232ba40d32a7b84a0fe16aa0a2b418d2bdf093335c9fbaf56b08e751c54e`  
		Last Modified: Fri, 27 Aug 2021 21:38:57 GMT  
		Size: 221.2 KB (221238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c7d84f077aa3ad717767ac56d4b1ea509bc7a9c81e57e3f4e210fe09205ee9`  
		Last Modified: Fri, 27 Aug 2021 21:38:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c90dd2a4fa5a2acd662ddc7f2ec01550257e4bbaae18ab7a94fdd288523cf8`  
		Last Modified: Fri, 27 Aug 2021 21:38:57 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:3852ee4130c6bfe6eb29489ab1f82c2aceed2d65ba3a11477360199bd6ba4bd3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2817762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d772c7d45678813ce17e2e65d11aa3e23e0517de39acbfe03eaaadf3558b6f40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 27 Aug 2021 17:41:29 GMT
ADD file:9b40ee281e8797067fb2ae207c406084cb81593090338a8b7cb09ade52168daa in / 
# Fri, 27 Aug 2021 17:41:30 GMT
CMD ["/bin/sh"]
# Sat, 28 Aug 2021 04:23:48 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 28 Aug 2021 04:23:49 GMT
RUN apk add --no-cache libssl1.1
# Sat, 28 Aug 2021 04:23:50 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Sat, 28 Aug 2021 04:24:07 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Sat, 28 Aug 2021 04:24:08 GMT
VOLUME [/spiped]
# Sat, 28 Aug 2021 04:24:08 GMT
WORKDIR /spiped
# Sat, 28 Aug 2021 04:24:09 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 28 Aug 2021 04:24:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Aug 2021 04:24:10 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:da14cb6b6dc946dbb2d84386bcaca84e2d46f650767cd11bdb3331ec9d623988`  
		Last Modified: Fri, 27 Aug 2021 17:42:25 GMT  
		Size: 2.6 MB (2603464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b447a66831aa123cebdb722d7d1efb39f1ffb26129fdf9b8937935375852a206`  
		Last Modified: Sat, 28 Aug 2021 04:24:46 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b103bd0361f6fb48151c8780e205c3fde97140b66762b27effcf2c3b73c05c`  
		Last Modified: Sat, 28 Aug 2021 04:24:47 GMT  
		Size: 7.3 KB (7283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce02139d2773db6b3c7033d9dbc6fdb427c918a69c29b8bb01669296d18c9fe`  
		Last Modified: Sat, 28 Aug 2021 04:24:47 GMT  
		Size: 205.3 KB (205277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c3cb214e79007442b4d21bc48516c0ef35753d8db03a0cc129fa63d01bedde`  
		Last Modified: Sat, 28 Aug 2021 04:24:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29859d07f0b507288c642deae1bae6cbe9d019152647a0c4e76bd86474fda106`  
		Last Modified: Sat, 28 Aug 2021 04:24:47 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6`

```console
$ docker pull spiped@sha256:002299301e9b7e3d62ece4463aaf97204581200e1c40a00c6d82aa89506328f4
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
$ docker pull spiped@sha256:a696ea93d50ac968bc64ce5ab01eaf4ff13ae39fa9f099b9cd19a8e7a9d07aee
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37320955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683078eccb0851809c92a9dfdb1dcdd47c187bd8a7a5cc960a8fa55b1ece7e86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 12 Oct 2021 01:20:42 GMT
ADD file:16dc2c6d1932194edec28d730b004fd6deca3d0f0e1a07bc5b8b6e8a1662f7af in / 
# Tue, 12 Oct 2021 01:20:42 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 16:21:25 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 12 Oct 2021 16:21:29 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 16:21:29 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Tue, 12 Oct 2021 16:21:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 16:21:56 GMT
VOLUME [/spiped]
# Tue, 12 Oct 2021 16:21:56 GMT
WORKDIR /spiped
# Tue, 12 Oct 2021 16:21:57 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 12 Oct 2021 16:21:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Oct 2021 16:21:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7d63c13d9b9b6ec5f05a2b07daadacaa9c610d01102a662ae9b1d082105f1ffa`  
		Last Modified: Tue, 12 Oct 2021 01:26:05 GMT  
		Size: 31.4 MB (31357311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c825e91f209a1656f91feea4a2861373b55da8c1c3eb72e742c7f31c3d367918`  
		Last Modified: Tue, 12 Oct 2021 16:22:19 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba3f6cb28bad6f7f95e8be3b815465b3d5585c01a7cde8e6c561a81fd08d8e7`  
		Last Modified: Tue, 12 Oct 2021 16:22:19 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbac5321939b951af500d72dc338b30ccdc61d354b3a466ce698a006ca3f4999`  
		Last Modified: Tue, 12 Oct 2021 16:22:20 GMT  
		Size: 6.0 MB (5960389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e58545b0e832a28e4b2fe9fe327f35158f38ccc204ce2c8fe1597803e860c0c2`  
		Last Modified: Tue, 12 Oct 2021 16:22:19 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c1557262dbc7e84098fd29719562170e4c257f980350cf3e68318ecd07a8956`  
		Last Modified: Tue, 12 Oct 2021 16:22:19 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; arm variant v5

```console
$ docker pull spiped@sha256:470773bf2dac565adf268ce74a10c0ca68c421d0de4192c4f6f29f15e8663e54
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33928107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee42cb8fa181c28acac6a722b80b4ea34b101698e1d8886a77f8323f3dbc1d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 12 Oct 2021 00:50:30 GMT
ADD file:fb1afabdc1f93b4866b4c4d696f272b4888519cb5bf35eb7ed1a4c021d1a04c8 in / 
# Tue, 12 Oct 2021 00:50:30 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 11:33:43 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 12 Oct 2021 11:33:53 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 11:33:53 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Tue, 12 Oct 2021 11:34:54 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 11:34:55 GMT
VOLUME [/spiped]
# Tue, 12 Oct 2021 11:34:55 GMT
WORKDIR /spiped
# Tue, 12 Oct 2021 11:34:56 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 12 Oct 2021 11:34:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Oct 2021 11:34:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:5c9bab66abc5c53391435f6fd66e0ff3571295d568f45ac7d2dc480bcbfd56e8`  
		Last Modified: Tue, 12 Oct 2021 01:06:07 GMT  
		Size: 28.9 MB (28899715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29fa5bfe046f908c4024b12760d6a235703129cf889a6b12fe9cb3c909e50ea`  
		Last Modified: Tue, 12 Oct 2021 11:35:35 GMT  
		Size: 1.7 KB (1725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f15e6ebdfdcc8907dc36ff08f672c463d0fbb6c59b0bb232ff1a229f64e4ea34`  
		Last Modified: Tue, 12 Oct 2021 11:35:35 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0030f062ce13c3eb3f6f0020460e01e4beebed73ca735660e5fe74df98d62119`  
		Last Modified: Tue, 12 Oct 2021 11:35:40 GMT  
		Size: 5.0 MB (5025142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9edc074a3eb9dffdb9440831266c18299dcccc42834d767fc489b92ca7f2a48`  
		Last Modified: Tue, 12 Oct 2021 11:35:35 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef7dd4a1c957efda249f4568cd568c8671c526848a4b9f57ffc9783bf81cef3`  
		Last Modified: Tue, 12 Oct 2021 11:35:35 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; arm variant v7

```console
$ docker pull spiped@sha256:958d2e76bb92a4709c36123b6553d179419227b06b733ec19cf1a4899da20853
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31309843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c0880cb9c6c234ff2fe6a3c163710a28845c22e1207ecd0b31cd8887cb77d26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 12 Oct 2021 01:28:36 GMT
ADD file:89eac94007ac04f9168737686fa0a6c737f2c28fc9e5918d4d512924fe1973be in / 
# Tue, 12 Oct 2021 01:28:37 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 03:43:34 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 12 Oct 2021 03:43:41 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 03:43:42 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Tue, 12 Oct 2021 03:44:37 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 03:44:37 GMT
VOLUME [/spiped]
# Tue, 12 Oct 2021 03:44:38 GMT
WORKDIR /spiped
# Tue, 12 Oct 2021 03:44:39 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 12 Oct 2021 03:44:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Oct 2021 03:44:40 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4e5300249f84466df4dc73ea0ce09938ca00c1718bb12619c4f26bd936162331`  
		Last Modified: Tue, 12 Oct 2021 01:44:28 GMT  
		Size: 26.6 MB (26561058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6ecc7e48d063e5bf0a086847e03c73699a183e8a9129e1b8ee3cab1482dde2d`  
		Last Modified: Tue, 12 Oct 2021 03:45:39 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584009012f86b47c7e4e6d1fd99c2d00976e77d0c5c66f0179ed3c7ea7c54725`  
		Last Modified: Tue, 12 Oct 2021 03:45:39 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aae397080ab7f297afe0c2760bc744f5c6ab5ff8f88b8e0830bc8ae8d97b565f`  
		Last Modified: Tue, 12 Oct 2021 03:45:44 GMT  
		Size: 4.7 MB (4745527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c697bb38b9e3862762d00df70d8a431fd891e25b33a03308c9e1cf59a02c712`  
		Last Modified: Tue, 12 Oct 2021 03:45:39 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c305948d80dae9d7e0b495eba60d890696dba8079d33af0619bb473c03c079`  
		Last Modified: Tue, 12 Oct 2021 03:45:39 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:0e89927947ad9449b0d9919da34674f7fd0095391138d87e11a147544a9a68d5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35310399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9587caa0158c348ca5fe2ca4f04dec822f9902fd9aa85fd89adbb258601bfd9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 12 Oct 2021 01:41:18 GMT
ADD file:d84144ad575672cd6cc8a00c8e5a88ab0545348f040fc249ea5fcf8193b2bce6 in / 
# Tue, 12 Oct 2021 01:41:18 GMT
CMD ["bash"]
# Fri, 12 Nov 2021 18:18:47 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 12 Nov 2021 18:18:51 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 12 Nov 2021 18:18:52 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Fri, 12 Nov 2021 18:19:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 12 Nov 2021 18:19:17 GMT
VOLUME [/spiped]
# Fri, 12 Nov 2021 18:19:18 GMT
WORKDIR /spiped
# Fri, 12 Nov 2021 18:19:20 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 12 Nov 2021 18:19:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 18:19:21 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a9eb63951c1c2ee8efcc12b696928fee3741a2d4eae76f2da3e161a5d90548bf`  
		Last Modified: Tue, 12 Oct 2021 01:48:13 GMT  
		Size: 30.0 MB (30043906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7073e48df5d25256c7c393e704c59a9f201985036d095eb06301c3db8136c68d`  
		Last Modified: Fri, 12 Nov 2021 18:20:24 GMT  
		Size: 1.6 KB (1619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4320355a643d17b982b97870451762d8b863c511b7d751f740c4a9fef0e2912`  
		Last Modified: Fri, 12 Nov 2021 18:20:23 GMT  
		Size: 923.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36f544201620c633914c2a7e3d6a50bffd46317df2cc5156cd6c0453609e14d`  
		Last Modified: Fri, 12 Nov 2021 18:20:25 GMT  
		Size: 5.3 MB (5263513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997c9a99799eb5bf9429e4dd669acfb00da7fc1efc80a08476c2b7f17f5041ca`  
		Last Modified: Fri, 12 Nov 2021 18:20:24 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac3d4565cd75cd143042ec6c135f1225a031c6caf0d66d8bdb4372e6b4a82c06`  
		Last Modified: Fri, 12 Nov 2021 18:20:24 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; 386

```console
$ docker pull spiped@sha256:7e62ad8ce0310713b81cee83e9f2df9a18a94cf41dc99ba28a629f7554aeefa3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40257794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e2bf1ef1d62cb3d5701cdee3834206614fd56059103a424063a602168d47abe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 12 Oct 2021 01:39:47 GMT
ADD file:42196ffa4c70af8d9f1e7b74edb3bb92d47296acf989adf615e8208230f8bd0c in / 
# Tue, 12 Oct 2021 01:39:47 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 22:29:57 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 12 Oct 2021 22:30:05 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 22:30:05 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Tue, 12 Oct 2021 22:31:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 22:31:03 GMT
VOLUME [/spiped]
# Tue, 12 Oct 2021 22:31:03 GMT
WORKDIR /spiped
# Tue, 12 Oct 2021 22:31:04 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 12 Oct 2021 22:31:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Oct 2021 22:31:05 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:87318d165b5c0fdf05c8ccf97d83084f56b4608075a3335b1a46c76295b82753`  
		Last Modified: Tue, 12 Oct 2021 01:47:39 GMT  
		Size: 32.4 MB (32370344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4928a77f1df28f1a46c20db916ae41f9f3331dc5058d03d8298439de44db7b91`  
		Last Modified: Tue, 12 Oct 2021 22:31:47 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb53cf6a9579bfadc1f1fd25438cdfad0ff235db1fe68eb4bb2afd7719b791d`  
		Last Modified: Tue, 12 Oct 2021 22:31:47 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aef6d6c4e04c173d1a0914846ba20d15a2f5f95d88f30069d1eca250898b325`  
		Last Modified: Tue, 12 Oct 2021 22:31:49 GMT  
		Size: 7.9 MB (7884197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b6984d7102b271e3fdc811759f7c556d04efe1259b67fab31e59565516fbed`  
		Last Modified: Tue, 12 Oct 2021 22:31:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e088d6a7c91ad6e879108222fefc2fff6a12de71734608e2b594ae36399c1d29`  
		Last Modified: Tue, 12 Oct 2021 22:31:47 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; mips64le

```console
$ docker pull spiped@sha256:eff58594b3d812760bbc2b4221d61e20cd31ab2ada880341e6e756d55b0e8dfa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35328007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eaccc3d11f7debbf79cd094b33cdae93860e3d40b42f7779edf587b67fc976c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 12 Oct 2021 01:11:15 GMT
ADD file:f90ca8957172106f42a9096c9a21082d51f3201aa78e6f64621a73117e2b7b6a in / 
# Tue, 12 Oct 2021 01:11:16 GMT
CMD ["bash"]
# Wed, 13 Oct 2021 01:30:36 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 13 Oct 2021 01:30:47 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 01:30:47 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Wed, 13 Oct 2021 01:31:57 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 13 Oct 2021 01:31:57 GMT
VOLUME [/spiped]
# Wed, 13 Oct 2021 01:31:58 GMT
WORKDIR /spiped
# Wed, 13 Oct 2021 01:31:58 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 13 Oct 2021 01:31:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Oct 2021 01:31:59 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:59ddca50ce05605e6234c1e7213c39cdedabc48ef11637e12156b7bd69afe161`  
		Last Modified: Tue, 12 Oct 2021 01:20:03 GMT  
		Size: 29.6 MB (29618732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195b13cd10a541ef73f29b46be3ae53a62b047ad5919580c0601496f9a63a3f3`  
		Last Modified: Wed, 13 Oct 2021 01:32:10 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11abea7ddca4b5031aa9fdff9ad5b49b60d36fd5940b7805f93333ca5da482f7`  
		Last Modified: Wed, 13 Oct 2021 01:32:10 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b0c25ac4296890c80ee4f1bea71c20c6a8251252085a00c9f764d7601ac9e7`  
		Last Modified: Wed, 13 Oct 2021 01:32:15 GMT  
		Size: 5.7 MB (5706076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb391de145f2fb5b8ba0dda5a96231a88d0c7e58514503ab861743a74f24c3ea`  
		Last Modified: Wed, 13 Oct 2021 01:32:10 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95bbf8647f8ba425f0ba8506aa7c276231190bb29fb4f34f2306f160f1c3795b`  
		Last Modified: Wed, 13 Oct 2021 01:32:10 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; ppc64le

```console
$ docker pull spiped@sha256:44b13757ab959642c428cd66c8a503318b7916932e88ee0f686aff3c40b6f88e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41263678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aadb76166ced7d8733fac685c49d5b3e6c4e0ca8713e0c26fa2829ab87bb9172`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 12 Oct 2021 01:25:45 GMT
ADD file:d8794fadf16c9948c3574ba28740d08393eca57766340333ad91f9c2a33eb719 in / 
# Tue, 12 Oct 2021 01:25:53 GMT
CMD ["bash"]
# Wed, 13 Oct 2021 08:03:47 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 13 Oct 2021 08:03:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 08:04:02 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Wed, 13 Oct 2021 08:07:07 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 13 Oct 2021 08:07:16 GMT
VOLUME [/spiped]
# Wed, 13 Oct 2021 08:07:24 GMT
WORKDIR /spiped
# Wed, 13 Oct 2021 08:07:26 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 13 Oct 2021 08:07:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Oct 2021 08:07:32 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6c28c1405c677dd809094d06190225b38cee3d24f18da38d287ef5bcc67884d6`  
		Last Modified: Tue, 12 Oct 2021 01:37:00 GMT  
		Size: 35.3 MB (35258729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c02b2acecad78932397dca6224b551528ccaf70fed1c60da8884b1ee077de8`  
		Last Modified: Wed, 13 Oct 2021 08:08:15 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e5dcbe4d07e13aa9f6162d201034eb2b26b9f69987315148425a39102ba3df`  
		Last Modified: Wed, 13 Oct 2021 08:08:15 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d805dc3af7457dd0105eca804e08afa7eed7d23d36613d054713cef0cd7f301a`  
		Last Modified: Wed, 13 Oct 2021 08:08:16 GMT  
		Size: 6.0 MB (6001677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c36c3789c72419dd7c04f766b8ef090133dd4afbffd43366f439be9bdcb7d88`  
		Last Modified: Wed, 13 Oct 2021 08:08:15 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1414313671940f5f943d32775bed04903cb0d2af90ece5729859bf3a6284b292`  
		Last Modified: Wed, 13 Oct 2021 08:08:15 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; s390x

```console
$ docker pull spiped@sha256:0ea844713c5be79b86f0ed403e6d7a38c6b37f92d690035d328f933e7d828d3c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34828428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:224bab1ef5e8e000f26cc5a15fc7f3d3851979e858ee4d475d6f18295d2e5c27`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 12 Oct 2021 00:42:27 GMT
ADD file:6038dd6db57fb05c3d39c02c3379667ccd2989e7667ff773a8020fe6a69a760c in / 
# Tue, 12 Oct 2021 00:42:29 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 04:31:53 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 12 Oct 2021 04:31:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 04:31:56 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Tue, 12 Oct 2021 04:32:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 04:32:12 GMT
VOLUME [/spiped]
# Tue, 12 Oct 2021 04:32:12 GMT
WORKDIR /spiped
# Tue, 12 Oct 2021 04:32:12 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 12 Oct 2021 04:32:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Oct 2021 04:32:12 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ded751c48f72503973be01be2794cc039490f22b039b8ac106e9f17de4980742`  
		Last Modified: Tue, 12 Oct 2021 00:48:05 GMT  
		Size: 29.6 MB (29641215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9339c2f00e96cfd5d66e69eeaec4b0592b4ff1f2798f167750a1ca9f15264c42`  
		Last Modified: Tue, 12 Oct 2021 04:32:43 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd1ae5a6b4870b8387c848046338d1914594cc3738bc5631e96eb22fba322290`  
		Last Modified: Tue, 12 Oct 2021 04:32:42 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61437e76afae45198095fc895e7d4154ce1ca4d68f4a7f7ad160c99b7bb4d341`  
		Last Modified: Tue, 12 Oct 2021 04:32:43 GMT  
		Size: 5.2 MB (5183956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90528d405e1a63caf7013a7715aa3ba6a0d0eabc5ce0955bc7a383eb3dd3cef8`  
		Last Modified: Tue, 12 Oct 2021 04:32:43 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5158295881f8176e354104f90f22e99b9211b9860e03e398f262f8a6b5828a4`  
		Last Modified: Tue, 12 Oct 2021 04:32:43 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6-alpine`

```console
$ docker pull spiped@sha256:94622cc2ebc9d6e307aeff3e1b8a1408af46869fdf4f99c1cfb2c7648ab83012
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
$ docker pull spiped@sha256:44015ddc42ceef8878c9b2bad7a6bcbf2b5d2ca42ab52cca20f9f66b2c15ffd8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3036014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c65d8337530e6b8e116202287d477945c4375886702df4698f8740106658a777`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 28 Aug 2021 00:56:12 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 28 Aug 2021 00:56:13 GMT
RUN apk add --no-cache libssl1.1
# Sat, 28 Aug 2021 00:56:13 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Sat, 28 Aug 2021 00:56:31 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Sat, 28 Aug 2021 00:56:31 GMT
VOLUME [/spiped]
# Sat, 28 Aug 2021 00:56:31 GMT
WORKDIR /spiped
# Sat, 28 Aug 2021 00:56:31 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 28 Aug 2021 00:56:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Aug 2021 00:56:32 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72fe484884c949a7fba8b7d917cbe40b9fa50036f4c10e4b82e3075576fe3fc`  
		Last Modified: Sat, 28 Aug 2021 00:56:49 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06083e8d35a44724cf84de43d971fb5b141e8ce6468a5c267c43c96f79869f23`  
		Last Modified: Sat, 28 Aug 2021 00:56:49 GMT  
		Size: 7.3 KB (7282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46037fda176acae1eef93fa1dde784253576faf4d880c75c8d7df76fdf212dda`  
		Last Modified: Sat, 28 Aug 2021 00:56:49 GMT  
		Size: 212.5 KB (212547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb3cd7f024c8cfa70e1c8e8f282e44395bbaa20cd69851af0552d8041deaea2`  
		Last Modified: Sat, 28 Aug 2021 00:56:49 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64fccea2af66d4ffdbdd93edf485c1e6e17f14ac10329842af6fea7741bd3504`  
		Last Modified: Sat, 28 Aug 2021 00:56:49 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:7e548b9910cf9bcbce660ff537e09660dbd9d84cbc06621e45fb2282f2f52270
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2838978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8539d235dbd2d180f98df622ec1586ed595c7026c53f57b67876cbe0b641be9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Sat, 28 Aug 2021 00:39:21 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 28 Aug 2021 00:39:23 GMT
RUN apk add --no-cache libssl1.1
# Sat, 28 Aug 2021 00:39:23 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Sat, 28 Aug 2021 00:39:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Sat, 28 Aug 2021 00:39:58 GMT
VOLUME [/spiped]
# Sat, 28 Aug 2021 00:39:58 GMT
WORKDIR /spiped
# Sat, 28 Aug 2021 00:39:59 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 28 Aug 2021 00:39:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Aug 2021 00:40:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3ec865614b924d3ebd8faaf1468ff031de3ccb2f178656d907e4a89f8673776`  
		Last Modified: Sat, 28 Aug 2021 00:40:31 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07908dc20812a0124cb96563b08ff2d4ebd32f0ca0cef02511faa0c127496e96`  
		Last Modified: Sat, 28 Aug 2021 00:40:31 GMT  
		Size: 7.3 KB (7290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae2ce7f8303145adfe2a17235c758d30fa18338c417eb73738b591c1dd3d1315`  
		Last Modified: Sat, 28 Aug 2021 00:40:31 GMT  
		Size: 202.5 KB (202499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d07f8ab6ed47190923d1d152d960c5fd80b7d9f27f84a289e8236a1e4f22843c`  
		Last Modified: Sat, 28 Aug 2021 00:40:31 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f17d0a64e682741c70413fc90f0d8a4dac61425dcc5c98ce054909120977e587`  
		Last Modified: Sat, 28 Aug 2021 00:40:31 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:24d05f05df7127b2aa61654a9d29c77a0c2a00f8ba29dbfc127a672700d5f652
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2635217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c197156cacbfdbdb870ce3391ad1bdf7d6c922d18648489e7549033356f432b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 27 Aug 2021 17:57:31 GMT
ADD file:a7da7992ccea54d3295231027614f138aa45c4d4a25ea6ec9bf7b316b9f67d95 in / 
# Fri, 27 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Sat, 28 Aug 2021 03:04:23 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 28 Aug 2021 03:04:26 GMT
RUN apk add --no-cache libssl1.1
# Sat, 28 Aug 2021 03:04:26 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Sat, 28 Aug 2021 03:04:59 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Sat, 28 Aug 2021 03:04:59 GMT
VOLUME [/spiped]
# Sat, 28 Aug 2021 03:05:00 GMT
WORKDIR /spiped
# Sat, 28 Aug 2021 03:05:00 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 28 Aug 2021 03:05:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Aug 2021 03:05:01 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a14774a5a62e0f454febaec7cb603e18a6a8e25ef9da4a4da85b155bdd5e5a7a`  
		Last Modified: Fri, 27 Aug 2021 17:59:00 GMT  
		Size: 2.4 MB (2430419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c187e6961a8f3ae8bf645e1fbec375c4f7c3d8146ab5ee5a09f57cd5615f33cb`  
		Last Modified: Sat, 28 Aug 2021 03:05:54 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e56c389f9017243d26a8fd61b3cc3385e2b4dcf930d608cc682a5ff3b437137`  
		Last Modified: Sat, 28 Aug 2021 03:05:54 GMT  
		Size: 7.3 KB (7298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b0da469457d5465481ffd06dc86cd457daaf02e8b501cbee7b9cb52b675525`  
		Last Modified: Sat, 28 Aug 2021 03:05:54 GMT  
		Size: 195.8 KB (195763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eea4333c9f229866ca36ab2d7e036e1d23031e78c62c3ad0bcbbeacaaf8f8e65`  
		Last Modified: Sat, 28 Aug 2021 03:05:54 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4907440a689992d3e1fbcc2fcef650c5ef7b7abe5b8b3aa9c97d6d697d5050fd`  
		Last Modified: Sat, 28 Aug 2021 03:05:54 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:cbaa0533059fb17c768fe05790c3675b5b5cecf35f0b461e5347d763b1322af8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2932006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49787cc7861893f9d6020342db1639e60d7af6850ca4866d08840d8438a2b0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 18:19:31 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 12 Nov 2021 18:19:33 GMT
RUN apk add --no-cache libssl1.1
# Fri, 12 Nov 2021 18:19:34 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Fri, 12 Nov 2021 18:19:54 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Fri, 12 Nov 2021 18:19:55 GMT
VOLUME [/spiped]
# Fri, 12 Nov 2021 18:19:56 GMT
WORKDIR /spiped
# Fri, 12 Nov 2021 18:19:58 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 12 Nov 2021 18:19:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 18:19:59 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbcce6bf922e4817964b0a9575d547fbb39004874a87c290658dcbb8939209e`  
		Last Modified: Fri, 12 Nov 2021 18:20:41 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b342172a90f6f6a837eeb8f0025e02facad5a97fdd12c0aeac68c2411928d16f`  
		Last Modified: Fri, 12 Nov 2021 18:20:41 GMT  
		Size: 7.8 KB (7751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8a670bc36ab2f74e650d7cb573c4c3542673b9488e2659efbc0d6b9db67529`  
		Last Modified: Fri, 12 Nov 2021 18:20:41 GMT  
		Size: 204.9 KB (204879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698de19c09a4c9763fb04c4946f3bffafe6556fcfe73a3d55bbb4255f65bd458`  
		Last Modified: Fri, 12 Nov 2021 18:20:41 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d1aa9a890181cdc95e60ea01849306cb72c967e13716722baa68c7bca76fdb`  
		Last Modified: Fri, 12 Nov 2021 18:20:42 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; 386

```console
$ docker pull spiped@sha256:da842be683e4aa6e7f0e6581d7d9bd1604d2d140a1b452e47a1ca595261af814
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3055327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c67a7b5670b88fbd238447f1f65531173381d0aff05ec6d63ef2df4dfb7b8c43`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 27 Aug 2021 17:38:29 GMT
ADD file:42a7bc5a08b546b47049dd0f89ae4e7a8c86342f87000f39ade3ff52916a6c2e in / 
# Fri, 27 Aug 2021 17:38:30 GMT
CMD ["/bin/sh"]
# Sat, 28 Aug 2021 00:35:24 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 28 Aug 2021 00:35:25 GMT
RUN apk add --no-cache libssl1.1
# Sat, 28 Aug 2021 00:35:25 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Sat, 28 Aug 2021 00:35:45 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Sat, 28 Aug 2021 00:35:45 GMT
VOLUME [/spiped]
# Sat, 28 Aug 2021 00:35:45 GMT
WORKDIR /spiped
# Sat, 28 Aug 2021 00:35:46 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 28 Aug 2021 00:35:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Aug 2021 00:35:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b11ae9fc5d8a106cfed3a6f6c75e5b5b5797c566fac4411622b4055df6541286`  
		Last Modified: Fri, 27 Aug 2021 17:39:18 GMT  
		Size: 2.8 MB (2822857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95070702ac27305ca355fc2880dec01d9e18d3c8a4a22842a599db59ea5467e0`  
		Last Modified: Sat, 28 Aug 2021 00:36:17 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35be501885b2efd06479a1d05af31f0d06d6b0a5c4dfb3f760af81657d7919ea`  
		Last Modified: Sat, 28 Aug 2021 00:36:17 GMT  
		Size: 7.3 KB (7287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f5e404d9d5a395b15445e0403dfa9a598ab9ecd02814798d33098ac6a8ba9c`  
		Last Modified: Sat, 28 Aug 2021 00:36:17 GMT  
		Size: 223.4 KB (223445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233b8287cb974321164bff4ca80e9a231471fecf0bbab1bbf130172709ae47ae`  
		Last Modified: Sat, 28 Aug 2021 00:36:17 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c88353a13d0403b037e398aa01ea54701b91f2adf180d6ed9df1b155b62c89`  
		Last Modified: Sat, 28 Aug 2021 00:36:17 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:3c83af52715b14ccfd27cc89b7b988ae73b9d05500efd053b99b027c0328f14d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3042554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f59b6df7881927f19f4b2dcab5974d93c4284e7e9ba9c21098a82d888389b26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 27 Aug 2021 19:39:54 GMT
ADD file:d213c56ffc24a5051e8060fd0fec1a0520367c10d88ab16321c36336b6c66098 in / 
# Fri, 27 Aug 2021 19:39:59 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 21:36:44 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 27 Aug 2021 21:36:56 GMT
RUN apk add --no-cache libssl1.1
# Fri, 27 Aug 2021 21:37:02 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Fri, 27 Aug 2021 21:37:39 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Fri, 27 Aug 2021 21:37:41 GMT
VOLUME [/spiped]
# Fri, 27 Aug 2021 21:37:48 GMT
WORKDIR /spiped
# Fri, 27 Aug 2021 21:37:54 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 27 Aug 2021 21:38:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Aug 2021 21:38:21 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:63da8ca98f7b4b94381aed56862a60aecf355d9428b9aeb7c61d5bd017100c18`  
		Last Modified: Fri, 27 Aug 2021 19:41:06 GMT  
		Size: 2.8 MB (2812284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f143c775bd94ef9de49da05aab2353301bc02ceb74a237332f8d9b23e193234b`  
		Last Modified: Fri, 27 Aug 2021 21:38:57 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9067169d42bea9851adf89b67776e5a280513855fb73120a8d2c5f0051a1097b`  
		Last Modified: Fri, 27 Aug 2021 21:38:57 GMT  
		Size: 7.3 KB (7292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe10232ba40d32a7b84a0fe16aa0a2b418d2bdf093335c9fbaf56b08e751c54e`  
		Last Modified: Fri, 27 Aug 2021 21:38:57 GMT  
		Size: 221.2 KB (221238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c7d84f077aa3ad717767ac56d4b1ea509bc7a9c81e57e3f4e210fe09205ee9`  
		Last Modified: Fri, 27 Aug 2021 21:38:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c90dd2a4fa5a2acd662ddc7f2ec01550257e4bbaae18ab7a94fdd288523cf8`  
		Last Modified: Fri, 27 Aug 2021 21:38:57 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:3852ee4130c6bfe6eb29489ab1f82c2aceed2d65ba3a11477360199bd6ba4bd3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2817762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d772c7d45678813ce17e2e65d11aa3e23e0517de39acbfe03eaaadf3558b6f40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 27 Aug 2021 17:41:29 GMT
ADD file:9b40ee281e8797067fb2ae207c406084cb81593090338a8b7cb09ade52168daa in / 
# Fri, 27 Aug 2021 17:41:30 GMT
CMD ["/bin/sh"]
# Sat, 28 Aug 2021 04:23:48 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 28 Aug 2021 04:23:49 GMT
RUN apk add --no-cache libssl1.1
# Sat, 28 Aug 2021 04:23:50 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Sat, 28 Aug 2021 04:24:07 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Sat, 28 Aug 2021 04:24:08 GMT
VOLUME [/spiped]
# Sat, 28 Aug 2021 04:24:08 GMT
WORKDIR /spiped
# Sat, 28 Aug 2021 04:24:09 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 28 Aug 2021 04:24:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Aug 2021 04:24:10 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:da14cb6b6dc946dbb2d84386bcaca84e2d46f650767cd11bdb3331ec9d623988`  
		Last Modified: Fri, 27 Aug 2021 17:42:25 GMT  
		Size: 2.6 MB (2603464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b447a66831aa123cebdb722d7d1efb39f1ffb26129fdf9b8937935375852a206`  
		Last Modified: Sat, 28 Aug 2021 04:24:46 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b103bd0361f6fb48151c8780e205c3fde97140b66762b27effcf2c3b73c05c`  
		Last Modified: Sat, 28 Aug 2021 04:24:47 GMT  
		Size: 7.3 KB (7283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce02139d2773db6b3c7033d9dbc6fdb427c918a69c29b8bb01669296d18c9fe`  
		Last Modified: Sat, 28 Aug 2021 04:24:47 GMT  
		Size: 205.3 KB (205277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c3cb214e79007442b4d21bc48516c0ef35753d8db03a0cc129fa63d01bedde`  
		Last Modified: Sat, 28 Aug 2021 04:24:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29859d07f0b507288c642deae1bae6cbe9d019152647a0c4e76bd86474fda106`  
		Last Modified: Sat, 28 Aug 2021 04:24:47 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6.1`

```console
$ docker pull spiped@sha256:002299301e9b7e3d62ece4463aaf97204581200e1c40a00c6d82aa89506328f4
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

### `spiped:1.6.1` - linux; amd64

```console
$ docker pull spiped@sha256:a696ea93d50ac968bc64ce5ab01eaf4ff13ae39fa9f099b9cd19a8e7a9d07aee
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37320955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683078eccb0851809c92a9dfdb1dcdd47c187bd8a7a5cc960a8fa55b1ece7e86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 12 Oct 2021 01:20:42 GMT
ADD file:16dc2c6d1932194edec28d730b004fd6deca3d0f0e1a07bc5b8b6e8a1662f7af in / 
# Tue, 12 Oct 2021 01:20:42 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 16:21:25 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 12 Oct 2021 16:21:29 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 16:21:29 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Tue, 12 Oct 2021 16:21:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 16:21:56 GMT
VOLUME [/spiped]
# Tue, 12 Oct 2021 16:21:56 GMT
WORKDIR /spiped
# Tue, 12 Oct 2021 16:21:57 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 12 Oct 2021 16:21:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Oct 2021 16:21:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7d63c13d9b9b6ec5f05a2b07daadacaa9c610d01102a662ae9b1d082105f1ffa`  
		Last Modified: Tue, 12 Oct 2021 01:26:05 GMT  
		Size: 31.4 MB (31357311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c825e91f209a1656f91feea4a2861373b55da8c1c3eb72e742c7f31c3d367918`  
		Last Modified: Tue, 12 Oct 2021 16:22:19 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba3f6cb28bad6f7f95e8be3b815465b3d5585c01a7cde8e6c561a81fd08d8e7`  
		Last Modified: Tue, 12 Oct 2021 16:22:19 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbac5321939b951af500d72dc338b30ccdc61d354b3a466ce698a006ca3f4999`  
		Last Modified: Tue, 12 Oct 2021 16:22:20 GMT  
		Size: 6.0 MB (5960389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e58545b0e832a28e4b2fe9fe327f35158f38ccc204ce2c8fe1597803e860c0c2`  
		Last Modified: Tue, 12 Oct 2021 16:22:19 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c1557262dbc7e84098fd29719562170e4c257f980350cf3e68318ecd07a8956`  
		Last Modified: Tue, 12 Oct 2021 16:22:19 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.1` - linux; arm variant v5

```console
$ docker pull spiped@sha256:470773bf2dac565adf268ce74a10c0ca68c421d0de4192c4f6f29f15e8663e54
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33928107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee42cb8fa181c28acac6a722b80b4ea34b101698e1d8886a77f8323f3dbc1d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 12 Oct 2021 00:50:30 GMT
ADD file:fb1afabdc1f93b4866b4c4d696f272b4888519cb5bf35eb7ed1a4c021d1a04c8 in / 
# Tue, 12 Oct 2021 00:50:30 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 11:33:43 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 12 Oct 2021 11:33:53 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 11:33:53 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Tue, 12 Oct 2021 11:34:54 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 11:34:55 GMT
VOLUME [/spiped]
# Tue, 12 Oct 2021 11:34:55 GMT
WORKDIR /spiped
# Tue, 12 Oct 2021 11:34:56 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 12 Oct 2021 11:34:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Oct 2021 11:34:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:5c9bab66abc5c53391435f6fd66e0ff3571295d568f45ac7d2dc480bcbfd56e8`  
		Last Modified: Tue, 12 Oct 2021 01:06:07 GMT  
		Size: 28.9 MB (28899715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29fa5bfe046f908c4024b12760d6a235703129cf889a6b12fe9cb3c909e50ea`  
		Last Modified: Tue, 12 Oct 2021 11:35:35 GMT  
		Size: 1.7 KB (1725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f15e6ebdfdcc8907dc36ff08f672c463d0fbb6c59b0bb232ff1a229f64e4ea34`  
		Last Modified: Tue, 12 Oct 2021 11:35:35 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0030f062ce13c3eb3f6f0020460e01e4beebed73ca735660e5fe74df98d62119`  
		Last Modified: Tue, 12 Oct 2021 11:35:40 GMT  
		Size: 5.0 MB (5025142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9edc074a3eb9dffdb9440831266c18299dcccc42834d767fc489b92ca7f2a48`  
		Last Modified: Tue, 12 Oct 2021 11:35:35 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef7dd4a1c957efda249f4568cd568c8671c526848a4b9f57ffc9783bf81cef3`  
		Last Modified: Tue, 12 Oct 2021 11:35:35 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.1` - linux; arm variant v7

```console
$ docker pull spiped@sha256:958d2e76bb92a4709c36123b6553d179419227b06b733ec19cf1a4899da20853
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31309843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c0880cb9c6c234ff2fe6a3c163710a28845c22e1207ecd0b31cd8887cb77d26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 12 Oct 2021 01:28:36 GMT
ADD file:89eac94007ac04f9168737686fa0a6c737f2c28fc9e5918d4d512924fe1973be in / 
# Tue, 12 Oct 2021 01:28:37 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 03:43:34 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 12 Oct 2021 03:43:41 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 03:43:42 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Tue, 12 Oct 2021 03:44:37 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 03:44:37 GMT
VOLUME [/spiped]
# Tue, 12 Oct 2021 03:44:38 GMT
WORKDIR /spiped
# Tue, 12 Oct 2021 03:44:39 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 12 Oct 2021 03:44:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Oct 2021 03:44:40 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4e5300249f84466df4dc73ea0ce09938ca00c1718bb12619c4f26bd936162331`  
		Last Modified: Tue, 12 Oct 2021 01:44:28 GMT  
		Size: 26.6 MB (26561058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6ecc7e48d063e5bf0a086847e03c73699a183e8a9129e1b8ee3cab1482dde2d`  
		Last Modified: Tue, 12 Oct 2021 03:45:39 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584009012f86b47c7e4e6d1fd99c2d00976e77d0c5c66f0179ed3c7ea7c54725`  
		Last Modified: Tue, 12 Oct 2021 03:45:39 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aae397080ab7f297afe0c2760bc744f5c6ab5ff8f88b8e0830bc8ae8d97b565f`  
		Last Modified: Tue, 12 Oct 2021 03:45:44 GMT  
		Size: 4.7 MB (4745527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c697bb38b9e3862762d00df70d8a431fd891e25b33a03308c9e1cf59a02c712`  
		Last Modified: Tue, 12 Oct 2021 03:45:39 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c305948d80dae9d7e0b495eba60d890696dba8079d33af0619bb473c03c079`  
		Last Modified: Tue, 12 Oct 2021 03:45:39 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.1` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:0e89927947ad9449b0d9919da34674f7fd0095391138d87e11a147544a9a68d5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35310399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9587caa0158c348ca5fe2ca4f04dec822f9902fd9aa85fd89adbb258601bfd9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 12 Oct 2021 01:41:18 GMT
ADD file:d84144ad575672cd6cc8a00c8e5a88ab0545348f040fc249ea5fcf8193b2bce6 in / 
# Tue, 12 Oct 2021 01:41:18 GMT
CMD ["bash"]
# Fri, 12 Nov 2021 18:18:47 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 12 Nov 2021 18:18:51 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 12 Nov 2021 18:18:52 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Fri, 12 Nov 2021 18:19:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 12 Nov 2021 18:19:17 GMT
VOLUME [/spiped]
# Fri, 12 Nov 2021 18:19:18 GMT
WORKDIR /spiped
# Fri, 12 Nov 2021 18:19:20 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 12 Nov 2021 18:19:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 18:19:21 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a9eb63951c1c2ee8efcc12b696928fee3741a2d4eae76f2da3e161a5d90548bf`  
		Last Modified: Tue, 12 Oct 2021 01:48:13 GMT  
		Size: 30.0 MB (30043906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7073e48df5d25256c7c393e704c59a9f201985036d095eb06301c3db8136c68d`  
		Last Modified: Fri, 12 Nov 2021 18:20:24 GMT  
		Size: 1.6 KB (1619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4320355a643d17b982b97870451762d8b863c511b7d751f740c4a9fef0e2912`  
		Last Modified: Fri, 12 Nov 2021 18:20:23 GMT  
		Size: 923.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36f544201620c633914c2a7e3d6a50bffd46317df2cc5156cd6c0453609e14d`  
		Last Modified: Fri, 12 Nov 2021 18:20:25 GMT  
		Size: 5.3 MB (5263513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997c9a99799eb5bf9429e4dd669acfb00da7fc1efc80a08476c2b7f17f5041ca`  
		Last Modified: Fri, 12 Nov 2021 18:20:24 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac3d4565cd75cd143042ec6c135f1225a031c6caf0d66d8bdb4372e6b4a82c06`  
		Last Modified: Fri, 12 Nov 2021 18:20:24 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.1` - linux; 386

```console
$ docker pull spiped@sha256:7e62ad8ce0310713b81cee83e9f2df9a18a94cf41dc99ba28a629f7554aeefa3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40257794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e2bf1ef1d62cb3d5701cdee3834206614fd56059103a424063a602168d47abe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 12 Oct 2021 01:39:47 GMT
ADD file:42196ffa4c70af8d9f1e7b74edb3bb92d47296acf989adf615e8208230f8bd0c in / 
# Tue, 12 Oct 2021 01:39:47 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 22:29:57 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 12 Oct 2021 22:30:05 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 22:30:05 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Tue, 12 Oct 2021 22:31:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 22:31:03 GMT
VOLUME [/spiped]
# Tue, 12 Oct 2021 22:31:03 GMT
WORKDIR /spiped
# Tue, 12 Oct 2021 22:31:04 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 12 Oct 2021 22:31:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Oct 2021 22:31:05 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:87318d165b5c0fdf05c8ccf97d83084f56b4608075a3335b1a46c76295b82753`  
		Last Modified: Tue, 12 Oct 2021 01:47:39 GMT  
		Size: 32.4 MB (32370344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4928a77f1df28f1a46c20db916ae41f9f3331dc5058d03d8298439de44db7b91`  
		Last Modified: Tue, 12 Oct 2021 22:31:47 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb53cf6a9579bfadc1f1fd25438cdfad0ff235db1fe68eb4bb2afd7719b791d`  
		Last Modified: Tue, 12 Oct 2021 22:31:47 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aef6d6c4e04c173d1a0914846ba20d15a2f5f95d88f30069d1eca250898b325`  
		Last Modified: Tue, 12 Oct 2021 22:31:49 GMT  
		Size: 7.9 MB (7884197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b6984d7102b271e3fdc811759f7c556d04efe1259b67fab31e59565516fbed`  
		Last Modified: Tue, 12 Oct 2021 22:31:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e088d6a7c91ad6e879108222fefc2fff6a12de71734608e2b594ae36399c1d29`  
		Last Modified: Tue, 12 Oct 2021 22:31:47 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.1` - linux; mips64le

```console
$ docker pull spiped@sha256:eff58594b3d812760bbc2b4221d61e20cd31ab2ada880341e6e756d55b0e8dfa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35328007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eaccc3d11f7debbf79cd094b33cdae93860e3d40b42f7779edf587b67fc976c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 12 Oct 2021 01:11:15 GMT
ADD file:f90ca8957172106f42a9096c9a21082d51f3201aa78e6f64621a73117e2b7b6a in / 
# Tue, 12 Oct 2021 01:11:16 GMT
CMD ["bash"]
# Wed, 13 Oct 2021 01:30:36 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 13 Oct 2021 01:30:47 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 01:30:47 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Wed, 13 Oct 2021 01:31:57 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 13 Oct 2021 01:31:57 GMT
VOLUME [/spiped]
# Wed, 13 Oct 2021 01:31:58 GMT
WORKDIR /spiped
# Wed, 13 Oct 2021 01:31:58 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 13 Oct 2021 01:31:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Oct 2021 01:31:59 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:59ddca50ce05605e6234c1e7213c39cdedabc48ef11637e12156b7bd69afe161`  
		Last Modified: Tue, 12 Oct 2021 01:20:03 GMT  
		Size: 29.6 MB (29618732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195b13cd10a541ef73f29b46be3ae53a62b047ad5919580c0601496f9a63a3f3`  
		Last Modified: Wed, 13 Oct 2021 01:32:10 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11abea7ddca4b5031aa9fdff9ad5b49b60d36fd5940b7805f93333ca5da482f7`  
		Last Modified: Wed, 13 Oct 2021 01:32:10 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b0c25ac4296890c80ee4f1bea71c20c6a8251252085a00c9f764d7601ac9e7`  
		Last Modified: Wed, 13 Oct 2021 01:32:15 GMT  
		Size: 5.7 MB (5706076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb391de145f2fb5b8ba0dda5a96231a88d0c7e58514503ab861743a74f24c3ea`  
		Last Modified: Wed, 13 Oct 2021 01:32:10 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95bbf8647f8ba425f0ba8506aa7c276231190bb29fb4f34f2306f160f1c3795b`  
		Last Modified: Wed, 13 Oct 2021 01:32:10 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.1` - linux; ppc64le

```console
$ docker pull spiped@sha256:44b13757ab959642c428cd66c8a503318b7916932e88ee0f686aff3c40b6f88e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41263678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aadb76166ced7d8733fac685c49d5b3e6c4e0ca8713e0c26fa2829ab87bb9172`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 12 Oct 2021 01:25:45 GMT
ADD file:d8794fadf16c9948c3574ba28740d08393eca57766340333ad91f9c2a33eb719 in / 
# Tue, 12 Oct 2021 01:25:53 GMT
CMD ["bash"]
# Wed, 13 Oct 2021 08:03:47 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 13 Oct 2021 08:03:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 08:04:02 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Wed, 13 Oct 2021 08:07:07 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 13 Oct 2021 08:07:16 GMT
VOLUME [/spiped]
# Wed, 13 Oct 2021 08:07:24 GMT
WORKDIR /spiped
# Wed, 13 Oct 2021 08:07:26 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 13 Oct 2021 08:07:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Oct 2021 08:07:32 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6c28c1405c677dd809094d06190225b38cee3d24f18da38d287ef5bcc67884d6`  
		Last Modified: Tue, 12 Oct 2021 01:37:00 GMT  
		Size: 35.3 MB (35258729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c02b2acecad78932397dca6224b551528ccaf70fed1c60da8884b1ee077de8`  
		Last Modified: Wed, 13 Oct 2021 08:08:15 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e5dcbe4d07e13aa9f6162d201034eb2b26b9f69987315148425a39102ba3df`  
		Last Modified: Wed, 13 Oct 2021 08:08:15 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d805dc3af7457dd0105eca804e08afa7eed7d23d36613d054713cef0cd7f301a`  
		Last Modified: Wed, 13 Oct 2021 08:08:16 GMT  
		Size: 6.0 MB (6001677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c36c3789c72419dd7c04f766b8ef090133dd4afbffd43366f439be9bdcb7d88`  
		Last Modified: Wed, 13 Oct 2021 08:08:15 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1414313671940f5f943d32775bed04903cb0d2af90ece5729859bf3a6284b292`  
		Last Modified: Wed, 13 Oct 2021 08:08:15 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.1` - linux; s390x

```console
$ docker pull spiped@sha256:0ea844713c5be79b86f0ed403e6d7a38c6b37f92d690035d328f933e7d828d3c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34828428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:224bab1ef5e8e000f26cc5a15fc7f3d3851979e858ee4d475d6f18295d2e5c27`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 12 Oct 2021 00:42:27 GMT
ADD file:6038dd6db57fb05c3d39c02c3379667ccd2989e7667ff773a8020fe6a69a760c in / 
# Tue, 12 Oct 2021 00:42:29 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 04:31:53 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 12 Oct 2021 04:31:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 04:31:56 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Tue, 12 Oct 2021 04:32:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 04:32:12 GMT
VOLUME [/spiped]
# Tue, 12 Oct 2021 04:32:12 GMT
WORKDIR /spiped
# Tue, 12 Oct 2021 04:32:12 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 12 Oct 2021 04:32:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Oct 2021 04:32:12 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ded751c48f72503973be01be2794cc039490f22b039b8ac106e9f17de4980742`  
		Last Modified: Tue, 12 Oct 2021 00:48:05 GMT  
		Size: 29.6 MB (29641215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9339c2f00e96cfd5d66e69eeaec4b0592b4ff1f2798f167750a1ca9f15264c42`  
		Last Modified: Tue, 12 Oct 2021 04:32:43 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd1ae5a6b4870b8387c848046338d1914594cc3738bc5631e96eb22fba322290`  
		Last Modified: Tue, 12 Oct 2021 04:32:42 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61437e76afae45198095fc895e7d4154ce1ca4d68f4a7f7ad160c99b7bb4d341`  
		Last Modified: Tue, 12 Oct 2021 04:32:43 GMT  
		Size: 5.2 MB (5183956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90528d405e1a63caf7013a7715aa3ba6a0d0eabc5ce0955bc7a383eb3dd3cef8`  
		Last Modified: Tue, 12 Oct 2021 04:32:43 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5158295881f8176e354104f90f22e99b9211b9860e03e398f262f8a6b5828a4`  
		Last Modified: Tue, 12 Oct 2021 04:32:43 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6.1-alpine`

```console
$ docker pull spiped@sha256:94622cc2ebc9d6e307aeff3e1b8a1408af46869fdf4f99c1cfb2c7648ab83012
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

### `spiped:1.6.1-alpine` - linux; amd64

```console
$ docker pull spiped@sha256:44015ddc42ceef8878c9b2bad7a6bcbf2b5d2ca42ab52cca20f9f66b2c15ffd8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3036014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c65d8337530e6b8e116202287d477945c4375886702df4698f8740106658a777`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 28 Aug 2021 00:56:12 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 28 Aug 2021 00:56:13 GMT
RUN apk add --no-cache libssl1.1
# Sat, 28 Aug 2021 00:56:13 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Sat, 28 Aug 2021 00:56:31 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Sat, 28 Aug 2021 00:56:31 GMT
VOLUME [/spiped]
# Sat, 28 Aug 2021 00:56:31 GMT
WORKDIR /spiped
# Sat, 28 Aug 2021 00:56:31 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 28 Aug 2021 00:56:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Aug 2021 00:56:32 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72fe484884c949a7fba8b7d917cbe40b9fa50036f4c10e4b82e3075576fe3fc`  
		Last Modified: Sat, 28 Aug 2021 00:56:49 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06083e8d35a44724cf84de43d971fb5b141e8ce6468a5c267c43c96f79869f23`  
		Last Modified: Sat, 28 Aug 2021 00:56:49 GMT  
		Size: 7.3 KB (7282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46037fda176acae1eef93fa1dde784253576faf4d880c75c8d7df76fdf212dda`  
		Last Modified: Sat, 28 Aug 2021 00:56:49 GMT  
		Size: 212.5 KB (212547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb3cd7f024c8cfa70e1c8e8f282e44395bbaa20cd69851af0552d8041deaea2`  
		Last Modified: Sat, 28 Aug 2021 00:56:49 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64fccea2af66d4ffdbdd93edf485c1e6e17f14ac10329842af6fea7741bd3504`  
		Last Modified: Sat, 28 Aug 2021 00:56:49 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.1-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:7e548b9910cf9bcbce660ff537e09660dbd9d84cbc06621e45fb2282f2f52270
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2838978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8539d235dbd2d180f98df622ec1586ed595c7026c53f57b67876cbe0b641be9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Sat, 28 Aug 2021 00:39:21 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 28 Aug 2021 00:39:23 GMT
RUN apk add --no-cache libssl1.1
# Sat, 28 Aug 2021 00:39:23 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Sat, 28 Aug 2021 00:39:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Sat, 28 Aug 2021 00:39:58 GMT
VOLUME [/spiped]
# Sat, 28 Aug 2021 00:39:58 GMT
WORKDIR /spiped
# Sat, 28 Aug 2021 00:39:59 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 28 Aug 2021 00:39:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Aug 2021 00:40:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3ec865614b924d3ebd8faaf1468ff031de3ccb2f178656d907e4a89f8673776`  
		Last Modified: Sat, 28 Aug 2021 00:40:31 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07908dc20812a0124cb96563b08ff2d4ebd32f0ca0cef02511faa0c127496e96`  
		Last Modified: Sat, 28 Aug 2021 00:40:31 GMT  
		Size: 7.3 KB (7290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae2ce7f8303145adfe2a17235c758d30fa18338c417eb73738b591c1dd3d1315`  
		Last Modified: Sat, 28 Aug 2021 00:40:31 GMT  
		Size: 202.5 KB (202499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d07f8ab6ed47190923d1d152d960c5fd80b7d9f27f84a289e8236a1e4f22843c`  
		Last Modified: Sat, 28 Aug 2021 00:40:31 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f17d0a64e682741c70413fc90f0d8a4dac61425dcc5c98ce054909120977e587`  
		Last Modified: Sat, 28 Aug 2021 00:40:31 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.1-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:24d05f05df7127b2aa61654a9d29c77a0c2a00f8ba29dbfc127a672700d5f652
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2635217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c197156cacbfdbdb870ce3391ad1bdf7d6c922d18648489e7549033356f432b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 27 Aug 2021 17:57:31 GMT
ADD file:a7da7992ccea54d3295231027614f138aa45c4d4a25ea6ec9bf7b316b9f67d95 in / 
# Fri, 27 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Sat, 28 Aug 2021 03:04:23 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 28 Aug 2021 03:04:26 GMT
RUN apk add --no-cache libssl1.1
# Sat, 28 Aug 2021 03:04:26 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Sat, 28 Aug 2021 03:04:59 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Sat, 28 Aug 2021 03:04:59 GMT
VOLUME [/spiped]
# Sat, 28 Aug 2021 03:05:00 GMT
WORKDIR /spiped
# Sat, 28 Aug 2021 03:05:00 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 28 Aug 2021 03:05:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Aug 2021 03:05:01 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a14774a5a62e0f454febaec7cb603e18a6a8e25ef9da4a4da85b155bdd5e5a7a`  
		Last Modified: Fri, 27 Aug 2021 17:59:00 GMT  
		Size: 2.4 MB (2430419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c187e6961a8f3ae8bf645e1fbec375c4f7c3d8146ab5ee5a09f57cd5615f33cb`  
		Last Modified: Sat, 28 Aug 2021 03:05:54 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e56c389f9017243d26a8fd61b3cc3385e2b4dcf930d608cc682a5ff3b437137`  
		Last Modified: Sat, 28 Aug 2021 03:05:54 GMT  
		Size: 7.3 KB (7298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b0da469457d5465481ffd06dc86cd457daaf02e8b501cbee7b9cb52b675525`  
		Last Modified: Sat, 28 Aug 2021 03:05:54 GMT  
		Size: 195.8 KB (195763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eea4333c9f229866ca36ab2d7e036e1d23031e78c62c3ad0bcbbeacaaf8f8e65`  
		Last Modified: Sat, 28 Aug 2021 03:05:54 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4907440a689992d3e1fbcc2fcef650c5ef7b7abe5b8b3aa9c97d6d697d5050fd`  
		Last Modified: Sat, 28 Aug 2021 03:05:54 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.1-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:cbaa0533059fb17c768fe05790c3675b5b5cecf35f0b461e5347d763b1322af8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2932006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49787cc7861893f9d6020342db1639e60d7af6850ca4866d08840d8438a2b0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 18:19:31 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 12 Nov 2021 18:19:33 GMT
RUN apk add --no-cache libssl1.1
# Fri, 12 Nov 2021 18:19:34 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Fri, 12 Nov 2021 18:19:54 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Fri, 12 Nov 2021 18:19:55 GMT
VOLUME [/spiped]
# Fri, 12 Nov 2021 18:19:56 GMT
WORKDIR /spiped
# Fri, 12 Nov 2021 18:19:58 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 12 Nov 2021 18:19:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 18:19:59 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbcce6bf922e4817964b0a9575d547fbb39004874a87c290658dcbb8939209e`  
		Last Modified: Fri, 12 Nov 2021 18:20:41 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b342172a90f6f6a837eeb8f0025e02facad5a97fdd12c0aeac68c2411928d16f`  
		Last Modified: Fri, 12 Nov 2021 18:20:41 GMT  
		Size: 7.8 KB (7751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8a670bc36ab2f74e650d7cb573c4c3542673b9488e2659efbc0d6b9db67529`  
		Last Modified: Fri, 12 Nov 2021 18:20:41 GMT  
		Size: 204.9 KB (204879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698de19c09a4c9763fb04c4946f3bffafe6556fcfe73a3d55bbb4255f65bd458`  
		Last Modified: Fri, 12 Nov 2021 18:20:41 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d1aa9a890181cdc95e60ea01849306cb72c967e13716722baa68c7bca76fdb`  
		Last Modified: Fri, 12 Nov 2021 18:20:42 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.1-alpine` - linux; 386

```console
$ docker pull spiped@sha256:da842be683e4aa6e7f0e6581d7d9bd1604d2d140a1b452e47a1ca595261af814
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3055327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c67a7b5670b88fbd238447f1f65531173381d0aff05ec6d63ef2df4dfb7b8c43`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 27 Aug 2021 17:38:29 GMT
ADD file:42a7bc5a08b546b47049dd0f89ae4e7a8c86342f87000f39ade3ff52916a6c2e in / 
# Fri, 27 Aug 2021 17:38:30 GMT
CMD ["/bin/sh"]
# Sat, 28 Aug 2021 00:35:24 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 28 Aug 2021 00:35:25 GMT
RUN apk add --no-cache libssl1.1
# Sat, 28 Aug 2021 00:35:25 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Sat, 28 Aug 2021 00:35:45 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Sat, 28 Aug 2021 00:35:45 GMT
VOLUME [/spiped]
# Sat, 28 Aug 2021 00:35:45 GMT
WORKDIR /spiped
# Sat, 28 Aug 2021 00:35:46 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 28 Aug 2021 00:35:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Aug 2021 00:35:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b11ae9fc5d8a106cfed3a6f6c75e5b5b5797c566fac4411622b4055df6541286`  
		Last Modified: Fri, 27 Aug 2021 17:39:18 GMT  
		Size: 2.8 MB (2822857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95070702ac27305ca355fc2880dec01d9e18d3c8a4a22842a599db59ea5467e0`  
		Last Modified: Sat, 28 Aug 2021 00:36:17 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35be501885b2efd06479a1d05af31f0d06d6b0a5c4dfb3f760af81657d7919ea`  
		Last Modified: Sat, 28 Aug 2021 00:36:17 GMT  
		Size: 7.3 KB (7287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f5e404d9d5a395b15445e0403dfa9a598ab9ecd02814798d33098ac6a8ba9c`  
		Last Modified: Sat, 28 Aug 2021 00:36:17 GMT  
		Size: 223.4 KB (223445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233b8287cb974321164bff4ca80e9a231471fecf0bbab1bbf130172709ae47ae`  
		Last Modified: Sat, 28 Aug 2021 00:36:17 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c88353a13d0403b037e398aa01ea54701b91f2adf180d6ed9df1b155b62c89`  
		Last Modified: Sat, 28 Aug 2021 00:36:17 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.1-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:3c83af52715b14ccfd27cc89b7b988ae73b9d05500efd053b99b027c0328f14d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3042554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f59b6df7881927f19f4b2dcab5974d93c4284e7e9ba9c21098a82d888389b26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 27 Aug 2021 19:39:54 GMT
ADD file:d213c56ffc24a5051e8060fd0fec1a0520367c10d88ab16321c36336b6c66098 in / 
# Fri, 27 Aug 2021 19:39:59 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 21:36:44 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 27 Aug 2021 21:36:56 GMT
RUN apk add --no-cache libssl1.1
# Fri, 27 Aug 2021 21:37:02 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Fri, 27 Aug 2021 21:37:39 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Fri, 27 Aug 2021 21:37:41 GMT
VOLUME [/spiped]
# Fri, 27 Aug 2021 21:37:48 GMT
WORKDIR /spiped
# Fri, 27 Aug 2021 21:37:54 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 27 Aug 2021 21:38:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Aug 2021 21:38:21 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:63da8ca98f7b4b94381aed56862a60aecf355d9428b9aeb7c61d5bd017100c18`  
		Last Modified: Fri, 27 Aug 2021 19:41:06 GMT  
		Size: 2.8 MB (2812284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f143c775bd94ef9de49da05aab2353301bc02ceb74a237332f8d9b23e193234b`  
		Last Modified: Fri, 27 Aug 2021 21:38:57 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9067169d42bea9851adf89b67776e5a280513855fb73120a8d2c5f0051a1097b`  
		Last Modified: Fri, 27 Aug 2021 21:38:57 GMT  
		Size: 7.3 KB (7292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe10232ba40d32a7b84a0fe16aa0a2b418d2bdf093335c9fbaf56b08e751c54e`  
		Last Modified: Fri, 27 Aug 2021 21:38:57 GMT  
		Size: 221.2 KB (221238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c7d84f077aa3ad717767ac56d4b1ea509bc7a9c81e57e3f4e210fe09205ee9`  
		Last Modified: Fri, 27 Aug 2021 21:38:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c90dd2a4fa5a2acd662ddc7f2ec01550257e4bbaae18ab7a94fdd288523cf8`  
		Last Modified: Fri, 27 Aug 2021 21:38:57 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.1-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:3852ee4130c6bfe6eb29489ab1f82c2aceed2d65ba3a11477360199bd6ba4bd3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2817762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d772c7d45678813ce17e2e65d11aa3e23e0517de39acbfe03eaaadf3558b6f40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 27 Aug 2021 17:41:29 GMT
ADD file:9b40ee281e8797067fb2ae207c406084cb81593090338a8b7cb09ade52168daa in / 
# Fri, 27 Aug 2021 17:41:30 GMT
CMD ["/bin/sh"]
# Sat, 28 Aug 2021 04:23:48 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 28 Aug 2021 04:23:49 GMT
RUN apk add --no-cache libssl1.1
# Sat, 28 Aug 2021 04:23:50 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Sat, 28 Aug 2021 04:24:07 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Sat, 28 Aug 2021 04:24:08 GMT
VOLUME [/spiped]
# Sat, 28 Aug 2021 04:24:08 GMT
WORKDIR /spiped
# Sat, 28 Aug 2021 04:24:09 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 28 Aug 2021 04:24:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Aug 2021 04:24:10 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:da14cb6b6dc946dbb2d84386bcaca84e2d46f650767cd11bdb3331ec9d623988`  
		Last Modified: Fri, 27 Aug 2021 17:42:25 GMT  
		Size: 2.6 MB (2603464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b447a66831aa123cebdb722d7d1efb39f1ffb26129fdf9b8937935375852a206`  
		Last Modified: Sat, 28 Aug 2021 04:24:46 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b103bd0361f6fb48151c8780e205c3fde97140b66762b27effcf2c3b73c05c`  
		Last Modified: Sat, 28 Aug 2021 04:24:47 GMT  
		Size: 7.3 KB (7283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce02139d2773db6b3c7033d9dbc6fdb427c918a69c29b8bb01669296d18c9fe`  
		Last Modified: Sat, 28 Aug 2021 04:24:47 GMT  
		Size: 205.3 KB (205277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c3cb214e79007442b4d21bc48516c0ef35753d8db03a0cc129fa63d01bedde`  
		Last Modified: Sat, 28 Aug 2021 04:24:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29859d07f0b507288c642deae1bae6cbe9d019152647a0c4e76bd86474fda106`  
		Last Modified: Sat, 28 Aug 2021 04:24:47 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:alpine`

```console
$ docker pull spiped@sha256:94622cc2ebc9d6e307aeff3e1b8a1408af46869fdf4f99c1cfb2c7648ab83012
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
$ docker pull spiped@sha256:44015ddc42ceef8878c9b2bad7a6bcbf2b5d2ca42ab52cca20f9f66b2c15ffd8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3036014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c65d8337530e6b8e116202287d477945c4375886702df4698f8740106658a777`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 28 Aug 2021 00:56:12 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 28 Aug 2021 00:56:13 GMT
RUN apk add --no-cache libssl1.1
# Sat, 28 Aug 2021 00:56:13 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Sat, 28 Aug 2021 00:56:31 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Sat, 28 Aug 2021 00:56:31 GMT
VOLUME [/spiped]
# Sat, 28 Aug 2021 00:56:31 GMT
WORKDIR /spiped
# Sat, 28 Aug 2021 00:56:31 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 28 Aug 2021 00:56:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Aug 2021 00:56:32 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72fe484884c949a7fba8b7d917cbe40b9fa50036f4c10e4b82e3075576fe3fc`  
		Last Modified: Sat, 28 Aug 2021 00:56:49 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06083e8d35a44724cf84de43d971fb5b141e8ce6468a5c267c43c96f79869f23`  
		Last Modified: Sat, 28 Aug 2021 00:56:49 GMT  
		Size: 7.3 KB (7282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46037fda176acae1eef93fa1dde784253576faf4d880c75c8d7df76fdf212dda`  
		Last Modified: Sat, 28 Aug 2021 00:56:49 GMT  
		Size: 212.5 KB (212547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb3cd7f024c8cfa70e1c8e8f282e44395bbaa20cd69851af0552d8041deaea2`  
		Last Modified: Sat, 28 Aug 2021 00:56:49 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64fccea2af66d4ffdbdd93edf485c1e6e17f14ac10329842af6fea7741bd3504`  
		Last Modified: Sat, 28 Aug 2021 00:56:49 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:7e548b9910cf9bcbce660ff537e09660dbd9d84cbc06621e45fb2282f2f52270
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2838978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8539d235dbd2d180f98df622ec1586ed595c7026c53f57b67876cbe0b641be9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Sat, 28 Aug 2021 00:39:21 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 28 Aug 2021 00:39:23 GMT
RUN apk add --no-cache libssl1.1
# Sat, 28 Aug 2021 00:39:23 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Sat, 28 Aug 2021 00:39:57 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Sat, 28 Aug 2021 00:39:58 GMT
VOLUME [/spiped]
# Sat, 28 Aug 2021 00:39:58 GMT
WORKDIR /spiped
# Sat, 28 Aug 2021 00:39:59 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 28 Aug 2021 00:39:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Aug 2021 00:40:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3ec865614b924d3ebd8faaf1468ff031de3ccb2f178656d907e4a89f8673776`  
		Last Modified: Sat, 28 Aug 2021 00:40:31 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07908dc20812a0124cb96563b08ff2d4ebd32f0ca0cef02511faa0c127496e96`  
		Last Modified: Sat, 28 Aug 2021 00:40:31 GMT  
		Size: 7.3 KB (7290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae2ce7f8303145adfe2a17235c758d30fa18338c417eb73738b591c1dd3d1315`  
		Last Modified: Sat, 28 Aug 2021 00:40:31 GMT  
		Size: 202.5 KB (202499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d07f8ab6ed47190923d1d152d960c5fd80b7d9f27f84a289e8236a1e4f22843c`  
		Last Modified: Sat, 28 Aug 2021 00:40:31 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f17d0a64e682741c70413fc90f0d8a4dac61425dcc5c98ce054909120977e587`  
		Last Modified: Sat, 28 Aug 2021 00:40:31 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:24d05f05df7127b2aa61654a9d29c77a0c2a00f8ba29dbfc127a672700d5f652
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2635217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c197156cacbfdbdb870ce3391ad1bdf7d6c922d18648489e7549033356f432b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 27 Aug 2021 17:57:31 GMT
ADD file:a7da7992ccea54d3295231027614f138aa45c4d4a25ea6ec9bf7b316b9f67d95 in / 
# Fri, 27 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Sat, 28 Aug 2021 03:04:23 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 28 Aug 2021 03:04:26 GMT
RUN apk add --no-cache libssl1.1
# Sat, 28 Aug 2021 03:04:26 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Sat, 28 Aug 2021 03:04:59 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Sat, 28 Aug 2021 03:04:59 GMT
VOLUME [/spiped]
# Sat, 28 Aug 2021 03:05:00 GMT
WORKDIR /spiped
# Sat, 28 Aug 2021 03:05:00 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 28 Aug 2021 03:05:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Aug 2021 03:05:01 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a14774a5a62e0f454febaec7cb603e18a6a8e25ef9da4a4da85b155bdd5e5a7a`  
		Last Modified: Fri, 27 Aug 2021 17:59:00 GMT  
		Size: 2.4 MB (2430419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c187e6961a8f3ae8bf645e1fbec375c4f7c3d8146ab5ee5a09f57cd5615f33cb`  
		Last Modified: Sat, 28 Aug 2021 03:05:54 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e56c389f9017243d26a8fd61b3cc3385e2b4dcf930d608cc682a5ff3b437137`  
		Last Modified: Sat, 28 Aug 2021 03:05:54 GMT  
		Size: 7.3 KB (7298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b0da469457d5465481ffd06dc86cd457daaf02e8b501cbee7b9cb52b675525`  
		Last Modified: Sat, 28 Aug 2021 03:05:54 GMT  
		Size: 195.8 KB (195763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eea4333c9f229866ca36ab2d7e036e1d23031e78c62c3ad0bcbbeacaaf8f8e65`  
		Last Modified: Sat, 28 Aug 2021 03:05:54 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4907440a689992d3e1fbcc2fcef650c5ef7b7abe5b8b3aa9c97d6d697d5050fd`  
		Last Modified: Sat, 28 Aug 2021 03:05:54 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:cbaa0533059fb17c768fe05790c3675b5b5cecf35f0b461e5347d763b1322af8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2932006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49787cc7861893f9d6020342db1639e60d7af6850ca4866d08840d8438a2b0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 18:19:31 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 12 Nov 2021 18:19:33 GMT
RUN apk add --no-cache libssl1.1
# Fri, 12 Nov 2021 18:19:34 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Fri, 12 Nov 2021 18:19:54 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Fri, 12 Nov 2021 18:19:55 GMT
VOLUME [/spiped]
# Fri, 12 Nov 2021 18:19:56 GMT
WORKDIR /spiped
# Fri, 12 Nov 2021 18:19:58 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 12 Nov 2021 18:19:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 18:19:59 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffbcce6bf922e4817964b0a9575d547fbb39004874a87c290658dcbb8939209e`  
		Last Modified: Fri, 12 Nov 2021 18:20:41 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b342172a90f6f6a837eeb8f0025e02facad5a97fdd12c0aeac68c2411928d16f`  
		Last Modified: Fri, 12 Nov 2021 18:20:41 GMT  
		Size: 7.8 KB (7751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8a670bc36ab2f74e650d7cb573c4c3542673b9488e2659efbc0d6b9db67529`  
		Last Modified: Fri, 12 Nov 2021 18:20:41 GMT  
		Size: 204.9 KB (204879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698de19c09a4c9763fb04c4946f3bffafe6556fcfe73a3d55bbb4255f65bd458`  
		Last Modified: Fri, 12 Nov 2021 18:20:41 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d1aa9a890181cdc95e60ea01849306cb72c967e13716722baa68c7bca76fdb`  
		Last Modified: Fri, 12 Nov 2021 18:20:42 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; 386

```console
$ docker pull spiped@sha256:da842be683e4aa6e7f0e6581d7d9bd1604d2d140a1b452e47a1ca595261af814
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3055327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c67a7b5670b88fbd238447f1f65531173381d0aff05ec6d63ef2df4dfb7b8c43`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 27 Aug 2021 17:38:29 GMT
ADD file:42a7bc5a08b546b47049dd0f89ae4e7a8c86342f87000f39ade3ff52916a6c2e in / 
# Fri, 27 Aug 2021 17:38:30 GMT
CMD ["/bin/sh"]
# Sat, 28 Aug 2021 00:35:24 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 28 Aug 2021 00:35:25 GMT
RUN apk add --no-cache libssl1.1
# Sat, 28 Aug 2021 00:35:25 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Sat, 28 Aug 2021 00:35:45 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Sat, 28 Aug 2021 00:35:45 GMT
VOLUME [/spiped]
# Sat, 28 Aug 2021 00:35:45 GMT
WORKDIR /spiped
# Sat, 28 Aug 2021 00:35:46 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 28 Aug 2021 00:35:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Aug 2021 00:35:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b11ae9fc5d8a106cfed3a6f6c75e5b5b5797c566fac4411622b4055df6541286`  
		Last Modified: Fri, 27 Aug 2021 17:39:18 GMT  
		Size: 2.8 MB (2822857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95070702ac27305ca355fc2880dec01d9e18d3c8a4a22842a599db59ea5467e0`  
		Last Modified: Sat, 28 Aug 2021 00:36:17 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35be501885b2efd06479a1d05af31f0d06d6b0a5c4dfb3f760af81657d7919ea`  
		Last Modified: Sat, 28 Aug 2021 00:36:17 GMT  
		Size: 7.3 KB (7287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f5e404d9d5a395b15445e0403dfa9a598ab9ecd02814798d33098ac6a8ba9c`  
		Last Modified: Sat, 28 Aug 2021 00:36:17 GMT  
		Size: 223.4 KB (223445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233b8287cb974321164bff4ca80e9a231471fecf0bbab1bbf130172709ae47ae`  
		Last Modified: Sat, 28 Aug 2021 00:36:17 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c88353a13d0403b037e398aa01ea54701b91f2adf180d6ed9df1b155b62c89`  
		Last Modified: Sat, 28 Aug 2021 00:36:17 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:3c83af52715b14ccfd27cc89b7b988ae73b9d05500efd053b99b027c0328f14d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3042554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f59b6df7881927f19f4b2dcab5974d93c4284e7e9ba9c21098a82d888389b26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 27 Aug 2021 19:39:54 GMT
ADD file:d213c56ffc24a5051e8060fd0fec1a0520367c10d88ab16321c36336b6c66098 in / 
# Fri, 27 Aug 2021 19:39:59 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 21:36:44 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 27 Aug 2021 21:36:56 GMT
RUN apk add --no-cache libssl1.1
# Fri, 27 Aug 2021 21:37:02 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Fri, 27 Aug 2021 21:37:39 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Fri, 27 Aug 2021 21:37:41 GMT
VOLUME [/spiped]
# Fri, 27 Aug 2021 21:37:48 GMT
WORKDIR /spiped
# Fri, 27 Aug 2021 21:37:54 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 27 Aug 2021 21:38:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Aug 2021 21:38:21 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:63da8ca98f7b4b94381aed56862a60aecf355d9428b9aeb7c61d5bd017100c18`  
		Last Modified: Fri, 27 Aug 2021 19:41:06 GMT  
		Size: 2.8 MB (2812284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f143c775bd94ef9de49da05aab2353301bc02ceb74a237332f8d9b23e193234b`  
		Last Modified: Fri, 27 Aug 2021 21:38:57 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9067169d42bea9851adf89b67776e5a280513855fb73120a8d2c5f0051a1097b`  
		Last Modified: Fri, 27 Aug 2021 21:38:57 GMT  
		Size: 7.3 KB (7292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe10232ba40d32a7b84a0fe16aa0a2b418d2bdf093335c9fbaf56b08e751c54e`  
		Last Modified: Fri, 27 Aug 2021 21:38:57 GMT  
		Size: 221.2 KB (221238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c7d84f077aa3ad717767ac56d4b1ea509bc7a9c81e57e3f4e210fe09205ee9`  
		Last Modified: Fri, 27 Aug 2021 21:38:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c90dd2a4fa5a2acd662ddc7f2ec01550257e4bbaae18ab7a94fdd288523cf8`  
		Last Modified: Fri, 27 Aug 2021 21:38:57 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; s390x

```console
$ docker pull spiped@sha256:3852ee4130c6bfe6eb29489ab1f82c2aceed2d65ba3a11477360199bd6ba4bd3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2817762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d772c7d45678813ce17e2e65d11aa3e23e0517de39acbfe03eaaadf3558b6f40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 27 Aug 2021 17:41:29 GMT
ADD file:9b40ee281e8797067fb2ae207c406084cb81593090338a8b7cb09ade52168daa in / 
# Fri, 27 Aug 2021 17:41:30 GMT
CMD ["/bin/sh"]
# Sat, 28 Aug 2021 04:23:48 GMT
RUN addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 28 Aug 2021 04:23:49 GMT
RUN apk add --no-cache libssl1.1
# Sat, 28 Aug 2021 04:23:50 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Sat, 28 Aug 2021 04:24:07 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del .build-deps
# Sat, 28 Aug 2021 04:24:08 GMT
VOLUME [/spiped]
# Sat, 28 Aug 2021 04:24:08 GMT
WORKDIR /spiped
# Sat, 28 Aug 2021 04:24:09 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 28 Aug 2021 04:24:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Aug 2021 04:24:10 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:da14cb6b6dc946dbb2d84386bcaca84e2d46f650767cd11bdb3331ec9d623988`  
		Last Modified: Fri, 27 Aug 2021 17:42:25 GMT  
		Size: 2.6 MB (2603464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b447a66831aa123cebdb722d7d1efb39f1ffb26129fdf9b8937935375852a206`  
		Last Modified: Sat, 28 Aug 2021 04:24:46 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b103bd0361f6fb48151c8780e205c3fde97140b66762b27effcf2c3b73c05c`  
		Last Modified: Sat, 28 Aug 2021 04:24:47 GMT  
		Size: 7.3 KB (7283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce02139d2773db6b3c7033d9dbc6fdb427c918a69c29b8bb01669296d18c9fe`  
		Last Modified: Sat, 28 Aug 2021 04:24:47 GMT  
		Size: 205.3 KB (205277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c3cb214e79007442b4d21bc48516c0ef35753d8db03a0cc129fa63d01bedde`  
		Last Modified: Sat, 28 Aug 2021 04:24:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29859d07f0b507288c642deae1bae6cbe9d019152647a0c4e76bd86474fda106`  
		Last Modified: Sat, 28 Aug 2021 04:24:47 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:latest`

```console
$ docker pull spiped@sha256:002299301e9b7e3d62ece4463aaf97204581200e1c40a00c6d82aa89506328f4
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
$ docker pull spiped@sha256:a696ea93d50ac968bc64ce5ab01eaf4ff13ae39fa9f099b9cd19a8e7a9d07aee
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37320955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683078eccb0851809c92a9dfdb1dcdd47c187bd8a7a5cc960a8fa55b1ece7e86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 12 Oct 2021 01:20:42 GMT
ADD file:16dc2c6d1932194edec28d730b004fd6deca3d0f0e1a07bc5b8b6e8a1662f7af in / 
# Tue, 12 Oct 2021 01:20:42 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 16:21:25 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 12 Oct 2021 16:21:29 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 16:21:29 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Tue, 12 Oct 2021 16:21:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 16:21:56 GMT
VOLUME [/spiped]
# Tue, 12 Oct 2021 16:21:56 GMT
WORKDIR /spiped
# Tue, 12 Oct 2021 16:21:57 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 12 Oct 2021 16:21:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Oct 2021 16:21:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7d63c13d9b9b6ec5f05a2b07daadacaa9c610d01102a662ae9b1d082105f1ffa`  
		Last Modified: Tue, 12 Oct 2021 01:26:05 GMT  
		Size: 31.4 MB (31357311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c825e91f209a1656f91feea4a2861373b55da8c1c3eb72e742c7f31c3d367918`  
		Last Modified: Tue, 12 Oct 2021 16:22:19 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba3f6cb28bad6f7f95e8be3b815465b3d5585c01a7cde8e6c561a81fd08d8e7`  
		Last Modified: Tue, 12 Oct 2021 16:22:19 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbac5321939b951af500d72dc338b30ccdc61d354b3a466ce698a006ca3f4999`  
		Last Modified: Tue, 12 Oct 2021 16:22:20 GMT  
		Size: 6.0 MB (5960389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e58545b0e832a28e4b2fe9fe327f35158f38ccc204ce2c8fe1597803e860c0c2`  
		Last Modified: Tue, 12 Oct 2021 16:22:19 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c1557262dbc7e84098fd29719562170e4c257f980350cf3e68318ecd07a8956`  
		Last Modified: Tue, 12 Oct 2021 16:22:19 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; arm variant v5

```console
$ docker pull spiped@sha256:470773bf2dac565adf268ce74a10c0ca68c421d0de4192c4f6f29f15e8663e54
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33928107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee42cb8fa181c28acac6a722b80b4ea34b101698e1d8886a77f8323f3dbc1d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 12 Oct 2021 00:50:30 GMT
ADD file:fb1afabdc1f93b4866b4c4d696f272b4888519cb5bf35eb7ed1a4c021d1a04c8 in / 
# Tue, 12 Oct 2021 00:50:30 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 11:33:43 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 12 Oct 2021 11:33:53 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 11:33:53 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Tue, 12 Oct 2021 11:34:54 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 11:34:55 GMT
VOLUME [/spiped]
# Tue, 12 Oct 2021 11:34:55 GMT
WORKDIR /spiped
# Tue, 12 Oct 2021 11:34:56 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 12 Oct 2021 11:34:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Oct 2021 11:34:57 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:5c9bab66abc5c53391435f6fd66e0ff3571295d568f45ac7d2dc480bcbfd56e8`  
		Last Modified: Tue, 12 Oct 2021 01:06:07 GMT  
		Size: 28.9 MB (28899715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29fa5bfe046f908c4024b12760d6a235703129cf889a6b12fe9cb3c909e50ea`  
		Last Modified: Tue, 12 Oct 2021 11:35:35 GMT  
		Size: 1.7 KB (1725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f15e6ebdfdcc8907dc36ff08f672c463d0fbb6c59b0bb232ff1a229f64e4ea34`  
		Last Modified: Tue, 12 Oct 2021 11:35:35 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0030f062ce13c3eb3f6f0020460e01e4beebed73ca735660e5fe74df98d62119`  
		Last Modified: Tue, 12 Oct 2021 11:35:40 GMT  
		Size: 5.0 MB (5025142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9edc074a3eb9dffdb9440831266c18299dcccc42834d767fc489b92ca7f2a48`  
		Last Modified: Tue, 12 Oct 2021 11:35:35 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef7dd4a1c957efda249f4568cd568c8671c526848a4b9f57ffc9783bf81cef3`  
		Last Modified: Tue, 12 Oct 2021 11:35:35 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; arm variant v7

```console
$ docker pull spiped@sha256:958d2e76bb92a4709c36123b6553d179419227b06b733ec19cf1a4899da20853
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31309843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c0880cb9c6c234ff2fe6a3c163710a28845c22e1207ecd0b31cd8887cb77d26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 12 Oct 2021 01:28:36 GMT
ADD file:89eac94007ac04f9168737686fa0a6c737f2c28fc9e5918d4d512924fe1973be in / 
# Tue, 12 Oct 2021 01:28:37 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 03:43:34 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 12 Oct 2021 03:43:41 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 03:43:42 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Tue, 12 Oct 2021 03:44:37 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 03:44:37 GMT
VOLUME [/spiped]
# Tue, 12 Oct 2021 03:44:38 GMT
WORKDIR /spiped
# Tue, 12 Oct 2021 03:44:39 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 12 Oct 2021 03:44:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Oct 2021 03:44:40 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4e5300249f84466df4dc73ea0ce09938ca00c1718bb12619c4f26bd936162331`  
		Last Modified: Tue, 12 Oct 2021 01:44:28 GMT  
		Size: 26.6 MB (26561058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6ecc7e48d063e5bf0a086847e03c73699a183e8a9129e1b8ee3cab1482dde2d`  
		Last Modified: Tue, 12 Oct 2021 03:45:39 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584009012f86b47c7e4e6d1fd99c2d00976e77d0c5c66f0179ed3c7ea7c54725`  
		Last Modified: Tue, 12 Oct 2021 03:45:39 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aae397080ab7f297afe0c2760bc744f5c6ab5ff8f88b8e0830bc8ae8d97b565f`  
		Last Modified: Tue, 12 Oct 2021 03:45:44 GMT  
		Size: 4.7 MB (4745527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c697bb38b9e3862762d00df70d8a431fd891e25b33a03308c9e1cf59a02c712`  
		Last Modified: Tue, 12 Oct 2021 03:45:39 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c305948d80dae9d7e0b495eba60d890696dba8079d33af0619bb473c03c079`  
		Last Modified: Tue, 12 Oct 2021 03:45:39 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:0e89927947ad9449b0d9919da34674f7fd0095391138d87e11a147544a9a68d5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35310399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9587caa0158c348ca5fe2ca4f04dec822f9902fd9aa85fd89adbb258601bfd9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 12 Oct 2021 01:41:18 GMT
ADD file:d84144ad575672cd6cc8a00c8e5a88ab0545348f040fc249ea5fcf8193b2bce6 in / 
# Tue, 12 Oct 2021 01:41:18 GMT
CMD ["bash"]
# Fri, 12 Nov 2021 18:18:47 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 12 Nov 2021 18:18:51 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 12 Nov 2021 18:18:52 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Fri, 12 Nov 2021 18:19:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 12 Nov 2021 18:19:17 GMT
VOLUME [/spiped]
# Fri, 12 Nov 2021 18:19:18 GMT
WORKDIR /spiped
# Fri, 12 Nov 2021 18:19:20 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 12 Nov 2021 18:19:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 18:19:21 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a9eb63951c1c2ee8efcc12b696928fee3741a2d4eae76f2da3e161a5d90548bf`  
		Last Modified: Tue, 12 Oct 2021 01:48:13 GMT  
		Size: 30.0 MB (30043906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7073e48df5d25256c7c393e704c59a9f201985036d095eb06301c3db8136c68d`  
		Last Modified: Fri, 12 Nov 2021 18:20:24 GMT  
		Size: 1.6 KB (1619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4320355a643d17b982b97870451762d8b863c511b7d751f740c4a9fef0e2912`  
		Last Modified: Fri, 12 Nov 2021 18:20:23 GMT  
		Size: 923.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36f544201620c633914c2a7e3d6a50bffd46317df2cc5156cd6c0453609e14d`  
		Last Modified: Fri, 12 Nov 2021 18:20:25 GMT  
		Size: 5.3 MB (5263513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997c9a99799eb5bf9429e4dd669acfb00da7fc1efc80a08476c2b7f17f5041ca`  
		Last Modified: Fri, 12 Nov 2021 18:20:24 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac3d4565cd75cd143042ec6c135f1225a031c6caf0d66d8bdb4372e6b4a82c06`  
		Last Modified: Fri, 12 Nov 2021 18:20:24 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; 386

```console
$ docker pull spiped@sha256:7e62ad8ce0310713b81cee83e9f2df9a18a94cf41dc99ba28a629f7554aeefa3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40257794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e2bf1ef1d62cb3d5701cdee3834206614fd56059103a424063a602168d47abe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 12 Oct 2021 01:39:47 GMT
ADD file:42196ffa4c70af8d9f1e7b74edb3bb92d47296acf989adf615e8208230f8bd0c in / 
# Tue, 12 Oct 2021 01:39:47 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 22:29:57 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 12 Oct 2021 22:30:05 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 22:30:05 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Tue, 12 Oct 2021 22:31:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 22:31:03 GMT
VOLUME [/spiped]
# Tue, 12 Oct 2021 22:31:03 GMT
WORKDIR /spiped
# Tue, 12 Oct 2021 22:31:04 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 12 Oct 2021 22:31:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Oct 2021 22:31:05 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:87318d165b5c0fdf05c8ccf97d83084f56b4608075a3335b1a46c76295b82753`  
		Last Modified: Tue, 12 Oct 2021 01:47:39 GMT  
		Size: 32.4 MB (32370344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4928a77f1df28f1a46c20db916ae41f9f3331dc5058d03d8298439de44db7b91`  
		Last Modified: Tue, 12 Oct 2021 22:31:47 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb53cf6a9579bfadc1f1fd25438cdfad0ff235db1fe68eb4bb2afd7719b791d`  
		Last Modified: Tue, 12 Oct 2021 22:31:47 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aef6d6c4e04c173d1a0914846ba20d15a2f5f95d88f30069d1eca250898b325`  
		Last Modified: Tue, 12 Oct 2021 22:31:49 GMT  
		Size: 7.9 MB (7884197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b6984d7102b271e3fdc811759f7c556d04efe1259b67fab31e59565516fbed`  
		Last Modified: Tue, 12 Oct 2021 22:31:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e088d6a7c91ad6e879108222fefc2fff6a12de71734608e2b594ae36399c1d29`  
		Last Modified: Tue, 12 Oct 2021 22:31:47 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; mips64le

```console
$ docker pull spiped@sha256:eff58594b3d812760bbc2b4221d61e20cd31ab2ada880341e6e756d55b0e8dfa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35328007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eaccc3d11f7debbf79cd094b33cdae93860e3d40b42f7779edf587b67fc976c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 12 Oct 2021 01:11:15 GMT
ADD file:f90ca8957172106f42a9096c9a21082d51f3201aa78e6f64621a73117e2b7b6a in / 
# Tue, 12 Oct 2021 01:11:16 GMT
CMD ["bash"]
# Wed, 13 Oct 2021 01:30:36 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 13 Oct 2021 01:30:47 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 01:30:47 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Wed, 13 Oct 2021 01:31:57 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 13 Oct 2021 01:31:57 GMT
VOLUME [/spiped]
# Wed, 13 Oct 2021 01:31:58 GMT
WORKDIR /spiped
# Wed, 13 Oct 2021 01:31:58 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 13 Oct 2021 01:31:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Oct 2021 01:31:59 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:59ddca50ce05605e6234c1e7213c39cdedabc48ef11637e12156b7bd69afe161`  
		Last Modified: Tue, 12 Oct 2021 01:20:03 GMT  
		Size: 29.6 MB (29618732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195b13cd10a541ef73f29b46be3ae53a62b047ad5919580c0601496f9a63a3f3`  
		Last Modified: Wed, 13 Oct 2021 01:32:10 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11abea7ddca4b5031aa9fdff9ad5b49b60d36fd5940b7805f93333ca5da482f7`  
		Last Modified: Wed, 13 Oct 2021 01:32:10 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b0c25ac4296890c80ee4f1bea71c20c6a8251252085a00c9f764d7601ac9e7`  
		Last Modified: Wed, 13 Oct 2021 01:32:15 GMT  
		Size: 5.7 MB (5706076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb391de145f2fb5b8ba0dda5a96231a88d0c7e58514503ab861743a74f24c3ea`  
		Last Modified: Wed, 13 Oct 2021 01:32:10 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95bbf8647f8ba425f0ba8506aa7c276231190bb29fb4f34f2306f160f1c3795b`  
		Last Modified: Wed, 13 Oct 2021 01:32:10 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; ppc64le

```console
$ docker pull spiped@sha256:44b13757ab959642c428cd66c8a503318b7916932e88ee0f686aff3c40b6f88e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41263678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aadb76166ced7d8733fac685c49d5b3e6c4e0ca8713e0c26fa2829ab87bb9172`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 12 Oct 2021 01:25:45 GMT
ADD file:d8794fadf16c9948c3574ba28740d08393eca57766340333ad91f9c2a33eb719 in / 
# Tue, 12 Oct 2021 01:25:53 GMT
CMD ["bash"]
# Wed, 13 Oct 2021 08:03:47 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 13 Oct 2021 08:03:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 08:04:02 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Wed, 13 Oct 2021 08:07:07 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 13 Oct 2021 08:07:16 GMT
VOLUME [/spiped]
# Wed, 13 Oct 2021 08:07:24 GMT
WORKDIR /spiped
# Wed, 13 Oct 2021 08:07:26 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 13 Oct 2021 08:07:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Oct 2021 08:07:32 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6c28c1405c677dd809094d06190225b38cee3d24f18da38d287ef5bcc67884d6`  
		Last Modified: Tue, 12 Oct 2021 01:37:00 GMT  
		Size: 35.3 MB (35258729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c02b2acecad78932397dca6224b551528ccaf70fed1c60da8884b1ee077de8`  
		Last Modified: Wed, 13 Oct 2021 08:08:15 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e5dcbe4d07e13aa9f6162d201034eb2b26b9f69987315148425a39102ba3df`  
		Last Modified: Wed, 13 Oct 2021 08:08:15 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d805dc3af7457dd0105eca804e08afa7eed7d23d36613d054713cef0cd7f301a`  
		Last Modified: Wed, 13 Oct 2021 08:08:16 GMT  
		Size: 6.0 MB (6001677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c36c3789c72419dd7c04f766b8ef090133dd4afbffd43366f439be9bdcb7d88`  
		Last Modified: Wed, 13 Oct 2021 08:08:15 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1414313671940f5f943d32775bed04903cb0d2af90ece5729859bf3a6284b292`  
		Last Modified: Wed, 13 Oct 2021 08:08:15 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; s390x

```console
$ docker pull spiped@sha256:0ea844713c5be79b86f0ed403e6d7a38c6b37f92d690035d328f933e7d828d3c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34828428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:224bab1ef5e8e000f26cc5a15fc7f3d3851979e858ee4d475d6f18295d2e5c27`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 12 Oct 2021 00:42:27 GMT
ADD file:6038dd6db57fb05c3d39c02c3379667ccd2989e7667ff773a8020fe6a69a760c in / 
# Tue, 12 Oct 2021 00:42:29 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 04:31:53 GMT
RUN groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 12 Oct 2021 04:31:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 04:31:56 GMT
ENV SPIPED_VERSION=1.6.1 SPIPED_DOWNLOAD_SHA256=8d7089979db79a531a0ecc507b113ac6f2cf5f19305571eff1d3413e0ab33713
# Tue, 12 Oct 2021 04:32:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 04:32:12 GMT
VOLUME [/spiped]
# Tue, 12 Oct 2021 04:32:12 GMT
WORKDIR /spiped
# Tue, 12 Oct 2021 04:32:12 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 12 Oct 2021 04:32:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Oct 2021 04:32:12 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ded751c48f72503973be01be2794cc039490f22b039b8ac106e9f17de4980742`  
		Last Modified: Tue, 12 Oct 2021 00:48:05 GMT  
		Size: 29.6 MB (29641215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9339c2f00e96cfd5d66e69eeaec4b0592b4ff1f2798f167750a1ca9f15264c42`  
		Last Modified: Tue, 12 Oct 2021 04:32:43 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd1ae5a6b4870b8387c848046338d1914594cc3738bc5631e96eb22fba322290`  
		Last Modified: Tue, 12 Oct 2021 04:32:42 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61437e76afae45198095fc895e7d4154ce1ca4d68f4a7f7ad160c99b7bb4d341`  
		Last Modified: Tue, 12 Oct 2021 04:32:43 GMT  
		Size: 5.2 MB (5183956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90528d405e1a63caf7013a7715aa3ba6a0d0eabc5ce0955bc7a383eb3dd3cef8`  
		Last Modified: Tue, 12 Oct 2021 04:32:43 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5158295881f8176e354104f90f22e99b9211b9860e03e398f262f8a6b5828a4`  
		Last Modified: Tue, 12 Oct 2021 04:32:43 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
