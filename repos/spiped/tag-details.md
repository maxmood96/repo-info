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
$ docker pull spiped@sha256:baf6bcaed017648a642add6562bf6e5de15eabf4be46737afba352c1fdd36ea0
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
$ docker pull spiped@sha256:907ddd7d8a3f64e3b9587d8bd37803871c7e0301273fd134fff16a4601b764b6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 MB (37421712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aebdf10111eb9350e84131fa07f10b1e016fae20fb35a2ef3054aac040d9ad51`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:37:06 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 25 Oct 2022 08:37:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:37:09 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 25 Oct 2022 08:37:30 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 25 Oct 2022 08:37:30 GMT
VOLUME [/spiped]
# Tue, 25 Oct 2022 08:37:30 GMT
WORKDIR /spiped
# Tue, 25 Oct 2022 08:37:30 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 25 Oct 2022 08:37:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 08:37:31 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee0ea61d941875664cd9c05776da1213111ea724a574da76b9b28c4b8f4528c`  
		Last Modified: Tue, 25 Oct 2022 08:37:47 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d4fedc70099c8ce233b3659781b1aed74d64581846c692bb49290d355171b7`  
		Last Modified: Tue, 25 Oct 2022 08:37:47 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16e54acaf0e36c17b7f590939d1cb4ad9b02cb94f13fb00f9f7b86745abe48b`  
		Last Modified: Tue, 25 Oct 2022 08:37:48 GMT  
		Size: 6.0 MB (5998416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56db037880c16bf262262d7370497379e30b11b3fd0281edee6eb60a36552277`  
		Last Modified: Tue, 25 Oct 2022 08:37:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc6a4030f16578da977873b98ae987b7321fb1952c6375b4fce536030b6e5836`  
		Last Modified: Tue, 25 Oct 2022 08:37:47 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; arm variant v5

```console
$ docker pull spiped@sha256:485847df99592ce46f57b80602930020570589bc92a57bcf52c0f12576823a04
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33949464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49edd13d49980a223e5a1a05715139ed281b0a6eb541dade9ed3f270ad4cd0bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 04 Oct 2022 23:49:11 GMT
ADD file:effb9e2e2f8c7539e1a2200d069a2592e8ba20c9d034b5a73fbf173b6987193c in / 
# Tue, 04 Oct 2022 23:49:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:50:43 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 05 Oct 2022 13:50:47 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:50:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 05 Oct 2022 13:51:10 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 05 Oct 2022 13:51:10 GMT
VOLUME [/spiped]
# Wed, 05 Oct 2022 13:51:10 GMT
WORKDIR /spiped
# Wed, 05 Oct 2022 13:51:10 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 05 Oct 2022 13:51:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Oct 2022 13:51:10 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7b9558bbfd8050a8e6af6e60560101c49bd53f81df6fa068419b44d028e465eb`  
		Last Modified: Tue, 04 Oct 2022 23:53:54 GMT  
		Size: 28.9 MB (28918381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:647fed87ad0da4e5831b9907161c1b43ec672b65a95198be6094e7480d581bad`  
		Last Modified: Wed, 05 Oct 2022 13:51:30 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788b6b58021116fa18c299ebb7fd9914e26e5b7845b44641398fe8122b749519`  
		Last Modified: Wed, 05 Oct 2022 13:51:30 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f22319e31ec1e1bba11547c2d32e6210b87ed0647fdf4dd64143be50dc2a30`  
		Last Modified: Wed, 05 Oct 2022 13:51:31 GMT  
		Size: 5.0 MB (5027834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79612caf3d4ffa418788cd8c7a273b28bfcb96d8c83830d22736b42d59752f99`  
		Last Modified: Wed, 05 Oct 2022 13:51:30 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dd3e9d639a80e9684a0fd3b86d20666922b4d42f0448143b7065898439f5d98`  
		Last Modified: Wed, 05 Oct 2022 13:51:30 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; arm variant v7

```console
$ docker pull spiped@sha256:be1ad2cbf3c4749f4f3ad1901e49f28ce59e393f77a5e8bbdc1934e9dc7f06b4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31330089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:615d8374859d2dc36d580e1ebc964ba4372deb8348516c86ea093fc7de8fe4bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 04 Oct 2022 23:58:46 GMT
ADD file:ca1bf27f17594a91224a252bd446f97c3b898210c571f2f26fa2e723d2bf521e in / 
# Tue, 04 Oct 2022 23:58:46 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 05:27:20 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 06 Oct 2022 05:27:24 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 05:27:24 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 06 Oct 2022 05:27:40 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 06 Oct 2022 05:27:40 GMT
VOLUME [/spiped]
# Thu, 06 Oct 2022 05:27:41 GMT
WORKDIR /spiped
# Thu, 06 Oct 2022 05:27:41 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 06 Oct 2022 05:27:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Oct 2022 05:27:41 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2bc64aeac2e429577e497affc8a416d2fc59158aa967f07aced793368e19455f`  
		Last Modified: Wed, 05 Oct 2022 00:05:09 GMT  
		Size: 26.6 MB (26579199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df40850a697b1085bcb37facda4649675c11747ceda87157bf7c9c485c5ce49`  
		Last Modified: Thu, 06 Oct 2022 05:28:13 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a82a9536a373fdbbbf4da2ce7b24365418abbd6ec023ca2e087e071f7168eb3`  
		Last Modified: Thu, 06 Oct 2022 05:28:14 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1716079ee90134175f14061acb4ed8f20fdd29fcc172fe6084aacd233b75d20`  
		Last Modified: Thu, 06 Oct 2022 05:28:14 GMT  
		Size: 4.7 MB (4747637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5db88c4deabc13e23b2452cc73b4731feb1b5fadd585289195eb377197614f6`  
		Last Modified: Thu, 06 Oct 2022 05:28:13 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96859a7277435ad4739e871037f955a296c0e4840e0c8388887ebe08a09da32d`  
		Last Modified: Thu, 06 Oct 2022 05:28:13 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:47adb086ffbc8238cc87a374d5545eb53d0e867848ace36033c5d207ed2868c1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35337515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8f97b2795173eb5045fd9730321b818e919dc60c5ecb739c65b4660fcbe02e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 14:23:07 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 05 Oct 2022 14:23:10 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 14:23:11 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 05 Oct 2022 14:23:29 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 05 Oct 2022 14:23:29 GMT
VOLUME [/spiped]
# Wed, 05 Oct 2022 14:23:30 GMT
WORKDIR /spiped
# Wed, 05 Oct 2022 14:23:32 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 05 Oct 2022 14:23:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Oct 2022 14:23:33 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f301477fc358e3377ddd636b2616c84fcf5124bd247b627567141c87be9f6de1`  
		Last Modified: Wed, 05 Oct 2022 14:24:01 GMT  
		Size: 1.6 KB (1620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9302fdee302af51fa37c04770a7b242e609fcccfd0cfd6ff1f84255fd78fddc2`  
		Last Modified: Wed, 05 Oct 2022 14:24:01 GMT  
		Size: 922.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dae3b94946b96722b37618a3af96e0d185b745edae682b8ce313a98448c0c78`  
		Last Modified: Wed, 05 Oct 2022 14:24:02 GMT  
		Size: 5.3 MB (5270141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae56107eb63a27bf608f2ed332d5a8af7040e6d0a2ea0d71bc4889978c765af4`  
		Last Modified: Wed, 05 Oct 2022 14:24:01 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cdd8dce6303958fb1fd5e08767c354bfb5f383d72f0a746b331d1994526d8dc`  
		Last Modified: Wed, 05 Oct 2022 14:24:01 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; 386

```console
$ docker pull spiped@sha256:28d8bdf2af4f3d895db835d3a8746fd5a569f41f63fb1ecfa5f1f7cfd8c8daa0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40288236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c91f70f71153acda4d046f399b07518ac65cd5150c34e1701fc88987574e1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 04 Oct 2022 23:39:40 GMT
ADD file:a66b7a182260a23fdb8b219600a8b48a5079997715006d9a5324dda11f9d0a7f in / 
# Tue, 04 Oct 2022 23:39:41 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 14:09:19 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 05 Oct 2022 14:09:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 14:09:24 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 05 Oct 2022 14:09:45 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 05 Oct 2022 14:09:45 GMT
VOLUME [/spiped]
# Wed, 05 Oct 2022 14:09:46 GMT
WORKDIR /spiped
# Wed, 05 Oct 2022 14:09:48 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 05 Oct 2022 14:09:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Oct 2022 14:09:49 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:711839e532aa3f129f9cfaa5125d0e379ddefd47f3da44d0674372663dfc6a9b`  
		Last Modified: Tue, 04 Oct 2022 23:45:35 GMT  
		Size: 32.4 MB (32396290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c93d3a5b3eec462b1c6ac59cb81a82a136592cec8dd1e4b01a7ff18f94fb6732`  
		Last Modified: Wed, 05 Oct 2022 14:10:18 GMT  
		Size: 1.6 KB (1610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d16e767b1ff67a46f1f079896d403560a4418176d4f3e8edd740703875ee2bd`  
		Last Modified: Wed, 05 Oct 2022 14:10:18 GMT  
		Size: 921.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c089c61d4bb583ef72de3d4af7e734b4b2c6db1c19ce43112038140b60539d3f`  
		Last Modified: Wed, 05 Oct 2022 14:10:19 GMT  
		Size: 7.9 MB (7888980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d79866b3db5ee7887f80f5f15edc439162fc445b37ebee95562f558be876c30`  
		Last Modified: Wed, 05 Oct 2022 14:10:18 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9ce86fb3faa98b26c3f4b6ca4fe16aba6bb731583f47837c5e19b3624ee014`  
		Last Modified: Wed, 05 Oct 2022 14:10:18 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; mips64le

```console
$ docker pull spiped@sha256:123ccf6bf7870f663a836d6b42768cb49fc6a2a67fe65eab98898130fbacb91a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35348950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5779a3f203e4c018cb40a9c1887dbd52b5852288eebd13cc7d46a2f593510175`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 05 Oct 2022 00:10:26 GMT
ADD file:48da6b2f4e0315e4f502001a00e4b2abb58d553de11a41901ba859a461052bea in / 
# Wed, 05 Oct 2022 00:10:29 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 05:02:44 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 06 Oct 2022 05:02:58 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 05:03:00 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 06 Oct 2022 05:04:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 06 Oct 2022 05:04:30 GMT
VOLUME [/spiped]
# Thu, 06 Oct 2022 05:04:33 GMT
WORKDIR /spiped
# Thu, 06 Oct 2022 05:04:35 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 06 Oct 2022 05:04:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Oct 2022 05:04:40 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3288c6e2e7130a1e313203f049bde0e57a05237441a3cab92c27f9ada139315b`  
		Last Modified: Wed, 05 Oct 2022 00:18:36 GMT  
		Size: 29.6 MB (29640851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fef092d9f7ba63a39ca1cdb3fe82522c963b4831657b64e7d9a20fb87c0d549`  
		Last Modified: Thu, 06 Oct 2022 05:04:58 GMT  
		Size: 1.6 KB (1616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a74beea1ecce269e87b3fa3a679d9c1426eb65ee3a9ca732085c10b4bbfdb95`  
		Last Modified: Thu, 06 Oct 2022 05:04:59 GMT  
		Size: 923.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a1d5db219d406d5845647ae1c960c206474eead0677d57a375a5ddd4cfb2312`  
		Last Modified: Thu, 06 Oct 2022 05:05:04 GMT  
		Size: 5.7 MB (5705121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d137b8d414adcef161b5b3df846629e84076f81350be9239b039a150906325`  
		Last Modified: Thu, 06 Oct 2022 05:04:59 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:712a5107ab173d0c81c031796885923796c56aa6822395457a89160d0b4b62f1`  
		Last Modified: Thu, 06 Oct 2022 05:04:58 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; ppc64le

```console
$ docker pull spiped@sha256:4f8c40985efdc328896edd611d5078c2fc2702512fb7dbf8313b4cae3921a64e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41292975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf972f162417a391365ea02bd55cac90c31e91cea94cde3b1785dc4e07b862c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 25 Oct 2022 03:13:50 GMT
ADD file:1f622759c37363caaa6e6b14831ec9369303345c096f3a018eba66a620b08d26 in / 
# Tue, 25 Oct 2022 03:13:52 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:56:49 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 25 Oct 2022 08:56:55 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:56:55 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 25 Oct 2022 08:57:29 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 25 Oct 2022 08:57:30 GMT
VOLUME [/spiped]
# Tue, 25 Oct 2022 08:57:30 GMT
WORKDIR /spiped
# Tue, 25 Oct 2022 08:57:31 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 25 Oct 2022 08:57:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 08:57:31 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6d95b62526dd55d76e7ec2bd4015a327b5bb37161f2ffe8bc2bb08d34a677716`  
		Last Modified: Tue, 25 Oct 2022 03:19:31 GMT  
		Size: 35.3 MB (35290086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e72bcd36564076a1be5059203c37728b7870c126ac7fe06f996ccf16f91855f`  
		Last Modified: Tue, 25 Oct 2022 08:58:00 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68fe46109a02177cec27f93ac157701520a7bb241f376b25305d5d3066a0e344`  
		Last Modified: Tue, 25 Oct 2022 08:58:00 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c94efcdf110ae18400e5415ff3d6b9e3922164053912c50c55ba08357401ef6`  
		Last Modified: Tue, 25 Oct 2022 08:58:02 GMT  
		Size: 6.0 MB (5999635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5edf8c734f5fda4c57a8d654d651fd56402b97e7bb5e2ebb9765410fc9b4ebbf`  
		Last Modified: Tue, 25 Oct 2022 08:58:00 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93111314cb3af703e6ce8c0a09396a4c6e0294ef4a359f1946bbaf70c6ab0b50`  
		Last Modified: Tue, 25 Oct 2022 08:58:00 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1` - linux; s390x

```console
$ docker pull spiped@sha256:d248ba3ec10b15e146e806977482172d735af6a76ebdaae3a2967a79fe3bc883
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34841904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d9b35607854f37e824aa0f514dec480476acd2e766c86c626aa4ab84e3e2daf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 25 Oct 2022 01:14:42 GMT
ADD file:1bb8efa7f80e494b9d2831490a7e74810350c1f9ee2d100596d2e1cb4c62f529 in / 
# Tue, 25 Oct 2022 01:14:44 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:17:40 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 25 Oct 2022 07:17:43 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:17:43 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 25 Oct 2022 07:17:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 25 Oct 2022 07:17:57 GMT
VOLUME [/spiped]
# Tue, 25 Oct 2022 07:17:57 GMT
WORKDIR /spiped
# Tue, 25 Oct 2022 07:17:57 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 25 Oct 2022 07:17:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 07:17:58 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:abc14eb2518761d53b91fc564a31b657914f96b531f99a74ac8268f0717b007e`  
		Last Modified: Tue, 25 Oct 2022 01:19:01 GMT  
		Size: 29.7 MB (29650722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:631fad7c1185ed0f5e182395eabf9dc221258ee09f822bb730b461cea4dc1e91`  
		Last Modified: Tue, 25 Oct 2022 07:18:32 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e288a715b6a67137c6dc2b11d4a1911512db2b794cec1c6e919ee3561176fa3a`  
		Last Modified: Tue, 25 Oct 2022 07:18:32 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65245ecca59da4154a971e90aee7b353bc9ed35f548d478ec6cb54c37b92c513`  
		Last Modified: Tue, 25 Oct 2022 07:18:33 GMT  
		Size: 5.2 MB (5187929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd3eec290beab4e4d33c1f802d534913b85ecef8963ecda079eef7cf0802983`  
		Last Modified: Tue, 25 Oct 2022 07:18:32 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27850183009b851f569533d6a829cf12d40c9fae07dd08ecd8856cc8ff5b6235`  
		Last Modified: Tue, 25 Oct 2022 07:18:32 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1-alpine`

```console
$ docker pull spiped@sha256:fd3dbe6f07d6ad025f0b57bdb6bccced1f2d4ed52ed5f2e95bd567ca1213858b
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
$ docker pull spiped@sha256:83b7108c070944539ec82ed9729e69afa1a5ad91eed9163efc95bcd8a3455efa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3036717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8704d25dde580015332a57e745db366aa241d3d99f8949b2c12e3f7c9ae8606`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 04:17:54 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 07 Oct 2022 04:17:55 GMT
RUN apk add --no-cache libssl1.1
# Fri, 07 Oct 2022 04:17:56 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 07 Oct 2022 04:18:06 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 07 Oct 2022 04:18:06 GMT
VOLUME [/spiped]
# Fri, 07 Oct 2022 04:18:06 GMT
WORKDIR /spiped
# Fri, 07 Oct 2022 04:18:06 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 07 Oct 2022 04:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Oct 2022 04:18:07 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:163365ead583145f60498102a9de8f3de170409f2ae8cecf962cf3ab512bb7b6`  
		Last Modified: Fri, 07 Oct 2022 04:18:24 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ebb86b08f67f6638bc3391b020d7e3c07ac692076e469c99ba197a3dc6180d`  
		Last Modified: Fri, 07 Oct 2022 04:18:24 GMT  
		Size: 7.7 KB (7743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0d696472090a4ef1527e0ceea219db2e5ca85866d16132e7f6a560e73c84d3`  
		Last Modified: Fri, 07 Oct 2022 04:18:24 GMT  
		Size: 221.2 KB (221183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ad76fb7ed47c485b828ec98e173c844febdb11324b807d8befb613a1c8f4e06`  
		Last Modified: Fri, 07 Oct 2022 04:18:24 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598391454db346484a0ec6968962627ae778f5ab04cf800247c9dd1ce7ab6878`  
		Last Modified: Fri, 07 Oct 2022 04:18:24 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:b551174a0a1d06027c49d92df5bfe5c2a7b4fbbd0eddc4befe5cd38bb470c37e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2829352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:600282cc6da8413cdcb193cc95ceb823009ccf91df6453209016ff2117ee2ea1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Sat, 08 Oct 2022 03:57:10 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 08 Oct 2022 03:57:11 GMT
RUN apk add --no-cache libssl1.1
# Sat, 08 Oct 2022 03:57:11 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 08 Oct 2022 03:57:20 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 08 Oct 2022 03:57:20 GMT
VOLUME [/spiped]
# Sat, 08 Oct 2022 03:57:20 GMT
WORKDIR /spiped
# Sat, 08 Oct 2022 03:57:20 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 08 Oct 2022 03:57:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 08 Oct 2022 03:57:20 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d22ef9a58b62ce73c21d40d894c34b6d8e3272bf2f543ed188286073c4424fc`  
		Last Modified: Sat, 08 Oct 2022 03:57:39 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62e41f642c74a0d9462ab3129be57e8d46bbce2ba02bd722a9c728e40688eb1e`  
		Last Modified: Sat, 08 Oct 2022 03:57:40 GMT  
		Size: 7.7 KB (7738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca6ab15f65d41991ef7df3456f45af9c8305074e870dc4f144bc85827af4027`  
		Last Modified: Sat, 08 Oct 2022 03:57:39 GMT  
		Size: 205.9 KB (205906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b3bbca61a66ee3759c7812bb413899b9d1c91b1d0b52d7c5566318da8a17f9`  
		Last Modified: Sat, 08 Oct 2022 03:57:39 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e86011e4d6eb7c1e4099a1c1683bf382adfd1ffc4a449a341ceddefc616cf3`  
		Last Modified: Sat, 08 Oct 2022 03:57:39 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:aa33c5a5d1b9aecc0ce4fe51343713ec1a58609fdb7d407f860cbfe5999b2365
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2626104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:054c7036b8c1b0ae94ff78d5b840bb90f42e59c57592b10023f0e4894e38cb79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:44 GMT
ADD file:75521fe16320b193092588f6f31052c85e736965ceb11673de18bd14965a45e6 in / 
# Tue, 09 Aug 2022 16:57:44 GMT
CMD ["/bin/sh"]
# Sat, 08 Oct 2022 04:01:24 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 08 Oct 2022 04:01:25 GMT
RUN apk add --no-cache libssl1.1
# Sat, 08 Oct 2022 04:01:25 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 08 Oct 2022 04:01:33 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 08 Oct 2022 04:01:33 GMT
VOLUME [/spiped]
# Sat, 08 Oct 2022 04:01:34 GMT
WORKDIR /spiped
# Sat, 08 Oct 2022 04:01:34 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 08 Oct 2022 04:01:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 08 Oct 2022 04:01:34 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c6556b3b6858c6fa1e328377cc2c4becdc9cd1bc3e7302aa7299936522cf93ba`  
		Last Modified: Tue, 09 Aug 2022 16:58:55 GMT  
		Size: 2.4 MB (2417065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f672e653be912401f24b90bba8ef9e28fbd027835c1d089b2d3fe9ab9203fc2`  
		Last Modified: Sat, 08 Oct 2022 04:02:07 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db927a95afdcc25384fd927be64e72535b615a678cfefa1c481f72c89a421d51`  
		Last Modified: Sat, 08 Oct 2022 04:02:07 GMT  
		Size: 7.7 KB (7736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7603e8707a28d96ef5c46ca4bb4263d32478fed3f18c6c5e799a126f4c8d64b4`  
		Last Modified: Sat, 08 Oct 2022 04:02:08 GMT  
		Size: 199.6 KB (199558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8453aa2dcfbeaef1a8acf8732c8db652f357b7c50d9094e343cd9f59e37c3664`  
		Last Modified: Sat, 08 Oct 2022 04:02:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b74b3d42386a46fe11be9e8ce6a933569a8712b0d20647a2e694473c22f61f2d`  
		Last Modified: Sat, 08 Oct 2022 04:02:07 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:e5b68da77cb9db28f4d5f80f8220af5803599cf23e9cce57f4b25405f32853f7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2931324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:681bb24795641aec826f9fcf710d73e0f839c1d83231b15da58521db752ad663`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 07:37:40 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 07 Oct 2022 07:37:41 GMT
RUN apk add --no-cache libssl1.1
# Fri, 07 Oct 2022 07:37:42 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 07 Oct 2022 07:37:53 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 07 Oct 2022 07:37:54 GMT
VOLUME [/spiped]
# Fri, 07 Oct 2022 07:37:55 GMT
WORKDIR /spiped
# Fri, 07 Oct 2022 07:37:57 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 07 Oct 2022 07:37:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Oct 2022 07:37:58 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7901c95a1447d090815ba8f9d5afa5abbdd9cdd431c948e1cac143e5cdacea73`  
		Last Modified: Fri, 07 Oct 2022 07:38:25 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081551fa64d93cc14b0e29df21933895b17862a013e29ac667046d4ea8db0b14`  
		Last Modified: Fri, 07 Oct 2022 07:38:25 GMT  
		Size: 7.7 KB (7713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94947ded225af3a68fa2d3e89d286cd5424a073fd1597c34b8fd81fd125c0684`  
		Last Modified: Fri, 07 Oct 2022 07:38:26 GMT  
		Size: 214.3 KB (214266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c443d577082fa11b6c6c4af1a7cf3bcc77598280a04be75044d38d529083f988`  
		Last Modified: Fri, 07 Oct 2022 07:38:25 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141acab92005d5c00bc4f4d6679742fb826be835ac933c9bc5495eb8256eb7e6`  
		Last Modified: Fri, 07 Oct 2022 07:38:25 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; 386

```console
$ docker pull spiped@sha256:6423a7f534f20d885a95067600857ce072688766c2ffa6bb9010fc6d7f7231ed
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3047843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c7719409551ce46332256dc9374bbbe5ebad7eebb18d4f5c3e768b35cabfc11`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:39 GMT
ADD file:b828bc14bc5ff03c8f7310fe0aed6ac5df19a393622d5d1d779a523234d07c0a in / 
# Tue, 09 Aug 2022 17:38:39 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 02:06:26 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 07 Oct 2022 02:06:27 GMT
RUN apk add --no-cache libssl1.1
# Fri, 07 Oct 2022 02:06:28 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 07 Oct 2022 02:06:40 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 07 Oct 2022 02:06:41 GMT
VOLUME [/spiped]
# Fri, 07 Oct 2022 02:06:42 GMT
WORKDIR /spiped
# Fri, 07 Oct 2022 02:06:44 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 07 Oct 2022 02:06:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Oct 2022 02:06:45 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6c0d3b419d848ea31ca748254611d5d5ce3b76e3d7bba520fd87400fbb75f3b9`  
		Last Modified: Tue, 09 Aug 2022 17:39:33 GMT  
		Size: 2.8 MB (2807121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982fdd64c4ca701476bab0ba1a71f21a0405e2b79db064444f6f738b3bdb2683`  
		Last Modified: Fri, 07 Oct 2022 02:07:15 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c854898389b43dbb9cdd413e814a0799ae7a3efd037dc62a2ab580f223d09dd9`  
		Last Modified: Fri, 07 Oct 2022 02:07:15 GMT  
		Size: 7.7 KB (7713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8e6b40665d81d34cbfaf2714f35b8921a3441a7458b416a69479dda6fded73`  
		Last Modified: Fri, 07 Oct 2022 02:07:15 GMT  
		Size: 231.3 KB (231328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e75809d30c75c96ac8571a0aad6037398080e8464c1fe900186204d14ed97ee5`  
		Last Modified: Fri, 07 Oct 2022 02:07:15 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e7f4311d12b79d5b5ed076ae0276fdc41d636eb2425cce1969ffbbecfaa48f`  
		Last Modified: Fri, 07 Oct 2022 02:07:15 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:23f7c4e2894e2b69ec8f99ad3e5bfc9eb384bfb0867a580c0a14296e9fda6808
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3033056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea36cd4aae1294ce2738686854cda02fd8af9cb087470d67f42ae503ef53dbe2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:17:09 GMT
ADD file:66b351666e41834033d334aeb3dc6998dea77aa22e8e254028c923fee67a41a8 in / 
# Tue, 09 Aug 2022 17:17:10 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 07:36:49 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 07 Oct 2022 07:36:51 GMT
RUN apk add --no-cache libssl1.1
# Fri, 07 Oct 2022 07:36:51 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 07 Oct 2022 07:37:05 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 07 Oct 2022 07:37:05 GMT
VOLUME [/spiped]
# Fri, 07 Oct 2022 07:37:06 GMT
WORKDIR /spiped
# Fri, 07 Oct 2022 07:37:06 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 07 Oct 2022 07:37:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Oct 2022 07:37:07 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c79e5d1a8c89b87020a754c8a5c8370faaa37bfb5bca1d8af66770d522ef1caf`  
		Last Modified: Tue, 09 Aug 2022 17:18:26 GMT  
		Size: 2.8 MB (2803320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6730e71fd53d14fc64b230b13be77ded2ae164bb8e0b21103c39d2320db3c383`  
		Last Modified: Fri, 07 Oct 2022 07:37:35 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a98530f24008a28aeac69a847b3e388d2db70cb4ec34485f3b180da38729d98`  
		Last Modified: Fri, 07 Oct 2022 07:37:35 GMT  
		Size: 7.7 KB (7744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:795c3cac559b59708bf223d2fd843ed2dfd7083c5bb42e2bdc5459c77bb508bf`  
		Last Modified: Fri, 07 Oct 2022 07:37:35 GMT  
		Size: 220.3 KB (220251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8832c249dd749cdd6d7eea870aa3a8ee137af08153d1b9a6cd50600958066aa`  
		Last Modified: Fri, 07 Oct 2022 07:37:35 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb4f5e799656197f8bfd5fad27d5caf0993b2a631ac187a703a21cf24dcc448`  
		Last Modified: Fri, 07 Oct 2022 07:37:35 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:e61ee0f946e5685eccc381e0c2947c6d1c7e028e9bbdc3073b69aa42393ce835
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2808515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18ab110d81e2e45f8012dd604cb9c6384aa690b85b579a296c5f4d7f81f7c50f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:41:46 GMT
ADD file:b43a065471bc4711415d3c67cd5b6559b0c48ee7ffe9761530477cf457a6dc34 in / 
# Tue, 09 Aug 2022 17:41:46 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 09:55:45 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 07 Oct 2022 09:55:47 GMT
RUN apk add --no-cache libssl1.1
# Fri, 07 Oct 2022 09:55:48 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 07 Oct 2022 09:55:58 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 07 Oct 2022 09:55:58 GMT
VOLUME [/spiped]
# Fri, 07 Oct 2022 09:55:59 GMT
WORKDIR /spiped
# Fri, 07 Oct 2022 09:56:00 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 07 Oct 2022 09:56:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Oct 2022 09:56:01 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:790c84f1f3409eab952345157df7fa804ba6b5f06d4ceb6f2dfa3c6de2064397`  
		Last Modified: Tue, 09 Aug 2022 17:42:45 GMT  
		Size: 2.6 MB (2590597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f248f8c884e8c56eafd62d4fd705bc4ea4e1b8f47c4adc22f91a07918fcbfe`  
		Last Modified: Fri, 07 Oct 2022 09:56:33 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b4454005be5f38ee0e54328e844699ab2a19fe01659f533914631aeea7d261`  
		Last Modified: Fri, 07 Oct 2022 09:56:34 GMT  
		Size: 7.7 KB (7745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8e9ba51e735f2b9db573be0890282a90d83d48ced508f0faf9252fcaa14778`  
		Last Modified: Fri, 07 Oct 2022 09:56:33 GMT  
		Size: 208.4 KB (208433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aad928e923cf65a5caa952da37a36601f59692024a6c316a0696524d7e16e6f`  
		Last Modified: Fri, 07 Oct 2022 09:56:34 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a43970caf685b3dd35775e85038478cdef00343f53b01cf826099af4248696`  
		Last Modified: Fri, 07 Oct 2022 09:56:33 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6`

```console
$ docker pull spiped@sha256:baf6bcaed017648a642add6562bf6e5de15eabf4be46737afba352c1fdd36ea0
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
$ docker pull spiped@sha256:907ddd7d8a3f64e3b9587d8bd37803871c7e0301273fd134fff16a4601b764b6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 MB (37421712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aebdf10111eb9350e84131fa07f10b1e016fae20fb35a2ef3054aac040d9ad51`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:37:06 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 25 Oct 2022 08:37:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:37:09 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 25 Oct 2022 08:37:30 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 25 Oct 2022 08:37:30 GMT
VOLUME [/spiped]
# Tue, 25 Oct 2022 08:37:30 GMT
WORKDIR /spiped
# Tue, 25 Oct 2022 08:37:30 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 25 Oct 2022 08:37:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 08:37:31 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee0ea61d941875664cd9c05776da1213111ea724a574da76b9b28c4b8f4528c`  
		Last Modified: Tue, 25 Oct 2022 08:37:47 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d4fedc70099c8ce233b3659781b1aed74d64581846c692bb49290d355171b7`  
		Last Modified: Tue, 25 Oct 2022 08:37:47 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16e54acaf0e36c17b7f590939d1cb4ad9b02cb94f13fb00f9f7b86745abe48b`  
		Last Modified: Tue, 25 Oct 2022 08:37:48 GMT  
		Size: 6.0 MB (5998416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56db037880c16bf262262d7370497379e30b11b3fd0281edee6eb60a36552277`  
		Last Modified: Tue, 25 Oct 2022 08:37:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc6a4030f16578da977873b98ae987b7321fb1952c6375b4fce536030b6e5836`  
		Last Modified: Tue, 25 Oct 2022 08:37:47 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; arm variant v5

```console
$ docker pull spiped@sha256:485847df99592ce46f57b80602930020570589bc92a57bcf52c0f12576823a04
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33949464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49edd13d49980a223e5a1a05715139ed281b0a6eb541dade9ed3f270ad4cd0bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 04 Oct 2022 23:49:11 GMT
ADD file:effb9e2e2f8c7539e1a2200d069a2592e8ba20c9d034b5a73fbf173b6987193c in / 
# Tue, 04 Oct 2022 23:49:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:50:43 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 05 Oct 2022 13:50:47 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:50:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 05 Oct 2022 13:51:10 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 05 Oct 2022 13:51:10 GMT
VOLUME [/spiped]
# Wed, 05 Oct 2022 13:51:10 GMT
WORKDIR /spiped
# Wed, 05 Oct 2022 13:51:10 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 05 Oct 2022 13:51:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Oct 2022 13:51:10 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7b9558bbfd8050a8e6af6e60560101c49bd53f81df6fa068419b44d028e465eb`  
		Last Modified: Tue, 04 Oct 2022 23:53:54 GMT  
		Size: 28.9 MB (28918381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:647fed87ad0da4e5831b9907161c1b43ec672b65a95198be6094e7480d581bad`  
		Last Modified: Wed, 05 Oct 2022 13:51:30 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788b6b58021116fa18c299ebb7fd9914e26e5b7845b44641398fe8122b749519`  
		Last Modified: Wed, 05 Oct 2022 13:51:30 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f22319e31ec1e1bba11547c2d32e6210b87ed0647fdf4dd64143be50dc2a30`  
		Last Modified: Wed, 05 Oct 2022 13:51:31 GMT  
		Size: 5.0 MB (5027834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79612caf3d4ffa418788cd8c7a273b28bfcb96d8c83830d22736b42d59752f99`  
		Last Modified: Wed, 05 Oct 2022 13:51:30 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dd3e9d639a80e9684a0fd3b86d20666922b4d42f0448143b7065898439f5d98`  
		Last Modified: Wed, 05 Oct 2022 13:51:30 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; arm variant v7

```console
$ docker pull spiped@sha256:be1ad2cbf3c4749f4f3ad1901e49f28ce59e393f77a5e8bbdc1934e9dc7f06b4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31330089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:615d8374859d2dc36d580e1ebc964ba4372deb8348516c86ea093fc7de8fe4bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 04 Oct 2022 23:58:46 GMT
ADD file:ca1bf27f17594a91224a252bd446f97c3b898210c571f2f26fa2e723d2bf521e in / 
# Tue, 04 Oct 2022 23:58:46 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 05:27:20 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 06 Oct 2022 05:27:24 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 05:27:24 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 06 Oct 2022 05:27:40 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 06 Oct 2022 05:27:40 GMT
VOLUME [/spiped]
# Thu, 06 Oct 2022 05:27:41 GMT
WORKDIR /spiped
# Thu, 06 Oct 2022 05:27:41 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 06 Oct 2022 05:27:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Oct 2022 05:27:41 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2bc64aeac2e429577e497affc8a416d2fc59158aa967f07aced793368e19455f`  
		Last Modified: Wed, 05 Oct 2022 00:05:09 GMT  
		Size: 26.6 MB (26579199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df40850a697b1085bcb37facda4649675c11747ceda87157bf7c9c485c5ce49`  
		Last Modified: Thu, 06 Oct 2022 05:28:13 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a82a9536a373fdbbbf4da2ce7b24365418abbd6ec023ca2e087e071f7168eb3`  
		Last Modified: Thu, 06 Oct 2022 05:28:14 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1716079ee90134175f14061acb4ed8f20fdd29fcc172fe6084aacd233b75d20`  
		Last Modified: Thu, 06 Oct 2022 05:28:14 GMT  
		Size: 4.7 MB (4747637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5db88c4deabc13e23b2452cc73b4731feb1b5fadd585289195eb377197614f6`  
		Last Modified: Thu, 06 Oct 2022 05:28:13 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96859a7277435ad4739e871037f955a296c0e4840e0c8388887ebe08a09da32d`  
		Last Modified: Thu, 06 Oct 2022 05:28:13 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:47adb086ffbc8238cc87a374d5545eb53d0e867848ace36033c5d207ed2868c1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35337515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8f97b2795173eb5045fd9730321b818e919dc60c5ecb739c65b4660fcbe02e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 14:23:07 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 05 Oct 2022 14:23:10 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 14:23:11 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 05 Oct 2022 14:23:29 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 05 Oct 2022 14:23:29 GMT
VOLUME [/spiped]
# Wed, 05 Oct 2022 14:23:30 GMT
WORKDIR /spiped
# Wed, 05 Oct 2022 14:23:32 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 05 Oct 2022 14:23:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Oct 2022 14:23:33 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f301477fc358e3377ddd636b2616c84fcf5124bd247b627567141c87be9f6de1`  
		Last Modified: Wed, 05 Oct 2022 14:24:01 GMT  
		Size: 1.6 KB (1620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9302fdee302af51fa37c04770a7b242e609fcccfd0cfd6ff1f84255fd78fddc2`  
		Last Modified: Wed, 05 Oct 2022 14:24:01 GMT  
		Size: 922.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dae3b94946b96722b37618a3af96e0d185b745edae682b8ce313a98448c0c78`  
		Last Modified: Wed, 05 Oct 2022 14:24:02 GMT  
		Size: 5.3 MB (5270141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae56107eb63a27bf608f2ed332d5a8af7040e6d0a2ea0d71bc4889978c765af4`  
		Last Modified: Wed, 05 Oct 2022 14:24:01 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cdd8dce6303958fb1fd5e08767c354bfb5f383d72f0a746b331d1994526d8dc`  
		Last Modified: Wed, 05 Oct 2022 14:24:01 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; 386

```console
$ docker pull spiped@sha256:28d8bdf2af4f3d895db835d3a8746fd5a569f41f63fb1ecfa5f1f7cfd8c8daa0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40288236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c91f70f71153acda4d046f399b07518ac65cd5150c34e1701fc88987574e1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 04 Oct 2022 23:39:40 GMT
ADD file:a66b7a182260a23fdb8b219600a8b48a5079997715006d9a5324dda11f9d0a7f in / 
# Tue, 04 Oct 2022 23:39:41 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 14:09:19 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 05 Oct 2022 14:09:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 14:09:24 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 05 Oct 2022 14:09:45 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 05 Oct 2022 14:09:45 GMT
VOLUME [/spiped]
# Wed, 05 Oct 2022 14:09:46 GMT
WORKDIR /spiped
# Wed, 05 Oct 2022 14:09:48 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 05 Oct 2022 14:09:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Oct 2022 14:09:49 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:711839e532aa3f129f9cfaa5125d0e379ddefd47f3da44d0674372663dfc6a9b`  
		Last Modified: Tue, 04 Oct 2022 23:45:35 GMT  
		Size: 32.4 MB (32396290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c93d3a5b3eec462b1c6ac59cb81a82a136592cec8dd1e4b01a7ff18f94fb6732`  
		Last Modified: Wed, 05 Oct 2022 14:10:18 GMT  
		Size: 1.6 KB (1610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d16e767b1ff67a46f1f079896d403560a4418176d4f3e8edd740703875ee2bd`  
		Last Modified: Wed, 05 Oct 2022 14:10:18 GMT  
		Size: 921.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c089c61d4bb583ef72de3d4af7e734b4b2c6db1c19ce43112038140b60539d3f`  
		Last Modified: Wed, 05 Oct 2022 14:10:19 GMT  
		Size: 7.9 MB (7888980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d79866b3db5ee7887f80f5f15edc439162fc445b37ebee95562f558be876c30`  
		Last Modified: Wed, 05 Oct 2022 14:10:18 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9ce86fb3faa98b26c3f4b6ca4fe16aba6bb731583f47837c5e19b3624ee014`  
		Last Modified: Wed, 05 Oct 2022 14:10:18 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; mips64le

```console
$ docker pull spiped@sha256:123ccf6bf7870f663a836d6b42768cb49fc6a2a67fe65eab98898130fbacb91a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35348950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5779a3f203e4c018cb40a9c1887dbd52b5852288eebd13cc7d46a2f593510175`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 05 Oct 2022 00:10:26 GMT
ADD file:48da6b2f4e0315e4f502001a00e4b2abb58d553de11a41901ba859a461052bea in / 
# Wed, 05 Oct 2022 00:10:29 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 05:02:44 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 06 Oct 2022 05:02:58 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 05:03:00 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 06 Oct 2022 05:04:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 06 Oct 2022 05:04:30 GMT
VOLUME [/spiped]
# Thu, 06 Oct 2022 05:04:33 GMT
WORKDIR /spiped
# Thu, 06 Oct 2022 05:04:35 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 06 Oct 2022 05:04:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Oct 2022 05:04:40 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3288c6e2e7130a1e313203f049bde0e57a05237441a3cab92c27f9ada139315b`  
		Last Modified: Wed, 05 Oct 2022 00:18:36 GMT  
		Size: 29.6 MB (29640851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fef092d9f7ba63a39ca1cdb3fe82522c963b4831657b64e7d9a20fb87c0d549`  
		Last Modified: Thu, 06 Oct 2022 05:04:58 GMT  
		Size: 1.6 KB (1616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a74beea1ecce269e87b3fa3a679d9c1426eb65ee3a9ca732085c10b4bbfdb95`  
		Last Modified: Thu, 06 Oct 2022 05:04:59 GMT  
		Size: 923.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a1d5db219d406d5845647ae1c960c206474eead0677d57a375a5ddd4cfb2312`  
		Last Modified: Thu, 06 Oct 2022 05:05:04 GMT  
		Size: 5.7 MB (5705121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d137b8d414adcef161b5b3df846629e84076f81350be9239b039a150906325`  
		Last Modified: Thu, 06 Oct 2022 05:04:59 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:712a5107ab173d0c81c031796885923796c56aa6822395457a89160d0b4b62f1`  
		Last Modified: Thu, 06 Oct 2022 05:04:58 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; ppc64le

```console
$ docker pull spiped@sha256:4f8c40985efdc328896edd611d5078c2fc2702512fb7dbf8313b4cae3921a64e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41292975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf972f162417a391365ea02bd55cac90c31e91cea94cde3b1785dc4e07b862c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 25 Oct 2022 03:13:50 GMT
ADD file:1f622759c37363caaa6e6b14831ec9369303345c096f3a018eba66a620b08d26 in / 
# Tue, 25 Oct 2022 03:13:52 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:56:49 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 25 Oct 2022 08:56:55 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:56:55 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 25 Oct 2022 08:57:29 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 25 Oct 2022 08:57:30 GMT
VOLUME [/spiped]
# Tue, 25 Oct 2022 08:57:30 GMT
WORKDIR /spiped
# Tue, 25 Oct 2022 08:57:31 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 25 Oct 2022 08:57:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 08:57:31 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6d95b62526dd55d76e7ec2bd4015a327b5bb37161f2ffe8bc2bb08d34a677716`  
		Last Modified: Tue, 25 Oct 2022 03:19:31 GMT  
		Size: 35.3 MB (35290086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e72bcd36564076a1be5059203c37728b7870c126ac7fe06f996ccf16f91855f`  
		Last Modified: Tue, 25 Oct 2022 08:58:00 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68fe46109a02177cec27f93ac157701520a7bb241f376b25305d5d3066a0e344`  
		Last Modified: Tue, 25 Oct 2022 08:58:00 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c94efcdf110ae18400e5415ff3d6b9e3922164053912c50c55ba08357401ef6`  
		Last Modified: Tue, 25 Oct 2022 08:58:02 GMT  
		Size: 6.0 MB (5999635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5edf8c734f5fda4c57a8d654d651fd56402b97e7bb5e2ebb9765410fc9b4ebbf`  
		Last Modified: Tue, 25 Oct 2022 08:58:00 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93111314cb3af703e6ce8c0a09396a4c6e0294ef4a359f1946bbaf70c6ab0b50`  
		Last Modified: Tue, 25 Oct 2022 08:58:00 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6` - linux; s390x

```console
$ docker pull spiped@sha256:d248ba3ec10b15e146e806977482172d735af6a76ebdaae3a2967a79fe3bc883
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34841904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d9b35607854f37e824aa0f514dec480476acd2e766c86c626aa4ab84e3e2daf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 25 Oct 2022 01:14:42 GMT
ADD file:1bb8efa7f80e494b9d2831490a7e74810350c1f9ee2d100596d2e1cb4c62f529 in / 
# Tue, 25 Oct 2022 01:14:44 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:17:40 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 25 Oct 2022 07:17:43 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:17:43 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 25 Oct 2022 07:17:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 25 Oct 2022 07:17:57 GMT
VOLUME [/spiped]
# Tue, 25 Oct 2022 07:17:57 GMT
WORKDIR /spiped
# Tue, 25 Oct 2022 07:17:57 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 25 Oct 2022 07:17:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 07:17:58 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:abc14eb2518761d53b91fc564a31b657914f96b531f99a74ac8268f0717b007e`  
		Last Modified: Tue, 25 Oct 2022 01:19:01 GMT  
		Size: 29.7 MB (29650722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:631fad7c1185ed0f5e182395eabf9dc221258ee09f822bb730b461cea4dc1e91`  
		Last Modified: Tue, 25 Oct 2022 07:18:32 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e288a715b6a67137c6dc2b11d4a1911512db2b794cec1c6e919ee3561176fa3a`  
		Last Modified: Tue, 25 Oct 2022 07:18:32 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65245ecca59da4154a971e90aee7b353bc9ed35f548d478ec6cb54c37b92c513`  
		Last Modified: Tue, 25 Oct 2022 07:18:33 GMT  
		Size: 5.2 MB (5187929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd3eec290beab4e4d33c1f802d534913b85ecef8963ecda079eef7cf0802983`  
		Last Modified: Tue, 25 Oct 2022 07:18:32 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27850183009b851f569533d6a829cf12d40c9fae07dd08ecd8856cc8ff5b6235`  
		Last Modified: Tue, 25 Oct 2022 07:18:32 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6-alpine`

```console
$ docker pull spiped@sha256:fd3dbe6f07d6ad025f0b57bdb6bccced1f2d4ed52ed5f2e95bd567ca1213858b
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
$ docker pull spiped@sha256:83b7108c070944539ec82ed9729e69afa1a5ad91eed9163efc95bcd8a3455efa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3036717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8704d25dde580015332a57e745db366aa241d3d99f8949b2c12e3f7c9ae8606`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 04:17:54 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 07 Oct 2022 04:17:55 GMT
RUN apk add --no-cache libssl1.1
# Fri, 07 Oct 2022 04:17:56 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 07 Oct 2022 04:18:06 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 07 Oct 2022 04:18:06 GMT
VOLUME [/spiped]
# Fri, 07 Oct 2022 04:18:06 GMT
WORKDIR /spiped
# Fri, 07 Oct 2022 04:18:06 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 07 Oct 2022 04:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Oct 2022 04:18:07 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:163365ead583145f60498102a9de8f3de170409f2ae8cecf962cf3ab512bb7b6`  
		Last Modified: Fri, 07 Oct 2022 04:18:24 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ebb86b08f67f6638bc3391b020d7e3c07ac692076e469c99ba197a3dc6180d`  
		Last Modified: Fri, 07 Oct 2022 04:18:24 GMT  
		Size: 7.7 KB (7743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0d696472090a4ef1527e0ceea219db2e5ca85866d16132e7f6a560e73c84d3`  
		Last Modified: Fri, 07 Oct 2022 04:18:24 GMT  
		Size: 221.2 KB (221183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ad76fb7ed47c485b828ec98e173c844febdb11324b807d8befb613a1c8f4e06`  
		Last Modified: Fri, 07 Oct 2022 04:18:24 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598391454db346484a0ec6968962627ae778f5ab04cf800247c9dd1ce7ab6878`  
		Last Modified: Fri, 07 Oct 2022 04:18:24 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:b551174a0a1d06027c49d92df5bfe5c2a7b4fbbd0eddc4befe5cd38bb470c37e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2829352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:600282cc6da8413cdcb193cc95ceb823009ccf91df6453209016ff2117ee2ea1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Sat, 08 Oct 2022 03:57:10 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 08 Oct 2022 03:57:11 GMT
RUN apk add --no-cache libssl1.1
# Sat, 08 Oct 2022 03:57:11 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 08 Oct 2022 03:57:20 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 08 Oct 2022 03:57:20 GMT
VOLUME [/spiped]
# Sat, 08 Oct 2022 03:57:20 GMT
WORKDIR /spiped
# Sat, 08 Oct 2022 03:57:20 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 08 Oct 2022 03:57:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 08 Oct 2022 03:57:20 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d22ef9a58b62ce73c21d40d894c34b6d8e3272bf2f543ed188286073c4424fc`  
		Last Modified: Sat, 08 Oct 2022 03:57:39 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62e41f642c74a0d9462ab3129be57e8d46bbce2ba02bd722a9c728e40688eb1e`  
		Last Modified: Sat, 08 Oct 2022 03:57:40 GMT  
		Size: 7.7 KB (7738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca6ab15f65d41991ef7df3456f45af9c8305074e870dc4f144bc85827af4027`  
		Last Modified: Sat, 08 Oct 2022 03:57:39 GMT  
		Size: 205.9 KB (205906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b3bbca61a66ee3759c7812bb413899b9d1c91b1d0b52d7c5566318da8a17f9`  
		Last Modified: Sat, 08 Oct 2022 03:57:39 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e86011e4d6eb7c1e4099a1c1683bf382adfd1ffc4a449a341ceddefc616cf3`  
		Last Modified: Sat, 08 Oct 2022 03:57:39 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:aa33c5a5d1b9aecc0ce4fe51343713ec1a58609fdb7d407f860cbfe5999b2365
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2626104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:054c7036b8c1b0ae94ff78d5b840bb90f42e59c57592b10023f0e4894e38cb79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:44 GMT
ADD file:75521fe16320b193092588f6f31052c85e736965ceb11673de18bd14965a45e6 in / 
# Tue, 09 Aug 2022 16:57:44 GMT
CMD ["/bin/sh"]
# Sat, 08 Oct 2022 04:01:24 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 08 Oct 2022 04:01:25 GMT
RUN apk add --no-cache libssl1.1
# Sat, 08 Oct 2022 04:01:25 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 08 Oct 2022 04:01:33 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 08 Oct 2022 04:01:33 GMT
VOLUME [/spiped]
# Sat, 08 Oct 2022 04:01:34 GMT
WORKDIR /spiped
# Sat, 08 Oct 2022 04:01:34 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 08 Oct 2022 04:01:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 08 Oct 2022 04:01:34 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c6556b3b6858c6fa1e328377cc2c4becdc9cd1bc3e7302aa7299936522cf93ba`  
		Last Modified: Tue, 09 Aug 2022 16:58:55 GMT  
		Size: 2.4 MB (2417065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f672e653be912401f24b90bba8ef9e28fbd027835c1d089b2d3fe9ab9203fc2`  
		Last Modified: Sat, 08 Oct 2022 04:02:07 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db927a95afdcc25384fd927be64e72535b615a678cfefa1c481f72c89a421d51`  
		Last Modified: Sat, 08 Oct 2022 04:02:07 GMT  
		Size: 7.7 KB (7736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7603e8707a28d96ef5c46ca4bb4263d32478fed3f18c6c5e799a126f4c8d64b4`  
		Last Modified: Sat, 08 Oct 2022 04:02:08 GMT  
		Size: 199.6 KB (199558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8453aa2dcfbeaef1a8acf8732c8db652f357b7c50d9094e343cd9f59e37c3664`  
		Last Modified: Sat, 08 Oct 2022 04:02:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b74b3d42386a46fe11be9e8ce6a933569a8712b0d20647a2e694473c22f61f2d`  
		Last Modified: Sat, 08 Oct 2022 04:02:07 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:e5b68da77cb9db28f4d5f80f8220af5803599cf23e9cce57f4b25405f32853f7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2931324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:681bb24795641aec826f9fcf710d73e0f839c1d83231b15da58521db752ad663`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 07:37:40 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 07 Oct 2022 07:37:41 GMT
RUN apk add --no-cache libssl1.1
# Fri, 07 Oct 2022 07:37:42 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 07 Oct 2022 07:37:53 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 07 Oct 2022 07:37:54 GMT
VOLUME [/spiped]
# Fri, 07 Oct 2022 07:37:55 GMT
WORKDIR /spiped
# Fri, 07 Oct 2022 07:37:57 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 07 Oct 2022 07:37:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Oct 2022 07:37:58 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7901c95a1447d090815ba8f9d5afa5abbdd9cdd431c948e1cac143e5cdacea73`  
		Last Modified: Fri, 07 Oct 2022 07:38:25 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081551fa64d93cc14b0e29df21933895b17862a013e29ac667046d4ea8db0b14`  
		Last Modified: Fri, 07 Oct 2022 07:38:25 GMT  
		Size: 7.7 KB (7713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94947ded225af3a68fa2d3e89d286cd5424a073fd1597c34b8fd81fd125c0684`  
		Last Modified: Fri, 07 Oct 2022 07:38:26 GMT  
		Size: 214.3 KB (214266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c443d577082fa11b6c6c4af1a7cf3bcc77598280a04be75044d38d529083f988`  
		Last Modified: Fri, 07 Oct 2022 07:38:25 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141acab92005d5c00bc4f4d6679742fb826be835ac933c9bc5495eb8256eb7e6`  
		Last Modified: Fri, 07 Oct 2022 07:38:25 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; 386

```console
$ docker pull spiped@sha256:6423a7f534f20d885a95067600857ce072688766c2ffa6bb9010fc6d7f7231ed
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3047843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c7719409551ce46332256dc9374bbbe5ebad7eebb18d4f5c3e768b35cabfc11`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:39 GMT
ADD file:b828bc14bc5ff03c8f7310fe0aed6ac5df19a393622d5d1d779a523234d07c0a in / 
# Tue, 09 Aug 2022 17:38:39 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 02:06:26 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 07 Oct 2022 02:06:27 GMT
RUN apk add --no-cache libssl1.1
# Fri, 07 Oct 2022 02:06:28 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 07 Oct 2022 02:06:40 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 07 Oct 2022 02:06:41 GMT
VOLUME [/spiped]
# Fri, 07 Oct 2022 02:06:42 GMT
WORKDIR /spiped
# Fri, 07 Oct 2022 02:06:44 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 07 Oct 2022 02:06:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Oct 2022 02:06:45 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6c0d3b419d848ea31ca748254611d5d5ce3b76e3d7bba520fd87400fbb75f3b9`  
		Last Modified: Tue, 09 Aug 2022 17:39:33 GMT  
		Size: 2.8 MB (2807121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982fdd64c4ca701476bab0ba1a71f21a0405e2b79db064444f6f738b3bdb2683`  
		Last Modified: Fri, 07 Oct 2022 02:07:15 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c854898389b43dbb9cdd413e814a0799ae7a3efd037dc62a2ab580f223d09dd9`  
		Last Modified: Fri, 07 Oct 2022 02:07:15 GMT  
		Size: 7.7 KB (7713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8e6b40665d81d34cbfaf2714f35b8921a3441a7458b416a69479dda6fded73`  
		Last Modified: Fri, 07 Oct 2022 02:07:15 GMT  
		Size: 231.3 KB (231328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e75809d30c75c96ac8571a0aad6037398080e8464c1fe900186204d14ed97ee5`  
		Last Modified: Fri, 07 Oct 2022 02:07:15 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e7f4311d12b79d5b5ed076ae0276fdc41d636eb2425cce1969ffbbecfaa48f`  
		Last Modified: Fri, 07 Oct 2022 02:07:15 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:23f7c4e2894e2b69ec8f99ad3e5bfc9eb384bfb0867a580c0a14296e9fda6808
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3033056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea36cd4aae1294ce2738686854cda02fd8af9cb087470d67f42ae503ef53dbe2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:17:09 GMT
ADD file:66b351666e41834033d334aeb3dc6998dea77aa22e8e254028c923fee67a41a8 in / 
# Tue, 09 Aug 2022 17:17:10 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 07:36:49 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 07 Oct 2022 07:36:51 GMT
RUN apk add --no-cache libssl1.1
# Fri, 07 Oct 2022 07:36:51 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 07 Oct 2022 07:37:05 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 07 Oct 2022 07:37:05 GMT
VOLUME [/spiped]
# Fri, 07 Oct 2022 07:37:06 GMT
WORKDIR /spiped
# Fri, 07 Oct 2022 07:37:06 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 07 Oct 2022 07:37:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Oct 2022 07:37:07 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c79e5d1a8c89b87020a754c8a5c8370faaa37bfb5bca1d8af66770d522ef1caf`  
		Last Modified: Tue, 09 Aug 2022 17:18:26 GMT  
		Size: 2.8 MB (2803320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6730e71fd53d14fc64b230b13be77ded2ae164bb8e0b21103c39d2320db3c383`  
		Last Modified: Fri, 07 Oct 2022 07:37:35 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a98530f24008a28aeac69a847b3e388d2db70cb4ec34485f3b180da38729d98`  
		Last Modified: Fri, 07 Oct 2022 07:37:35 GMT  
		Size: 7.7 KB (7744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:795c3cac559b59708bf223d2fd843ed2dfd7083c5bb42e2bdc5459c77bb508bf`  
		Last Modified: Fri, 07 Oct 2022 07:37:35 GMT  
		Size: 220.3 KB (220251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8832c249dd749cdd6d7eea870aa3a8ee137af08153d1b9a6cd50600958066aa`  
		Last Modified: Fri, 07 Oct 2022 07:37:35 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb4f5e799656197f8bfd5fad27d5caf0993b2a631ac187a703a21cf24dcc448`  
		Last Modified: Fri, 07 Oct 2022 07:37:35 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:e61ee0f946e5685eccc381e0c2947c6d1c7e028e9bbdc3073b69aa42393ce835
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2808515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18ab110d81e2e45f8012dd604cb9c6384aa690b85b579a296c5f4d7f81f7c50f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:41:46 GMT
ADD file:b43a065471bc4711415d3c67cd5b6559b0c48ee7ffe9761530477cf457a6dc34 in / 
# Tue, 09 Aug 2022 17:41:46 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 09:55:45 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 07 Oct 2022 09:55:47 GMT
RUN apk add --no-cache libssl1.1
# Fri, 07 Oct 2022 09:55:48 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 07 Oct 2022 09:55:58 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 07 Oct 2022 09:55:58 GMT
VOLUME [/spiped]
# Fri, 07 Oct 2022 09:55:59 GMT
WORKDIR /spiped
# Fri, 07 Oct 2022 09:56:00 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 07 Oct 2022 09:56:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Oct 2022 09:56:01 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:790c84f1f3409eab952345157df7fa804ba6b5f06d4ceb6f2dfa3c6de2064397`  
		Last Modified: Tue, 09 Aug 2022 17:42:45 GMT  
		Size: 2.6 MB (2590597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f248f8c884e8c56eafd62d4fd705bc4ea4e1b8f47c4adc22f91a07918fcbfe`  
		Last Modified: Fri, 07 Oct 2022 09:56:33 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b4454005be5f38ee0e54328e844699ab2a19fe01659f533914631aeea7d261`  
		Last Modified: Fri, 07 Oct 2022 09:56:34 GMT  
		Size: 7.7 KB (7745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8e9ba51e735f2b9db573be0890282a90d83d48ced508f0faf9252fcaa14778`  
		Last Modified: Fri, 07 Oct 2022 09:56:33 GMT  
		Size: 208.4 KB (208433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aad928e923cf65a5caa952da37a36601f59692024a6c316a0696524d7e16e6f`  
		Last Modified: Fri, 07 Oct 2022 09:56:34 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a43970caf685b3dd35775e85038478cdef00343f53b01cf826099af4248696`  
		Last Modified: Fri, 07 Oct 2022 09:56:33 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6.2`

```console
$ docker pull spiped@sha256:baf6bcaed017648a642add6562bf6e5de15eabf4be46737afba352c1fdd36ea0
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
$ docker pull spiped@sha256:907ddd7d8a3f64e3b9587d8bd37803871c7e0301273fd134fff16a4601b764b6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 MB (37421712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aebdf10111eb9350e84131fa07f10b1e016fae20fb35a2ef3054aac040d9ad51`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:37:06 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 25 Oct 2022 08:37:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:37:09 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 25 Oct 2022 08:37:30 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 25 Oct 2022 08:37:30 GMT
VOLUME [/spiped]
# Tue, 25 Oct 2022 08:37:30 GMT
WORKDIR /spiped
# Tue, 25 Oct 2022 08:37:30 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 25 Oct 2022 08:37:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 08:37:31 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee0ea61d941875664cd9c05776da1213111ea724a574da76b9b28c4b8f4528c`  
		Last Modified: Tue, 25 Oct 2022 08:37:47 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d4fedc70099c8ce233b3659781b1aed74d64581846c692bb49290d355171b7`  
		Last Modified: Tue, 25 Oct 2022 08:37:47 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16e54acaf0e36c17b7f590939d1cb4ad9b02cb94f13fb00f9f7b86745abe48b`  
		Last Modified: Tue, 25 Oct 2022 08:37:48 GMT  
		Size: 6.0 MB (5998416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56db037880c16bf262262d7370497379e30b11b3fd0281edee6eb60a36552277`  
		Last Modified: Tue, 25 Oct 2022 08:37:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc6a4030f16578da977873b98ae987b7321fb1952c6375b4fce536030b6e5836`  
		Last Modified: Tue, 25 Oct 2022 08:37:47 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; arm variant v5

```console
$ docker pull spiped@sha256:485847df99592ce46f57b80602930020570589bc92a57bcf52c0f12576823a04
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33949464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49edd13d49980a223e5a1a05715139ed281b0a6eb541dade9ed3f270ad4cd0bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 04 Oct 2022 23:49:11 GMT
ADD file:effb9e2e2f8c7539e1a2200d069a2592e8ba20c9d034b5a73fbf173b6987193c in / 
# Tue, 04 Oct 2022 23:49:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:50:43 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 05 Oct 2022 13:50:47 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:50:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 05 Oct 2022 13:51:10 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 05 Oct 2022 13:51:10 GMT
VOLUME [/spiped]
# Wed, 05 Oct 2022 13:51:10 GMT
WORKDIR /spiped
# Wed, 05 Oct 2022 13:51:10 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 05 Oct 2022 13:51:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Oct 2022 13:51:10 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7b9558bbfd8050a8e6af6e60560101c49bd53f81df6fa068419b44d028e465eb`  
		Last Modified: Tue, 04 Oct 2022 23:53:54 GMT  
		Size: 28.9 MB (28918381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:647fed87ad0da4e5831b9907161c1b43ec672b65a95198be6094e7480d581bad`  
		Last Modified: Wed, 05 Oct 2022 13:51:30 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788b6b58021116fa18c299ebb7fd9914e26e5b7845b44641398fe8122b749519`  
		Last Modified: Wed, 05 Oct 2022 13:51:30 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f22319e31ec1e1bba11547c2d32e6210b87ed0647fdf4dd64143be50dc2a30`  
		Last Modified: Wed, 05 Oct 2022 13:51:31 GMT  
		Size: 5.0 MB (5027834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79612caf3d4ffa418788cd8c7a273b28bfcb96d8c83830d22736b42d59752f99`  
		Last Modified: Wed, 05 Oct 2022 13:51:30 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dd3e9d639a80e9684a0fd3b86d20666922b4d42f0448143b7065898439f5d98`  
		Last Modified: Wed, 05 Oct 2022 13:51:30 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; arm variant v7

```console
$ docker pull spiped@sha256:be1ad2cbf3c4749f4f3ad1901e49f28ce59e393f77a5e8bbdc1934e9dc7f06b4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31330089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:615d8374859d2dc36d580e1ebc964ba4372deb8348516c86ea093fc7de8fe4bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 04 Oct 2022 23:58:46 GMT
ADD file:ca1bf27f17594a91224a252bd446f97c3b898210c571f2f26fa2e723d2bf521e in / 
# Tue, 04 Oct 2022 23:58:46 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 05:27:20 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 06 Oct 2022 05:27:24 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 05:27:24 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 06 Oct 2022 05:27:40 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 06 Oct 2022 05:27:40 GMT
VOLUME [/spiped]
# Thu, 06 Oct 2022 05:27:41 GMT
WORKDIR /spiped
# Thu, 06 Oct 2022 05:27:41 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 06 Oct 2022 05:27:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Oct 2022 05:27:41 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2bc64aeac2e429577e497affc8a416d2fc59158aa967f07aced793368e19455f`  
		Last Modified: Wed, 05 Oct 2022 00:05:09 GMT  
		Size: 26.6 MB (26579199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df40850a697b1085bcb37facda4649675c11747ceda87157bf7c9c485c5ce49`  
		Last Modified: Thu, 06 Oct 2022 05:28:13 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a82a9536a373fdbbbf4da2ce7b24365418abbd6ec023ca2e087e071f7168eb3`  
		Last Modified: Thu, 06 Oct 2022 05:28:14 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1716079ee90134175f14061acb4ed8f20fdd29fcc172fe6084aacd233b75d20`  
		Last Modified: Thu, 06 Oct 2022 05:28:14 GMT  
		Size: 4.7 MB (4747637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5db88c4deabc13e23b2452cc73b4731feb1b5fadd585289195eb377197614f6`  
		Last Modified: Thu, 06 Oct 2022 05:28:13 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96859a7277435ad4739e871037f955a296c0e4840e0c8388887ebe08a09da32d`  
		Last Modified: Thu, 06 Oct 2022 05:28:13 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:47adb086ffbc8238cc87a374d5545eb53d0e867848ace36033c5d207ed2868c1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35337515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8f97b2795173eb5045fd9730321b818e919dc60c5ecb739c65b4660fcbe02e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 14:23:07 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 05 Oct 2022 14:23:10 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 14:23:11 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 05 Oct 2022 14:23:29 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 05 Oct 2022 14:23:29 GMT
VOLUME [/spiped]
# Wed, 05 Oct 2022 14:23:30 GMT
WORKDIR /spiped
# Wed, 05 Oct 2022 14:23:32 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 05 Oct 2022 14:23:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Oct 2022 14:23:33 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f301477fc358e3377ddd636b2616c84fcf5124bd247b627567141c87be9f6de1`  
		Last Modified: Wed, 05 Oct 2022 14:24:01 GMT  
		Size: 1.6 KB (1620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9302fdee302af51fa37c04770a7b242e609fcccfd0cfd6ff1f84255fd78fddc2`  
		Last Modified: Wed, 05 Oct 2022 14:24:01 GMT  
		Size: 922.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dae3b94946b96722b37618a3af96e0d185b745edae682b8ce313a98448c0c78`  
		Last Modified: Wed, 05 Oct 2022 14:24:02 GMT  
		Size: 5.3 MB (5270141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae56107eb63a27bf608f2ed332d5a8af7040e6d0a2ea0d71bc4889978c765af4`  
		Last Modified: Wed, 05 Oct 2022 14:24:01 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cdd8dce6303958fb1fd5e08767c354bfb5f383d72f0a746b331d1994526d8dc`  
		Last Modified: Wed, 05 Oct 2022 14:24:01 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; 386

```console
$ docker pull spiped@sha256:28d8bdf2af4f3d895db835d3a8746fd5a569f41f63fb1ecfa5f1f7cfd8c8daa0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40288236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c91f70f71153acda4d046f399b07518ac65cd5150c34e1701fc88987574e1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 04 Oct 2022 23:39:40 GMT
ADD file:a66b7a182260a23fdb8b219600a8b48a5079997715006d9a5324dda11f9d0a7f in / 
# Tue, 04 Oct 2022 23:39:41 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 14:09:19 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 05 Oct 2022 14:09:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 14:09:24 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 05 Oct 2022 14:09:45 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 05 Oct 2022 14:09:45 GMT
VOLUME [/spiped]
# Wed, 05 Oct 2022 14:09:46 GMT
WORKDIR /spiped
# Wed, 05 Oct 2022 14:09:48 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 05 Oct 2022 14:09:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Oct 2022 14:09:49 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:711839e532aa3f129f9cfaa5125d0e379ddefd47f3da44d0674372663dfc6a9b`  
		Last Modified: Tue, 04 Oct 2022 23:45:35 GMT  
		Size: 32.4 MB (32396290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c93d3a5b3eec462b1c6ac59cb81a82a136592cec8dd1e4b01a7ff18f94fb6732`  
		Last Modified: Wed, 05 Oct 2022 14:10:18 GMT  
		Size: 1.6 KB (1610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d16e767b1ff67a46f1f079896d403560a4418176d4f3e8edd740703875ee2bd`  
		Last Modified: Wed, 05 Oct 2022 14:10:18 GMT  
		Size: 921.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c089c61d4bb583ef72de3d4af7e734b4b2c6db1c19ce43112038140b60539d3f`  
		Last Modified: Wed, 05 Oct 2022 14:10:19 GMT  
		Size: 7.9 MB (7888980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d79866b3db5ee7887f80f5f15edc439162fc445b37ebee95562f558be876c30`  
		Last Modified: Wed, 05 Oct 2022 14:10:18 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9ce86fb3faa98b26c3f4b6ca4fe16aba6bb731583f47837c5e19b3624ee014`  
		Last Modified: Wed, 05 Oct 2022 14:10:18 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; mips64le

```console
$ docker pull spiped@sha256:123ccf6bf7870f663a836d6b42768cb49fc6a2a67fe65eab98898130fbacb91a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35348950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5779a3f203e4c018cb40a9c1887dbd52b5852288eebd13cc7d46a2f593510175`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 05 Oct 2022 00:10:26 GMT
ADD file:48da6b2f4e0315e4f502001a00e4b2abb58d553de11a41901ba859a461052bea in / 
# Wed, 05 Oct 2022 00:10:29 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 05:02:44 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 06 Oct 2022 05:02:58 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 05:03:00 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 06 Oct 2022 05:04:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 06 Oct 2022 05:04:30 GMT
VOLUME [/spiped]
# Thu, 06 Oct 2022 05:04:33 GMT
WORKDIR /spiped
# Thu, 06 Oct 2022 05:04:35 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 06 Oct 2022 05:04:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Oct 2022 05:04:40 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3288c6e2e7130a1e313203f049bde0e57a05237441a3cab92c27f9ada139315b`  
		Last Modified: Wed, 05 Oct 2022 00:18:36 GMT  
		Size: 29.6 MB (29640851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fef092d9f7ba63a39ca1cdb3fe82522c963b4831657b64e7d9a20fb87c0d549`  
		Last Modified: Thu, 06 Oct 2022 05:04:58 GMT  
		Size: 1.6 KB (1616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a74beea1ecce269e87b3fa3a679d9c1426eb65ee3a9ca732085c10b4bbfdb95`  
		Last Modified: Thu, 06 Oct 2022 05:04:59 GMT  
		Size: 923.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a1d5db219d406d5845647ae1c960c206474eead0677d57a375a5ddd4cfb2312`  
		Last Modified: Thu, 06 Oct 2022 05:05:04 GMT  
		Size: 5.7 MB (5705121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d137b8d414adcef161b5b3df846629e84076f81350be9239b039a150906325`  
		Last Modified: Thu, 06 Oct 2022 05:04:59 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:712a5107ab173d0c81c031796885923796c56aa6822395457a89160d0b4b62f1`  
		Last Modified: Thu, 06 Oct 2022 05:04:58 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; ppc64le

```console
$ docker pull spiped@sha256:4f8c40985efdc328896edd611d5078c2fc2702512fb7dbf8313b4cae3921a64e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41292975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf972f162417a391365ea02bd55cac90c31e91cea94cde3b1785dc4e07b862c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 25 Oct 2022 03:13:50 GMT
ADD file:1f622759c37363caaa6e6b14831ec9369303345c096f3a018eba66a620b08d26 in / 
# Tue, 25 Oct 2022 03:13:52 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:56:49 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 25 Oct 2022 08:56:55 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:56:55 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 25 Oct 2022 08:57:29 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 25 Oct 2022 08:57:30 GMT
VOLUME [/spiped]
# Tue, 25 Oct 2022 08:57:30 GMT
WORKDIR /spiped
# Tue, 25 Oct 2022 08:57:31 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 25 Oct 2022 08:57:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 08:57:31 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6d95b62526dd55d76e7ec2bd4015a327b5bb37161f2ffe8bc2bb08d34a677716`  
		Last Modified: Tue, 25 Oct 2022 03:19:31 GMT  
		Size: 35.3 MB (35290086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e72bcd36564076a1be5059203c37728b7870c126ac7fe06f996ccf16f91855f`  
		Last Modified: Tue, 25 Oct 2022 08:58:00 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68fe46109a02177cec27f93ac157701520a7bb241f376b25305d5d3066a0e344`  
		Last Modified: Tue, 25 Oct 2022 08:58:00 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c94efcdf110ae18400e5415ff3d6b9e3922164053912c50c55ba08357401ef6`  
		Last Modified: Tue, 25 Oct 2022 08:58:02 GMT  
		Size: 6.0 MB (5999635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5edf8c734f5fda4c57a8d654d651fd56402b97e7bb5e2ebb9765410fc9b4ebbf`  
		Last Modified: Tue, 25 Oct 2022 08:58:00 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93111314cb3af703e6ce8c0a09396a4c6e0294ef4a359f1946bbaf70c6ab0b50`  
		Last Modified: Tue, 25 Oct 2022 08:58:00 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2` - linux; s390x

```console
$ docker pull spiped@sha256:d248ba3ec10b15e146e806977482172d735af6a76ebdaae3a2967a79fe3bc883
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34841904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d9b35607854f37e824aa0f514dec480476acd2e766c86c626aa4ab84e3e2daf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 25 Oct 2022 01:14:42 GMT
ADD file:1bb8efa7f80e494b9d2831490a7e74810350c1f9ee2d100596d2e1cb4c62f529 in / 
# Tue, 25 Oct 2022 01:14:44 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:17:40 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 25 Oct 2022 07:17:43 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:17:43 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 25 Oct 2022 07:17:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 25 Oct 2022 07:17:57 GMT
VOLUME [/spiped]
# Tue, 25 Oct 2022 07:17:57 GMT
WORKDIR /spiped
# Tue, 25 Oct 2022 07:17:57 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 25 Oct 2022 07:17:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 07:17:58 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:abc14eb2518761d53b91fc564a31b657914f96b531f99a74ac8268f0717b007e`  
		Last Modified: Tue, 25 Oct 2022 01:19:01 GMT  
		Size: 29.7 MB (29650722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:631fad7c1185ed0f5e182395eabf9dc221258ee09f822bb730b461cea4dc1e91`  
		Last Modified: Tue, 25 Oct 2022 07:18:32 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e288a715b6a67137c6dc2b11d4a1911512db2b794cec1c6e919ee3561176fa3a`  
		Last Modified: Tue, 25 Oct 2022 07:18:32 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65245ecca59da4154a971e90aee7b353bc9ed35f548d478ec6cb54c37b92c513`  
		Last Modified: Tue, 25 Oct 2022 07:18:33 GMT  
		Size: 5.2 MB (5187929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd3eec290beab4e4d33c1f802d534913b85ecef8963ecda079eef7cf0802983`  
		Last Modified: Tue, 25 Oct 2022 07:18:32 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27850183009b851f569533d6a829cf12d40c9fae07dd08ecd8856cc8ff5b6235`  
		Last Modified: Tue, 25 Oct 2022 07:18:32 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:1.6.2-alpine`

```console
$ docker pull spiped@sha256:fd3dbe6f07d6ad025f0b57bdb6bccced1f2d4ed52ed5f2e95bd567ca1213858b
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
$ docker pull spiped@sha256:83b7108c070944539ec82ed9729e69afa1a5ad91eed9163efc95bcd8a3455efa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3036717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8704d25dde580015332a57e745db366aa241d3d99f8949b2c12e3f7c9ae8606`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 04:17:54 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 07 Oct 2022 04:17:55 GMT
RUN apk add --no-cache libssl1.1
# Fri, 07 Oct 2022 04:17:56 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 07 Oct 2022 04:18:06 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 07 Oct 2022 04:18:06 GMT
VOLUME [/spiped]
# Fri, 07 Oct 2022 04:18:06 GMT
WORKDIR /spiped
# Fri, 07 Oct 2022 04:18:06 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 07 Oct 2022 04:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Oct 2022 04:18:07 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:163365ead583145f60498102a9de8f3de170409f2ae8cecf962cf3ab512bb7b6`  
		Last Modified: Fri, 07 Oct 2022 04:18:24 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ebb86b08f67f6638bc3391b020d7e3c07ac692076e469c99ba197a3dc6180d`  
		Last Modified: Fri, 07 Oct 2022 04:18:24 GMT  
		Size: 7.7 KB (7743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0d696472090a4ef1527e0ceea219db2e5ca85866d16132e7f6a560e73c84d3`  
		Last Modified: Fri, 07 Oct 2022 04:18:24 GMT  
		Size: 221.2 KB (221183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ad76fb7ed47c485b828ec98e173c844febdb11324b807d8befb613a1c8f4e06`  
		Last Modified: Fri, 07 Oct 2022 04:18:24 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598391454db346484a0ec6968962627ae778f5ab04cf800247c9dd1ce7ab6878`  
		Last Modified: Fri, 07 Oct 2022 04:18:24 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:b551174a0a1d06027c49d92df5bfe5c2a7b4fbbd0eddc4befe5cd38bb470c37e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2829352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:600282cc6da8413cdcb193cc95ceb823009ccf91df6453209016ff2117ee2ea1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Sat, 08 Oct 2022 03:57:10 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 08 Oct 2022 03:57:11 GMT
RUN apk add --no-cache libssl1.1
# Sat, 08 Oct 2022 03:57:11 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 08 Oct 2022 03:57:20 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 08 Oct 2022 03:57:20 GMT
VOLUME [/spiped]
# Sat, 08 Oct 2022 03:57:20 GMT
WORKDIR /spiped
# Sat, 08 Oct 2022 03:57:20 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 08 Oct 2022 03:57:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 08 Oct 2022 03:57:20 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d22ef9a58b62ce73c21d40d894c34b6d8e3272bf2f543ed188286073c4424fc`  
		Last Modified: Sat, 08 Oct 2022 03:57:39 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62e41f642c74a0d9462ab3129be57e8d46bbce2ba02bd722a9c728e40688eb1e`  
		Last Modified: Sat, 08 Oct 2022 03:57:40 GMT  
		Size: 7.7 KB (7738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca6ab15f65d41991ef7df3456f45af9c8305074e870dc4f144bc85827af4027`  
		Last Modified: Sat, 08 Oct 2022 03:57:39 GMT  
		Size: 205.9 KB (205906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b3bbca61a66ee3759c7812bb413899b9d1c91b1d0b52d7c5566318da8a17f9`  
		Last Modified: Sat, 08 Oct 2022 03:57:39 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e86011e4d6eb7c1e4099a1c1683bf382adfd1ffc4a449a341ceddefc616cf3`  
		Last Modified: Sat, 08 Oct 2022 03:57:39 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:aa33c5a5d1b9aecc0ce4fe51343713ec1a58609fdb7d407f860cbfe5999b2365
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2626104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:054c7036b8c1b0ae94ff78d5b840bb90f42e59c57592b10023f0e4894e38cb79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:44 GMT
ADD file:75521fe16320b193092588f6f31052c85e736965ceb11673de18bd14965a45e6 in / 
# Tue, 09 Aug 2022 16:57:44 GMT
CMD ["/bin/sh"]
# Sat, 08 Oct 2022 04:01:24 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 08 Oct 2022 04:01:25 GMT
RUN apk add --no-cache libssl1.1
# Sat, 08 Oct 2022 04:01:25 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 08 Oct 2022 04:01:33 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 08 Oct 2022 04:01:33 GMT
VOLUME [/spiped]
# Sat, 08 Oct 2022 04:01:34 GMT
WORKDIR /spiped
# Sat, 08 Oct 2022 04:01:34 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 08 Oct 2022 04:01:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 08 Oct 2022 04:01:34 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c6556b3b6858c6fa1e328377cc2c4becdc9cd1bc3e7302aa7299936522cf93ba`  
		Last Modified: Tue, 09 Aug 2022 16:58:55 GMT  
		Size: 2.4 MB (2417065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f672e653be912401f24b90bba8ef9e28fbd027835c1d089b2d3fe9ab9203fc2`  
		Last Modified: Sat, 08 Oct 2022 04:02:07 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db927a95afdcc25384fd927be64e72535b615a678cfefa1c481f72c89a421d51`  
		Last Modified: Sat, 08 Oct 2022 04:02:07 GMT  
		Size: 7.7 KB (7736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7603e8707a28d96ef5c46ca4bb4263d32478fed3f18c6c5e799a126f4c8d64b4`  
		Last Modified: Sat, 08 Oct 2022 04:02:08 GMT  
		Size: 199.6 KB (199558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8453aa2dcfbeaef1a8acf8732c8db652f357b7c50d9094e343cd9f59e37c3664`  
		Last Modified: Sat, 08 Oct 2022 04:02:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b74b3d42386a46fe11be9e8ce6a933569a8712b0d20647a2e694473c22f61f2d`  
		Last Modified: Sat, 08 Oct 2022 04:02:07 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:e5b68da77cb9db28f4d5f80f8220af5803599cf23e9cce57f4b25405f32853f7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2931324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:681bb24795641aec826f9fcf710d73e0f839c1d83231b15da58521db752ad663`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 07:37:40 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 07 Oct 2022 07:37:41 GMT
RUN apk add --no-cache libssl1.1
# Fri, 07 Oct 2022 07:37:42 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 07 Oct 2022 07:37:53 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 07 Oct 2022 07:37:54 GMT
VOLUME [/spiped]
# Fri, 07 Oct 2022 07:37:55 GMT
WORKDIR /spiped
# Fri, 07 Oct 2022 07:37:57 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 07 Oct 2022 07:37:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Oct 2022 07:37:58 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7901c95a1447d090815ba8f9d5afa5abbdd9cdd431c948e1cac143e5cdacea73`  
		Last Modified: Fri, 07 Oct 2022 07:38:25 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081551fa64d93cc14b0e29df21933895b17862a013e29ac667046d4ea8db0b14`  
		Last Modified: Fri, 07 Oct 2022 07:38:25 GMT  
		Size: 7.7 KB (7713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94947ded225af3a68fa2d3e89d286cd5424a073fd1597c34b8fd81fd125c0684`  
		Last Modified: Fri, 07 Oct 2022 07:38:26 GMT  
		Size: 214.3 KB (214266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c443d577082fa11b6c6c4af1a7cf3bcc77598280a04be75044d38d529083f988`  
		Last Modified: Fri, 07 Oct 2022 07:38:25 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141acab92005d5c00bc4f4d6679742fb826be835ac933c9bc5495eb8256eb7e6`  
		Last Modified: Fri, 07 Oct 2022 07:38:25 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; 386

```console
$ docker pull spiped@sha256:6423a7f534f20d885a95067600857ce072688766c2ffa6bb9010fc6d7f7231ed
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3047843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c7719409551ce46332256dc9374bbbe5ebad7eebb18d4f5c3e768b35cabfc11`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:39 GMT
ADD file:b828bc14bc5ff03c8f7310fe0aed6ac5df19a393622d5d1d779a523234d07c0a in / 
# Tue, 09 Aug 2022 17:38:39 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 02:06:26 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 07 Oct 2022 02:06:27 GMT
RUN apk add --no-cache libssl1.1
# Fri, 07 Oct 2022 02:06:28 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 07 Oct 2022 02:06:40 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 07 Oct 2022 02:06:41 GMT
VOLUME [/spiped]
# Fri, 07 Oct 2022 02:06:42 GMT
WORKDIR /spiped
# Fri, 07 Oct 2022 02:06:44 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 07 Oct 2022 02:06:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Oct 2022 02:06:45 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6c0d3b419d848ea31ca748254611d5d5ce3b76e3d7bba520fd87400fbb75f3b9`  
		Last Modified: Tue, 09 Aug 2022 17:39:33 GMT  
		Size: 2.8 MB (2807121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982fdd64c4ca701476bab0ba1a71f21a0405e2b79db064444f6f738b3bdb2683`  
		Last Modified: Fri, 07 Oct 2022 02:07:15 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c854898389b43dbb9cdd413e814a0799ae7a3efd037dc62a2ab580f223d09dd9`  
		Last Modified: Fri, 07 Oct 2022 02:07:15 GMT  
		Size: 7.7 KB (7713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8e6b40665d81d34cbfaf2714f35b8921a3441a7458b416a69479dda6fded73`  
		Last Modified: Fri, 07 Oct 2022 02:07:15 GMT  
		Size: 231.3 KB (231328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e75809d30c75c96ac8571a0aad6037398080e8464c1fe900186204d14ed97ee5`  
		Last Modified: Fri, 07 Oct 2022 02:07:15 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e7f4311d12b79d5b5ed076ae0276fdc41d636eb2425cce1969ffbbecfaa48f`  
		Last Modified: Fri, 07 Oct 2022 02:07:15 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:23f7c4e2894e2b69ec8f99ad3e5bfc9eb384bfb0867a580c0a14296e9fda6808
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3033056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea36cd4aae1294ce2738686854cda02fd8af9cb087470d67f42ae503ef53dbe2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:17:09 GMT
ADD file:66b351666e41834033d334aeb3dc6998dea77aa22e8e254028c923fee67a41a8 in / 
# Tue, 09 Aug 2022 17:17:10 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 07:36:49 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 07 Oct 2022 07:36:51 GMT
RUN apk add --no-cache libssl1.1
# Fri, 07 Oct 2022 07:36:51 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 07 Oct 2022 07:37:05 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 07 Oct 2022 07:37:05 GMT
VOLUME [/spiped]
# Fri, 07 Oct 2022 07:37:06 GMT
WORKDIR /spiped
# Fri, 07 Oct 2022 07:37:06 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 07 Oct 2022 07:37:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Oct 2022 07:37:07 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c79e5d1a8c89b87020a754c8a5c8370faaa37bfb5bca1d8af66770d522ef1caf`  
		Last Modified: Tue, 09 Aug 2022 17:18:26 GMT  
		Size: 2.8 MB (2803320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6730e71fd53d14fc64b230b13be77ded2ae164bb8e0b21103c39d2320db3c383`  
		Last Modified: Fri, 07 Oct 2022 07:37:35 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a98530f24008a28aeac69a847b3e388d2db70cb4ec34485f3b180da38729d98`  
		Last Modified: Fri, 07 Oct 2022 07:37:35 GMT  
		Size: 7.7 KB (7744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:795c3cac559b59708bf223d2fd843ed2dfd7083c5bb42e2bdc5459c77bb508bf`  
		Last Modified: Fri, 07 Oct 2022 07:37:35 GMT  
		Size: 220.3 KB (220251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8832c249dd749cdd6d7eea870aa3a8ee137af08153d1b9a6cd50600958066aa`  
		Last Modified: Fri, 07 Oct 2022 07:37:35 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb4f5e799656197f8bfd5fad27d5caf0993b2a631ac187a703a21cf24dcc448`  
		Last Modified: Fri, 07 Oct 2022 07:37:35 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:1.6.2-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:e61ee0f946e5685eccc381e0c2947c6d1c7e028e9bbdc3073b69aa42393ce835
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2808515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18ab110d81e2e45f8012dd604cb9c6384aa690b85b579a296c5f4d7f81f7c50f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:41:46 GMT
ADD file:b43a065471bc4711415d3c67cd5b6559b0c48ee7ffe9761530477cf457a6dc34 in / 
# Tue, 09 Aug 2022 17:41:46 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 09:55:45 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 07 Oct 2022 09:55:47 GMT
RUN apk add --no-cache libssl1.1
# Fri, 07 Oct 2022 09:55:48 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 07 Oct 2022 09:55:58 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 07 Oct 2022 09:55:58 GMT
VOLUME [/spiped]
# Fri, 07 Oct 2022 09:55:59 GMT
WORKDIR /spiped
# Fri, 07 Oct 2022 09:56:00 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 07 Oct 2022 09:56:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Oct 2022 09:56:01 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:790c84f1f3409eab952345157df7fa804ba6b5f06d4ceb6f2dfa3c6de2064397`  
		Last Modified: Tue, 09 Aug 2022 17:42:45 GMT  
		Size: 2.6 MB (2590597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f248f8c884e8c56eafd62d4fd705bc4ea4e1b8f47c4adc22f91a07918fcbfe`  
		Last Modified: Fri, 07 Oct 2022 09:56:33 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b4454005be5f38ee0e54328e844699ab2a19fe01659f533914631aeea7d261`  
		Last Modified: Fri, 07 Oct 2022 09:56:34 GMT  
		Size: 7.7 KB (7745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8e9ba51e735f2b9db573be0890282a90d83d48ced508f0faf9252fcaa14778`  
		Last Modified: Fri, 07 Oct 2022 09:56:33 GMT  
		Size: 208.4 KB (208433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aad928e923cf65a5caa952da37a36601f59692024a6c316a0696524d7e16e6f`  
		Last Modified: Fri, 07 Oct 2022 09:56:34 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a43970caf685b3dd35775e85038478cdef00343f53b01cf826099af4248696`  
		Last Modified: Fri, 07 Oct 2022 09:56:33 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:alpine`

```console
$ docker pull spiped@sha256:fd3dbe6f07d6ad025f0b57bdb6bccced1f2d4ed52ed5f2e95bd567ca1213858b
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
$ docker pull spiped@sha256:83b7108c070944539ec82ed9729e69afa1a5ad91eed9163efc95bcd8a3455efa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3036717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8704d25dde580015332a57e745db366aa241d3d99f8949b2c12e3f7c9ae8606`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 04:17:54 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 07 Oct 2022 04:17:55 GMT
RUN apk add --no-cache libssl1.1
# Fri, 07 Oct 2022 04:17:56 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 07 Oct 2022 04:18:06 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 07 Oct 2022 04:18:06 GMT
VOLUME [/spiped]
# Fri, 07 Oct 2022 04:18:06 GMT
WORKDIR /spiped
# Fri, 07 Oct 2022 04:18:06 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 07 Oct 2022 04:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Oct 2022 04:18:07 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:163365ead583145f60498102a9de8f3de170409f2ae8cecf962cf3ab512bb7b6`  
		Last Modified: Fri, 07 Oct 2022 04:18:24 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ebb86b08f67f6638bc3391b020d7e3c07ac692076e469c99ba197a3dc6180d`  
		Last Modified: Fri, 07 Oct 2022 04:18:24 GMT  
		Size: 7.7 KB (7743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0d696472090a4ef1527e0ceea219db2e5ca85866d16132e7f6a560e73c84d3`  
		Last Modified: Fri, 07 Oct 2022 04:18:24 GMT  
		Size: 221.2 KB (221183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ad76fb7ed47c485b828ec98e173c844febdb11324b807d8befb613a1c8f4e06`  
		Last Modified: Fri, 07 Oct 2022 04:18:24 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598391454db346484a0ec6968962627ae778f5ab04cf800247c9dd1ce7ab6878`  
		Last Modified: Fri, 07 Oct 2022 04:18:24 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:b551174a0a1d06027c49d92df5bfe5c2a7b4fbbd0eddc4befe5cd38bb470c37e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2829352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:600282cc6da8413cdcb193cc95ceb823009ccf91df6453209016ff2117ee2ea1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Sat, 08 Oct 2022 03:57:10 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 08 Oct 2022 03:57:11 GMT
RUN apk add --no-cache libssl1.1
# Sat, 08 Oct 2022 03:57:11 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 08 Oct 2022 03:57:20 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 08 Oct 2022 03:57:20 GMT
VOLUME [/spiped]
# Sat, 08 Oct 2022 03:57:20 GMT
WORKDIR /spiped
# Sat, 08 Oct 2022 03:57:20 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 08 Oct 2022 03:57:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 08 Oct 2022 03:57:20 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d22ef9a58b62ce73c21d40d894c34b6d8e3272bf2f543ed188286073c4424fc`  
		Last Modified: Sat, 08 Oct 2022 03:57:39 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62e41f642c74a0d9462ab3129be57e8d46bbce2ba02bd722a9c728e40688eb1e`  
		Last Modified: Sat, 08 Oct 2022 03:57:40 GMT  
		Size: 7.7 KB (7738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca6ab15f65d41991ef7df3456f45af9c8305074e870dc4f144bc85827af4027`  
		Last Modified: Sat, 08 Oct 2022 03:57:39 GMT  
		Size: 205.9 KB (205906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b3bbca61a66ee3759c7812bb413899b9d1c91b1d0b52d7c5566318da8a17f9`  
		Last Modified: Sat, 08 Oct 2022 03:57:39 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e86011e4d6eb7c1e4099a1c1683bf382adfd1ffc4a449a341ceddefc616cf3`  
		Last Modified: Sat, 08 Oct 2022 03:57:39 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:aa33c5a5d1b9aecc0ce4fe51343713ec1a58609fdb7d407f860cbfe5999b2365
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2626104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:054c7036b8c1b0ae94ff78d5b840bb90f42e59c57592b10023f0e4894e38cb79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:44 GMT
ADD file:75521fe16320b193092588f6f31052c85e736965ceb11673de18bd14965a45e6 in / 
# Tue, 09 Aug 2022 16:57:44 GMT
CMD ["/bin/sh"]
# Sat, 08 Oct 2022 04:01:24 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Sat, 08 Oct 2022 04:01:25 GMT
RUN apk add --no-cache libssl1.1
# Sat, 08 Oct 2022 04:01:25 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sat, 08 Oct 2022 04:01:33 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Sat, 08 Oct 2022 04:01:33 GMT
VOLUME [/spiped]
# Sat, 08 Oct 2022 04:01:34 GMT
WORKDIR /spiped
# Sat, 08 Oct 2022 04:01:34 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Sat, 08 Oct 2022 04:01:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 08 Oct 2022 04:01:34 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c6556b3b6858c6fa1e328377cc2c4becdc9cd1bc3e7302aa7299936522cf93ba`  
		Last Modified: Tue, 09 Aug 2022 16:58:55 GMT  
		Size: 2.4 MB (2417065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f672e653be912401f24b90bba8ef9e28fbd027835c1d089b2d3fe9ab9203fc2`  
		Last Modified: Sat, 08 Oct 2022 04:02:07 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db927a95afdcc25384fd927be64e72535b615a678cfefa1c481f72c89a421d51`  
		Last Modified: Sat, 08 Oct 2022 04:02:07 GMT  
		Size: 7.7 KB (7736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7603e8707a28d96ef5c46ca4bb4263d32478fed3f18c6c5e799a126f4c8d64b4`  
		Last Modified: Sat, 08 Oct 2022 04:02:08 GMT  
		Size: 199.6 KB (199558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8453aa2dcfbeaef1a8acf8732c8db652f357b7c50d9094e343cd9f59e37c3664`  
		Last Modified: Sat, 08 Oct 2022 04:02:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b74b3d42386a46fe11be9e8ce6a933569a8712b0d20647a2e694473c22f61f2d`  
		Last Modified: Sat, 08 Oct 2022 04:02:07 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:e5b68da77cb9db28f4d5f80f8220af5803599cf23e9cce57f4b25405f32853f7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2931324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:681bb24795641aec826f9fcf710d73e0f839c1d83231b15da58521db752ad663`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 07:37:40 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 07 Oct 2022 07:37:41 GMT
RUN apk add --no-cache libssl1.1
# Fri, 07 Oct 2022 07:37:42 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 07 Oct 2022 07:37:53 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 07 Oct 2022 07:37:54 GMT
VOLUME [/spiped]
# Fri, 07 Oct 2022 07:37:55 GMT
WORKDIR /spiped
# Fri, 07 Oct 2022 07:37:57 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 07 Oct 2022 07:37:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Oct 2022 07:37:58 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7901c95a1447d090815ba8f9d5afa5abbdd9cdd431c948e1cac143e5cdacea73`  
		Last Modified: Fri, 07 Oct 2022 07:38:25 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081551fa64d93cc14b0e29df21933895b17862a013e29ac667046d4ea8db0b14`  
		Last Modified: Fri, 07 Oct 2022 07:38:25 GMT  
		Size: 7.7 KB (7713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94947ded225af3a68fa2d3e89d286cd5424a073fd1597c34b8fd81fd125c0684`  
		Last Modified: Fri, 07 Oct 2022 07:38:26 GMT  
		Size: 214.3 KB (214266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c443d577082fa11b6c6c4af1a7cf3bcc77598280a04be75044d38d529083f988`  
		Last Modified: Fri, 07 Oct 2022 07:38:25 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141acab92005d5c00bc4f4d6679742fb826be835ac933c9bc5495eb8256eb7e6`  
		Last Modified: Fri, 07 Oct 2022 07:38:25 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; 386

```console
$ docker pull spiped@sha256:6423a7f534f20d885a95067600857ce072688766c2ffa6bb9010fc6d7f7231ed
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3047843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c7719409551ce46332256dc9374bbbe5ebad7eebb18d4f5c3e768b35cabfc11`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:39 GMT
ADD file:b828bc14bc5ff03c8f7310fe0aed6ac5df19a393622d5d1d779a523234d07c0a in / 
# Tue, 09 Aug 2022 17:38:39 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 02:06:26 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 07 Oct 2022 02:06:27 GMT
RUN apk add --no-cache libssl1.1
# Fri, 07 Oct 2022 02:06:28 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 07 Oct 2022 02:06:40 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 07 Oct 2022 02:06:41 GMT
VOLUME [/spiped]
# Fri, 07 Oct 2022 02:06:42 GMT
WORKDIR /spiped
# Fri, 07 Oct 2022 02:06:44 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 07 Oct 2022 02:06:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Oct 2022 02:06:45 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6c0d3b419d848ea31ca748254611d5d5ce3b76e3d7bba520fd87400fbb75f3b9`  
		Last Modified: Tue, 09 Aug 2022 17:39:33 GMT  
		Size: 2.8 MB (2807121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982fdd64c4ca701476bab0ba1a71f21a0405e2b79db064444f6f738b3bdb2683`  
		Last Modified: Fri, 07 Oct 2022 02:07:15 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c854898389b43dbb9cdd413e814a0799ae7a3efd037dc62a2ab580f223d09dd9`  
		Last Modified: Fri, 07 Oct 2022 02:07:15 GMT  
		Size: 7.7 KB (7713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8e6b40665d81d34cbfaf2714f35b8921a3441a7458b416a69479dda6fded73`  
		Last Modified: Fri, 07 Oct 2022 02:07:15 GMT  
		Size: 231.3 KB (231328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e75809d30c75c96ac8571a0aad6037398080e8464c1fe900186204d14ed97ee5`  
		Last Modified: Fri, 07 Oct 2022 02:07:15 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e7f4311d12b79d5b5ed076ae0276fdc41d636eb2425cce1969ffbbecfaa48f`  
		Last Modified: Fri, 07 Oct 2022 02:07:15 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:23f7c4e2894e2b69ec8f99ad3e5bfc9eb384bfb0867a580c0a14296e9fda6808
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3033056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea36cd4aae1294ce2738686854cda02fd8af9cb087470d67f42ae503ef53dbe2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:17:09 GMT
ADD file:66b351666e41834033d334aeb3dc6998dea77aa22e8e254028c923fee67a41a8 in / 
# Tue, 09 Aug 2022 17:17:10 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 07:36:49 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 07 Oct 2022 07:36:51 GMT
RUN apk add --no-cache libssl1.1
# Fri, 07 Oct 2022 07:36:51 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 07 Oct 2022 07:37:05 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 07 Oct 2022 07:37:05 GMT
VOLUME [/spiped]
# Fri, 07 Oct 2022 07:37:06 GMT
WORKDIR /spiped
# Fri, 07 Oct 2022 07:37:06 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 07 Oct 2022 07:37:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Oct 2022 07:37:07 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c79e5d1a8c89b87020a754c8a5c8370faaa37bfb5bca1d8af66770d522ef1caf`  
		Last Modified: Tue, 09 Aug 2022 17:18:26 GMT  
		Size: 2.8 MB (2803320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6730e71fd53d14fc64b230b13be77ded2ae164bb8e0b21103c39d2320db3c383`  
		Last Modified: Fri, 07 Oct 2022 07:37:35 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a98530f24008a28aeac69a847b3e388d2db70cb4ec34485f3b180da38729d98`  
		Last Modified: Fri, 07 Oct 2022 07:37:35 GMT  
		Size: 7.7 KB (7744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:795c3cac559b59708bf223d2fd843ed2dfd7083c5bb42e2bdc5459c77bb508bf`  
		Last Modified: Fri, 07 Oct 2022 07:37:35 GMT  
		Size: 220.3 KB (220251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8832c249dd749cdd6d7eea870aa3a8ee137af08153d1b9a6cd50600958066aa`  
		Last Modified: Fri, 07 Oct 2022 07:37:35 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb4f5e799656197f8bfd5fad27d5caf0993b2a631ac187a703a21cf24dcc448`  
		Last Modified: Fri, 07 Oct 2022 07:37:35 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; s390x

```console
$ docker pull spiped@sha256:e61ee0f946e5685eccc381e0c2947c6d1c7e028e9bbdc3073b69aa42393ce835
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2808515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18ab110d81e2e45f8012dd604cb9c6384aa690b85b579a296c5f4d7f81f7c50f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 09 Aug 2022 17:41:46 GMT
ADD file:b43a065471bc4711415d3c67cd5b6559b0c48ee7ffe9761530477cf457a6dc34 in / 
# Tue, 09 Aug 2022 17:41:46 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 09:55:45 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Fri, 07 Oct 2022 09:55:47 GMT
RUN apk add --no-cache libssl1.1
# Fri, 07 Oct 2022 09:55:48 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Fri, 07 Oct 2022 09:55:58 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Fri, 07 Oct 2022 09:55:58 GMT
VOLUME [/spiped]
# Fri, 07 Oct 2022 09:55:59 GMT
WORKDIR /spiped
# Fri, 07 Oct 2022 09:56:00 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Fri, 07 Oct 2022 09:56:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Oct 2022 09:56:01 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:790c84f1f3409eab952345157df7fa804ba6b5f06d4ceb6f2dfa3c6de2064397`  
		Last Modified: Tue, 09 Aug 2022 17:42:45 GMT  
		Size: 2.6 MB (2590597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f248f8c884e8c56eafd62d4fd705bc4ea4e1b8f47c4adc22f91a07918fcbfe`  
		Last Modified: Fri, 07 Oct 2022 09:56:33 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b4454005be5f38ee0e54328e844699ab2a19fe01659f533914631aeea7d261`  
		Last Modified: Fri, 07 Oct 2022 09:56:34 GMT  
		Size: 7.7 KB (7745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8e9ba51e735f2b9db573be0890282a90d83d48ced508f0faf9252fcaa14778`  
		Last Modified: Fri, 07 Oct 2022 09:56:33 GMT  
		Size: 208.4 KB (208433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aad928e923cf65a5caa952da37a36601f59692024a6c316a0696524d7e16e6f`  
		Last Modified: Fri, 07 Oct 2022 09:56:34 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a43970caf685b3dd35775e85038478cdef00343f53b01cf826099af4248696`  
		Last Modified: Fri, 07 Oct 2022 09:56:33 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `spiped:latest`

```console
$ docker pull spiped@sha256:baf6bcaed017648a642add6562bf6e5de15eabf4be46737afba352c1fdd36ea0
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
$ docker pull spiped@sha256:907ddd7d8a3f64e3b9587d8bd37803871c7e0301273fd134fff16a4601b764b6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 MB (37421712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aebdf10111eb9350e84131fa07f10b1e016fae20fb35a2ef3054aac040d9ad51`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:37:06 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 25 Oct 2022 08:37:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:37:09 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 25 Oct 2022 08:37:30 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 25 Oct 2022 08:37:30 GMT
VOLUME [/spiped]
# Tue, 25 Oct 2022 08:37:30 GMT
WORKDIR /spiped
# Tue, 25 Oct 2022 08:37:30 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 25 Oct 2022 08:37:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 08:37:31 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee0ea61d941875664cd9c05776da1213111ea724a574da76b9b28c4b8f4528c`  
		Last Modified: Tue, 25 Oct 2022 08:37:47 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d4fedc70099c8ce233b3659781b1aed74d64581846c692bb49290d355171b7`  
		Last Modified: Tue, 25 Oct 2022 08:37:47 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16e54acaf0e36c17b7f590939d1cb4ad9b02cb94f13fb00f9f7b86745abe48b`  
		Last Modified: Tue, 25 Oct 2022 08:37:48 GMT  
		Size: 6.0 MB (5998416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56db037880c16bf262262d7370497379e30b11b3fd0281edee6eb60a36552277`  
		Last Modified: Tue, 25 Oct 2022 08:37:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc6a4030f16578da977873b98ae987b7321fb1952c6375b4fce536030b6e5836`  
		Last Modified: Tue, 25 Oct 2022 08:37:47 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; arm variant v5

```console
$ docker pull spiped@sha256:485847df99592ce46f57b80602930020570589bc92a57bcf52c0f12576823a04
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33949464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49edd13d49980a223e5a1a05715139ed281b0a6eb541dade9ed3f270ad4cd0bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 04 Oct 2022 23:49:11 GMT
ADD file:effb9e2e2f8c7539e1a2200d069a2592e8ba20c9d034b5a73fbf173b6987193c in / 
# Tue, 04 Oct 2022 23:49:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:50:43 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 05 Oct 2022 13:50:47 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:50:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 05 Oct 2022 13:51:10 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 05 Oct 2022 13:51:10 GMT
VOLUME [/spiped]
# Wed, 05 Oct 2022 13:51:10 GMT
WORKDIR /spiped
# Wed, 05 Oct 2022 13:51:10 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 05 Oct 2022 13:51:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Oct 2022 13:51:10 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7b9558bbfd8050a8e6af6e60560101c49bd53f81df6fa068419b44d028e465eb`  
		Last Modified: Tue, 04 Oct 2022 23:53:54 GMT  
		Size: 28.9 MB (28918381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:647fed87ad0da4e5831b9907161c1b43ec672b65a95198be6094e7480d581bad`  
		Last Modified: Wed, 05 Oct 2022 13:51:30 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788b6b58021116fa18c299ebb7fd9914e26e5b7845b44641398fe8122b749519`  
		Last Modified: Wed, 05 Oct 2022 13:51:30 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f22319e31ec1e1bba11547c2d32e6210b87ed0647fdf4dd64143be50dc2a30`  
		Last Modified: Wed, 05 Oct 2022 13:51:31 GMT  
		Size: 5.0 MB (5027834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79612caf3d4ffa418788cd8c7a273b28bfcb96d8c83830d22736b42d59752f99`  
		Last Modified: Wed, 05 Oct 2022 13:51:30 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dd3e9d639a80e9684a0fd3b86d20666922b4d42f0448143b7065898439f5d98`  
		Last Modified: Wed, 05 Oct 2022 13:51:30 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; arm variant v7

```console
$ docker pull spiped@sha256:be1ad2cbf3c4749f4f3ad1901e49f28ce59e393f77a5e8bbdc1934e9dc7f06b4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31330089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:615d8374859d2dc36d580e1ebc964ba4372deb8348516c86ea093fc7de8fe4bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 04 Oct 2022 23:58:46 GMT
ADD file:ca1bf27f17594a91224a252bd446f97c3b898210c571f2f26fa2e723d2bf521e in / 
# Tue, 04 Oct 2022 23:58:46 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 05:27:20 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 06 Oct 2022 05:27:24 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 05:27:24 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 06 Oct 2022 05:27:40 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 06 Oct 2022 05:27:40 GMT
VOLUME [/spiped]
# Thu, 06 Oct 2022 05:27:41 GMT
WORKDIR /spiped
# Thu, 06 Oct 2022 05:27:41 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 06 Oct 2022 05:27:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Oct 2022 05:27:41 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2bc64aeac2e429577e497affc8a416d2fc59158aa967f07aced793368e19455f`  
		Last Modified: Wed, 05 Oct 2022 00:05:09 GMT  
		Size: 26.6 MB (26579199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df40850a697b1085bcb37facda4649675c11747ceda87157bf7c9c485c5ce49`  
		Last Modified: Thu, 06 Oct 2022 05:28:13 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a82a9536a373fdbbbf4da2ce7b24365418abbd6ec023ca2e087e071f7168eb3`  
		Last Modified: Thu, 06 Oct 2022 05:28:14 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1716079ee90134175f14061acb4ed8f20fdd29fcc172fe6084aacd233b75d20`  
		Last Modified: Thu, 06 Oct 2022 05:28:14 GMT  
		Size: 4.7 MB (4747637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5db88c4deabc13e23b2452cc73b4731feb1b5fadd585289195eb377197614f6`  
		Last Modified: Thu, 06 Oct 2022 05:28:13 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96859a7277435ad4739e871037f955a296c0e4840e0c8388887ebe08a09da32d`  
		Last Modified: Thu, 06 Oct 2022 05:28:13 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:47adb086ffbc8238cc87a374d5545eb53d0e867848ace36033c5d207ed2868c1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35337515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8f97b2795173eb5045fd9730321b818e919dc60c5ecb739c65b4660fcbe02e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 14:23:07 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 05 Oct 2022 14:23:10 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 14:23:11 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 05 Oct 2022 14:23:29 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 05 Oct 2022 14:23:29 GMT
VOLUME [/spiped]
# Wed, 05 Oct 2022 14:23:30 GMT
WORKDIR /spiped
# Wed, 05 Oct 2022 14:23:32 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 05 Oct 2022 14:23:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Oct 2022 14:23:33 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f301477fc358e3377ddd636b2616c84fcf5124bd247b627567141c87be9f6de1`  
		Last Modified: Wed, 05 Oct 2022 14:24:01 GMT  
		Size: 1.6 KB (1620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9302fdee302af51fa37c04770a7b242e609fcccfd0cfd6ff1f84255fd78fddc2`  
		Last Modified: Wed, 05 Oct 2022 14:24:01 GMT  
		Size: 922.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dae3b94946b96722b37618a3af96e0d185b745edae682b8ce313a98448c0c78`  
		Last Modified: Wed, 05 Oct 2022 14:24:02 GMT  
		Size: 5.3 MB (5270141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae56107eb63a27bf608f2ed332d5a8af7040e6d0a2ea0d71bc4889978c765af4`  
		Last Modified: Wed, 05 Oct 2022 14:24:01 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cdd8dce6303958fb1fd5e08767c354bfb5f383d72f0a746b331d1994526d8dc`  
		Last Modified: Wed, 05 Oct 2022 14:24:01 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; 386

```console
$ docker pull spiped@sha256:28d8bdf2af4f3d895db835d3a8746fd5a569f41f63fb1ecfa5f1f7cfd8c8daa0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40288236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c91f70f71153acda4d046f399b07518ac65cd5150c34e1701fc88987574e1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 04 Oct 2022 23:39:40 GMT
ADD file:a66b7a182260a23fdb8b219600a8b48a5079997715006d9a5324dda11f9d0a7f in / 
# Tue, 04 Oct 2022 23:39:41 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 14:09:19 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Wed, 05 Oct 2022 14:09:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 14:09:24 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 05 Oct 2022 14:09:45 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 05 Oct 2022 14:09:45 GMT
VOLUME [/spiped]
# Wed, 05 Oct 2022 14:09:46 GMT
WORKDIR /spiped
# Wed, 05 Oct 2022 14:09:48 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Wed, 05 Oct 2022 14:09:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Oct 2022 14:09:49 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:711839e532aa3f129f9cfaa5125d0e379ddefd47f3da44d0674372663dfc6a9b`  
		Last Modified: Tue, 04 Oct 2022 23:45:35 GMT  
		Size: 32.4 MB (32396290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c93d3a5b3eec462b1c6ac59cb81a82a136592cec8dd1e4b01a7ff18f94fb6732`  
		Last Modified: Wed, 05 Oct 2022 14:10:18 GMT  
		Size: 1.6 KB (1610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d16e767b1ff67a46f1f079896d403560a4418176d4f3e8edd740703875ee2bd`  
		Last Modified: Wed, 05 Oct 2022 14:10:18 GMT  
		Size: 921.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c089c61d4bb583ef72de3d4af7e734b4b2c6db1c19ce43112038140b60539d3f`  
		Last Modified: Wed, 05 Oct 2022 14:10:19 GMT  
		Size: 7.9 MB (7888980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d79866b3db5ee7887f80f5f15edc439162fc445b37ebee95562f558be876c30`  
		Last Modified: Wed, 05 Oct 2022 14:10:18 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9ce86fb3faa98b26c3f4b6ca4fe16aba6bb731583f47837c5e19b3624ee014`  
		Last Modified: Wed, 05 Oct 2022 14:10:18 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; mips64le

```console
$ docker pull spiped@sha256:123ccf6bf7870f663a836d6b42768cb49fc6a2a67fe65eab98898130fbacb91a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35348950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5779a3f203e4c018cb40a9c1887dbd52b5852288eebd13cc7d46a2f593510175`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 05 Oct 2022 00:10:26 GMT
ADD file:48da6b2f4e0315e4f502001a00e4b2abb58d553de11a41901ba859a461052bea in / 
# Wed, 05 Oct 2022 00:10:29 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 05:02:44 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Thu, 06 Oct 2022 05:02:58 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 05:03:00 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 06 Oct 2022 05:04:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 06 Oct 2022 05:04:30 GMT
VOLUME [/spiped]
# Thu, 06 Oct 2022 05:04:33 GMT
WORKDIR /spiped
# Thu, 06 Oct 2022 05:04:35 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Thu, 06 Oct 2022 05:04:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Oct 2022 05:04:40 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3288c6e2e7130a1e313203f049bde0e57a05237441a3cab92c27f9ada139315b`  
		Last Modified: Wed, 05 Oct 2022 00:18:36 GMT  
		Size: 29.6 MB (29640851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fef092d9f7ba63a39ca1cdb3fe82522c963b4831657b64e7d9a20fb87c0d549`  
		Last Modified: Thu, 06 Oct 2022 05:04:58 GMT  
		Size: 1.6 KB (1616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a74beea1ecce269e87b3fa3a679d9c1426eb65ee3a9ca732085c10b4bbfdb95`  
		Last Modified: Thu, 06 Oct 2022 05:04:59 GMT  
		Size: 923.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a1d5db219d406d5845647ae1c960c206474eead0677d57a375a5ddd4cfb2312`  
		Last Modified: Thu, 06 Oct 2022 05:05:04 GMT  
		Size: 5.7 MB (5705121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d137b8d414adcef161b5b3df846629e84076f81350be9239b039a150906325`  
		Last Modified: Thu, 06 Oct 2022 05:04:59 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:712a5107ab173d0c81c031796885923796c56aa6822395457a89160d0b4b62f1`  
		Last Modified: Thu, 06 Oct 2022 05:04:58 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; ppc64le

```console
$ docker pull spiped@sha256:4f8c40985efdc328896edd611d5078c2fc2702512fb7dbf8313b4cae3921a64e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41292975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf972f162417a391365ea02bd55cac90c31e91cea94cde3b1785dc4e07b862c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 25 Oct 2022 03:13:50 GMT
ADD file:1f622759c37363caaa6e6b14831ec9369303345c096f3a018eba66a620b08d26 in / 
# Tue, 25 Oct 2022 03:13:52 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:56:49 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 25 Oct 2022 08:56:55 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:56:55 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 25 Oct 2022 08:57:29 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 25 Oct 2022 08:57:30 GMT
VOLUME [/spiped]
# Tue, 25 Oct 2022 08:57:30 GMT
WORKDIR /spiped
# Tue, 25 Oct 2022 08:57:31 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 25 Oct 2022 08:57:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 08:57:31 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6d95b62526dd55d76e7ec2bd4015a327b5bb37161f2ffe8bc2bb08d34a677716`  
		Last Modified: Tue, 25 Oct 2022 03:19:31 GMT  
		Size: 35.3 MB (35290086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e72bcd36564076a1be5059203c37728b7870c126ac7fe06f996ccf16f91855f`  
		Last Modified: Tue, 25 Oct 2022 08:58:00 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68fe46109a02177cec27f93ac157701520a7bb241f376b25305d5d3066a0e344`  
		Last Modified: Tue, 25 Oct 2022 08:58:00 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c94efcdf110ae18400e5415ff3d6b9e3922164053912c50c55ba08357401ef6`  
		Last Modified: Tue, 25 Oct 2022 08:58:02 GMT  
		Size: 6.0 MB (5999635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5edf8c734f5fda4c57a8d654d651fd56402b97e7bb5e2ebb9765410fc9b4ebbf`  
		Last Modified: Tue, 25 Oct 2022 08:58:00 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93111314cb3af703e6ce8c0a09396a4c6e0294ef4a359f1946bbaf70c6ab0b50`  
		Last Modified: Tue, 25 Oct 2022 08:58:00 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; s390x

```console
$ docker pull spiped@sha256:d248ba3ec10b15e146e806977482172d735af6a76ebdaae3a2967a79fe3bc883
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34841904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d9b35607854f37e824aa0f514dec480476acd2e766c86c626aa4ab84e3e2daf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 25 Oct 2022 01:14:42 GMT
ADD file:1bb8efa7f80e494b9d2831490a7e74810350c1f9ee2d100596d2e1cb4c62f529 in / 
# Tue, 25 Oct 2022 01:14:44 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:17:40 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 25 Oct 2022 07:17:43 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl1.1 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:17:43 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 25 Oct 2022 07:17:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 25 Oct 2022 07:17:57 GMT
VOLUME [/spiped]
# Tue, 25 Oct 2022 07:17:57 GMT
WORKDIR /spiped
# Tue, 25 Oct 2022 07:17:57 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 25 Oct 2022 07:17:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 07:17:58 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:abc14eb2518761d53b91fc564a31b657914f96b531f99a74ac8268f0717b007e`  
		Last Modified: Tue, 25 Oct 2022 01:19:01 GMT  
		Size: 29.7 MB (29650722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:631fad7c1185ed0f5e182395eabf9dc221258ee09f822bb730b461cea4dc1e91`  
		Last Modified: Tue, 25 Oct 2022 07:18:32 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e288a715b6a67137c6dc2b11d4a1911512db2b794cec1c6e919ee3561176fa3a`  
		Last Modified: Tue, 25 Oct 2022 07:18:32 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65245ecca59da4154a971e90aee7b353bc9ed35f548d478ec6cb54c37b92c513`  
		Last Modified: Tue, 25 Oct 2022 07:18:33 GMT  
		Size: 5.2 MB (5187929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd3eec290beab4e4d33c1f802d534913b85ecef8963ecda079eef7cf0802983`  
		Last Modified: Tue, 25 Oct 2022 07:18:32 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27850183009b851f569533d6a829cf12d40c9fae07dd08ecd8856cc8ff5b6235`  
		Last Modified: Tue, 25 Oct 2022 07:18:32 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
