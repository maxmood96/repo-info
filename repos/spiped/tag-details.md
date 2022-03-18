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
$ docker pull spiped@sha256:d0d169a896962896013eb85ba8c10fcb5e5ab61c7b17b88e2e41a14dd75dedd5
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
$ docker pull spiped@sha256:b8d2ab2976a3b82a57e4ac9fc033752dfaf040d529691989e424cd5c99d8bbd3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37346333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68b6bef8dc6e1cbd84fb52a34b7b7d7df36d02946bf4bdfca5aa1b7f2d52176f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:59 GMT
ADD file:36919ae6bb25e3269eff949443129a01a8a43fb967fe6563939ebe1e1e9b8228 in / 
# Thu, 17 Mar 2022 04:03:59 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 15:52:38 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 17 Mar 2022 15:52:43 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 15:52:43 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 15:53:21 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 17 Mar 2022 15:53:21 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 15:53:22 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 15:53:22 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 15:53:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 15:53:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ae13dd57832654086618a81dbc128846aa092489260c326ee95429b63c3cf213`  
		Last Modified: Thu, 17 Mar 2022 04:10:05 GMT  
		Size: 31.4 MB (31376572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a76f2896127d7514587b03a8586b6c4bf68ca03ee67882432f282d5a3dc8e5d1`  
		Last Modified: Thu, 17 Mar 2022 15:54:13 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac159b91e9882052a2a7c77bf3ec73c84ea2c50d117cf1129e7e552374d62c2`  
		Last Modified: Thu, 17 Mar 2022 15:54:13 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd11eb085d6fc73cdb158b796cc6592d653f2f64bc48fd6bd88b02289f0dcfc`  
		Last Modified: Thu, 17 Mar 2022 15:54:15 GMT  
		Size: 6.0 MB (5966507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1610fbfaf3d68521b5f2784f03d10b65adac79bb491680dce45623e5cfd64b9`  
		Last Modified: Thu, 17 Mar 2022 15:54:13 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba1c750cce13a53c755ec9a30804efe928ee400172b3e12bbeb62b7d06178d3`  
		Last Modified: Thu, 17 Mar 2022 15:54:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; arm variant v5

```console
$ docker pull spiped@sha256:8a2e0011c5701f972d5ba018f0874593df829ac6c310b4bc74e48f548a82b624
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33950244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1fb2363cc87afddb3e829dfa3fbc4638f7d761ca756e0c04ae478180c55d43`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 05:19:45 GMT
ADD file:1eb4f937d40230354e20e28ed781234acd4be2b0dab72f87131a3eac66349719 in / 
# Thu, 17 Mar 2022 05:19:46 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 19:07:31 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 17 Mar 2022 19:07:41 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 19:07:41 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 19:08:46 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 17 Mar 2022 19:08:46 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 19:08:47 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 19:08:50 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 19:08:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 19:08:52 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4da455e7774c0e977d862a56ab6d85f33ce5dd5a77d45a0a74a272e9eae6bea0`  
		Last Modified: Thu, 17 Mar 2022 05:35:01 GMT  
		Size: 28.9 MB (28919702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ccaa8f7993c69ae0db39ad4c2027a13ce97175da89f5be82de6a2ca2a97c7d1`  
		Last Modified: Thu, 17 Mar 2022 19:09:25 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9512592020427919bc6c45a56ea8a3e87091e9b9b72c5f4081ddbdfda9fbe931`  
		Last Modified: Thu, 17 Mar 2022 19:09:26 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2010aa0813bd04163cffb9ff94e259b6216dc2c427790ff8bbb2f3b7ccb45846`  
		Last Modified: Thu, 17 Mar 2022 19:09:28 GMT  
		Size: 5.0 MB (5027289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3447d294931d6120cea1ca769318e6e3730d1d3a01afc8a3f8046adb9872d7`  
		Last Modified: Thu, 17 Mar 2022 19:09:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ba318f72a277eedbbb07d36dd5fe2c4195238cb2bd1aa540f8a89a169f22a2`  
		Last Modified: Thu, 17 Mar 2022 19:09:25 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; arm variant v7

```console
$ docker pull spiped@sha256:ac215edcc30b28977b317d77ccaaae94761d4354587e9800d101bb637e1149d0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31315718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4d7a6cecd75cfc07f7f336a43f8c0c2bd623ff9d78a61a9c7442249f5b36df1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 01 Mar 2022 02:02:56 GMT
ADD file:c6b519323fd1fa09b9f8c8608778872e8fa6208cb0b42aaccdef4479a469f5f4 in / 
# Tue, 01 Mar 2022 02:02:57 GMT
CMD ["bash"]
# Wed, 02 Mar 2022 16:17:58 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 02 Mar 2022 16:18:05 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 16:18:05 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 02 Mar 2022 16:18:49 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 02 Mar 2022 16:18:50 GMT
VOLUME [/spiped]
# Wed, 02 Mar 2022 16:18:50 GMT
WORKDIR /spiped
# Wed, 02 Mar 2022 16:18:51 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 02 Mar 2022 16:18:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 16:18:52 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:59dbb2ac3829352dd707e28e037734c9fbdef5b03aea31e3929ddcead949afee`  
		Last Modified: Tue, 01 Mar 2022 02:19:09 GMT  
		Size: 26.6 MB (26565105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d308a84eca5cd40a5b3b38f20aba12ad984055514266c5f21895dbd7ae398c4`  
		Last Modified: Wed, 02 Mar 2022 16:19:54 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885c743661aaee24e106ee3f2083d0acdcff80bbbfb0663485d199324303dbe2`  
		Last Modified: Wed, 02 Mar 2022 16:19:54 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1b566deb17f5e2852900d444a17df344a45e23a180e0dfc06251a994ef5333c`  
		Last Modified: Wed, 02 Mar 2022 16:19:59 GMT  
		Size: 4.7 MB (4747364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f044884cf1737497ba826896f6b7e83d791a1b320f0dc816a7862caffe3d2848`  
		Last Modified: Wed, 02 Mar 2022 16:19:54 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e071d50afe6ad4ee58ac45ec6df078835658702fde56f4230838ffb45ed917e5`  
		Last Modified: Wed, 02 Mar 2022 16:19:54 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:fd6ccb6336851679362386de45250510a5e80ef3c4e7df2ae724eaa4c9667ed0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35335910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7240db44c2f7942501fdbf02463d450aff3590fc9bc59ad1940947b652f01fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 03:21:57 GMT
ADD file:e52e032f1ace6abd44b3647d43c1b8ae30bac6de804eef09c6ccd793057996fd in / 
# Thu, 17 Mar 2022 03:21:58 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 21:04:34 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 17 Mar 2022 21:04:37 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 21:04:37 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 21:04:55 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 17 Mar 2022 21:04:56 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 21:04:57 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 21:04:59 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 21:04:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 21:05:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:32252aec0777ac025a158bc2a8317650a4f2a0a875387011b1165013874f8723`  
		Last Modified: Thu, 17 Mar 2022 03:28:36 GMT  
		Size: 30.1 MB (30063013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f39180b559e5aed1b40421eec8f7b61457cc16f2cfee7f2da5aa250b61d4370`  
		Last Modified: Thu, 17 Mar 2022 21:05:48 GMT  
		Size: 1.6 KB (1617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcd781ba64e538c462ceeb478df86f9e82f9043472f590c90b8b77e1c69b494`  
		Last Modified: Thu, 17 Mar 2022 21:05:49 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6acdb1b2ac977841bfba332aa093360fd27c5ae5aeeeb8ed34c5da6d36cbc01`  
		Last Modified: Thu, 17 Mar 2022 21:05:50 GMT  
		Size: 5.3 MB (5269921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f5b809a8f2f8d99685a97d9b9b90ed684e872055f59a0bef726c106ed92eae`  
		Last Modified: Thu, 17 Mar 2022 21:05:49 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815c0e22b949966496c66a9c25b6ae9090833f44298de5096f6f6673d2b5eeed`  
		Last Modified: Thu, 17 Mar 2022 21:05:49 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; 386

```console
$ docker pull spiped@sha256:ed2f5c92201304d5bbfd3a42f000b351c22b4d58f49e952733cb43f825a3e301
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40281229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e319a53a099b51990813e4b7cfcd49725cfe0eda506064c73bbb2bc420375e97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 08:15:53 GMT
ADD file:2d6be3846f0e5fabd85bc9409b1e2223cad4c57c76f96e9f81489ba78a72a1f5 in / 
# Thu, 17 Mar 2022 08:15:54 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 21:38:49 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 17 Mar 2022 21:38:53 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 21:38:53 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 21:39:26 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 17 Mar 2022 21:39:26 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 21:39:27 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 21:39:27 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 21:39:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 21:39:27 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:176085117cac9b2cf2cf57b3a10c9811dbd2773497fbac3086b5024070447e97`  
		Last Modified: Thu, 17 Mar 2022 08:24:00 GMT  
		Size: 32.4 MB (32386475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f0023ca52fa68e0b790d53b1989cc86a09c03c3f5ba512bd7254e660798701`  
		Last Modified: Thu, 17 Mar 2022 21:40:39 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f169664f6c06e48b52c02faa7212ffdbed368d76e4046ee62757dcdad99ec1`  
		Last Modified: Thu, 17 Mar 2022 21:40:39 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e208248e53ac127f9ba59ef6496e619a4aa53b7da6cada4f8c9eefab9d6eb759`  
		Last Modified: Thu, 17 Mar 2022 21:40:42 GMT  
		Size: 7.9 MB (7891501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e182dd8aad03bcc4a4fc70c4d5477e38448020a78e7598e41bc1d584729d764b`  
		Last Modified: Thu, 17 Mar 2022 21:40:39 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4315719c3c75933b98aafbac692d4aa273eec4588f2647f7ad5ae7032b336ba2`  
		Last Modified: Thu, 17 Mar 2022 21:40:39 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; mips64le

```console
$ docker pull spiped@sha256:ad61e440c067a6b168769664de1c184685e3582a1422d3c2d1681ba457ff7215
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35347773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556e5433be4b6d7d5c9e1b8aea73caac9038b7fa0ced3fcc6d085d06eae244cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 08:53:04 GMT
ADD file:795ac4eba576bc4c995df2a18b10ce802ee8a05417cdc53f5aa09452ecf2e832 in / 
# Thu, 17 Mar 2022 08:53:08 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 21:25:08 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 18 Mar 2022 21:25:24 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 21:25:27 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 18 Mar 2022 21:27:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 18 Mar 2022 21:27:04 GMT
VOLUME [/spiped]
# Fri, 18 Mar 2022 21:27:07 GMT
WORKDIR /spiped
# Fri, 18 Mar 2022 21:27:09 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 18 Mar 2022 21:27:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 21:27:15 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4799d88734ae94287a665c0e14621a744706cfbe17a0cf27ae9b0cc630927b11`  
		Last Modified: Thu, 17 Mar 2022 10:43:20 GMT  
		Size: 29.6 MB (29639810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c3bb983a06c1d0519d23a6efec25298a548ce43495f86ad94ed19dc18240d6`  
		Last Modified: Fri, 18 Mar 2022 21:27:38 GMT  
		Size: 1.6 KB (1614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0dd02a98e85a0552aa2aef9bcf7cc1127e26a8aebbd1b4174d51b68e253093`  
		Last Modified: Fri, 18 Mar 2022 21:27:38 GMT  
		Size: 926.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73a235ac7d157ff9e32cdc51b831aae0fde62bfb42dcc02a77a0e52df565b34`  
		Last Modified: Fri, 18 Mar 2022 21:27:44 GMT  
		Size: 5.7 MB (5704986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c944593c2417013162356e68bb977d4fdaff97eba73de773bb2f61032d200cca`  
		Last Modified: Fri, 18 Mar 2022 21:27:39 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b86ea964515b4d10fea8515b90d3d4557e4f7db1a99f2e9d9cadd52c34ea59`  
		Last Modified: Fri, 18 Mar 2022 21:27:38 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; ppc64le

```console
$ docker pull spiped@sha256:9797106231608e33cf1bf6b4aa3121e668221249a4393633d99fd2d54dd41dc1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41281331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:387b2511d5857028002168cda350ddc9cba69bb5e9c7efe68e8aba8e77b6237e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 11:17:54 GMT
ADD file:e8555f1cb439a45786b92e929cfa154b51f668c5b4cd69e4ce98340c5998fe0c in / 
# Thu, 17 Mar 2022 11:18:00 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 11:32:51 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 18 Mar 2022 11:33:08 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 11:33:11 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 18 Mar 2022 11:35:53 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 18 Mar 2022 11:36:02 GMT
VOLUME [/spiped]
# Fri, 18 Mar 2022 11:36:08 GMT
WORKDIR /spiped
# Fri, 18 Mar 2022 11:36:16 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 18 Mar 2022 11:36:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 11:36:29 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:aec78dc45d7b3df12df0672d13e22005592b453f03ff2580efac2598dddd680b`  
		Last Modified: Thu, 17 Mar 2022 11:28:17 GMT  
		Size: 35.3 MB (35279758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833a842281729982038158055afe9827cf83082a73928d160267a96c3a210909`  
		Last Modified: Fri, 18 Mar 2022 11:38:42 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb19a8bea8ac6452690b2abb425c234fa132fc999d44dc8678c047c83a2b8768`  
		Last Modified: Fri, 18 Mar 2022 11:38:42 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298a5cd67fcc1d54d133544fddcaee22c2d52b321bea99ddebfdc5e92cf5b9c5`  
		Last Modified: Fri, 18 Mar 2022 11:38:43 GMT  
		Size: 6.0 MB (5998310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:304b3fc5bf6eef287d420bb4471463e5dd7f258b64abc28ac0fa3cc28c389078`  
		Last Modified: Fri, 18 Mar 2022 11:38:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ae40f3931d22932d6ae2313ffce38370977d00b771c456e04802d1dd5b8724`  
		Last Modified: Fri, 18 Mar 2022 11:38:42 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; s390x

```console
$ docker pull spiped@sha256:04aafcacad77a9b72d2d47a38a232c9e3645a438c0131b47a4018b46f979be32
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34844908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ff67ace7af078b229b5928d2f0d8eba4dfc9336bd01cc8af778512ed9b34cbd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 03:06:58 GMT
ADD file:52f9267b4c57ac585a0d3d47a6f2ae1a71398264173ad4f190332957fa629c67 in / 
# Thu, 17 Mar 2022 03:07:01 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 16:49:57 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 17 Mar 2022 16:50:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 16:50:00 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 16:50:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 17 Mar 2022 16:50:12 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 16:50:12 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 16:50:12 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 16:50:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 16:50:12 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d101968410e5005df630b0572aec03c88de55b8de81f3cf7e6a57e1ce2e5a8e5`  
		Last Modified: Thu, 17 Mar 2022 03:12:46 GMT  
		Size: 29.7 MB (29655795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6ffc821fd848073df862253a81ff1adea16b2b909005db2cbce4ee66eb2a85`  
		Last Modified: Thu, 17 Mar 2022 16:50:52 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b47ffd2d769d0417b9b329e411c5d0abcf3eeb26d24af586ae0aaaf90e42b6a7`  
		Last Modified: Thu, 17 Mar 2022 16:50:52 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e66ff429e104d86eab7bf4adb5dc2db5a803f49496c73e98e298fe5b252e89`  
		Last Modified: Thu, 17 Mar 2022 16:50:53 GMT  
		Size: 5.2 MB (5185854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7601978f39168626ccd46b4478d2d3ca54a1a90e2436bddd43a901fe451ddb54`  
		Last Modified: Thu, 17 Mar 2022 16:50:53 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a37fe55f363c9febb17d5ff4cde072423c7d7197dbe1fdcda48d4483abe56b9`  
		Last Modified: Thu, 17 Mar 2022 16:50:52 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1-alpine`

```console
$ docker pull spiped@sha256:651bee70b611b34012354942ee14d8cd1c394a654381018891a216b65438b06d
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
$ docker pull spiped@sha256:fa4240521d3ff244261dfbcea3a9e63b5f2858626355d782bd7b97a37a706e0e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3037036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46fd9df2bffa7e91039d2ee71224e10bea88319d02d25fc53832aef21376ecd6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 04:01:58 GMT
ADD file:cf4b631a115c2bbfbd81cad2d3041bceb64a8136aac92ba8a63b6c51d60af764 in / 
# Thu, 17 Mar 2022 04:01:59 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 15:53:28 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 17 Mar 2022 15:53:30 GMT
RUN apk add --no-cache libssl1.1
# Thu, 17 Mar 2022 15:53:30 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 15:53:51 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 17 Mar 2022 15:53:52 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 15:53:52 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 15:53:52 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 15:53:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 15:53:53 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3d243047344378e9b7136d552d48feb7ea8b6fe14ce0990e0cc011d5e369626a`  
		Last Modified: Thu, 17 Mar 2022 04:02:41 GMT  
		Size: 2.8 MB (2812636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28609b3adb4c05998e1162db6c538ca407f2280011d95fcd8a244d805a5b735`  
		Last Modified: Thu, 17 Mar 2022 15:54:31 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b4dfa35cdb53635d719c0c532ec9937293bcefd0cfc46f8bd1feecfdf05a95`  
		Last Modified: Thu, 17 Mar 2022 15:54:31 GMT  
		Size: 7.8 KB (7789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1305ebaa04a3fbf473d9073ba19d8e7c200053717456c94b4aa81ad2379537a`  
		Last Modified: Thu, 17 Mar 2022 15:54:34 GMT  
		Size: 214.9 KB (214875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a9314de395635f68354281ea4e4c80ccd1a83382ea0c0797d439c77466a954`  
		Last Modified: Thu, 17 Mar 2022 15:54:31 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8620fb27c9cb715ea3d3d0940cbfe238f1c60983b2586367d7f672d1d83ff6e`  
		Last Modified: Thu, 17 Mar 2022 15:54:31 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:59826251d3a0ad2527c0bafdc1ea568962d7f5f3528b1e98d3aaa3926d652ac4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2833671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25087c53823bfdb0b76bf4d89b11576da2bbb0a43269741c3f40a8aa03ddd93a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 02:26:45 GMT
ADD file:9c8618405ef54d562132919ffe49c862d014b402e0e4813b87bf01574fa04c0e in / 
# Thu, 17 Mar 2022 02:26:45 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 10:53:28 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 17 Mar 2022 10:53:30 GMT
RUN apk add --no-cache libssl1.1
# Thu, 17 Mar 2022 10:53:31 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 10:53:50 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 17 Mar 2022 10:53:50 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 10:53:51 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 10:53:52 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 10:53:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 10:53:52 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:787f016efa9bc7812361be134f731e845b97fba19169cf3615e7048c0412380e`  
		Last Modified: Thu, 17 Mar 2022 02:28:24 GMT  
		Size: 2.6 MB (2624973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8491e25887dfb5f3955a484700defebb2ff52083efbde9795a85971df7a476f1`  
		Last Modified: Thu, 17 Mar 2022 10:54:24 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35d33f304fab5de548bc59cc09d332370e572391cf8e6547a78ecad3df48c27`  
		Last Modified: Thu, 17 Mar 2022 10:54:24 GMT  
		Size: 7.8 KB (7780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a10fd4be356562398de356a11d85dbf1d36467d9069e828647d3827e6c97cda2`  
		Last Modified: Thu, 17 Mar 2022 10:54:24 GMT  
		Size: 199.2 KB (199175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08779a270c83a7fa3e6660371def3ae5d7436e7afc2058d26fc7277c6465b79e`  
		Last Modified: Thu, 17 Mar 2022 10:54:24 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98221b50c485d80403bee1e97ffcda727cc378c9408fe0b9d2d32656e2e8ba42`  
		Last Modified: Thu, 17 Mar 2022 10:54:24 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:277d22d33ab8cd23ff5bf04d4e60841c8a335de8fdb772173601e9a4d4cb00bf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3802328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f94c64b2c706a58b82aa60bafca69c1fd15fb76714e5ca4aae0f1e4a47e3f1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Mon, 27 Dec 2021 18:00:04 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Mon, 27 Dec 2021 18:00:06 GMT
RUN apk add --no-cache libssl1.1
# Mon, 27 Dec 2021 18:00:06 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Mon, 27 Dec 2021 18:00:25 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Mon, 27 Dec 2021 18:00:26 GMT
VOLUME [/spiped]
# Mon, 27 Dec 2021 18:00:26 GMT
WORKDIR /spiped
# Mon, 27 Dec 2021 18:00:27 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Mon, 27 Dec 2021 18:00:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Dec 2021 18:00:28 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca194041621ab40d8e7f24b7f7e82aa07760b2dafcd26472bd7fae96171989a`  
		Last Modified: Mon, 27 Dec 2021 18:01:41 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e934f04cb0ca6a107389bcb614eb02143fb079eef09a47a9248e3c4ff07864`  
		Last Modified: Mon, 27 Dec 2021 18:01:41 GMT  
		Size: 7.7 KB (7749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4111e5d44f2316d799c8b9144d8f35765b0bf330b8d596d99e504969cd48e07a`  
		Last Modified: Mon, 27 Dec 2021 18:01:42 GMT  
		Size: 1.4 MB (1358077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46d751b026ad913b2a48630c96460959a733e75728d55aafbd389197bf81857`  
		Last Modified: Mon, 27 Dec 2021 18:01:41 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5140561b01c4c6ae8b47c729fd289d7eef4a2b0e9c427a6bd35a86747e966206`  
		Last Modified: Mon, 27 Dec 2021 18:01:41 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:d99e51a55cc06f9f9bb1a381fbcccc5b8a617221ede6d99e80fa0f1455d9a7c7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2931463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70fa2e490f06ca016a59e8ccb25bdf2aca9f52652ffd37b739b119385121ed0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 03:19:52 GMT
ADD file:cd7d91362950471ca4678cf3833dc47119ab519dea51424c847bbbb21e1649d4 in / 
# Thu, 17 Mar 2022 03:19:52 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 21:05:07 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 17 Mar 2022 21:05:08 GMT
RUN apk add --no-cache libssl1.1
# Thu, 17 Mar 2022 21:05:09 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 21:05:19 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 17 Mar 2022 21:05:20 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 21:05:21 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 21:05:23 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 21:05:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 21:05:24 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:148d739a8e6b9342daa1f5b428d3a3c6118f340f21df28c16e06f918ef150147`  
		Last Modified: Thu, 17 Mar 2022 03:20:45 GMT  
		Size: 2.7 MB (2714807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfe03b788288bfc55a2e69551194eb50a0e5968d87eb615e001116670eca8d1`  
		Last Modified: Thu, 17 Mar 2022 21:06:08 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ebbe0c7d8e482b1cc3a2c35380a3da9aba32e7419814e8463d19e20ab058a5`  
		Last Modified: Thu, 17 Mar 2022 21:06:08 GMT  
		Size: 7.8 KB (7750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd44380493879dfe08522b418a1697db90bf574f812b27abf9f5363d6130acfa`  
		Last Modified: Thu, 17 Mar 2022 21:06:08 GMT  
		Size: 207.2 KB (207231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:684fec7d45ce25526ac84e65dbb141f72835e9b00faa35ffd4bd2d1b5f98b3c6`  
		Last Modified: Thu, 17 Mar 2022 21:06:08 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:526257cb94ed56c056f2917a4a8e8c81f2c1b9b6911487da82418348ffa037f0`  
		Last Modified: Thu, 17 Mar 2022 21:06:09 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; 386

```console
$ docker pull spiped@sha256:29c7cebe60cecc9f7cbb75c243694894ccead716974c52d9e7f9a99a1e7931c3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3056990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65970f53cd34df6344b60d5b1f188ae0408dfd33dd9036a90562f4b4d4d4ef83`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 08:13:03 GMT
ADD file:22216bc654d9177244235f242fa83cae3b283b3c145cad7ccf11c0d29f5f0ff2 in / 
# Thu, 17 Mar 2022 08:13:03 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 21:39:40 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 17 Mar 2022 21:39:42 GMT
RUN apk add --no-cache libssl1.1
# Thu, 17 Mar 2022 21:39:42 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 21:40:00 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 17 Mar 2022 21:40:00 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 21:40:00 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 21:40:00 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 21:40:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 21:40:01 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:93317a1f65ec94b67aefe728a598022610246404e3a68d391c76cd0e5244a2a0`  
		Last Modified: Thu, 17 Mar 2022 08:13:56 GMT  
		Size: 2.8 MB (2821789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8535b315fbad030f6fe4b11974d789b28ec85b2e79677eb197239c4e2d58ad07`  
		Last Modified: Thu, 17 Mar 2022 21:41:04 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47d449347fe74957e2caaf9718edfca3c882962cffbce71dd4e6207078459b6`  
		Last Modified: Thu, 17 Mar 2022 21:41:04 GMT  
		Size: 7.8 KB (7782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c09f03ca1752043d6dfd052d7aae794162b6013a723e0efc9477f848ca481c5`  
		Last Modified: Thu, 17 Mar 2022 21:41:04 GMT  
		Size: 225.7 KB (225683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd9e35cc22870710eefd82f88e16ed34c080e8c4f505037f17080f14e818cd1a`  
		Last Modified: Thu, 17 Mar 2022 21:41:04 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1021ec3b3986cf8edf968a928a55219fb145dbe088f59a3ffb7144791d7831d`  
		Last Modified: Thu, 17 Mar 2022 21:41:04 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:8c23f5e4d58ef3fce86009c4f9d2b536e5dd7645357d02dc8f3143a45d24b62a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3036720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:525943d93e23029964172e9971ee55221214131aa72607d782b906782cebd905`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 11:14:04 GMT
ADD file:ddc94e1e084c05807db26adcc95b47a137fa47fb391e75998b338ada65e00c1c in / 
# Thu, 17 Mar 2022 11:14:09 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 11:36:53 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 18 Mar 2022 11:37:02 GMT
RUN apk add --no-cache libssl1.1
# Fri, 18 Mar 2022 11:37:05 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 18 Mar 2022 11:37:26 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 18 Mar 2022 11:37:34 GMT
VOLUME [/spiped]
# Fri, 18 Mar 2022 11:37:48 GMT
WORKDIR /spiped
# Fri, 18 Mar 2022 11:37:52 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 18 Mar 2022 11:38:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 11:38:06 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:eef85fcc847498263d979ef7ec75680d05e90815eb83a9ec4db135b990c0d8b8`  
		Last Modified: Thu, 17 Mar 2022 11:15:15 GMT  
		Size: 2.8 MB (2814051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b49ab39683ef52a5765c0c691555d28af162d2ce40131084fc25680453944b9`  
		Last Modified: Fri, 18 Mar 2022 11:39:07 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0d0f21c26195ed58e548c0bcc057466eedf6289e9074e2e6ed7b00f9554c9d`  
		Last Modified: Fri, 18 Mar 2022 11:39:07 GMT  
		Size: 7.8 KB (7775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171521d6689bb8ec8d5ba220e3dd1b5f396f561fc0874d47a72700d90af2e327`  
		Last Modified: Fri, 18 Mar 2022 11:39:07 GMT  
		Size: 213.2 KB (213153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83dadace8041954e55061d0cfb5738223cde3d3a5d9d2e8383f501df563e7af0`  
		Last Modified: Fri, 18 Mar 2022 11:39:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dafb87341a132f89d6162605f157f7d2acca5cf1a07120fea5bee84acb259934`  
		Last Modified: Fri, 18 Mar 2022 11:39:07 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:9136888efc8105d1e53c8364999ed1226816696570a294b7173cfa406b46c7a1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2812933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81e94b253317064b662cf7864dd5a73b05b9b2469182896a3975c29f156fa5b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 03:04:28 GMT
ADD file:f623c69acb1859b41ef29e8f20f4e6c7072d9c6d7210d745afc615251bfe418f in / 
# Thu, 17 Mar 2022 03:04:28 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 16:50:20 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 17 Mar 2022 16:50:21 GMT
RUN apk add --no-cache libssl1.1
# Thu, 17 Mar 2022 16:50:21 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 16:50:26 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 17 Mar 2022 16:50:27 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 16:50:27 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 16:50:27 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 16:50:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 16:50:27 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d51040c5bfbf434887bfed2557335a411e6ef760d04cc178d455d1c3ec1b721c`  
		Last Modified: Thu, 17 Mar 2022 03:05:26 GMT  
		Size: 2.6 MB (2601715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a5592bce39ceb295366e2e0046df438f4b7588eaa316b2c6dce8e9e7846009`  
		Last Modified: Thu, 17 Mar 2022 16:51:05 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7d640b6d89c9475c948efa4b038dd5070d832d259ec02b3b02404a0fb56b1f`  
		Last Modified: Thu, 17 Mar 2022 16:51:05 GMT  
		Size: 7.8 KB (7786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc076029660bad5fd7c4dd63b63e13ef4a631b1bcfeb96aa738308da36262fe`  
		Last Modified: Thu, 17 Mar 2022 16:51:05 GMT  
		Size: 201.7 KB (201691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4701bc04231bf0a6e5b37d89cc796ed88c42f042536e43f8ec6561f5334b985`  
		Last Modified: Thu, 17 Mar 2022 16:51:05 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e367ce3174808cf7f69deca196856b3a6eadb9c900975bb8b47d69171568c601`  
		Last Modified: Thu, 17 Mar 2022 16:51:05 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6`

```console
$ docker pull spiped@sha256:d0d169a896962896013eb85ba8c10fcb5e5ab61c7b17b88e2e41a14dd75dedd5
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
$ docker pull spiped@sha256:b8d2ab2976a3b82a57e4ac9fc033752dfaf040d529691989e424cd5c99d8bbd3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37346333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68b6bef8dc6e1cbd84fb52a34b7b7d7df36d02946bf4bdfca5aa1b7f2d52176f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:59 GMT
ADD file:36919ae6bb25e3269eff949443129a01a8a43fb967fe6563939ebe1e1e9b8228 in / 
# Thu, 17 Mar 2022 04:03:59 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 15:52:38 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 17 Mar 2022 15:52:43 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 15:52:43 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 15:53:21 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 17 Mar 2022 15:53:21 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 15:53:22 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 15:53:22 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 15:53:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 15:53:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ae13dd57832654086618a81dbc128846aa092489260c326ee95429b63c3cf213`  
		Last Modified: Thu, 17 Mar 2022 04:10:05 GMT  
		Size: 31.4 MB (31376572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a76f2896127d7514587b03a8586b6c4bf68ca03ee67882432f282d5a3dc8e5d1`  
		Last Modified: Thu, 17 Mar 2022 15:54:13 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac159b91e9882052a2a7c77bf3ec73c84ea2c50d117cf1129e7e552374d62c2`  
		Last Modified: Thu, 17 Mar 2022 15:54:13 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd11eb085d6fc73cdb158b796cc6592d653f2f64bc48fd6bd88b02289f0dcfc`  
		Last Modified: Thu, 17 Mar 2022 15:54:15 GMT  
		Size: 6.0 MB (5966507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1610fbfaf3d68521b5f2784f03d10b65adac79bb491680dce45623e5cfd64b9`  
		Last Modified: Thu, 17 Mar 2022 15:54:13 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba1c750cce13a53c755ec9a30804efe928ee400172b3e12bbeb62b7d06178d3`  
		Last Modified: Thu, 17 Mar 2022 15:54:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; arm variant v5

```console
$ docker pull spiped@sha256:8a2e0011c5701f972d5ba018f0874593df829ac6c310b4bc74e48f548a82b624
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33950244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1fb2363cc87afddb3e829dfa3fbc4638f7d761ca756e0c04ae478180c55d43`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 05:19:45 GMT
ADD file:1eb4f937d40230354e20e28ed781234acd4be2b0dab72f87131a3eac66349719 in / 
# Thu, 17 Mar 2022 05:19:46 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 19:07:31 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 17 Mar 2022 19:07:41 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 19:07:41 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 19:08:46 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 17 Mar 2022 19:08:46 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 19:08:47 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 19:08:50 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 19:08:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 19:08:52 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4da455e7774c0e977d862a56ab6d85f33ce5dd5a77d45a0a74a272e9eae6bea0`  
		Last Modified: Thu, 17 Mar 2022 05:35:01 GMT  
		Size: 28.9 MB (28919702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ccaa8f7993c69ae0db39ad4c2027a13ce97175da89f5be82de6a2ca2a97c7d1`  
		Last Modified: Thu, 17 Mar 2022 19:09:25 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9512592020427919bc6c45a56ea8a3e87091e9b9b72c5f4081ddbdfda9fbe931`  
		Last Modified: Thu, 17 Mar 2022 19:09:26 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2010aa0813bd04163cffb9ff94e259b6216dc2c427790ff8bbb2f3b7ccb45846`  
		Last Modified: Thu, 17 Mar 2022 19:09:28 GMT  
		Size: 5.0 MB (5027289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3447d294931d6120cea1ca769318e6e3730d1d3a01afc8a3f8046adb9872d7`  
		Last Modified: Thu, 17 Mar 2022 19:09:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ba318f72a277eedbbb07d36dd5fe2c4195238cb2bd1aa540f8a89a169f22a2`  
		Last Modified: Thu, 17 Mar 2022 19:09:25 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; arm variant v7

```console
$ docker pull spiped@sha256:ac215edcc30b28977b317d77ccaaae94761d4354587e9800d101bb637e1149d0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31315718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4d7a6cecd75cfc07f7f336a43f8c0c2bd623ff9d78a61a9c7442249f5b36df1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 01 Mar 2022 02:02:56 GMT
ADD file:c6b519323fd1fa09b9f8c8608778872e8fa6208cb0b42aaccdef4479a469f5f4 in / 
# Tue, 01 Mar 2022 02:02:57 GMT
CMD ["bash"]
# Wed, 02 Mar 2022 16:17:58 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 02 Mar 2022 16:18:05 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 16:18:05 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 02 Mar 2022 16:18:49 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 02 Mar 2022 16:18:50 GMT
VOLUME [/spiped]
# Wed, 02 Mar 2022 16:18:50 GMT
WORKDIR /spiped
# Wed, 02 Mar 2022 16:18:51 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 02 Mar 2022 16:18:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 16:18:52 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:59dbb2ac3829352dd707e28e037734c9fbdef5b03aea31e3929ddcead949afee`  
		Last Modified: Tue, 01 Mar 2022 02:19:09 GMT  
		Size: 26.6 MB (26565105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d308a84eca5cd40a5b3b38f20aba12ad984055514266c5f21895dbd7ae398c4`  
		Last Modified: Wed, 02 Mar 2022 16:19:54 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885c743661aaee24e106ee3f2083d0acdcff80bbbfb0663485d199324303dbe2`  
		Last Modified: Wed, 02 Mar 2022 16:19:54 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1b566deb17f5e2852900d444a17df344a45e23a180e0dfc06251a994ef5333c`  
		Last Modified: Wed, 02 Mar 2022 16:19:59 GMT  
		Size: 4.7 MB (4747364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f044884cf1737497ba826896f6b7e83d791a1b320f0dc816a7862caffe3d2848`  
		Last Modified: Wed, 02 Mar 2022 16:19:54 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e071d50afe6ad4ee58ac45ec6df078835658702fde56f4230838ffb45ed917e5`  
		Last Modified: Wed, 02 Mar 2022 16:19:54 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:fd6ccb6336851679362386de45250510a5e80ef3c4e7df2ae724eaa4c9667ed0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35335910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7240db44c2f7942501fdbf02463d450aff3590fc9bc59ad1940947b652f01fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 03:21:57 GMT
ADD file:e52e032f1ace6abd44b3647d43c1b8ae30bac6de804eef09c6ccd793057996fd in / 
# Thu, 17 Mar 2022 03:21:58 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 21:04:34 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 17 Mar 2022 21:04:37 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 21:04:37 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 21:04:55 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 17 Mar 2022 21:04:56 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 21:04:57 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 21:04:59 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 21:04:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 21:05:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:32252aec0777ac025a158bc2a8317650a4f2a0a875387011b1165013874f8723`  
		Last Modified: Thu, 17 Mar 2022 03:28:36 GMT  
		Size: 30.1 MB (30063013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f39180b559e5aed1b40421eec8f7b61457cc16f2cfee7f2da5aa250b61d4370`  
		Last Modified: Thu, 17 Mar 2022 21:05:48 GMT  
		Size: 1.6 KB (1617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcd781ba64e538c462ceeb478df86f9e82f9043472f590c90b8b77e1c69b494`  
		Last Modified: Thu, 17 Mar 2022 21:05:49 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6acdb1b2ac977841bfba332aa093360fd27c5ae5aeeeb8ed34c5da6d36cbc01`  
		Last Modified: Thu, 17 Mar 2022 21:05:50 GMT  
		Size: 5.3 MB (5269921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f5b809a8f2f8d99685a97d9b9b90ed684e872055f59a0bef726c106ed92eae`  
		Last Modified: Thu, 17 Mar 2022 21:05:49 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815c0e22b949966496c66a9c25b6ae9090833f44298de5096f6f6673d2b5eeed`  
		Last Modified: Thu, 17 Mar 2022 21:05:49 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; 386

```console
$ docker pull spiped@sha256:ed2f5c92201304d5bbfd3a42f000b351c22b4d58f49e952733cb43f825a3e301
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40281229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e319a53a099b51990813e4b7cfcd49725cfe0eda506064c73bbb2bc420375e97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 08:15:53 GMT
ADD file:2d6be3846f0e5fabd85bc9409b1e2223cad4c57c76f96e9f81489ba78a72a1f5 in / 
# Thu, 17 Mar 2022 08:15:54 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 21:38:49 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 17 Mar 2022 21:38:53 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 21:38:53 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 21:39:26 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 17 Mar 2022 21:39:26 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 21:39:27 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 21:39:27 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 21:39:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 21:39:27 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:176085117cac9b2cf2cf57b3a10c9811dbd2773497fbac3086b5024070447e97`  
		Last Modified: Thu, 17 Mar 2022 08:24:00 GMT  
		Size: 32.4 MB (32386475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f0023ca52fa68e0b790d53b1989cc86a09c03c3f5ba512bd7254e660798701`  
		Last Modified: Thu, 17 Mar 2022 21:40:39 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f169664f6c06e48b52c02faa7212ffdbed368d76e4046ee62757dcdad99ec1`  
		Last Modified: Thu, 17 Mar 2022 21:40:39 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e208248e53ac127f9ba59ef6496e619a4aa53b7da6cada4f8c9eefab9d6eb759`  
		Last Modified: Thu, 17 Mar 2022 21:40:42 GMT  
		Size: 7.9 MB (7891501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e182dd8aad03bcc4a4fc70c4d5477e38448020a78e7598e41bc1d584729d764b`  
		Last Modified: Thu, 17 Mar 2022 21:40:39 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4315719c3c75933b98aafbac692d4aa273eec4588f2647f7ad5ae7032b336ba2`  
		Last Modified: Thu, 17 Mar 2022 21:40:39 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; mips64le

```console
$ docker pull spiped@sha256:ad61e440c067a6b168769664de1c184685e3582a1422d3c2d1681ba457ff7215
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35347773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556e5433be4b6d7d5c9e1b8aea73caac9038b7fa0ced3fcc6d085d06eae244cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 08:53:04 GMT
ADD file:795ac4eba576bc4c995df2a18b10ce802ee8a05417cdc53f5aa09452ecf2e832 in / 
# Thu, 17 Mar 2022 08:53:08 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 21:25:08 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 18 Mar 2022 21:25:24 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 21:25:27 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 18 Mar 2022 21:27:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 18 Mar 2022 21:27:04 GMT
VOLUME [/spiped]
# Fri, 18 Mar 2022 21:27:07 GMT
WORKDIR /spiped
# Fri, 18 Mar 2022 21:27:09 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 18 Mar 2022 21:27:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 21:27:15 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4799d88734ae94287a665c0e14621a744706cfbe17a0cf27ae9b0cc630927b11`  
		Last Modified: Thu, 17 Mar 2022 10:43:20 GMT  
		Size: 29.6 MB (29639810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c3bb983a06c1d0519d23a6efec25298a548ce43495f86ad94ed19dc18240d6`  
		Last Modified: Fri, 18 Mar 2022 21:27:38 GMT  
		Size: 1.6 KB (1614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0dd02a98e85a0552aa2aef9bcf7cc1127e26a8aebbd1b4174d51b68e253093`  
		Last Modified: Fri, 18 Mar 2022 21:27:38 GMT  
		Size: 926.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73a235ac7d157ff9e32cdc51b831aae0fde62bfb42dcc02a77a0e52df565b34`  
		Last Modified: Fri, 18 Mar 2022 21:27:44 GMT  
		Size: 5.7 MB (5704986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c944593c2417013162356e68bb977d4fdaff97eba73de773bb2f61032d200cca`  
		Last Modified: Fri, 18 Mar 2022 21:27:39 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b86ea964515b4d10fea8515b90d3d4557e4f7db1a99f2e9d9cadd52c34ea59`  
		Last Modified: Fri, 18 Mar 2022 21:27:38 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; ppc64le

```console
$ docker pull spiped@sha256:9797106231608e33cf1bf6b4aa3121e668221249a4393633d99fd2d54dd41dc1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41281331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:387b2511d5857028002168cda350ddc9cba69bb5e9c7efe68e8aba8e77b6237e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 11:17:54 GMT
ADD file:e8555f1cb439a45786b92e929cfa154b51f668c5b4cd69e4ce98340c5998fe0c in / 
# Thu, 17 Mar 2022 11:18:00 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 11:32:51 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 18 Mar 2022 11:33:08 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 11:33:11 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 18 Mar 2022 11:35:53 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 18 Mar 2022 11:36:02 GMT
VOLUME [/spiped]
# Fri, 18 Mar 2022 11:36:08 GMT
WORKDIR /spiped
# Fri, 18 Mar 2022 11:36:16 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 18 Mar 2022 11:36:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 11:36:29 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:aec78dc45d7b3df12df0672d13e22005592b453f03ff2580efac2598dddd680b`  
		Last Modified: Thu, 17 Mar 2022 11:28:17 GMT  
		Size: 35.3 MB (35279758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833a842281729982038158055afe9827cf83082a73928d160267a96c3a210909`  
		Last Modified: Fri, 18 Mar 2022 11:38:42 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb19a8bea8ac6452690b2abb425c234fa132fc999d44dc8678c047c83a2b8768`  
		Last Modified: Fri, 18 Mar 2022 11:38:42 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298a5cd67fcc1d54d133544fddcaee22c2d52b321bea99ddebfdc5e92cf5b9c5`  
		Last Modified: Fri, 18 Mar 2022 11:38:43 GMT  
		Size: 6.0 MB (5998310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:304b3fc5bf6eef287d420bb4471463e5dd7f258b64abc28ac0fa3cc28c389078`  
		Last Modified: Fri, 18 Mar 2022 11:38:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ae40f3931d22932d6ae2313ffce38370977d00b771c456e04802d1dd5b8724`  
		Last Modified: Fri, 18 Mar 2022 11:38:42 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; s390x

```console
$ docker pull spiped@sha256:04aafcacad77a9b72d2d47a38a232c9e3645a438c0131b47a4018b46f979be32
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34844908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ff67ace7af078b229b5928d2f0d8eba4dfc9336bd01cc8af778512ed9b34cbd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 03:06:58 GMT
ADD file:52f9267b4c57ac585a0d3d47a6f2ae1a71398264173ad4f190332957fa629c67 in / 
# Thu, 17 Mar 2022 03:07:01 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 16:49:57 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 17 Mar 2022 16:50:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 16:50:00 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 16:50:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 17 Mar 2022 16:50:12 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 16:50:12 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 16:50:12 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 16:50:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 16:50:12 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d101968410e5005df630b0572aec03c88de55b8de81f3cf7e6a57e1ce2e5a8e5`  
		Last Modified: Thu, 17 Mar 2022 03:12:46 GMT  
		Size: 29.7 MB (29655795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6ffc821fd848073df862253a81ff1adea16b2b909005db2cbce4ee66eb2a85`  
		Last Modified: Thu, 17 Mar 2022 16:50:52 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b47ffd2d769d0417b9b329e411c5d0abcf3eeb26d24af586ae0aaaf90e42b6a7`  
		Last Modified: Thu, 17 Mar 2022 16:50:52 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e66ff429e104d86eab7bf4adb5dc2db5a803f49496c73e98e298fe5b252e89`  
		Last Modified: Thu, 17 Mar 2022 16:50:53 GMT  
		Size: 5.2 MB (5185854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7601978f39168626ccd46b4478d2d3ca54a1a90e2436bddd43a901fe451ddb54`  
		Last Modified: Thu, 17 Mar 2022 16:50:53 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a37fe55f363c9febb17d5ff4cde072423c7d7197dbe1fdcda48d4483abe56b9`  
		Last Modified: Thu, 17 Mar 2022 16:50:52 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6-alpine`

```console
$ docker pull spiped@sha256:651bee70b611b34012354942ee14d8cd1c394a654381018891a216b65438b06d
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
$ docker pull spiped@sha256:fa4240521d3ff244261dfbcea3a9e63b5f2858626355d782bd7b97a37a706e0e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3037036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46fd9df2bffa7e91039d2ee71224e10bea88319d02d25fc53832aef21376ecd6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 04:01:58 GMT
ADD file:cf4b631a115c2bbfbd81cad2d3041bceb64a8136aac92ba8a63b6c51d60af764 in / 
# Thu, 17 Mar 2022 04:01:59 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 15:53:28 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 17 Mar 2022 15:53:30 GMT
RUN apk add --no-cache libssl1.1
# Thu, 17 Mar 2022 15:53:30 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 15:53:51 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 17 Mar 2022 15:53:52 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 15:53:52 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 15:53:52 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 15:53:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 15:53:53 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3d243047344378e9b7136d552d48feb7ea8b6fe14ce0990e0cc011d5e369626a`  
		Last Modified: Thu, 17 Mar 2022 04:02:41 GMT  
		Size: 2.8 MB (2812636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28609b3adb4c05998e1162db6c538ca407f2280011d95fcd8a244d805a5b735`  
		Last Modified: Thu, 17 Mar 2022 15:54:31 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b4dfa35cdb53635d719c0c532ec9937293bcefd0cfc46f8bd1feecfdf05a95`  
		Last Modified: Thu, 17 Mar 2022 15:54:31 GMT  
		Size: 7.8 KB (7789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1305ebaa04a3fbf473d9073ba19d8e7c200053717456c94b4aa81ad2379537a`  
		Last Modified: Thu, 17 Mar 2022 15:54:34 GMT  
		Size: 214.9 KB (214875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a9314de395635f68354281ea4e4c80ccd1a83382ea0c0797d439c77466a954`  
		Last Modified: Thu, 17 Mar 2022 15:54:31 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8620fb27c9cb715ea3d3d0940cbfe238f1c60983b2586367d7f672d1d83ff6e`  
		Last Modified: Thu, 17 Mar 2022 15:54:31 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:59826251d3a0ad2527c0bafdc1ea568962d7f5f3528b1e98d3aaa3926d652ac4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2833671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25087c53823bfdb0b76bf4d89b11576da2bbb0a43269741c3f40a8aa03ddd93a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 02:26:45 GMT
ADD file:9c8618405ef54d562132919ffe49c862d014b402e0e4813b87bf01574fa04c0e in / 
# Thu, 17 Mar 2022 02:26:45 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 10:53:28 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 17 Mar 2022 10:53:30 GMT
RUN apk add --no-cache libssl1.1
# Thu, 17 Mar 2022 10:53:31 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 10:53:50 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 17 Mar 2022 10:53:50 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 10:53:51 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 10:53:52 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 10:53:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 10:53:52 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:787f016efa9bc7812361be134f731e845b97fba19169cf3615e7048c0412380e`  
		Last Modified: Thu, 17 Mar 2022 02:28:24 GMT  
		Size: 2.6 MB (2624973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8491e25887dfb5f3955a484700defebb2ff52083efbde9795a85971df7a476f1`  
		Last Modified: Thu, 17 Mar 2022 10:54:24 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35d33f304fab5de548bc59cc09d332370e572391cf8e6547a78ecad3df48c27`  
		Last Modified: Thu, 17 Mar 2022 10:54:24 GMT  
		Size: 7.8 KB (7780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a10fd4be356562398de356a11d85dbf1d36467d9069e828647d3827e6c97cda2`  
		Last Modified: Thu, 17 Mar 2022 10:54:24 GMT  
		Size: 199.2 KB (199175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08779a270c83a7fa3e6660371def3ae5d7436e7afc2058d26fc7277c6465b79e`  
		Last Modified: Thu, 17 Mar 2022 10:54:24 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98221b50c485d80403bee1e97ffcda727cc378c9408fe0b9d2d32656e2e8ba42`  
		Last Modified: Thu, 17 Mar 2022 10:54:24 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:277d22d33ab8cd23ff5bf04d4e60841c8a335de8fdb772173601e9a4d4cb00bf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3802328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f94c64b2c706a58b82aa60bafca69c1fd15fb76714e5ca4aae0f1e4a47e3f1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Mon, 27 Dec 2021 18:00:04 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Mon, 27 Dec 2021 18:00:06 GMT
RUN apk add --no-cache libssl1.1
# Mon, 27 Dec 2021 18:00:06 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Mon, 27 Dec 2021 18:00:25 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Mon, 27 Dec 2021 18:00:26 GMT
VOLUME [/spiped]
# Mon, 27 Dec 2021 18:00:26 GMT
WORKDIR /spiped
# Mon, 27 Dec 2021 18:00:27 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Mon, 27 Dec 2021 18:00:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Dec 2021 18:00:28 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca194041621ab40d8e7f24b7f7e82aa07760b2dafcd26472bd7fae96171989a`  
		Last Modified: Mon, 27 Dec 2021 18:01:41 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e934f04cb0ca6a107389bcb614eb02143fb079eef09a47a9248e3c4ff07864`  
		Last Modified: Mon, 27 Dec 2021 18:01:41 GMT  
		Size: 7.7 KB (7749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4111e5d44f2316d799c8b9144d8f35765b0bf330b8d596d99e504969cd48e07a`  
		Last Modified: Mon, 27 Dec 2021 18:01:42 GMT  
		Size: 1.4 MB (1358077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46d751b026ad913b2a48630c96460959a733e75728d55aafbd389197bf81857`  
		Last Modified: Mon, 27 Dec 2021 18:01:41 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5140561b01c4c6ae8b47c729fd289d7eef4a2b0e9c427a6bd35a86747e966206`  
		Last Modified: Mon, 27 Dec 2021 18:01:41 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:d99e51a55cc06f9f9bb1a381fbcccc5b8a617221ede6d99e80fa0f1455d9a7c7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2931463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70fa2e490f06ca016a59e8ccb25bdf2aca9f52652ffd37b739b119385121ed0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 03:19:52 GMT
ADD file:cd7d91362950471ca4678cf3833dc47119ab519dea51424c847bbbb21e1649d4 in / 
# Thu, 17 Mar 2022 03:19:52 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 21:05:07 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 17 Mar 2022 21:05:08 GMT
RUN apk add --no-cache libssl1.1
# Thu, 17 Mar 2022 21:05:09 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 21:05:19 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 17 Mar 2022 21:05:20 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 21:05:21 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 21:05:23 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 21:05:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 21:05:24 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:148d739a8e6b9342daa1f5b428d3a3c6118f340f21df28c16e06f918ef150147`  
		Last Modified: Thu, 17 Mar 2022 03:20:45 GMT  
		Size: 2.7 MB (2714807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfe03b788288bfc55a2e69551194eb50a0e5968d87eb615e001116670eca8d1`  
		Last Modified: Thu, 17 Mar 2022 21:06:08 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ebbe0c7d8e482b1cc3a2c35380a3da9aba32e7419814e8463d19e20ab058a5`  
		Last Modified: Thu, 17 Mar 2022 21:06:08 GMT  
		Size: 7.8 KB (7750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd44380493879dfe08522b418a1697db90bf574f812b27abf9f5363d6130acfa`  
		Last Modified: Thu, 17 Mar 2022 21:06:08 GMT  
		Size: 207.2 KB (207231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:684fec7d45ce25526ac84e65dbb141f72835e9b00faa35ffd4bd2d1b5f98b3c6`  
		Last Modified: Thu, 17 Mar 2022 21:06:08 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:526257cb94ed56c056f2917a4a8e8c81f2c1b9b6911487da82418348ffa037f0`  
		Last Modified: Thu, 17 Mar 2022 21:06:09 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; 386

```console
$ docker pull spiped@sha256:29c7cebe60cecc9f7cbb75c243694894ccead716974c52d9e7f9a99a1e7931c3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3056990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65970f53cd34df6344b60d5b1f188ae0408dfd33dd9036a90562f4b4d4d4ef83`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 08:13:03 GMT
ADD file:22216bc654d9177244235f242fa83cae3b283b3c145cad7ccf11c0d29f5f0ff2 in / 
# Thu, 17 Mar 2022 08:13:03 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 21:39:40 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 17 Mar 2022 21:39:42 GMT
RUN apk add --no-cache libssl1.1
# Thu, 17 Mar 2022 21:39:42 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 21:40:00 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 17 Mar 2022 21:40:00 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 21:40:00 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 21:40:00 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 21:40:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 21:40:01 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:93317a1f65ec94b67aefe728a598022610246404e3a68d391c76cd0e5244a2a0`  
		Last Modified: Thu, 17 Mar 2022 08:13:56 GMT  
		Size: 2.8 MB (2821789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8535b315fbad030f6fe4b11974d789b28ec85b2e79677eb197239c4e2d58ad07`  
		Last Modified: Thu, 17 Mar 2022 21:41:04 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47d449347fe74957e2caaf9718edfca3c882962cffbce71dd4e6207078459b6`  
		Last Modified: Thu, 17 Mar 2022 21:41:04 GMT  
		Size: 7.8 KB (7782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c09f03ca1752043d6dfd052d7aae794162b6013a723e0efc9477f848ca481c5`  
		Last Modified: Thu, 17 Mar 2022 21:41:04 GMT  
		Size: 225.7 KB (225683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd9e35cc22870710eefd82f88e16ed34c080e8c4f505037f17080f14e818cd1a`  
		Last Modified: Thu, 17 Mar 2022 21:41:04 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1021ec3b3986cf8edf968a928a55219fb145dbe088f59a3ffb7144791d7831d`  
		Last Modified: Thu, 17 Mar 2022 21:41:04 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:8c23f5e4d58ef3fce86009c4f9d2b536e5dd7645357d02dc8f3143a45d24b62a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3036720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:525943d93e23029964172e9971ee55221214131aa72607d782b906782cebd905`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 11:14:04 GMT
ADD file:ddc94e1e084c05807db26adcc95b47a137fa47fb391e75998b338ada65e00c1c in / 
# Thu, 17 Mar 2022 11:14:09 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 11:36:53 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 18 Mar 2022 11:37:02 GMT
RUN apk add --no-cache libssl1.1
# Fri, 18 Mar 2022 11:37:05 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 18 Mar 2022 11:37:26 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 18 Mar 2022 11:37:34 GMT
VOLUME [/spiped]
# Fri, 18 Mar 2022 11:37:48 GMT
WORKDIR /spiped
# Fri, 18 Mar 2022 11:37:52 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 18 Mar 2022 11:38:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 11:38:06 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:eef85fcc847498263d979ef7ec75680d05e90815eb83a9ec4db135b990c0d8b8`  
		Last Modified: Thu, 17 Mar 2022 11:15:15 GMT  
		Size: 2.8 MB (2814051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b49ab39683ef52a5765c0c691555d28af162d2ce40131084fc25680453944b9`  
		Last Modified: Fri, 18 Mar 2022 11:39:07 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0d0f21c26195ed58e548c0bcc057466eedf6289e9074e2e6ed7b00f9554c9d`  
		Last Modified: Fri, 18 Mar 2022 11:39:07 GMT  
		Size: 7.8 KB (7775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171521d6689bb8ec8d5ba220e3dd1b5f396f561fc0874d47a72700d90af2e327`  
		Last Modified: Fri, 18 Mar 2022 11:39:07 GMT  
		Size: 213.2 KB (213153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83dadace8041954e55061d0cfb5738223cde3d3a5d9d2e8383f501df563e7af0`  
		Last Modified: Fri, 18 Mar 2022 11:39:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dafb87341a132f89d6162605f157f7d2acca5cf1a07120fea5bee84acb259934`  
		Last Modified: Fri, 18 Mar 2022 11:39:07 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:9136888efc8105d1e53c8364999ed1226816696570a294b7173cfa406b46c7a1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2812933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81e94b253317064b662cf7864dd5a73b05b9b2469182896a3975c29f156fa5b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 03:04:28 GMT
ADD file:f623c69acb1859b41ef29e8f20f4e6c7072d9c6d7210d745afc615251bfe418f in / 
# Thu, 17 Mar 2022 03:04:28 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 16:50:20 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 17 Mar 2022 16:50:21 GMT
RUN apk add --no-cache libssl1.1
# Thu, 17 Mar 2022 16:50:21 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 16:50:26 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 17 Mar 2022 16:50:27 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 16:50:27 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 16:50:27 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 16:50:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 16:50:27 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d51040c5bfbf434887bfed2557335a411e6ef760d04cc178d455d1c3ec1b721c`  
		Last Modified: Thu, 17 Mar 2022 03:05:26 GMT  
		Size: 2.6 MB (2601715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a5592bce39ceb295366e2e0046df438f4b7588eaa316b2c6dce8e9e7846009`  
		Last Modified: Thu, 17 Mar 2022 16:51:05 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7d640b6d89c9475c948efa4b038dd5070d832d259ec02b3b02404a0fb56b1f`  
		Last Modified: Thu, 17 Mar 2022 16:51:05 GMT  
		Size: 7.8 KB (7786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc076029660bad5fd7c4dd63b63e13ef4a631b1bcfeb96aa738308da36262fe`  
		Last Modified: Thu, 17 Mar 2022 16:51:05 GMT  
		Size: 201.7 KB (201691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4701bc04231bf0a6e5b37d89cc796ed88c42f042536e43f8ec6561f5334b985`  
		Last Modified: Thu, 17 Mar 2022 16:51:05 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e367ce3174808cf7f69deca196856b3a6eadb9c900975bb8b47d69171568c601`  
		Last Modified: Thu, 17 Mar 2022 16:51:05 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6.2`

```console
$ docker pull spiped@sha256:d0d169a896962896013eb85ba8c10fcb5e5ab61c7b17b88e2e41a14dd75dedd5
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
$ docker pull spiped@sha256:b8d2ab2976a3b82a57e4ac9fc033752dfaf040d529691989e424cd5c99d8bbd3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37346333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68b6bef8dc6e1cbd84fb52a34b7b7d7df36d02946bf4bdfca5aa1b7f2d52176f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:59 GMT
ADD file:36919ae6bb25e3269eff949443129a01a8a43fb967fe6563939ebe1e1e9b8228 in / 
# Thu, 17 Mar 2022 04:03:59 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 15:52:38 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 17 Mar 2022 15:52:43 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 15:52:43 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 15:53:21 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 17 Mar 2022 15:53:21 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 15:53:22 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 15:53:22 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 15:53:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 15:53:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ae13dd57832654086618a81dbc128846aa092489260c326ee95429b63c3cf213`  
		Last Modified: Thu, 17 Mar 2022 04:10:05 GMT  
		Size: 31.4 MB (31376572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a76f2896127d7514587b03a8586b6c4bf68ca03ee67882432f282d5a3dc8e5d1`  
		Last Modified: Thu, 17 Mar 2022 15:54:13 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac159b91e9882052a2a7c77bf3ec73c84ea2c50d117cf1129e7e552374d62c2`  
		Last Modified: Thu, 17 Mar 2022 15:54:13 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd11eb085d6fc73cdb158b796cc6592d653f2f64bc48fd6bd88b02289f0dcfc`  
		Last Modified: Thu, 17 Mar 2022 15:54:15 GMT  
		Size: 6.0 MB (5966507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1610fbfaf3d68521b5f2784f03d10b65adac79bb491680dce45623e5cfd64b9`  
		Last Modified: Thu, 17 Mar 2022 15:54:13 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba1c750cce13a53c755ec9a30804efe928ee400172b3e12bbeb62b7d06178d3`  
		Last Modified: Thu, 17 Mar 2022 15:54:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; arm variant v5

```console
$ docker pull spiped@sha256:8a2e0011c5701f972d5ba018f0874593df829ac6c310b4bc74e48f548a82b624
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33950244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1fb2363cc87afddb3e829dfa3fbc4638f7d761ca756e0c04ae478180c55d43`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 05:19:45 GMT
ADD file:1eb4f937d40230354e20e28ed781234acd4be2b0dab72f87131a3eac66349719 in / 
# Thu, 17 Mar 2022 05:19:46 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 19:07:31 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 17 Mar 2022 19:07:41 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 19:07:41 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 19:08:46 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 17 Mar 2022 19:08:46 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 19:08:47 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 19:08:50 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 19:08:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 19:08:52 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4da455e7774c0e977d862a56ab6d85f33ce5dd5a77d45a0a74a272e9eae6bea0`  
		Last Modified: Thu, 17 Mar 2022 05:35:01 GMT  
		Size: 28.9 MB (28919702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ccaa8f7993c69ae0db39ad4c2027a13ce97175da89f5be82de6a2ca2a97c7d1`  
		Last Modified: Thu, 17 Mar 2022 19:09:25 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9512592020427919bc6c45a56ea8a3e87091e9b9b72c5f4081ddbdfda9fbe931`  
		Last Modified: Thu, 17 Mar 2022 19:09:26 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2010aa0813bd04163cffb9ff94e259b6216dc2c427790ff8bbb2f3b7ccb45846`  
		Last Modified: Thu, 17 Mar 2022 19:09:28 GMT  
		Size: 5.0 MB (5027289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3447d294931d6120cea1ca769318e6e3730d1d3a01afc8a3f8046adb9872d7`  
		Last Modified: Thu, 17 Mar 2022 19:09:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ba318f72a277eedbbb07d36dd5fe2c4195238cb2bd1aa540f8a89a169f22a2`  
		Last Modified: Thu, 17 Mar 2022 19:09:25 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; arm variant v7

```console
$ docker pull spiped@sha256:ac215edcc30b28977b317d77ccaaae94761d4354587e9800d101bb637e1149d0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31315718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4d7a6cecd75cfc07f7f336a43f8c0c2bd623ff9d78a61a9c7442249f5b36df1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 01 Mar 2022 02:02:56 GMT
ADD file:c6b519323fd1fa09b9f8c8608778872e8fa6208cb0b42aaccdef4479a469f5f4 in / 
# Tue, 01 Mar 2022 02:02:57 GMT
CMD ["bash"]
# Wed, 02 Mar 2022 16:17:58 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 02 Mar 2022 16:18:05 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 16:18:05 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 02 Mar 2022 16:18:49 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 02 Mar 2022 16:18:50 GMT
VOLUME [/spiped]
# Wed, 02 Mar 2022 16:18:50 GMT
WORKDIR /spiped
# Wed, 02 Mar 2022 16:18:51 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 02 Mar 2022 16:18:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 16:18:52 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:59dbb2ac3829352dd707e28e037734c9fbdef5b03aea31e3929ddcead949afee`  
		Last Modified: Tue, 01 Mar 2022 02:19:09 GMT  
		Size: 26.6 MB (26565105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d308a84eca5cd40a5b3b38f20aba12ad984055514266c5f21895dbd7ae398c4`  
		Last Modified: Wed, 02 Mar 2022 16:19:54 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885c743661aaee24e106ee3f2083d0acdcff80bbbfb0663485d199324303dbe2`  
		Last Modified: Wed, 02 Mar 2022 16:19:54 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1b566deb17f5e2852900d444a17df344a45e23a180e0dfc06251a994ef5333c`  
		Last Modified: Wed, 02 Mar 2022 16:19:59 GMT  
		Size: 4.7 MB (4747364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f044884cf1737497ba826896f6b7e83d791a1b320f0dc816a7862caffe3d2848`  
		Last Modified: Wed, 02 Mar 2022 16:19:54 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e071d50afe6ad4ee58ac45ec6df078835658702fde56f4230838ffb45ed917e5`  
		Last Modified: Wed, 02 Mar 2022 16:19:54 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:fd6ccb6336851679362386de45250510a5e80ef3c4e7df2ae724eaa4c9667ed0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35335910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7240db44c2f7942501fdbf02463d450aff3590fc9bc59ad1940947b652f01fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 03:21:57 GMT
ADD file:e52e032f1ace6abd44b3647d43c1b8ae30bac6de804eef09c6ccd793057996fd in / 
# Thu, 17 Mar 2022 03:21:58 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 21:04:34 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 17 Mar 2022 21:04:37 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 21:04:37 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 21:04:55 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 17 Mar 2022 21:04:56 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 21:04:57 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 21:04:59 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 21:04:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 21:05:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:32252aec0777ac025a158bc2a8317650a4f2a0a875387011b1165013874f8723`  
		Last Modified: Thu, 17 Mar 2022 03:28:36 GMT  
		Size: 30.1 MB (30063013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f39180b559e5aed1b40421eec8f7b61457cc16f2cfee7f2da5aa250b61d4370`  
		Last Modified: Thu, 17 Mar 2022 21:05:48 GMT  
		Size: 1.6 KB (1617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcd781ba64e538c462ceeb478df86f9e82f9043472f590c90b8b77e1c69b494`  
		Last Modified: Thu, 17 Mar 2022 21:05:49 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6acdb1b2ac977841bfba332aa093360fd27c5ae5aeeeb8ed34c5da6d36cbc01`  
		Last Modified: Thu, 17 Mar 2022 21:05:50 GMT  
		Size: 5.3 MB (5269921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f5b809a8f2f8d99685a97d9b9b90ed684e872055f59a0bef726c106ed92eae`  
		Last Modified: Thu, 17 Mar 2022 21:05:49 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815c0e22b949966496c66a9c25b6ae9090833f44298de5096f6f6673d2b5eeed`  
		Last Modified: Thu, 17 Mar 2022 21:05:49 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; 386

```console
$ docker pull spiped@sha256:ed2f5c92201304d5bbfd3a42f000b351c22b4d58f49e952733cb43f825a3e301
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40281229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e319a53a099b51990813e4b7cfcd49725cfe0eda506064c73bbb2bc420375e97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 08:15:53 GMT
ADD file:2d6be3846f0e5fabd85bc9409b1e2223cad4c57c76f96e9f81489ba78a72a1f5 in / 
# Thu, 17 Mar 2022 08:15:54 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 21:38:49 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 17 Mar 2022 21:38:53 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 21:38:53 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 21:39:26 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 17 Mar 2022 21:39:26 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 21:39:27 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 21:39:27 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 21:39:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 21:39:27 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:176085117cac9b2cf2cf57b3a10c9811dbd2773497fbac3086b5024070447e97`  
		Last Modified: Thu, 17 Mar 2022 08:24:00 GMT  
		Size: 32.4 MB (32386475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f0023ca52fa68e0b790d53b1989cc86a09c03c3f5ba512bd7254e660798701`  
		Last Modified: Thu, 17 Mar 2022 21:40:39 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f169664f6c06e48b52c02faa7212ffdbed368d76e4046ee62757dcdad99ec1`  
		Last Modified: Thu, 17 Mar 2022 21:40:39 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e208248e53ac127f9ba59ef6496e619a4aa53b7da6cada4f8c9eefab9d6eb759`  
		Last Modified: Thu, 17 Mar 2022 21:40:42 GMT  
		Size: 7.9 MB (7891501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e182dd8aad03bcc4a4fc70c4d5477e38448020a78e7598e41bc1d584729d764b`  
		Last Modified: Thu, 17 Mar 2022 21:40:39 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4315719c3c75933b98aafbac692d4aa273eec4588f2647f7ad5ae7032b336ba2`  
		Last Modified: Thu, 17 Mar 2022 21:40:39 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; mips64le

```console
$ docker pull spiped@sha256:ad61e440c067a6b168769664de1c184685e3582a1422d3c2d1681ba457ff7215
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35347773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556e5433be4b6d7d5c9e1b8aea73caac9038b7fa0ced3fcc6d085d06eae244cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 08:53:04 GMT
ADD file:795ac4eba576bc4c995df2a18b10ce802ee8a05417cdc53f5aa09452ecf2e832 in / 
# Thu, 17 Mar 2022 08:53:08 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 21:25:08 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 18 Mar 2022 21:25:24 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 21:25:27 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 18 Mar 2022 21:27:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 18 Mar 2022 21:27:04 GMT
VOLUME [/spiped]
# Fri, 18 Mar 2022 21:27:07 GMT
WORKDIR /spiped
# Fri, 18 Mar 2022 21:27:09 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 18 Mar 2022 21:27:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 21:27:15 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4799d88734ae94287a665c0e14621a744706cfbe17a0cf27ae9b0cc630927b11`  
		Last Modified: Thu, 17 Mar 2022 10:43:20 GMT  
		Size: 29.6 MB (29639810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c3bb983a06c1d0519d23a6efec25298a548ce43495f86ad94ed19dc18240d6`  
		Last Modified: Fri, 18 Mar 2022 21:27:38 GMT  
		Size: 1.6 KB (1614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0dd02a98e85a0552aa2aef9bcf7cc1127e26a8aebbd1b4174d51b68e253093`  
		Last Modified: Fri, 18 Mar 2022 21:27:38 GMT  
		Size: 926.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73a235ac7d157ff9e32cdc51b831aae0fde62bfb42dcc02a77a0e52df565b34`  
		Last Modified: Fri, 18 Mar 2022 21:27:44 GMT  
		Size: 5.7 MB (5704986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c944593c2417013162356e68bb977d4fdaff97eba73de773bb2f61032d200cca`  
		Last Modified: Fri, 18 Mar 2022 21:27:39 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b86ea964515b4d10fea8515b90d3d4557e4f7db1a99f2e9d9cadd52c34ea59`  
		Last Modified: Fri, 18 Mar 2022 21:27:38 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; ppc64le

```console
$ docker pull spiped@sha256:9797106231608e33cf1bf6b4aa3121e668221249a4393633d99fd2d54dd41dc1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41281331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:387b2511d5857028002168cda350ddc9cba69bb5e9c7efe68e8aba8e77b6237e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 11:17:54 GMT
ADD file:e8555f1cb439a45786b92e929cfa154b51f668c5b4cd69e4ce98340c5998fe0c in / 
# Thu, 17 Mar 2022 11:18:00 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 11:32:51 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 18 Mar 2022 11:33:08 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 11:33:11 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 18 Mar 2022 11:35:53 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 18 Mar 2022 11:36:02 GMT
VOLUME [/spiped]
# Fri, 18 Mar 2022 11:36:08 GMT
WORKDIR /spiped
# Fri, 18 Mar 2022 11:36:16 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 18 Mar 2022 11:36:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 11:36:29 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:aec78dc45d7b3df12df0672d13e22005592b453f03ff2580efac2598dddd680b`  
		Last Modified: Thu, 17 Mar 2022 11:28:17 GMT  
		Size: 35.3 MB (35279758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833a842281729982038158055afe9827cf83082a73928d160267a96c3a210909`  
		Last Modified: Fri, 18 Mar 2022 11:38:42 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb19a8bea8ac6452690b2abb425c234fa132fc999d44dc8678c047c83a2b8768`  
		Last Modified: Fri, 18 Mar 2022 11:38:42 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298a5cd67fcc1d54d133544fddcaee22c2d52b321bea99ddebfdc5e92cf5b9c5`  
		Last Modified: Fri, 18 Mar 2022 11:38:43 GMT  
		Size: 6.0 MB (5998310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:304b3fc5bf6eef287d420bb4471463e5dd7f258b64abc28ac0fa3cc28c389078`  
		Last Modified: Fri, 18 Mar 2022 11:38:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ae40f3931d22932d6ae2313ffce38370977d00b771c456e04802d1dd5b8724`  
		Last Modified: Fri, 18 Mar 2022 11:38:42 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; s390x

```console
$ docker pull spiped@sha256:04aafcacad77a9b72d2d47a38a232c9e3645a438c0131b47a4018b46f979be32
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34844908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ff67ace7af078b229b5928d2f0d8eba4dfc9336bd01cc8af778512ed9b34cbd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 03:06:58 GMT
ADD file:52f9267b4c57ac585a0d3d47a6f2ae1a71398264173ad4f190332957fa629c67 in / 
# Thu, 17 Mar 2022 03:07:01 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 16:49:57 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 17 Mar 2022 16:50:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 16:50:00 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 16:50:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 17 Mar 2022 16:50:12 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 16:50:12 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 16:50:12 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 16:50:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 16:50:12 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d101968410e5005df630b0572aec03c88de55b8de81f3cf7e6a57e1ce2e5a8e5`  
		Last Modified: Thu, 17 Mar 2022 03:12:46 GMT  
		Size: 29.7 MB (29655795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6ffc821fd848073df862253a81ff1adea16b2b909005db2cbce4ee66eb2a85`  
		Last Modified: Thu, 17 Mar 2022 16:50:52 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b47ffd2d769d0417b9b329e411c5d0abcf3eeb26d24af586ae0aaaf90e42b6a7`  
		Last Modified: Thu, 17 Mar 2022 16:50:52 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e66ff429e104d86eab7bf4adb5dc2db5a803f49496c73e98e298fe5b252e89`  
		Last Modified: Thu, 17 Mar 2022 16:50:53 GMT  
		Size: 5.2 MB (5185854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7601978f39168626ccd46b4478d2d3ca54a1a90e2436bddd43a901fe451ddb54`  
		Last Modified: Thu, 17 Mar 2022 16:50:53 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a37fe55f363c9febb17d5ff4cde072423c7d7197dbe1fdcda48d4483abe56b9`  
		Last Modified: Thu, 17 Mar 2022 16:50:52 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6.2-alpine`

```console
$ docker pull spiped@sha256:651bee70b611b34012354942ee14d8cd1c394a654381018891a216b65438b06d
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
$ docker pull spiped@sha256:fa4240521d3ff244261dfbcea3a9e63b5f2858626355d782bd7b97a37a706e0e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3037036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46fd9df2bffa7e91039d2ee71224e10bea88319d02d25fc53832aef21376ecd6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 04:01:58 GMT
ADD file:cf4b631a115c2bbfbd81cad2d3041bceb64a8136aac92ba8a63b6c51d60af764 in / 
# Thu, 17 Mar 2022 04:01:59 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 15:53:28 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 17 Mar 2022 15:53:30 GMT
RUN apk add --no-cache libssl1.1
# Thu, 17 Mar 2022 15:53:30 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 15:53:51 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 17 Mar 2022 15:53:52 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 15:53:52 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 15:53:52 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 15:53:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 15:53:53 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3d243047344378e9b7136d552d48feb7ea8b6fe14ce0990e0cc011d5e369626a`  
		Last Modified: Thu, 17 Mar 2022 04:02:41 GMT  
		Size: 2.8 MB (2812636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28609b3adb4c05998e1162db6c538ca407f2280011d95fcd8a244d805a5b735`  
		Last Modified: Thu, 17 Mar 2022 15:54:31 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b4dfa35cdb53635d719c0c532ec9937293bcefd0cfc46f8bd1feecfdf05a95`  
		Last Modified: Thu, 17 Mar 2022 15:54:31 GMT  
		Size: 7.8 KB (7789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1305ebaa04a3fbf473d9073ba19d8e7c200053717456c94b4aa81ad2379537a`  
		Last Modified: Thu, 17 Mar 2022 15:54:34 GMT  
		Size: 214.9 KB (214875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a9314de395635f68354281ea4e4c80ccd1a83382ea0c0797d439c77466a954`  
		Last Modified: Thu, 17 Mar 2022 15:54:31 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8620fb27c9cb715ea3d3d0940cbfe238f1c60983b2586367d7f672d1d83ff6e`  
		Last Modified: Thu, 17 Mar 2022 15:54:31 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:59826251d3a0ad2527c0bafdc1ea568962d7f5f3528b1e98d3aaa3926d652ac4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2833671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25087c53823bfdb0b76bf4d89b11576da2bbb0a43269741c3f40a8aa03ddd93a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 02:26:45 GMT
ADD file:9c8618405ef54d562132919ffe49c862d014b402e0e4813b87bf01574fa04c0e in / 
# Thu, 17 Mar 2022 02:26:45 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 10:53:28 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 17 Mar 2022 10:53:30 GMT
RUN apk add --no-cache libssl1.1
# Thu, 17 Mar 2022 10:53:31 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 10:53:50 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 17 Mar 2022 10:53:50 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 10:53:51 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 10:53:52 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 10:53:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 10:53:52 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:787f016efa9bc7812361be134f731e845b97fba19169cf3615e7048c0412380e`  
		Last Modified: Thu, 17 Mar 2022 02:28:24 GMT  
		Size: 2.6 MB (2624973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8491e25887dfb5f3955a484700defebb2ff52083efbde9795a85971df7a476f1`  
		Last Modified: Thu, 17 Mar 2022 10:54:24 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35d33f304fab5de548bc59cc09d332370e572391cf8e6547a78ecad3df48c27`  
		Last Modified: Thu, 17 Mar 2022 10:54:24 GMT  
		Size: 7.8 KB (7780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a10fd4be356562398de356a11d85dbf1d36467d9069e828647d3827e6c97cda2`  
		Last Modified: Thu, 17 Mar 2022 10:54:24 GMT  
		Size: 199.2 KB (199175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08779a270c83a7fa3e6660371def3ae5d7436e7afc2058d26fc7277c6465b79e`  
		Last Modified: Thu, 17 Mar 2022 10:54:24 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98221b50c485d80403bee1e97ffcda727cc378c9408fe0b9d2d32656e2e8ba42`  
		Last Modified: Thu, 17 Mar 2022 10:54:24 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:277d22d33ab8cd23ff5bf04d4e60841c8a335de8fdb772173601e9a4d4cb00bf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3802328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f94c64b2c706a58b82aa60bafca69c1fd15fb76714e5ca4aae0f1e4a47e3f1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Mon, 27 Dec 2021 18:00:04 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Mon, 27 Dec 2021 18:00:06 GMT
RUN apk add --no-cache libssl1.1
# Mon, 27 Dec 2021 18:00:06 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Mon, 27 Dec 2021 18:00:25 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Mon, 27 Dec 2021 18:00:26 GMT
VOLUME [/spiped]
# Mon, 27 Dec 2021 18:00:26 GMT
WORKDIR /spiped
# Mon, 27 Dec 2021 18:00:27 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Mon, 27 Dec 2021 18:00:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Dec 2021 18:00:28 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca194041621ab40d8e7f24b7f7e82aa07760b2dafcd26472bd7fae96171989a`  
		Last Modified: Mon, 27 Dec 2021 18:01:41 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e934f04cb0ca6a107389bcb614eb02143fb079eef09a47a9248e3c4ff07864`  
		Last Modified: Mon, 27 Dec 2021 18:01:41 GMT  
		Size: 7.7 KB (7749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4111e5d44f2316d799c8b9144d8f35765b0bf330b8d596d99e504969cd48e07a`  
		Last Modified: Mon, 27 Dec 2021 18:01:42 GMT  
		Size: 1.4 MB (1358077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46d751b026ad913b2a48630c96460959a733e75728d55aafbd389197bf81857`  
		Last Modified: Mon, 27 Dec 2021 18:01:41 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5140561b01c4c6ae8b47c729fd289d7eef4a2b0e9c427a6bd35a86747e966206`  
		Last Modified: Mon, 27 Dec 2021 18:01:41 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:d99e51a55cc06f9f9bb1a381fbcccc5b8a617221ede6d99e80fa0f1455d9a7c7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2931463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70fa2e490f06ca016a59e8ccb25bdf2aca9f52652ffd37b739b119385121ed0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 03:19:52 GMT
ADD file:cd7d91362950471ca4678cf3833dc47119ab519dea51424c847bbbb21e1649d4 in / 
# Thu, 17 Mar 2022 03:19:52 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 21:05:07 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 17 Mar 2022 21:05:08 GMT
RUN apk add --no-cache libssl1.1
# Thu, 17 Mar 2022 21:05:09 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 21:05:19 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 17 Mar 2022 21:05:20 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 21:05:21 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 21:05:23 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 21:05:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 21:05:24 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:148d739a8e6b9342daa1f5b428d3a3c6118f340f21df28c16e06f918ef150147`  
		Last Modified: Thu, 17 Mar 2022 03:20:45 GMT  
		Size: 2.7 MB (2714807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfe03b788288bfc55a2e69551194eb50a0e5968d87eb615e001116670eca8d1`  
		Last Modified: Thu, 17 Mar 2022 21:06:08 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ebbe0c7d8e482b1cc3a2c35380a3da9aba32e7419814e8463d19e20ab058a5`  
		Last Modified: Thu, 17 Mar 2022 21:06:08 GMT  
		Size: 7.8 KB (7750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd44380493879dfe08522b418a1697db90bf574f812b27abf9f5363d6130acfa`  
		Last Modified: Thu, 17 Mar 2022 21:06:08 GMT  
		Size: 207.2 KB (207231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:684fec7d45ce25526ac84e65dbb141f72835e9b00faa35ffd4bd2d1b5f98b3c6`  
		Last Modified: Thu, 17 Mar 2022 21:06:08 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:526257cb94ed56c056f2917a4a8e8c81f2c1b9b6911487da82418348ffa037f0`  
		Last Modified: Thu, 17 Mar 2022 21:06:09 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; 386

```console
$ docker pull spiped@sha256:29c7cebe60cecc9f7cbb75c243694894ccead716974c52d9e7f9a99a1e7931c3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3056990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65970f53cd34df6344b60d5b1f188ae0408dfd33dd9036a90562f4b4d4d4ef83`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 08:13:03 GMT
ADD file:22216bc654d9177244235f242fa83cae3b283b3c145cad7ccf11c0d29f5f0ff2 in / 
# Thu, 17 Mar 2022 08:13:03 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 21:39:40 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 17 Mar 2022 21:39:42 GMT
RUN apk add --no-cache libssl1.1
# Thu, 17 Mar 2022 21:39:42 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 21:40:00 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 17 Mar 2022 21:40:00 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 21:40:00 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 21:40:00 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 21:40:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 21:40:01 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:93317a1f65ec94b67aefe728a598022610246404e3a68d391c76cd0e5244a2a0`  
		Last Modified: Thu, 17 Mar 2022 08:13:56 GMT  
		Size: 2.8 MB (2821789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8535b315fbad030f6fe4b11974d789b28ec85b2e79677eb197239c4e2d58ad07`  
		Last Modified: Thu, 17 Mar 2022 21:41:04 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47d449347fe74957e2caaf9718edfca3c882962cffbce71dd4e6207078459b6`  
		Last Modified: Thu, 17 Mar 2022 21:41:04 GMT  
		Size: 7.8 KB (7782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c09f03ca1752043d6dfd052d7aae794162b6013a723e0efc9477f848ca481c5`  
		Last Modified: Thu, 17 Mar 2022 21:41:04 GMT  
		Size: 225.7 KB (225683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd9e35cc22870710eefd82f88e16ed34c080e8c4f505037f17080f14e818cd1a`  
		Last Modified: Thu, 17 Mar 2022 21:41:04 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1021ec3b3986cf8edf968a928a55219fb145dbe088f59a3ffb7144791d7831d`  
		Last Modified: Thu, 17 Mar 2022 21:41:04 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:8c23f5e4d58ef3fce86009c4f9d2b536e5dd7645357d02dc8f3143a45d24b62a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3036720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:525943d93e23029964172e9971ee55221214131aa72607d782b906782cebd905`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 11:14:04 GMT
ADD file:ddc94e1e084c05807db26adcc95b47a137fa47fb391e75998b338ada65e00c1c in / 
# Thu, 17 Mar 2022 11:14:09 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 11:36:53 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 18 Mar 2022 11:37:02 GMT
RUN apk add --no-cache libssl1.1
# Fri, 18 Mar 2022 11:37:05 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 18 Mar 2022 11:37:26 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 18 Mar 2022 11:37:34 GMT
VOLUME [/spiped]
# Fri, 18 Mar 2022 11:37:48 GMT
WORKDIR /spiped
# Fri, 18 Mar 2022 11:37:52 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 18 Mar 2022 11:38:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 11:38:06 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:eef85fcc847498263d979ef7ec75680d05e90815eb83a9ec4db135b990c0d8b8`  
		Last Modified: Thu, 17 Mar 2022 11:15:15 GMT  
		Size: 2.8 MB (2814051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b49ab39683ef52a5765c0c691555d28af162d2ce40131084fc25680453944b9`  
		Last Modified: Fri, 18 Mar 2022 11:39:07 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0d0f21c26195ed58e548c0bcc057466eedf6289e9074e2e6ed7b00f9554c9d`  
		Last Modified: Fri, 18 Mar 2022 11:39:07 GMT  
		Size: 7.8 KB (7775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171521d6689bb8ec8d5ba220e3dd1b5f396f561fc0874d47a72700d90af2e327`  
		Last Modified: Fri, 18 Mar 2022 11:39:07 GMT  
		Size: 213.2 KB (213153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83dadace8041954e55061d0cfb5738223cde3d3a5d9d2e8383f501df563e7af0`  
		Last Modified: Fri, 18 Mar 2022 11:39:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dafb87341a132f89d6162605f157f7d2acca5cf1a07120fea5bee84acb259934`  
		Last Modified: Fri, 18 Mar 2022 11:39:07 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:9136888efc8105d1e53c8364999ed1226816696570a294b7173cfa406b46c7a1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2812933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81e94b253317064b662cf7864dd5a73b05b9b2469182896a3975c29f156fa5b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 03:04:28 GMT
ADD file:f623c69acb1859b41ef29e8f20f4e6c7072d9c6d7210d745afc615251bfe418f in / 
# Thu, 17 Mar 2022 03:04:28 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 16:50:20 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 17 Mar 2022 16:50:21 GMT
RUN apk add --no-cache libssl1.1
# Thu, 17 Mar 2022 16:50:21 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 16:50:26 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 17 Mar 2022 16:50:27 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 16:50:27 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 16:50:27 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 16:50:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 16:50:27 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d51040c5bfbf434887bfed2557335a411e6ef760d04cc178d455d1c3ec1b721c`  
		Last Modified: Thu, 17 Mar 2022 03:05:26 GMT  
		Size: 2.6 MB (2601715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a5592bce39ceb295366e2e0046df438f4b7588eaa316b2c6dce8e9e7846009`  
		Last Modified: Thu, 17 Mar 2022 16:51:05 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7d640b6d89c9475c948efa4b038dd5070d832d259ec02b3b02404a0fb56b1f`  
		Last Modified: Thu, 17 Mar 2022 16:51:05 GMT  
		Size: 7.8 KB (7786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc076029660bad5fd7c4dd63b63e13ef4a631b1bcfeb96aa738308da36262fe`  
		Last Modified: Thu, 17 Mar 2022 16:51:05 GMT  
		Size: 201.7 KB (201691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4701bc04231bf0a6e5b37d89cc796ed88c42f042536e43f8ec6561f5334b985`  
		Last Modified: Thu, 17 Mar 2022 16:51:05 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e367ce3174808cf7f69deca196856b3a6eadb9c900975bb8b47d69171568c601`  
		Last Modified: Thu, 17 Mar 2022 16:51:05 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:alpine`

```console
$ docker pull spiped@sha256:651bee70b611b34012354942ee14d8cd1c394a654381018891a216b65438b06d
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
$ docker pull spiped@sha256:fa4240521d3ff244261dfbcea3a9e63b5f2858626355d782bd7b97a37a706e0e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3037036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46fd9df2bffa7e91039d2ee71224e10bea88319d02d25fc53832aef21376ecd6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 04:01:58 GMT
ADD file:cf4b631a115c2bbfbd81cad2d3041bceb64a8136aac92ba8a63b6c51d60af764 in / 
# Thu, 17 Mar 2022 04:01:59 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 15:53:28 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 17 Mar 2022 15:53:30 GMT
RUN apk add --no-cache libssl1.1
# Thu, 17 Mar 2022 15:53:30 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 15:53:51 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 17 Mar 2022 15:53:52 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 15:53:52 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 15:53:52 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 15:53:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 15:53:53 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3d243047344378e9b7136d552d48feb7ea8b6fe14ce0990e0cc011d5e369626a`  
		Last Modified: Thu, 17 Mar 2022 04:02:41 GMT  
		Size: 2.8 MB (2812636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28609b3adb4c05998e1162db6c538ca407f2280011d95fcd8a244d805a5b735`  
		Last Modified: Thu, 17 Mar 2022 15:54:31 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b4dfa35cdb53635d719c0c532ec9937293bcefd0cfc46f8bd1feecfdf05a95`  
		Last Modified: Thu, 17 Mar 2022 15:54:31 GMT  
		Size: 7.8 KB (7789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1305ebaa04a3fbf473d9073ba19d8e7c200053717456c94b4aa81ad2379537a`  
		Last Modified: Thu, 17 Mar 2022 15:54:34 GMT  
		Size: 214.9 KB (214875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a9314de395635f68354281ea4e4c80ccd1a83382ea0c0797d439c77466a954`  
		Last Modified: Thu, 17 Mar 2022 15:54:31 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8620fb27c9cb715ea3d3d0940cbfe238f1c60983b2586367d7f672d1d83ff6e`  
		Last Modified: Thu, 17 Mar 2022 15:54:31 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:59826251d3a0ad2527c0bafdc1ea568962d7f5f3528b1e98d3aaa3926d652ac4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2833671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25087c53823bfdb0b76bf4d89b11576da2bbb0a43269741c3f40a8aa03ddd93a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 02:26:45 GMT
ADD file:9c8618405ef54d562132919ffe49c862d014b402e0e4813b87bf01574fa04c0e in / 
# Thu, 17 Mar 2022 02:26:45 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 10:53:28 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 17 Mar 2022 10:53:30 GMT
RUN apk add --no-cache libssl1.1
# Thu, 17 Mar 2022 10:53:31 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 10:53:50 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 17 Mar 2022 10:53:50 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 10:53:51 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 10:53:52 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 10:53:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 10:53:52 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:787f016efa9bc7812361be134f731e845b97fba19169cf3615e7048c0412380e`  
		Last Modified: Thu, 17 Mar 2022 02:28:24 GMT  
		Size: 2.6 MB (2624973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8491e25887dfb5f3955a484700defebb2ff52083efbde9795a85971df7a476f1`  
		Last Modified: Thu, 17 Mar 2022 10:54:24 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35d33f304fab5de548bc59cc09d332370e572391cf8e6547a78ecad3df48c27`  
		Last Modified: Thu, 17 Mar 2022 10:54:24 GMT  
		Size: 7.8 KB (7780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a10fd4be356562398de356a11d85dbf1d36467d9069e828647d3827e6c97cda2`  
		Last Modified: Thu, 17 Mar 2022 10:54:24 GMT  
		Size: 199.2 KB (199175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08779a270c83a7fa3e6660371def3ae5d7436e7afc2058d26fc7277c6465b79e`  
		Last Modified: Thu, 17 Mar 2022 10:54:24 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98221b50c485d80403bee1e97ffcda727cc378c9408fe0b9d2d32656e2e8ba42`  
		Last Modified: Thu, 17 Mar 2022 10:54:24 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:277d22d33ab8cd23ff5bf04d4e60841c8a335de8fdb772173601e9a4d4cb00bf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3802328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f94c64b2c706a58b82aa60bafca69c1fd15fb76714e5ca4aae0f1e4a47e3f1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Mon, 27 Dec 2021 18:00:04 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Mon, 27 Dec 2021 18:00:06 GMT
RUN apk add --no-cache libssl1.1
# Mon, 27 Dec 2021 18:00:06 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Mon, 27 Dec 2021 18:00:25 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Mon, 27 Dec 2021 18:00:26 GMT
VOLUME [/spiped]
# Mon, 27 Dec 2021 18:00:26 GMT
WORKDIR /spiped
# Mon, 27 Dec 2021 18:00:27 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Mon, 27 Dec 2021 18:00:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Dec 2021 18:00:28 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca194041621ab40d8e7f24b7f7e82aa07760b2dafcd26472bd7fae96171989a`  
		Last Modified: Mon, 27 Dec 2021 18:01:41 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e934f04cb0ca6a107389bcb614eb02143fb079eef09a47a9248e3c4ff07864`  
		Last Modified: Mon, 27 Dec 2021 18:01:41 GMT  
		Size: 7.7 KB (7749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4111e5d44f2316d799c8b9144d8f35765b0bf330b8d596d99e504969cd48e07a`  
		Last Modified: Mon, 27 Dec 2021 18:01:42 GMT  
		Size: 1.4 MB (1358077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46d751b026ad913b2a48630c96460959a733e75728d55aafbd389197bf81857`  
		Last Modified: Mon, 27 Dec 2021 18:01:41 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5140561b01c4c6ae8b47c729fd289d7eef4a2b0e9c427a6bd35a86747e966206`  
		Last Modified: Mon, 27 Dec 2021 18:01:41 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:d99e51a55cc06f9f9bb1a381fbcccc5b8a617221ede6d99e80fa0f1455d9a7c7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2931463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70fa2e490f06ca016a59e8ccb25bdf2aca9f52652ffd37b739b119385121ed0c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 03:19:52 GMT
ADD file:cd7d91362950471ca4678cf3833dc47119ab519dea51424c847bbbb21e1649d4 in / 
# Thu, 17 Mar 2022 03:19:52 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 21:05:07 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 17 Mar 2022 21:05:08 GMT
RUN apk add --no-cache libssl1.1
# Thu, 17 Mar 2022 21:05:09 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 21:05:19 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 17 Mar 2022 21:05:20 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 21:05:21 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 21:05:23 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 21:05:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 21:05:24 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:148d739a8e6b9342daa1f5b428d3a3c6118f340f21df28c16e06f918ef150147`  
		Last Modified: Thu, 17 Mar 2022 03:20:45 GMT  
		Size: 2.7 MB (2714807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfe03b788288bfc55a2e69551194eb50a0e5968d87eb615e001116670eca8d1`  
		Last Modified: Thu, 17 Mar 2022 21:06:08 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ebbe0c7d8e482b1cc3a2c35380a3da9aba32e7419814e8463d19e20ab058a5`  
		Last Modified: Thu, 17 Mar 2022 21:06:08 GMT  
		Size: 7.8 KB (7750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd44380493879dfe08522b418a1697db90bf574f812b27abf9f5363d6130acfa`  
		Last Modified: Thu, 17 Mar 2022 21:06:08 GMT  
		Size: 207.2 KB (207231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:684fec7d45ce25526ac84e65dbb141f72835e9b00faa35ffd4bd2d1b5f98b3c6`  
		Last Modified: Thu, 17 Mar 2022 21:06:08 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:526257cb94ed56c056f2917a4a8e8c81f2c1b9b6911487da82418348ffa037f0`  
		Last Modified: Thu, 17 Mar 2022 21:06:09 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; 386

```console
$ docker pull spiped@sha256:29c7cebe60cecc9f7cbb75c243694894ccead716974c52d9e7f9a99a1e7931c3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3056990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65970f53cd34df6344b60d5b1f188ae0408dfd33dd9036a90562f4b4d4d4ef83`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 08:13:03 GMT
ADD file:22216bc654d9177244235f242fa83cae3b283b3c145cad7ccf11c0d29f5f0ff2 in / 
# Thu, 17 Mar 2022 08:13:03 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 21:39:40 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 17 Mar 2022 21:39:42 GMT
RUN apk add --no-cache libssl1.1
# Thu, 17 Mar 2022 21:39:42 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 21:40:00 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 17 Mar 2022 21:40:00 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 21:40:00 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 21:40:00 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 21:40:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 21:40:01 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:93317a1f65ec94b67aefe728a598022610246404e3a68d391c76cd0e5244a2a0`  
		Last Modified: Thu, 17 Mar 2022 08:13:56 GMT  
		Size: 2.8 MB (2821789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8535b315fbad030f6fe4b11974d789b28ec85b2e79677eb197239c4e2d58ad07`  
		Last Modified: Thu, 17 Mar 2022 21:41:04 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47d449347fe74957e2caaf9718edfca3c882962cffbce71dd4e6207078459b6`  
		Last Modified: Thu, 17 Mar 2022 21:41:04 GMT  
		Size: 7.8 KB (7782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c09f03ca1752043d6dfd052d7aae794162b6013a723e0efc9477f848ca481c5`  
		Last Modified: Thu, 17 Mar 2022 21:41:04 GMT  
		Size: 225.7 KB (225683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd9e35cc22870710eefd82f88e16ed34c080e8c4f505037f17080f14e818cd1a`  
		Last Modified: Thu, 17 Mar 2022 21:41:04 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1021ec3b3986cf8edf968a928a55219fb145dbe088f59a3ffb7144791d7831d`  
		Last Modified: Thu, 17 Mar 2022 21:41:04 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:8c23f5e4d58ef3fce86009c4f9d2b536e5dd7645357d02dc8f3143a45d24b62a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3036720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:525943d93e23029964172e9971ee55221214131aa72607d782b906782cebd905`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 11:14:04 GMT
ADD file:ddc94e1e084c05807db26adcc95b47a137fa47fb391e75998b338ada65e00c1c in / 
# Thu, 17 Mar 2022 11:14:09 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 11:36:53 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 18 Mar 2022 11:37:02 GMT
RUN apk add --no-cache libssl1.1
# Fri, 18 Mar 2022 11:37:05 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 18 Mar 2022 11:37:26 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 18 Mar 2022 11:37:34 GMT
VOLUME [/spiped]
# Fri, 18 Mar 2022 11:37:48 GMT
WORKDIR /spiped
# Fri, 18 Mar 2022 11:37:52 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 18 Mar 2022 11:38:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 11:38:06 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:eef85fcc847498263d979ef7ec75680d05e90815eb83a9ec4db135b990c0d8b8`  
		Last Modified: Thu, 17 Mar 2022 11:15:15 GMT  
		Size: 2.8 MB (2814051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b49ab39683ef52a5765c0c691555d28af162d2ce40131084fc25680453944b9`  
		Last Modified: Fri, 18 Mar 2022 11:39:07 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0d0f21c26195ed58e548c0bcc057466eedf6289e9074e2e6ed7b00f9554c9d`  
		Last Modified: Fri, 18 Mar 2022 11:39:07 GMT  
		Size: 7.8 KB (7775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171521d6689bb8ec8d5ba220e3dd1b5f396f561fc0874d47a72700d90af2e327`  
		Last Modified: Fri, 18 Mar 2022 11:39:07 GMT  
		Size: 213.2 KB (213153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83dadace8041954e55061d0cfb5738223cde3d3a5d9d2e8383f501df563e7af0`  
		Last Modified: Fri, 18 Mar 2022 11:39:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dafb87341a132f89d6162605f157f7d2acca5cf1a07120fea5bee84acb259934`  
		Last Modified: Fri, 18 Mar 2022 11:39:07 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; s390x

```console
$ docker pull spiped@sha256:9136888efc8105d1e53c8364999ed1226816696570a294b7173cfa406b46c7a1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2812933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81e94b253317064b662cf7864dd5a73b05b9b2469182896a3975c29f156fa5b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 03:04:28 GMT
ADD file:f623c69acb1859b41ef29e8f20f4e6c7072d9c6d7210d745afc615251bfe418f in / 
# Thu, 17 Mar 2022 03:04:28 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 16:50:20 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Thu, 17 Mar 2022 16:50:21 GMT
RUN apk add --no-cache libssl1.1
# Thu, 17 Mar 2022 16:50:21 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 16:50:26 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Thu, 17 Mar 2022 16:50:27 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 16:50:27 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 16:50:27 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 16:50:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 16:50:27 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d51040c5bfbf434887bfed2557335a411e6ef760d04cc178d455d1c3ec1b721c`  
		Last Modified: Thu, 17 Mar 2022 03:05:26 GMT  
		Size: 2.6 MB (2601715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a5592bce39ceb295366e2e0046df438f4b7588eaa316b2c6dce8e9e7846009`  
		Last Modified: Thu, 17 Mar 2022 16:51:05 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7d640b6d89c9475c948efa4b038dd5070d832d259ec02b3b02404a0fb56b1f`  
		Last Modified: Thu, 17 Mar 2022 16:51:05 GMT  
		Size: 7.8 KB (7786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc076029660bad5fd7c4dd63b63e13ef4a631b1bcfeb96aa738308da36262fe`  
		Last Modified: Thu, 17 Mar 2022 16:51:05 GMT  
		Size: 201.7 KB (201691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4701bc04231bf0a6e5b37d89cc796ed88c42f042536e43f8ec6561f5334b985`  
		Last Modified: Thu, 17 Mar 2022 16:51:05 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e367ce3174808cf7f69deca196856b3a6eadb9c900975bb8b47d69171568c601`  
		Last Modified: Thu, 17 Mar 2022 16:51:05 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:latest`

```console
$ docker pull spiped@sha256:d0d169a896962896013eb85ba8c10fcb5e5ab61c7b17b88e2e41a14dd75dedd5
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
$ docker pull spiped@sha256:b8d2ab2976a3b82a57e4ac9fc033752dfaf040d529691989e424cd5c99d8bbd3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37346333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68b6bef8dc6e1cbd84fb52a34b7b7d7df36d02946bf4bdfca5aa1b7f2d52176f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:59 GMT
ADD file:36919ae6bb25e3269eff949443129a01a8a43fb967fe6563939ebe1e1e9b8228 in / 
# Thu, 17 Mar 2022 04:03:59 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 15:52:38 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 17 Mar 2022 15:52:43 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 15:52:43 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 15:53:21 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 17 Mar 2022 15:53:21 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 15:53:22 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 15:53:22 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 15:53:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 15:53:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ae13dd57832654086618a81dbc128846aa092489260c326ee95429b63c3cf213`  
		Last Modified: Thu, 17 Mar 2022 04:10:05 GMT  
		Size: 31.4 MB (31376572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a76f2896127d7514587b03a8586b6c4bf68ca03ee67882432f282d5a3dc8e5d1`  
		Last Modified: Thu, 17 Mar 2022 15:54:13 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac159b91e9882052a2a7c77bf3ec73c84ea2c50d117cf1129e7e552374d62c2`  
		Last Modified: Thu, 17 Mar 2022 15:54:13 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd11eb085d6fc73cdb158b796cc6592d653f2f64bc48fd6bd88b02289f0dcfc`  
		Last Modified: Thu, 17 Mar 2022 15:54:15 GMT  
		Size: 6.0 MB (5966507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1610fbfaf3d68521b5f2784f03d10b65adac79bb491680dce45623e5cfd64b9`  
		Last Modified: Thu, 17 Mar 2022 15:54:13 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba1c750cce13a53c755ec9a30804efe928ee400172b3e12bbeb62b7d06178d3`  
		Last Modified: Thu, 17 Mar 2022 15:54:13 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; arm variant v5

```console
$ docker pull spiped@sha256:8a2e0011c5701f972d5ba018f0874593df829ac6c310b4bc74e48f548a82b624
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33950244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1fb2363cc87afddb3e829dfa3fbc4638f7d761ca756e0c04ae478180c55d43`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 05:19:45 GMT
ADD file:1eb4f937d40230354e20e28ed781234acd4be2b0dab72f87131a3eac66349719 in / 
# Thu, 17 Mar 2022 05:19:46 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 19:07:31 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 17 Mar 2022 19:07:41 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 19:07:41 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 19:08:46 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 17 Mar 2022 19:08:46 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 19:08:47 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 19:08:50 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 19:08:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 19:08:52 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4da455e7774c0e977d862a56ab6d85f33ce5dd5a77d45a0a74a272e9eae6bea0`  
		Last Modified: Thu, 17 Mar 2022 05:35:01 GMT  
		Size: 28.9 MB (28919702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ccaa8f7993c69ae0db39ad4c2027a13ce97175da89f5be82de6a2ca2a97c7d1`  
		Last Modified: Thu, 17 Mar 2022 19:09:25 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9512592020427919bc6c45a56ea8a3e87091e9b9b72c5f4081ddbdfda9fbe931`  
		Last Modified: Thu, 17 Mar 2022 19:09:26 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2010aa0813bd04163cffb9ff94e259b6216dc2c427790ff8bbb2f3b7ccb45846`  
		Last Modified: Thu, 17 Mar 2022 19:09:28 GMT  
		Size: 5.0 MB (5027289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3447d294931d6120cea1ca769318e6e3730d1d3a01afc8a3f8046adb9872d7`  
		Last Modified: Thu, 17 Mar 2022 19:09:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ba318f72a277eedbbb07d36dd5fe2c4195238cb2bd1aa540f8a89a169f22a2`  
		Last Modified: Thu, 17 Mar 2022 19:09:25 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; arm variant v7

```console
$ docker pull spiped@sha256:ac215edcc30b28977b317d77ccaaae94761d4354587e9800d101bb637e1149d0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31315718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4d7a6cecd75cfc07f7f336a43f8c0c2bd623ff9d78a61a9c7442249f5b36df1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 01 Mar 2022 02:02:56 GMT
ADD file:c6b519323fd1fa09b9f8c8608778872e8fa6208cb0b42aaccdef4479a469f5f4 in / 
# Tue, 01 Mar 2022 02:02:57 GMT
CMD ["bash"]
# Wed, 02 Mar 2022 16:17:58 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 02 Mar 2022 16:18:05 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 16:18:05 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 02 Mar 2022 16:18:49 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 02 Mar 2022 16:18:50 GMT
VOLUME [/spiped]
# Wed, 02 Mar 2022 16:18:50 GMT
WORKDIR /spiped
# Wed, 02 Mar 2022 16:18:51 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 02 Mar 2022 16:18:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 16:18:52 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:59dbb2ac3829352dd707e28e037734c9fbdef5b03aea31e3929ddcead949afee`  
		Last Modified: Tue, 01 Mar 2022 02:19:09 GMT  
		Size: 26.6 MB (26565105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d308a84eca5cd40a5b3b38f20aba12ad984055514266c5f21895dbd7ae398c4`  
		Last Modified: Wed, 02 Mar 2022 16:19:54 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:885c743661aaee24e106ee3f2083d0acdcff80bbbfb0663485d199324303dbe2`  
		Last Modified: Wed, 02 Mar 2022 16:19:54 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1b566deb17f5e2852900d444a17df344a45e23a180e0dfc06251a994ef5333c`  
		Last Modified: Wed, 02 Mar 2022 16:19:59 GMT  
		Size: 4.7 MB (4747364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f044884cf1737497ba826896f6b7e83d791a1b320f0dc816a7862caffe3d2848`  
		Last Modified: Wed, 02 Mar 2022 16:19:54 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e071d50afe6ad4ee58ac45ec6df078835658702fde56f4230838ffb45ed917e5`  
		Last Modified: Wed, 02 Mar 2022 16:19:54 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:fd6ccb6336851679362386de45250510a5e80ef3c4e7df2ae724eaa4c9667ed0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35335910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7240db44c2f7942501fdbf02463d450aff3590fc9bc59ad1940947b652f01fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 03:21:57 GMT
ADD file:e52e032f1ace6abd44b3647d43c1b8ae30bac6de804eef09c6ccd793057996fd in / 
# Thu, 17 Mar 2022 03:21:58 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 21:04:34 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 17 Mar 2022 21:04:37 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 21:04:37 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 21:04:55 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 17 Mar 2022 21:04:56 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 21:04:57 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 21:04:59 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 21:04:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 21:05:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:32252aec0777ac025a158bc2a8317650a4f2a0a875387011b1165013874f8723`  
		Last Modified: Thu, 17 Mar 2022 03:28:36 GMT  
		Size: 30.1 MB (30063013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f39180b559e5aed1b40421eec8f7b61457cc16f2cfee7f2da5aa250b61d4370`  
		Last Modified: Thu, 17 Mar 2022 21:05:48 GMT  
		Size: 1.6 KB (1617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcd781ba64e538c462ceeb478df86f9e82f9043472f590c90b8b77e1c69b494`  
		Last Modified: Thu, 17 Mar 2022 21:05:49 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6acdb1b2ac977841bfba332aa093360fd27c5ae5aeeeb8ed34c5da6d36cbc01`  
		Last Modified: Thu, 17 Mar 2022 21:05:50 GMT  
		Size: 5.3 MB (5269921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f5b809a8f2f8d99685a97d9b9b90ed684e872055f59a0bef726c106ed92eae`  
		Last Modified: Thu, 17 Mar 2022 21:05:49 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815c0e22b949966496c66a9c25b6ae9090833f44298de5096f6f6673d2b5eeed`  
		Last Modified: Thu, 17 Mar 2022 21:05:49 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; 386

```console
$ docker pull spiped@sha256:ed2f5c92201304d5bbfd3a42f000b351c22b4d58f49e952733cb43f825a3e301
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40281229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e319a53a099b51990813e4b7cfcd49725cfe0eda506064c73bbb2bc420375e97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 08:15:53 GMT
ADD file:2d6be3846f0e5fabd85bc9409b1e2223cad4c57c76f96e9f81489ba78a72a1f5 in / 
# Thu, 17 Mar 2022 08:15:54 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 21:38:49 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 17 Mar 2022 21:38:53 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 21:38:53 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 21:39:26 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 17 Mar 2022 21:39:26 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 21:39:27 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 21:39:27 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 21:39:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 21:39:27 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:176085117cac9b2cf2cf57b3a10c9811dbd2773497fbac3086b5024070447e97`  
		Last Modified: Thu, 17 Mar 2022 08:24:00 GMT  
		Size: 32.4 MB (32386475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f0023ca52fa68e0b790d53b1989cc86a09c03c3f5ba512bd7254e660798701`  
		Last Modified: Thu, 17 Mar 2022 21:40:39 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f169664f6c06e48b52c02faa7212ffdbed368d76e4046ee62757dcdad99ec1`  
		Last Modified: Thu, 17 Mar 2022 21:40:39 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e208248e53ac127f9ba59ef6496e619a4aa53b7da6cada4f8c9eefab9d6eb759`  
		Last Modified: Thu, 17 Mar 2022 21:40:42 GMT  
		Size: 7.9 MB (7891501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e182dd8aad03bcc4a4fc70c4d5477e38448020a78e7598e41bc1d584729d764b`  
		Last Modified: Thu, 17 Mar 2022 21:40:39 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4315719c3c75933b98aafbac692d4aa273eec4588f2647f7ad5ae7032b336ba2`  
		Last Modified: Thu, 17 Mar 2022 21:40:39 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; mips64le

```console
$ docker pull spiped@sha256:ad61e440c067a6b168769664de1c184685e3582a1422d3c2d1681ba457ff7215
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35347773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556e5433be4b6d7d5c9e1b8aea73caac9038b7fa0ced3fcc6d085d06eae244cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 08:53:04 GMT
ADD file:795ac4eba576bc4c995df2a18b10ce802ee8a05417cdc53f5aa09452ecf2e832 in / 
# Thu, 17 Mar 2022 08:53:08 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 21:25:08 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 18 Mar 2022 21:25:24 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 21:25:27 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 18 Mar 2022 21:27:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 18 Mar 2022 21:27:04 GMT
VOLUME [/spiped]
# Fri, 18 Mar 2022 21:27:07 GMT
WORKDIR /spiped
# Fri, 18 Mar 2022 21:27:09 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 18 Mar 2022 21:27:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 21:27:15 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4799d88734ae94287a665c0e14621a744706cfbe17a0cf27ae9b0cc630927b11`  
		Last Modified: Thu, 17 Mar 2022 10:43:20 GMT  
		Size: 29.6 MB (29639810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c3bb983a06c1d0519d23a6efec25298a548ce43495f86ad94ed19dc18240d6`  
		Last Modified: Fri, 18 Mar 2022 21:27:38 GMT  
		Size: 1.6 KB (1614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0dd02a98e85a0552aa2aef9bcf7cc1127e26a8aebbd1b4174d51b68e253093`  
		Last Modified: Fri, 18 Mar 2022 21:27:38 GMT  
		Size: 926.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73a235ac7d157ff9e32cdc51b831aae0fde62bfb42dcc02a77a0e52df565b34`  
		Last Modified: Fri, 18 Mar 2022 21:27:44 GMT  
		Size: 5.7 MB (5704986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c944593c2417013162356e68bb977d4fdaff97eba73de773bb2f61032d200cca`  
		Last Modified: Fri, 18 Mar 2022 21:27:39 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b86ea964515b4d10fea8515b90d3d4557e4f7db1a99f2e9d9cadd52c34ea59`  
		Last Modified: Fri, 18 Mar 2022 21:27:38 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; ppc64le

```console
$ docker pull spiped@sha256:9797106231608e33cf1bf6b4aa3121e668221249a4393633d99fd2d54dd41dc1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41281331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:387b2511d5857028002168cda350ddc9cba69bb5e9c7efe68e8aba8e77b6237e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 11:17:54 GMT
ADD file:e8555f1cb439a45786b92e929cfa154b51f668c5b4cd69e4ce98340c5998fe0c in / 
# Thu, 17 Mar 2022 11:18:00 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 11:32:51 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Fri, 18 Mar 2022 11:33:08 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 11:33:11 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 18 Mar 2022 11:35:53 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 18 Mar 2022 11:36:02 GMT
VOLUME [/spiped]
# Fri, 18 Mar 2022 11:36:08 GMT
WORKDIR /spiped
# Fri, 18 Mar 2022 11:36:16 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 18 Mar 2022 11:36:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 11:36:29 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:aec78dc45d7b3df12df0672d13e22005592b453f03ff2580efac2598dddd680b`  
		Last Modified: Thu, 17 Mar 2022 11:28:17 GMT  
		Size: 35.3 MB (35279758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833a842281729982038158055afe9827cf83082a73928d160267a96c3a210909`  
		Last Modified: Fri, 18 Mar 2022 11:38:42 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb19a8bea8ac6452690b2abb425c234fa132fc999d44dc8678c047c83a2b8768`  
		Last Modified: Fri, 18 Mar 2022 11:38:42 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298a5cd67fcc1d54d133544fddcaee22c2d52b321bea99ddebfdc5e92cf5b9c5`  
		Last Modified: Fri, 18 Mar 2022 11:38:43 GMT  
		Size: 6.0 MB (5998310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:304b3fc5bf6eef287d420bb4471463e5dd7f258b64abc28ac0fa3cc28c389078`  
		Last Modified: Fri, 18 Mar 2022 11:38:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ae40f3931d22932d6ae2313ffce38370977d00b771c456e04802d1dd5b8724`  
		Last Modified: Fri, 18 Mar 2022 11:38:42 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; s390x

```console
$ docker pull spiped@sha256:04aafcacad77a9b72d2d47a38a232c9e3645a438c0131b47a4018b46f979be32
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34844908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ff67ace7af078b229b5928d2f0d8eba4dfc9336bd01cc8af778512ed9b34cbd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 17 Mar 2022 03:06:58 GMT
ADD file:52f9267b4c57ac585a0d3d47a6f2ae1a71398264173ad4f190332957fa629c67 in / 
# Thu, 17 Mar 2022 03:07:01 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 16:49:57 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 17 Mar 2022 16:50:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 16:50:00 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 17 Mar 2022 16:50:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 17 Mar 2022 16:50:12 GMT
VOLUME [/spiped]
# Thu, 17 Mar 2022 16:50:12 GMT
WORKDIR /spiped
# Thu, 17 Mar 2022 16:50:12 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 17 Mar 2022 16:50:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 16:50:12 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d101968410e5005df630b0572aec03c88de55b8de81f3cf7e6a57e1ce2e5a8e5`  
		Last Modified: Thu, 17 Mar 2022 03:12:46 GMT  
		Size: 29.7 MB (29655795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6ffc821fd848073df862253a81ff1adea16b2b909005db2cbce4ee66eb2a85`  
		Last Modified: Thu, 17 Mar 2022 16:50:52 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b47ffd2d769d0417b9b329e411c5d0abcf3eeb26d24af586ae0aaaf90e42b6a7`  
		Last Modified: Thu, 17 Mar 2022 16:50:52 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e66ff429e104d86eab7bf4adb5dc2db5a803f49496c73e98e298fe5b252e89`  
		Last Modified: Thu, 17 Mar 2022 16:50:53 GMT  
		Size: 5.2 MB (5185854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7601978f39168626ccd46b4478d2d3ca54a1a90e2436bddd43a901fe451ddb54`  
		Last Modified: Thu, 17 Mar 2022 16:50:53 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a37fe55f363c9febb17d5ff4cde072423c7d7197dbe1fdcda48d4483abe56b9`  
		Last Modified: Thu, 17 Mar 2022 16:50:52 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
