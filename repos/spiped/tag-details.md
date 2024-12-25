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
$ docker pull spiped@sha256:7677d10bae50eab7bce723d61c919ef49c2c23d9c8c623a799b235047d821d84
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `spiped:1` - linux; amd64

```console
$ docker pull spiped@sha256:a7dd97a20081470a35cadd6169785d86caf3bf93d4987ebc5a4ae955bf303419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37105291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b451eb143d5594952a98dae1b0b0ef55ef97e913b3a344634368967860ca265e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd767aded3e0e4a452f4aa3ac09696385e71487127ca9739d1024c9ba463dd6e`  
		Last Modified: Tue, 24 Dec 2024 22:15:30 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9838d1339bbeadb079dd51218b3aade84cf88d1d115d999a4e4a3b1390c6fd4d`  
		Last Modified: Tue, 24 Dec 2024 22:15:30 GMT  
		Size: 2.4 MB (2401313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc193ce4740ac330677795e51eadea142972081c95fb4aee71923f4bce5243a6`  
		Last Modified: Tue, 24 Dec 2024 22:15:30 GMT  
		Size: 6.5 MB (6470860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5809551b454860f1e4058c63d28c028953b2e2ed893867755dfad49a923b71b`  
		Last Modified: Tue, 24 Dec 2024 22:15:30 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf961f7ac0e0eac310dd1632c7de4baf508b1b42e304b43c676e6b0d87003251`  
		Last Modified: Tue, 24 Dec 2024 22:15:31 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:3c0a59ebccbc3c7ef4acba7e77ca62ad7fd18b73c0c346cca42e8c285ef812e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3530854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c03182376f3f3fc440c34bcd0513b7114b779c642cdfaddfd78510e6a4cbc26d`

```dockerfile
```

-	Layers:
	-	`sha256:3ce4c62fb5412f9b49941e62f081b29f85902c6d533daaeaa4a008b619e31115`  
		Last Modified: Tue, 24 Dec 2024 22:15:30 GMT  
		Size: 3.5 MB (3515814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8736e4f073ce4ba6ce28e2b8fd9ac45b95124e6b3f5d7e229a8d4e5cc5fe38f0`  
		Last Modified: Tue, 24 Dec 2024 22:15:30 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm variant v5

```console
$ docker pull spiped@sha256:5a0ff595b4809d9f657cd755f82afad83a5400ebed7098e1c9e1d4485c696680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32891708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51914d90458025639148f873fa2737154d95a4acf426a39d1531c3a28bd9d634`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1734912000'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:61230a432de02dc9fd57340d88179517d7f651caeb2a5e2fa6ec333d17ed65c5`  
		Last Modified: Tue, 24 Dec 2024 21:33:31 GMT  
		Size: 25.8 MB (25754907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff406d9a466b89f1ee0d62de835144d8a20f4e4090e34b1f99d314c32300fa6`  
		Last Modified: Wed, 25 Dec 2024 01:30:01 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594b7318a0e87718e415649e74ad23b30870383adb319e8129e2e6357cbdffb5`  
		Last Modified: Wed, 25 Dec 2024 01:30:01 GMT  
		Size: 2.0 MB (1997182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9516f1676319d8b0d371e636fabf37d16151918abd539b6e6ac36b86503e6d`  
		Last Modified: Wed, 25 Dec 2024 01:30:01 GMT  
		Size: 5.1 MB (5138080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bfb3f5aa819cbf256ea5483de4b098613c94f4a25dd3ed8178e207ec003c48`  
		Last Modified: Wed, 25 Dec 2024 01:30:01 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e148c2154289a52718590456f627dfcd48b0419ce7ddee43087b88c75cd869f1`  
		Last Modified: Wed, 25 Dec 2024 01:30:01 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:69d4d0d616215b625bef7a1c0b1514bf42fac5c0e5d1b41de1c4711e04a42b77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3501486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f06323f57f358722230b775cbb482532200f4955cf8da6065825b11122ff47f`

```dockerfile
```

-	Layers:
	-	`sha256:6ecc6ea63b5f6f3da3546e6b73304075502f588e6acc90ef3a8e171576b48316`  
		Last Modified: Wed, 25 Dec 2024 01:30:01 GMT  
		Size: 3.5 MB (3486344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85a19088103eac42e407f88234f0df6a4a43a3b22b502e66b2e4a90f8715b1ac`  
		Last Modified: Wed, 25 Dec 2024 01:30:00 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm variant v7

```console
$ docker pull spiped@sha256:ede738edc1dd3664cdc2056ab1070988ba5b5d5b50c94c0e1c426873eb1fe883
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 MB (30671063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb2b65bc9e81bf68c58ab1fdd7fa057c179c5b191be2380bba0e61fdd126632f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:24f0da30a772db626789cda3e7b0911098d07574c40b30be943d43dec3ed685f`  
		Last Modified: Tue, 24 Dec 2024 21:33:51 GMT  
		Size: 23.9 MB (23933522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381ee1c72da2fe25de158dc79f791a4e5f2640cce1929d519a43ded3ea5e8a90`  
		Last Modified: Wed, 25 Dec 2024 03:28:59 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3dd3a794351508157cfcb738934464fb3ef893c8545d3be6205d6fec4dbbb0`  
		Last Modified: Wed, 25 Dec 2024 03:28:59 GMT  
		Size: 1.9 MB (1855604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c52c57bab55640fb8a84e36fbbb54a20d3afaa69e2090b3a59b1e93bf25067`  
		Last Modified: Wed, 25 Dec 2024 03:28:59 GMT  
		Size: 4.9 MB (4880401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c13ef05b160d3362c6c826f740b9767e4308a41b09f72e0d685c89355ee776`  
		Last Modified: Wed, 25 Dec 2024 03:28:59 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197345a1fb9ad8e6138a397d8df5bc7d45ec166e6e184644bb752ad28b7b5bd0`  
		Last Modified: Wed, 25 Dec 2024 03:29:00 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:eeaa7583a0a22f13495b38c77a31bf4d901a2495c1f9b48530daa385142eb131
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3500976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90fc682623c6de4b402365a3d369ab05ba6ebb046ebe8d29a563d598d97b1cae`

```dockerfile
```

-	Layers:
	-	`sha256:0b21e96fc1d27b03f925dc09a0800453ca5c69103cdc7292ff53064aca0701a3`  
		Last Modified: Wed, 25 Dec 2024 03:29:00 GMT  
		Size: 3.5 MB (3485835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbed3956028284093ae6a4a6b3d472e942fc6c36a001c85a509eb87710e78c96`  
		Last Modified: Wed, 25 Dec 2024 03:28:59 GMT  
		Size: 15.1 KB (15141 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:683cabe7e0eed7297111985eb6618a1960ad0847dc683136c0d994533c1b8696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35788363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f41a2307bf8709f5a95d5444cab15e3d95355c41c58ec6099d7f1ba6f57a2e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f769b1854757b5b4ae5743b8d429389bae7f0381b4be0aa48e86934db98748`  
		Last Modified: Wed, 25 Dec 2024 01:28:10 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9162f0dcd326913bb139c0781a3f428fded3f0baf7a48a0e56bbf8888d8607`  
		Last Modified: Wed, 25 Dec 2024 01:28:10 GMT  
		Size: 2.2 MB (2247004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b572a3c9e43b9eb92754465fbc7cdce3e8618940970c40887e91b1af73f6f933`  
		Last Modified: Wed, 25 Dec 2024 01:28:10 GMT  
		Size: 5.5 MB (5481100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af2cae35c937b304605d6a2d691806a3d816c7f2e32109c5b779e858f5d4cbe`  
		Last Modified: Wed, 25 Dec 2024 01:28:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32afe8fd289c0f8521d68cf2b4f2e1c650e34bc7a288beeb7fe2591ea223d3f0`  
		Last Modified: Wed, 25 Dec 2024 01:28:11 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:b223557fee24382404079822852eba4258babd849ae1e1fbea690ee9f0f74396
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3502216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36302ad039f457150bc5b5ef223e749f9f31cc12131f2bcfbcfab37635663f6a`

```dockerfile
```

-	Layers:
	-	`sha256:479e2b82d5ed62e0627a20bcf029de82590c35225fc11641db3f69c4723440e4`  
		Last Modified: Wed, 25 Dec 2024 01:28:10 GMT  
		Size: 3.5 MB (3487042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e21ed0a3ae7d4cb9c6d7d5e8f71fabcc40673cde1f3c45025b5694a723e26c4`  
		Last Modified: Wed, 25 Dec 2024 01:28:10 GMT  
		Size: 15.2 KB (15174 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; 386

```console
$ docker pull spiped@sha256:d3bad81148a63f9e65b6a8e5edb28b22407f9870ac1b9daddb8dd62fb89eaa4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37547000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:381f29b36739ed9815e40d19ed03aef86c4c05e189b507ae287e9c56285da723`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:fba9c0797a7b5bba079e0fd9d815a8878aea58430ea12c84047010f98fbe34d7`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 29.2 MB (29205387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b1e932b36b88542e04dada12c3f21f0f34b8d16e96a07d2182f0ceb3cfc52a`  
		Last Modified: Tue, 24 Dec 2024 22:14:41 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a49d5b20f552856ebdc1f91a1818ed41a9a9c5b31b7191cf1e6f0fc09c95916`  
		Last Modified: Tue, 24 Dec 2024 22:14:41 GMT  
		Size: 2.4 MB (2398659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb97d01b24b3952ed0462f79f171d4926106395407dc96963a036f27f041bee`  
		Last Modified: Tue, 24 Dec 2024 22:14:41 GMT  
		Size: 5.9 MB (5941415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956df477ffa74406f5801dbb1143462f11d46d675392b087e13191d2810bf2d3`  
		Last Modified: Tue, 24 Dec 2024 22:14:41 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e154e0ef38fb7a31b609c417e6eca590c4cd2d87d656d7080a5a92c051be3d86`  
		Last Modified: Tue, 24 Dec 2024 22:14:42 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:094af1deb53cda626632725ba7f785a3213f615908d1a27b653d88e399c296e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67332a7e6a2833848d5d47240f969c1fcbf987e8ddbe6ac3739f79b812e9260d`

```dockerfile
```

-	Layers:
	-	`sha256:e9b7f1f48aad35bf0976821f09af4acdc310a8d7795f1eab0893279d31f5f028`  
		Last Modified: Tue, 24 Dec 2024 22:14:41 GMT  
		Size: 3.5 MB (3509741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa8ea9d57c1c96e289bc572430f49d54b1289bd2768065d0e9d7626693bef7f3`  
		Last Modified: Tue, 24 Dec 2024 22:14:41 GMT  
		Size: 15.0 KB (15004 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; mips64le

```console
$ docker pull spiped@sha256:d89a09b29a3053b1374ac6c3b197938d6f41e4c00d5bb716fd65e61d7c97975a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36152100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d8acb258cdf976c86134a73453ccf189b3ecbe6040145d37d213c14ad71531`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1733097600'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:29ac4ae2849b0c84c0ef17659082268617abeb406402ef46b6fa9140e6d2064d`  
		Last Modified: Tue, 03 Dec 2024 01:28:15 GMT  
		Size: 28.5 MB (28505909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2a37d1c3544aae9cf855e4f9d96754f7d5aad9c9a3f7d42a3eb8987d04b10a`  
		Last Modified: Tue, 03 Dec 2024 15:43:23 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687c3b1191976c7d74198e8e57529daabebefb487799f83eb7d8681422ef72b8`  
		Last Modified: Tue, 03 Dec 2024 15:43:24 GMT  
		Size: 1.8 MB (1841107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71cc921943a3967383a50f905dd8868956c3ac63ebb385d9cec2f3cb34a9f87e`  
		Last Modified: Tue, 03 Dec 2024 15:43:24 GMT  
		Size: 5.8 MB (5803545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c26a9ead4b058916305bb6fd71d2599865275170bdb57724c307edf3509f326`  
		Last Modified: Tue, 03 Dec 2024 15:43:23 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9104292331624763e6d460ca187a0f85b64d1f486b86284c07c95592b8e94da1`  
		Last Modified: Tue, 03 Dec 2024 15:43:24 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:ee8a92a1ad8cafc8ea99877f6bfd0d92dc91949f54b840b48821ce544aa9bcda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ab156a72eff661cd8aed8bf33e1b225c9f5f2c967cb69cf1c020b44d53b44d`

```dockerfile
```

-	Layers:
	-	`sha256:2bd3fbc5d440f518558673839c4fcba7382ea6d548360ed2c57eb7bd0f049a65`  
		Last Modified: Tue, 03 Dec 2024 15:43:23 GMT  
		Size: 14.9 KB (14897 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; ppc64le

```console
$ docker pull spiped@sha256:fa1c0e0ca44831854510e672c54f19e7f6f438f1b478e6e12eb6fc349cb6036e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41069658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:badc1dcf78bdd756328e48de377c9ac83765d7fd252f4f6aed46a14bd58061e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4a1ea4d3c9e0863e99d27aae6dac9a4b908a6413e758c7785d8fefe555b0e760`  
		Last Modified: Wed, 25 Dec 2024 00:32:48 GMT  
		Size: 32.1 MB (32063240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a10da46285624ad419bea829c84e2e283422614dc35af1abbcae2a21f755880`  
		Last Modified: Wed, 25 Dec 2024 06:00:22 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a18aaec69dfb91f7d658b963b1908aea3dd52a5d0ca1bd2882ce20e4891f72`  
		Last Modified: Wed, 25 Dec 2024 06:00:22 GMT  
		Size: 2.6 MB (2582060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944f472562e3088d879887732f39ea7cd0325819e2e8a179e0bb9564d18b57bb`  
		Last Modified: Wed, 25 Dec 2024 06:00:22 GMT  
		Size: 6.4 MB (6422816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df99d607fa9056ce8bb98db90549b7cbb6134b22361fc8c6293e8b883590d69`  
		Last Modified: Wed, 25 Dec 2024 06:00:22 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a6e26267e78fc9b2b7d66526922f89447996b9b8966d139452965d17fe008d`  
		Last Modified: Wed, 25 Dec 2024 06:00:23 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:39bf9515ccb9ec3a1513b875efcfece99ec844387b12732b93639b1c4dd870c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3516571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ca2573bd1e1ca8bceff7576088a8e2dcc6308a088e8fdc6c45ca47102b82647`

```dockerfile
```

-	Layers:
	-	`sha256:eee07c1e01812a3751985b1f438d18380d58d390e5da5ae1e3bbdca47c05c113`  
		Last Modified: Wed, 25 Dec 2024 06:00:22 GMT  
		Size: 3.5 MB (3501483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb349bf5733a427d8d67d73d6730d8117ab8dc2f68442180e877e7a53062a071`  
		Last Modified: Wed, 25 Dec 2024 06:00:22 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; s390x

```console
$ docker pull spiped@sha256:6c8b9b684784fd7e276e9642a6f67e29c09b10a5e70c83ce74be972322034cdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34334969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8363621faa6e61fe5ffedc99a0ac820582911b3efb820dd5c5e56288cfdca21d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:0e7e84bd4cca9e29f08dfac96d436e65bdd31929520e73147137b382fbc89b70`  
		Last Modified: Tue, 24 Dec 2024 21:33:49 GMT  
		Size: 26.9 MB (26878901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc416ec43cf7816408db05f15f973105968e740cadc2d8bf781d0f18b1662e2`  
		Last Modified: Wed, 25 Dec 2024 00:06:46 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43bde2f7b43f7809ecb4a99fef725c7668af05efd43fab2b2de7d0e9cdeed7df`  
		Last Modified: Wed, 25 Dec 2024 00:06:46 GMT  
		Size: 2.1 MB (2068729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c405c4f3d636ce991eec1df48ab2acbafb141f057b012887daeac232eeae8852`  
		Last Modified: Wed, 25 Dec 2024 00:06:46 GMT  
		Size: 5.4 MB (5385800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb5fd31da13e128253de1c3be9f0eaccc9791741f2ddbd7f64c404738ccfceb`  
		Last Modified: Wed, 25 Dec 2024 00:06:46 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67aa610193b9571e7f56cc25183b12debeda63c2b610cd66c4e3029c6fb31fb4`  
		Last Modified: Wed, 25 Dec 2024 00:06:46 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:3d6bf018776d6e6d237fde4d2f785340bcd6e32728626dba860c50d1995f0203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3519040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:054b3ee947046ff8f0f3b14b7e50d2f17b81f1ba09225a49e6d135180a585d01`

```dockerfile
```

-	Layers:
	-	`sha256:be1536a048742b7927962b19f3ec187b33b5f53d994d3883fb3398e0cc303f31`  
		Last Modified: Wed, 25 Dec 2024 00:06:46 GMT  
		Size: 3.5 MB (3504000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3dec620d34fc6d656f7478c968b406037c961f5f26c3e0b72bdd506d2fdceac`  
		Last Modified: Wed, 25 Dec 2024 00:06:46 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1-alpine`

```console
$ docker pull spiped@sha256:e32b4b32ec1bebd57bcef51d51943394d621e20004e559d74d0a5fadbb262fc5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `spiped:1-alpine` - linux; amd64

```console
$ docker pull spiped@sha256:daefb5299ff2e9476112aa9c609b5264e2c34f92126f0bb20e29d5c14ef90fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6132905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29aab44abfc742685430558f3458335cf0cd806c6d386b3eed8c756a4666be89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44372b8a42e415e28022098de7f58892719831ddb3b69d1982475c01e1ebcee9`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4d3d0195931e82893a059b29aa5e09859b561a5699199003caa76db025a103`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 7.6 KB (7552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faaff9889bcd7686a7e389188c9b1da11b944593c3f367ce73321c9cd1f9f4d3`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 2.5 MB (2500052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742ceb23f0c29b5b00035c6ae582d5ff76d9120d036d2c2963228c0b95b636c1`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcda00b0c3a86b025e7acc0393e7b903b2a7e0174aa346d91d7ec0647b02082d`  
		Last Modified: Tue, 12 Nov 2024 02:37:27 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:dd862b700b2f279233f9ae16d5c25154680ee1dfcd86f522a853623380c7e63f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 KB (88486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60c4488d7285be9cc92fe8c34981fd09686e9eece95b44097621805a9422d86`

```dockerfile
```

-	Layers:
	-	`sha256:0c0c153d8884f2d689fb54feef58d5b3f507c9257a4da7ef17c63cc34edfbab7`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 74.2 KB (74181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f273e32436d0f59afb7e53948d572f8c2a58adad3690545a558a4a9074424b5`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 14.3 KB (14305 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:5b42c6f2c6f6d4daf16d2b7f02566b892213498a607898ec86fe4f13ba174433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5530602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae2a9c2c8102d9dfaf0e25652471e9e17f0128392eb62b35fd98ecf2ae3a790b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2124325dc5cb0e691b81062d52602d82e66cf4a54d05d890bdf506e6eb914835`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8bc56b9fe431e43e990d6ce1df319af96d7a3c550c23870b2c1051a27fbe06`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 7.6 KB (7555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4007f0c3a790e3d7107168b4005f37de82f1c1c5d974f34ba3933bbc0419ea4a`  
		Last Modified: Tue, 12 Nov 2024 06:29:08 GMT  
		Size: 2.2 MB (2155051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11376d8ca4651e301f66a4e1203da53694eb1be5d78239a60c000768c941525`  
		Last Modified: Tue, 12 Nov 2024 06:29:08 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a2a3ed2d5ea66800cdf4bb8bb04faca0e1725b756688c0d63daf5bcca2d310`  
		Last Modified: Tue, 12 Nov 2024 06:29:08 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:66e0dc5536fdbd525be5c4d9f9f3ae6c4cffce04ff577a831143d54d7876dc1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cf059becbf5ff9f78307636057df7a043c0d5e6d27cb25c8d761b7fba67b075`

```dockerfile
```

-	Layers:
	-	`sha256:2e10f6bc35866f5a553ae9a114eafa57e88f05f4423cbac2a76088422ce325c0`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 14.2 KB (14192 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:f1b28e18aa159ad4b27d738d0e6271ba9f7f14fea5025db3ead37944a1c1d38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5104726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f5914ed409d7a9b8d1d4b37a7f11dafe085591b60fe58b70ea028c271c80290`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3f756621e1fede5561bf3c8b16df49f95f70f146e0dcf052b5be6ab859f7ad`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a57661377f6134602ff6bb1e331bb44ffa59d55b34e7f1afc7758704aa905f`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17e1750441e507ad7e1f0363aabe05175114a5764b1e7ab139af0e89e3e8ae2`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 2.0 MB (2000280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db3501f51148e9fbda41edee3f07843a542820b52626ecebc0d123cff9f86f0`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c83efd7947156d56b945c49da1d15a267824161f7cbb06f182a19f951d46eb`  
		Last Modified: Tue, 12 Nov 2024 15:31:29 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f8e99759c16c5acd111b0a4c9cd95892c25016f5ee89821b4b3146e5fb36a615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 KB (88624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a9f2d3ac23f0f25dd218dfc12896c53ce47fc6066ee717cb9a9a1d076cf976`

```dockerfile
```

-	Layers:
	-	`sha256:f93fe0699906bc92245e1be0751778f7df38efd418fdd621e6f0a882f7176f1d`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 74.2 KB (74217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1987893a490fa099b5341b220483d8eff205a754295987430790b44538df2716`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 14.4 KB (14407 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:53804ac33977b62680e560b74ba5b5d22713391963530048538f60555cfdefeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7006326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90940b6c3a5d028791331563f8e8ed1afdd05d1d06aee6494da2e04dd2b1ffe6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a88c0f1cd0fd5f6079c67eac729ff5a805c5a469e26e47e580751968b7f372`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd36a7367ed608d19a699ca4c0a2062ff5094acc1d3815baf34a01aa293c2714`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 7.6 KB (7563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a95d0832d1bc79736bef4c10b336d5f18b8b548b754a6753537e54c463a1a3`  
		Last Modified: Tue, 12 Nov 2024 10:30:10 GMT  
		Size: 2.9 MB (2909644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9945356ed175181e01d175895b560aaf6dbe437550ce277dd031a8348f84876f`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198174201e9ff5bde070dcb1468a1be3c27943e332be9207cbf99edd10b46552`  
		Last Modified: Tue, 12 Nov 2024 10:30:10 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:0673de50fe1b90d9eba54ceb48d9f764a97f6d383426370685df181b70f7cc63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 KB (88676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6fa5047039d1fadd0ae7378601b830022268a3ada3f00c912dbcdabf45cdea0`

```dockerfile
```

-	Layers:
	-	`sha256:b7546d292551cf31ac3bd93e1e6e162b689c94b9443030c420887493a945351d`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 74.2 KB (74237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95d4514b51e612f28c127e3cff2d26e19284f01ad6b7f8ee94cea702f485a8e0`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 14.4 KB (14439 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; 386

```console
$ docker pull spiped@sha256:6d46f04e30a3105fc3141267e91ffb5ba3050aa7be87148dcc59dd960122b8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5825462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bbcb7b0f29ba9dab0f0c1726527e43ed4016181bd95ab9debba9300da8dad8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97a6fd63828fbfe315eb146a6e09131a00451eb6df7364f89b2838fc8967506`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71549e122188c29598764406aede3a2d7f39ee116980cb024522fa714099248e`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 7.6 KB (7562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9082d20944f15111e92d68546d0843fef30343a5d20401f9dbbbaa559107f7`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 2.3 MB (2347284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a12d1f809df9acb5e86279c66f9f620f87d4359dd8b552217833aabf984c725`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565e15916b0ca46193b8a9e1c83bc74904a8fd5ac8d51710d11a9cd1974c67f2`  
		Last Modified: Tue, 12 Nov 2024 02:10:45 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:ae024814f19ccf108f4c49012d543026dcebbcda6cf432b72e679e80eac307c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 KB (88425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f85c7eb8498f8dab641cf09ac2320681a6bfeb6471034d0b8f17c0413c26f96`

```dockerfile
```

-	Layers:
	-	`sha256:c338f2f328277430db1def5c4614e72997853bf84529ed6d44202ce3949aad37`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 74.2 KB (74156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5902723b69c008d179c3e0da07749f803cb6ad90ba97a9c3feb151d76dadba00`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 14.3 KB (14269 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:8afb3bf99c94a591d0eba15d96253b003415424195f369f761365ded0250911e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5946540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c165f7c09f005647071973ca64009e4fcfbb357266bce909503a70125b3cc603`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acff226d267e2f526a684557f036f58a914c59247be39068651a3bbb5be99c8`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8522a836c3199ccf9b49cd625b0801b4893ca92b819606a20a60eef862d763fa`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0aca5aa27b0c34935f8383d3017c2e1b574336e405b6e683e2fd18f0544bc9d`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 2.4 MB (2365118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39730da67a08ee98eba5461d059c4ae17310847df8147206ae9dd3c915a2a053`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1466bf84e7abe5d6dc8431df5577ea2e1eb5767f85402df0d10e38bd9b21175`  
		Last Modified: Tue, 12 Nov 2024 08:08:13 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:68986bada3dc3e301441051f41dd84386659fa6521bcfba1865e24368e919451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 KB (86614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbbad23dc8d88c7da7f63057b1a78301962cad8edf146f8c53a7fdcd9a7b558`

```dockerfile
```

-	Layers:
	-	`sha256:8af705f7ad2b931357ae0f8d34cff42c83b9ea58f0a34298a04cbebcab791e59`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 72.3 KB (72261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90553d9dcd0f0a8f53c333aed2eed7edd767d790498bd322ce254e64fa3dd8cb`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 14.4 KB (14353 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:da6591d15c86f3bf43fab6ccc0035a0650a5756859870abdd3276d24eedff6a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5551193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b8476d53de131526ad9562517c1b099c24ce9385a5730746d1e83247619389c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46aa88ab9b012a876209b14e6deee5c7982f819f8de6d7b9ed357459d28c597e`  
		Last Modified: Wed, 13 Nov 2024 01:24:28 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5bdf98d05f4226e17074c09dea718e6191052243811401bf5891cdfb4f1005a`  
		Last Modified: Wed, 13 Nov 2024 01:24:28 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1cc53836a810c0768e9eb515600a82be8862a3129239035de56d851625f2890`  
		Last Modified: Wed, 13 Nov 2024 01:24:29 GMT  
		Size: 2.2 MB (2170750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd669ab852fa6faffdff5b54301703ace4f36faf005d628470fcef6f3ba9296`  
		Last Modified: Wed, 13 Nov 2024 01:24:29 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31ad710654b9957b395b764e0751fb8ceb335cd3970bee0870c731d0c9d1631`  
		Last Modified: Wed, 13 Nov 2024 01:24:30 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:35c0217a072785ece237b37268cd30f7410f423b96bd889e56db03a674044795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 KB (86610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21f8f74486982bdb4f701b16321ebb5b430c4a06622f6960273f474bfbb2188e`

```dockerfile
```

-	Layers:
	-	`sha256:88a28221c4fd9d156a4ebf0935fa189d8524bb92c8fdc1d76981cf7435c2056e`  
		Last Modified: Wed, 13 Nov 2024 01:24:28 GMT  
		Size: 72.3 KB (72257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a28652304d303135a92cbe69570122aaa332626746b8080a921073de8775bb3`  
		Last Modified: Wed, 13 Nov 2024 01:24:28 GMT  
		Size: 14.4 KB (14353 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:30464ff5097e65f47e6a755c9c779d3075ff07a1e9de556d11e7c96a7a94bd7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5713802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eb33bd33066b8fc5173e375f27f7f9452ab4ccf03a15c2a86c9ee2c7b389d04`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8899981d6f06508315b3001ebf4f1bde53ab20235caaa013f5ba8c77a73e8adb`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6687c63f48eb23b685aac39d34fd10d946be39a35d263efb7f96ab22c27e5540`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acea042cc930aa404c9b71350854bad5f8f7641916069b37d0d586596d4bbd2d`  
		Last Modified: Tue, 12 Nov 2024 08:43:36 GMT  
		Size: 2.2 MB (2243236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43854f54c63f7333c81ead906bd289eb4a3559aed20097234270a6b9ac8a472c`  
		Last Modified: Tue, 12 Nov 2024 08:43:36 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d137c29c807dddaad7226bf07aa3e0a203dd1839e595b93c07975336ff0379`  
		Last Modified: Tue, 12 Nov 2024 08:43:36 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:0eae92830e9bc1adf13eac44f18f428cde18ca2b63aae15579bcf3fef67941d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 KB (86532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23d8e6d1cfce745a53aeb2213c583ad2b0372bccd118edc86a78c30b8dc0d5b8`

```dockerfile
```

-	Layers:
	-	`sha256:511653a9b9e8708d56eb05048ec62f75f94b92d11463839efcc6c8f9d950ddbd`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 72.2 KB (72227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23d284526c8ef1bc8f766ba9f4b30d40ffacde5f0411805933554ef0edf6dc33`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 14.3 KB (14305 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6`

```console
$ docker pull spiped@sha256:7677d10bae50eab7bce723d61c919ef49c2c23d9c8c623a799b235047d821d84
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `spiped:1.6` - linux; amd64

```console
$ docker pull spiped@sha256:a7dd97a20081470a35cadd6169785d86caf3bf93d4987ebc5a4ae955bf303419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37105291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b451eb143d5594952a98dae1b0b0ef55ef97e913b3a344634368967860ca265e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd767aded3e0e4a452f4aa3ac09696385e71487127ca9739d1024c9ba463dd6e`  
		Last Modified: Tue, 24 Dec 2024 22:15:30 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9838d1339bbeadb079dd51218b3aade84cf88d1d115d999a4e4a3b1390c6fd4d`  
		Last Modified: Tue, 24 Dec 2024 22:15:30 GMT  
		Size: 2.4 MB (2401313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc193ce4740ac330677795e51eadea142972081c95fb4aee71923f4bce5243a6`  
		Last Modified: Tue, 24 Dec 2024 22:15:30 GMT  
		Size: 6.5 MB (6470860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5809551b454860f1e4058c63d28c028953b2e2ed893867755dfad49a923b71b`  
		Last Modified: Tue, 24 Dec 2024 22:15:30 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf961f7ac0e0eac310dd1632c7de4baf508b1b42e304b43c676e6b0d87003251`  
		Last Modified: Tue, 24 Dec 2024 22:15:31 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:3c0a59ebccbc3c7ef4acba7e77ca62ad7fd18b73c0c346cca42e8c285ef812e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3530854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c03182376f3f3fc440c34bcd0513b7114b779c642cdfaddfd78510e6a4cbc26d`

```dockerfile
```

-	Layers:
	-	`sha256:3ce4c62fb5412f9b49941e62f081b29f85902c6d533daaeaa4a008b619e31115`  
		Last Modified: Tue, 24 Dec 2024 22:15:30 GMT  
		Size: 3.5 MB (3515814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8736e4f073ce4ba6ce28e2b8fd9ac45b95124e6b3f5d7e229a8d4e5cc5fe38f0`  
		Last Modified: Tue, 24 Dec 2024 22:15:30 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm variant v5

```console
$ docker pull spiped@sha256:5a0ff595b4809d9f657cd755f82afad83a5400ebed7098e1c9e1d4485c696680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32891708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51914d90458025639148f873fa2737154d95a4acf426a39d1531c3a28bd9d634`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1734912000'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:61230a432de02dc9fd57340d88179517d7f651caeb2a5e2fa6ec333d17ed65c5`  
		Last Modified: Tue, 24 Dec 2024 21:33:31 GMT  
		Size: 25.8 MB (25754907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff406d9a466b89f1ee0d62de835144d8a20f4e4090e34b1f99d314c32300fa6`  
		Last Modified: Wed, 25 Dec 2024 01:30:01 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594b7318a0e87718e415649e74ad23b30870383adb319e8129e2e6357cbdffb5`  
		Last Modified: Wed, 25 Dec 2024 01:30:01 GMT  
		Size: 2.0 MB (1997182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9516f1676319d8b0d371e636fabf37d16151918abd539b6e6ac36b86503e6d`  
		Last Modified: Wed, 25 Dec 2024 01:30:01 GMT  
		Size: 5.1 MB (5138080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bfb3f5aa819cbf256ea5483de4b098613c94f4a25dd3ed8178e207ec003c48`  
		Last Modified: Wed, 25 Dec 2024 01:30:01 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e148c2154289a52718590456f627dfcd48b0419ce7ddee43087b88c75cd869f1`  
		Last Modified: Wed, 25 Dec 2024 01:30:01 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:69d4d0d616215b625bef7a1c0b1514bf42fac5c0e5d1b41de1c4711e04a42b77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3501486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f06323f57f358722230b775cbb482532200f4955cf8da6065825b11122ff47f`

```dockerfile
```

-	Layers:
	-	`sha256:6ecc6ea63b5f6f3da3546e6b73304075502f588e6acc90ef3a8e171576b48316`  
		Last Modified: Wed, 25 Dec 2024 01:30:01 GMT  
		Size: 3.5 MB (3486344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85a19088103eac42e407f88234f0df6a4a43a3b22b502e66b2e4a90f8715b1ac`  
		Last Modified: Wed, 25 Dec 2024 01:30:00 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm variant v7

```console
$ docker pull spiped@sha256:ede738edc1dd3664cdc2056ab1070988ba5b5d5b50c94c0e1c426873eb1fe883
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 MB (30671063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb2b65bc9e81bf68c58ab1fdd7fa057c179c5b191be2380bba0e61fdd126632f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:24f0da30a772db626789cda3e7b0911098d07574c40b30be943d43dec3ed685f`  
		Last Modified: Tue, 24 Dec 2024 21:33:51 GMT  
		Size: 23.9 MB (23933522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381ee1c72da2fe25de158dc79f791a4e5f2640cce1929d519a43ded3ea5e8a90`  
		Last Modified: Wed, 25 Dec 2024 03:28:59 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3dd3a794351508157cfcb738934464fb3ef893c8545d3be6205d6fec4dbbb0`  
		Last Modified: Wed, 25 Dec 2024 03:28:59 GMT  
		Size: 1.9 MB (1855604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c52c57bab55640fb8a84e36fbbb54a20d3afaa69e2090b3a59b1e93bf25067`  
		Last Modified: Wed, 25 Dec 2024 03:28:59 GMT  
		Size: 4.9 MB (4880401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c13ef05b160d3362c6c826f740b9767e4308a41b09f72e0d685c89355ee776`  
		Last Modified: Wed, 25 Dec 2024 03:28:59 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197345a1fb9ad8e6138a397d8df5bc7d45ec166e6e184644bb752ad28b7b5bd0`  
		Last Modified: Wed, 25 Dec 2024 03:29:00 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:eeaa7583a0a22f13495b38c77a31bf4d901a2495c1f9b48530daa385142eb131
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3500976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90fc682623c6de4b402365a3d369ab05ba6ebb046ebe8d29a563d598d97b1cae`

```dockerfile
```

-	Layers:
	-	`sha256:0b21e96fc1d27b03f925dc09a0800453ca5c69103cdc7292ff53064aca0701a3`  
		Last Modified: Wed, 25 Dec 2024 03:29:00 GMT  
		Size: 3.5 MB (3485835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbed3956028284093ae6a4a6b3d472e942fc6c36a001c85a509eb87710e78c96`  
		Last Modified: Wed, 25 Dec 2024 03:28:59 GMT  
		Size: 15.1 KB (15141 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:683cabe7e0eed7297111985eb6618a1960ad0847dc683136c0d994533c1b8696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35788363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f41a2307bf8709f5a95d5444cab15e3d95355c41c58ec6099d7f1ba6f57a2e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f769b1854757b5b4ae5743b8d429389bae7f0381b4be0aa48e86934db98748`  
		Last Modified: Wed, 25 Dec 2024 01:28:10 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9162f0dcd326913bb139c0781a3f428fded3f0baf7a48a0e56bbf8888d8607`  
		Last Modified: Wed, 25 Dec 2024 01:28:10 GMT  
		Size: 2.2 MB (2247004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b572a3c9e43b9eb92754465fbc7cdce3e8618940970c40887e91b1af73f6f933`  
		Last Modified: Wed, 25 Dec 2024 01:28:10 GMT  
		Size: 5.5 MB (5481100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af2cae35c937b304605d6a2d691806a3d816c7f2e32109c5b779e858f5d4cbe`  
		Last Modified: Wed, 25 Dec 2024 01:28:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32afe8fd289c0f8521d68cf2b4f2e1c650e34bc7a288beeb7fe2591ea223d3f0`  
		Last Modified: Wed, 25 Dec 2024 01:28:11 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:b223557fee24382404079822852eba4258babd849ae1e1fbea690ee9f0f74396
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3502216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36302ad039f457150bc5b5ef223e749f9f31cc12131f2bcfbcfab37635663f6a`

```dockerfile
```

-	Layers:
	-	`sha256:479e2b82d5ed62e0627a20bcf029de82590c35225fc11641db3f69c4723440e4`  
		Last Modified: Wed, 25 Dec 2024 01:28:10 GMT  
		Size: 3.5 MB (3487042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e21ed0a3ae7d4cb9c6d7d5e8f71fabcc40673cde1f3c45025b5694a723e26c4`  
		Last Modified: Wed, 25 Dec 2024 01:28:10 GMT  
		Size: 15.2 KB (15174 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; 386

```console
$ docker pull spiped@sha256:d3bad81148a63f9e65b6a8e5edb28b22407f9870ac1b9daddb8dd62fb89eaa4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37547000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:381f29b36739ed9815e40d19ed03aef86c4c05e189b507ae287e9c56285da723`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:fba9c0797a7b5bba079e0fd9d815a8878aea58430ea12c84047010f98fbe34d7`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 29.2 MB (29205387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b1e932b36b88542e04dada12c3f21f0f34b8d16e96a07d2182f0ceb3cfc52a`  
		Last Modified: Tue, 24 Dec 2024 22:14:41 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a49d5b20f552856ebdc1f91a1818ed41a9a9c5b31b7191cf1e6f0fc09c95916`  
		Last Modified: Tue, 24 Dec 2024 22:14:41 GMT  
		Size: 2.4 MB (2398659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb97d01b24b3952ed0462f79f171d4926106395407dc96963a036f27f041bee`  
		Last Modified: Tue, 24 Dec 2024 22:14:41 GMT  
		Size: 5.9 MB (5941415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956df477ffa74406f5801dbb1143462f11d46d675392b087e13191d2810bf2d3`  
		Last Modified: Tue, 24 Dec 2024 22:14:41 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e154e0ef38fb7a31b609c417e6eca590c4cd2d87d656d7080a5a92c051be3d86`  
		Last Modified: Tue, 24 Dec 2024 22:14:42 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:094af1deb53cda626632725ba7f785a3213f615908d1a27b653d88e399c296e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67332a7e6a2833848d5d47240f969c1fcbf987e8ddbe6ac3739f79b812e9260d`

```dockerfile
```

-	Layers:
	-	`sha256:e9b7f1f48aad35bf0976821f09af4acdc310a8d7795f1eab0893279d31f5f028`  
		Last Modified: Tue, 24 Dec 2024 22:14:41 GMT  
		Size: 3.5 MB (3509741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa8ea9d57c1c96e289bc572430f49d54b1289bd2768065d0e9d7626693bef7f3`  
		Last Modified: Tue, 24 Dec 2024 22:14:41 GMT  
		Size: 15.0 KB (15004 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; mips64le

```console
$ docker pull spiped@sha256:d89a09b29a3053b1374ac6c3b197938d6f41e4c00d5bb716fd65e61d7c97975a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36152100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d8acb258cdf976c86134a73453ccf189b3ecbe6040145d37d213c14ad71531`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1733097600'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:29ac4ae2849b0c84c0ef17659082268617abeb406402ef46b6fa9140e6d2064d`  
		Last Modified: Tue, 03 Dec 2024 01:28:15 GMT  
		Size: 28.5 MB (28505909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2a37d1c3544aae9cf855e4f9d96754f7d5aad9c9a3f7d42a3eb8987d04b10a`  
		Last Modified: Tue, 03 Dec 2024 15:43:23 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687c3b1191976c7d74198e8e57529daabebefb487799f83eb7d8681422ef72b8`  
		Last Modified: Tue, 03 Dec 2024 15:43:24 GMT  
		Size: 1.8 MB (1841107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71cc921943a3967383a50f905dd8868956c3ac63ebb385d9cec2f3cb34a9f87e`  
		Last Modified: Tue, 03 Dec 2024 15:43:24 GMT  
		Size: 5.8 MB (5803545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c26a9ead4b058916305bb6fd71d2599865275170bdb57724c307edf3509f326`  
		Last Modified: Tue, 03 Dec 2024 15:43:23 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9104292331624763e6d460ca187a0f85b64d1f486b86284c07c95592b8e94da1`  
		Last Modified: Tue, 03 Dec 2024 15:43:24 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:ee8a92a1ad8cafc8ea99877f6bfd0d92dc91949f54b840b48821ce544aa9bcda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ab156a72eff661cd8aed8bf33e1b225c9f5f2c967cb69cf1c020b44d53b44d`

```dockerfile
```

-	Layers:
	-	`sha256:2bd3fbc5d440f518558673839c4fcba7382ea6d548360ed2c57eb7bd0f049a65`  
		Last Modified: Tue, 03 Dec 2024 15:43:23 GMT  
		Size: 14.9 KB (14897 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; ppc64le

```console
$ docker pull spiped@sha256:fa1c0e0ca44831854510e672c54f19e7f6f438f1b478e6e12eb6fc349cb6036e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41069658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:badc1dcf78bdd756328e48de377c9ac83765d7fd252f4f6aed46a14bd58061e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4a1ea4d3c9e0863e99d27aae6dac9a4b908a6413e758c7785d8fefe555b0e760`  
		Last Modified: Wed, 25 Dec 2024 00:32:48 GMT  
		Size: 32.1 MB (32063240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a10da46285624ad419bea829c84e2e283422614dc35af1abbcae2a21f755880`  
		Last Modified: Wed, 25 Dec 2024 06:00:22 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a18aaec69dfb91f7d658b963b1908aea3dd52a5d0ca1bd2882ce20e4891f72`  
		Last Modified: Wed, 25 Dec 2024 06:00:22 GMT  
		Size: 2.6 MB (2582060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944f472562e3088d879887732f39ea7cd0325819e2e8a179e0bb9564d18b57bb`  
		Last Modified: Wed, 25 Dec 2024 06:00:22 GMT  
		Size: 6.4 MB (6422816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df99d607fa9056ce8bb98db90549b7cbb6134b22361fc8c6293e8b883590d69`  
		Last Modified: Wed, 25 Dec 2024 06:00:22 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a6e26267e78fc9b2b7d66526922f89447996b9b8966d139452965d17fe008d`  
		Last Modified: Wed, 25 Dec 2024 06:00:23 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:39bf9515ccb9ec3a1513b875efcfece99ec844387b12732b93639b1c4dd870c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3516571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ca2573bd1e1ca8bceff7576088a8e2dcc6308a088e8fdc6c45ca47102b82647`

```dockerfile
```

-	Layers:
	-	`sha256:eee07c1e01812a3751985b1f438d18380d58d390e5da5ae1e3bbdca47c05c113`  
		Last Modified: Wed, 25 Dec 2024 06:00:22 GMT  
		Size: 3.5 MB (3501483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb349bf5733a427d8d67d73d6730d8117ab8dc2f68442180e877e7a53062a071`  
		Last Modified: Wed, 25 Dec 2024 06:00:22 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; s390x

```console
$ docker pull spiped@sha256:6c8b9b684784fd7e276e9642a6f67e29c09b10a5e70c83ce74be972322034cdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34334969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8363621faa6e61fe5ffedc99a0ac820582911b3efb820dd5c5e56288cfdca21d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:0e7e84bd4cca9e29f08dfac96d436e65bdd31929520e73147137b382fbc89b70`  
		Last Modified: Tue, 24 Dec 2024 21:33:49 GMT  
		Size: 26.9 MB (26878901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc416ec43cf7816408db05f15f973105968e740cadc2d8bf781d0f18b1662e2`  
		Last Modified: Wed, 25 Dec 2024 00:06:46 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43bde2f7b43f7809ecb4a99fef725c7668af05efd43fab2b2de7d0e9cdeed7df`  
		Last Modified: Wed, 25 Dec 2024 00:06:46 GMT  
		Size: 2.1 MB (2068729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c405c4f3d636ce991eec1df48ab2acbafb141f057b012887daeac232eeae8852`  
		Last Modified: Wed, 25 Dec 2024 00:06:46 GMT  
		Size: 5.4 MB (5385800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb5fd31da13e128253de1c3be9f0eaccc9791741f2ddbd7f64c404738ccfceb`  
		Last Modified: Wed, 25 Dec 2024 00:06:46 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67aa610193b9571e7f56cc25183b12debeda63c2b610cd66c4e3029c6fb31fb4`  
		Last Modified: Wed, 25 Dec 2024 00:06:46 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:3d6bf018776d6e6d237fde4d2f785340bcd6e32728626dba860c50d1995f0203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3519040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:054b3ee947046ff8f0f3b14b7e50d2f17b81f1ba09225a49e6d135180a585d01`

```dockerfile
```

-	Layers:
	-	`sha256:be1536a048742b7927962b19f3ec187b33b5f53d994d3883fb3398e0cc303f31`  
		Last Modified: Wed, 25 Dec 2024 00:06:46 GMT  
		Size: 3.5 MB (3504000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3dec620d34fc6d656f7478c968b406037c961f5f26c3e0b72bdd506d2fdceac`  
		Last Modified: Wed, 25 Dec 2024 00:06:46 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6-alpine`

```console
$ docker pull spiped@sha256:e32b4b32ec1bebd57bcef51d51943394d621e20004e559d74d0a5fadbb262fc5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `spiped:1.6-alpine` - linux; amd64

```console
$ docker pull spiped@sha256:daefb5299ff2e9476112aa9c609b5264e2c34f92126f0bb20e29d5c14ef90fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6132905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29aab44abfc742685430558f3458335cf0cd806c6d386b3eed8c756a4666be89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44372b8a42e415e28022098de7f58892719831ddb3b69d1982475c01e1ebcee9`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4d3d0195931e82893a059b29aa5e09859b561a5699199003caa76db025a103`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 7.6 KB (7552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faaff9889bcd7686a7e389188c9b1da11b944593c3f367ce73321c9cd1f9f4d3`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 2.5 MB (2500052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742ceb23f0c29b5b00035c6ae582d5ff76d9120d036d2c2963228c0b95b636c1`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcda00b0c3a86b025e7acc0393e7b903b2a7e0174aa346d91d7ec0647b02082d`  
		Last Modified: Tue, 12 Nov 2024 02:37:27 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:dd862b700b2f279233f9ae16d5c25154680ee1dfcd86f522a853623380c7e63f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 KB (88486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60c4488d7285be9cc92fe8c34981fd09686e9eece95b44097621805a9422d86`

```dockerfile
```

-	Layers:
	-	`sha256:0c0c153d8884f2d689fb54feef58d5b3f507c9257a4da7ef17c63cc34edfbab7`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 74.2 KB (74181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f273e32436d0f59afb7e53948d572f8c2a58adad3690545a558a4a9074424b5`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 14.3 KB (14305 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:5b42c6f2c6f6d4daf16d2b7f02566b892213498a607898ec86fe4f13ba174433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5530602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae2a9c2c8102d9dfaf0e25652471e9e17f0128392eb62b35fd98ecf2ae3a790b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2124325dc5cb0e691b81062d52602d82e66cf4a54d05d890bdf506e6eb914835`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8bc56b9fe431e43e990d6ce1df319af96d7a3c550c23870b2c1051a27fbe06`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 7.6 KB (7555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4007f0c3a790e3d7107168b4005f37de82f1c1c5d974f34ba3933bbc0419ea4a`  
		Last Modified: Tue, 12 Nov 2024 06:29:08 GMT  
		Size: 2.2 MB (2155051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11376d8ca4651e301f66a4e1203da53694eb1be5d78239a60c000768c941525`  
		Last Modified: Tue, 12 Nov 2024 06:29:08 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a2a3ed2d5ea66800cdf4bb8bb04faca0e1725b756688c0d63daf5bcca2d310`  
		Last Modified: Tue, 12 Nov 2024 06:29:08 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:66e0dc5536fdbd525be5c4d9f9f3ae6c4cffce04ff577a831143d54d7876dc1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cf059becbf5ff9f78307636057df7a043c0d5e6d27cb25c8d761b7fba67b075`

```dockerfile
```

-	Layers:
	-	`sha256:2e10f6bc35866f5a553ae9a114eafa57e88f05f4423cbac2a76088422ce325c0`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 14.2 KB (14192 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:f1b28e18aa159ad4b27d738d0e6271ba9f7f14fea5025db3ead37944a1c1d38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5104726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f5914ed409d7a9b8d1d4b37a7f11dafe085591b60fe58b70ea028c271c80290`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3f756621e1fede5561bf3c8b16df49f95f70f146e0dcf052b5be6ab859f7ad`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a57661377f6134602ff6bb1e331bb44ffa59d55b34e7f1afc7758704aa905f`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17e1750441e507ad7e1f0363aabe05175114a5764b1e7ab139af0e89e3e8ae2`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 2.0 MB (2000280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db3501f51148e9fbda41edee3f07843a542820b52626ecebc0d123cff9f86f0`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c83efd7947156d56b945c49da1d15a267824161f7cbb06f182a19f951d46eb`  
		Last Modified: Tue, 12 Nov 2024 15:31:29 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f8e99759c16c5acd111b0a4c9cd95892c25016f5ee89821b4b3146e5fb36a615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 KB (88624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a9f2d3ac23f0f25dd218dfc12896c53ce47fc6066ee717cb9a9a1d076cf976`

```dockerfile
```

-	Layers:
	-	`sha256:f93fe0699906bc92245e1be0751778f7df38efd418fdd621e6f0a882f7176f1d`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 74.2 KB (74217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1987893a490fa099b5341b220483d8eff205a754295987430790b44538df2716`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 14.4 KB (14407 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:53804ac33977b62680e560b74ba5b5d22713391963530048538f60555cfdefeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7006326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90940b6c3a5d028791331563f8e8ed1afdd05d1d06aee6494da2e04dd2b1ffe6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a88c0f1cd0fd5f6079c67eac729ff5a805c5a469e26e47e580751968b7f372`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd36a7367ed608d19a699ca4c0a2062ff5094acc1d3815baf34a01aa293c2714`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 7.6 KB (7563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a95d0832d1bc79736bef4c10b336d5f18b8b548b754a6753537e54c463a1a3`  
		Last Modified: Tue, 12 Nov 2024 10:30:10 GMT  
		Size: 2.9 MB (2909644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9945356ed175181e01d175895b560aaf6dbe437550ce277dd031a8348f84876f`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198174201e9ff5bde070dcb1468a1be3c27943e332be9207cbf99edd10b46552`  
		Last Modified: Tue, 12 Nov 2024 10:30:10 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:0673de50fe1b90d9eba54ceb48d9f764a97f6d383426370685df181b70f7cc63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 KB (88676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6fa5047039d1fadd0ae7378601b830022268a3ada3f00c912dbcdabf45cdea0`

```dockerfile
```

-	Layers:
	-	`sha256:b7546d292551cf31ac3bd93e1e6e162b689c94b9443030c420887493a945351d`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 74.2 KB (74237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95d4514b51e612f28c127e3cff2d26e19284f01ad6b7f8ee94cea702f485a8e0`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 14.4 KB (14439 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; 386

```console
$ docker pull spiped@sha256:6d46f04e30a3105fc3141267e91ffb5ba3050aa7be87148dcc59dd960122b8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5825462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bbcb7b0f29ba9dab0f0c1726527e43ed4016181bd95ab9debba9300da8dad8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97a6fd63828fbfe315eb146a6e09131a00451eb6df7364f89b2838fc8967506`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71549e122188c29598764406aede3a2d7f39ee116980cb024522fa714099248e`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 7.6 KB (7562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9082d20944f15111e92d68546d0843fef30343a5d20401f9dbbbaa559107f7`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 2.3 MB (2347284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a12d1f809df9acb5e86279c66f9f620f87d4359dd8b552217833aabf984c725`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565e15916b0ca46193b8a9e1c83bc74904a8fd5ac8d51710d11a9cd1974c67f2`  
		Last Modified: Tue, 12 Nov 2024 02:10:45 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:ae024814f19ccf108f4c49012d543026dcebbcda6cf432b72e679e80eac307c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 KB (88425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f85c7eb8498f8dab641cf09ac2320681a6bfeb6471034d0b8f17c0413c26f96`

```dockerfile
```

-	Layers:
	-	`sha256:c338f2f328277430db1def5c4614e72997853bf84529ed6d44202ce3949aad37`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 74.2 KB (74156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5902723b69c008d179c3e0da07749f803cb6ad90ba97a9c3feb151d76dadba00`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 14.3 KB (14269 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:8afb3bf99c94a591d0eba15d96253b003415424195f369f761365ded0250911e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5946540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c165f7c09f005647071973ca64009e4fcfbb357266bce909503a70125b3cc603`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acff226d267e2f526a684557f036f58a914c59247be39068651a3bbb5be99c8`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8522a836c3199ccf9b49cd625b0801b4893ca92b819606a20a60eef862d763fa`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0aca5aa27b0c34935f8383d3017c2e1b574336e405b6e683e2fd18f0544bc9d`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 2.4 MB (2365118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39730da67a08ee98eba5461d059c4ae17310847df8147206ae9dd3c915a2a053`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1466bf84e7abe5d6dc8431df5577ea2e1eb5767f85402df0d10e38bd9b21175`  
		Last Modified: Tue, 12 Nov 2024 08:08:13 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:68986bada3dc3e301441051f41dd84386659fa6521bcfba1865e24368e919451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 KB (86614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbbad23dc8d88c7da7f63057b1a78301962cad8edf146f8c53a7fdcd9a7b558`

```dockerfile
```

-	Layers:
	-	`sha256:8af705f7ad2b931357ae0f8d34cff42c83b9ea58f0a34298a04cbebcab791e59`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 72.3 KB (72261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90553d9dcd0f0a8f53c333aed2eed7edd767d790498bd322ce254e64fa3dd8cb`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 14.4 KB (14353 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:da6591d15c86f3bf43fab6ccc0035a0650a5756859870abdd3276d24eedff6a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5551193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b8476d53de131526ad9562517c1b099c24ce9385a5730746d1e83247619389c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46aa88ab9b012a876209b14e6deee5c7982f819f8de6d7b9ed357459d28c597e`  
		Last Modified: Wed, 13 Nov 2024 01:24:28 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5bdf98d05f4226e17074c09dea718e6191052243811401bf5891cdfb4f1005a`  
		Last Modified: Wed, 13 Nov 2024 01:24:28 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1cc53836a810c0768e9eb515600a82be8862a3129239035de56d851625f2890`  
		Last Modified: Wed, 13 Nov 2024 01:24:29 GMT  
		Size: 2.2 MB (2170750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd669ab852fa6faffdff5b54301703ace4f36faf005d628470fcef6f3ba9296`  
		Last Modified: Wed, 13 Nov 2024 01:24:29 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31ad710654b9957b395b764e0751fb8ceb335cd3970bee0870c731d0c9d1631`  
		Last Modified: Wed, 13 Nov 2024 01:24:30 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:35c0217a072785ece237b37268cd30f7410f423b96bd889e56db03a674044795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 KB (86610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21f8f74486982bdb4f701b16321ebb5b430c4a06622f6960273f474bfbb2188e`

```dockerfile
```

-	Layers:
	-	`sha256:88a28221c4fd9d156a4ebf0935fa189d8524bb92c8fdc1d76981cf7435c2056e`  
		Last Modified: Wed, 13 Nov 2024 01:24:28 GMT  
		Size: 72.3 KB (72257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a28652304d303135a92cbe69570122aaa332626746b8080a921073de8775bb3`  
		Last Modified: Wed, 13 Nov 2024 01:24:28 GMT  
		Size: 14.4 KB (14353 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:30464ff5097e65f47e6a755c9c779d3075ff07a1e9de556d11e7c96a7a94bd7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5713802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eb33bd33066b8fc5173e375f27f7f9452ab4ccf03a15c2a86c9ee2c7b389d04`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8899981d6f06508315b3001ebf4f1bde53ab20235caaa013f5ba8c77a73e8adb`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6687c63f48eb23b685aac39d34fd10d946be39a35d263efb7f96ab22c27e5540`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acea042cc930aa404c9b71350854bad5f8f7641916069b37d0d586596d4bbd2d`  
		Last Modified: Tue, 12 Nov 2024 08:43:36 GMT  
		Size: 2.2 MB (2243236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43854f54c63f7333c81ead906bd289eb4a3559aed20097234270a6b9ac8a472c`  
		Last Modified: Tue, 12 Nov 2024 08:43:36 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d137c29c807dddaad7226bf07aa3e0a203dd1839e595b93c07975336ff0379`  
		Last Modified: Tue, 12 Nov 2024 08:43:36 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:0eae92830e9bc1adf13eac44f18f428cde18ca2b63aae15579bcf3fef67941d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 KB (86532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23d8e6d1cfce745a53aeb2213c583ad2b0372bccd118edc86a78c30b8dc0d5b8`

```dockerfile
```

-	Layers:
	-	`sha256:511653a9b9e8708d56eb05048ec62f75f94b92d11463839efcc6c8f9d950ddbd`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 72.2 KB (72227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23d284526c8ef1bc8f766ba9f4b30d40ffacde5f0411805933554ef0edf6dc33`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 14.3 KB (14305 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6.2`

```console
$ docker pull spiped@sha256:7677d10bae50eab7bce723d61c919ef49c2c23d9c8c623a799b235047d821d84
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `spiped:1.6.2` - linux; amd64

```console
$ docker pull spiped@sha256:a7dd97a20081470a35cadd6169785d86caf3bf93d4987ebc5a4ae955bf303419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37105291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b451eb143d5594952a98dae1b0b0ef55ef97e913b3a344634368967860ca265e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd767aded3e0e4a452f4aa3ac09696385e71487127ca9739d1024c9ba463dd6e`  
		Last Modified: Tue, 24 Dec 2024 22:15:30 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9838d1339bbeadb079dd51218b3aade84cf88d1d115d999a4e4a3b1390c6fd4d`  
		Last Modified: Tue, 24 Dec 2024 22:15:30 GMT  
		Size: 2.4 MB (2401313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc193ce4740ac330677795e51eadea142972081c95fb4aee71923f4bce5243a6`  
		Last Modified: Tue, 24 Dec 2024 22:15:30 GMT  
		Size: 6.5 MB (6470860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5809551b454860f1e4058c63d28c028953b2e2ed893867755dfad49a923b71b`  
		Last Modified: Tue, 24 Dec 2024 22:15:30 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf961f7ac0e0eac310dd1632c7de4baf508b1b42e304b43c676e6b0d87003251`  
		Last Modified: Tue, 24 Dec 2024 22:15:31 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2` - unknown; unknown

```console
$ docker pull spiped@sha256:3c0a59ebccbc3c7ef4acba7e77ca62ad7fd18b73c0c346cca42e8c285ef812e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3530854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c03182376f3f3fc440c34bcd0513b7114b779c642cdfaddfd78510e6a4cbc26d`

```dockerfile
```

-	Layers:
	-	`sha256:3ce4c62fb5412f9b49941e62f081b29f85902c6d533daaeaa4a008b619e31115`  
		Last Modified: Tue, 24 Dec 2024 22:15:30 GMT  
		Size: 3.5 MB (3515814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8736e4f073ce4ba6ce28e2b8fd9ac45b95124e6b3f5d7e229a8d4e5cc5fe38f0`  
		Last Modified: Tue, 24 Dec 2024 22:15:30 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2` - linux; arm variant v5

```console
$ docker pull spiped@sha256:5a0ff595b4809d9f657cd755f82afad83a5400ebed7098e1c9e1d4485c696680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32891708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51914d90458025639148f873fa2737154d95a4acf426a39d1531c3a28bd9d634`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1734912000'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:61230a432de02dc9fd57340d88179517d7f651caeb2a5e2fa6ec333d17ed65c5`  
		Last Modified: Tue, 24 Dec 2024 21:33:31 GMT  
		Size: 25.8 MB (25754907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff406d9a466b89f1ee0d62de835144d8a20f4e4090e34b1f99d314c32300fa6`  
		Last Modified: Wed, 25 Dec 2024 01:30:01 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594b7318a0e87718e415649e74ad23b30870383adb319e8129e2e6357cbdffb5`  
		Last Modified: Wed, 25 Dec 2024 01:30:01 GMT  
		Size: 2.0 MB (1997182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9516f1676319d8b0d371e636fabf37d16151918abd539b6e6ac36b86503e6d`  
		Last Modified: Wed, 25 Dec 2024 01:30:01 GMT  
		Size: 5.1 MB (5138080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bfb3f5aa819cbf256ea5483de4b098613c94f4a25dd3ed8178e207ec003c48`  
		Last Modified: Wed, 25 Dec 2024 01:30:01 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e148c2154289a52718590456f627dfcd48b0419ce7ddee43087b88c75cd869f1`  
		Last Modified: Wed, 25 Dec 2024 01:30:01 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2` - unknown; unknown

```console
$ docker pull spiped@sha256:69d4d0d616215b625bef7a1c0b1514bf42fac5c0e5d1b41de1c4711e04a42b77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3501486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f06323f57f358722230b775cbb482532200f4955cf8da6065825b11122ff47f`

```dockerfile
```

-	Layers:
	-	`sha256:6ecc6ea63b5f6f3da3546e6b73304075502f588e6acc90ef3a8e171576b48316`  
		Last Modified: Wed, 25 Dec 2024 01:30:01 GMT  
		Size: 3.5 MB (3486344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85a19088103eac42e407f88234f0df6a4a43a3b22b502e66b2e4a90f8715b1ac`  
		Last Modified: Wed, 25 Dec 2024 01:30:00 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2` - linux; arm variant v7

```console
$ docker pull spiped@sha256:ede738edc1dd3664cdc2056ab1070988ba5b5d5b50c94c0e1c426873eb1fe883
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 MB (30671063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb2b65bc9e81bf68c58ab1fdd7fa057c179c5b191be2380bba0e61fdd126632f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:24f0da30a772db626789cda3e7b0911098d07574c40b30be943d43dec3ed685f`  
		Last Modified: Tue, 24 Dec 2024 21:33:51 GMT  
		Size: 23.9 MB (23933522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381ee1c72da2fe25de158dc79f791a4e5f2640cce1929d519a43ded3ea5e8a90`  
		Last Modified: Wed, 25 Dec 2024 03:28:59 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3dd3a794351508157cfcb738934464fb3ef893c8545d3be6205d6fec4dbbb0`  
		Last Modified: Wed, 25 Dec 2024 03:28:59 GMT  
		Size: 1.9 MB (1855604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c52c57bab55640fb8a84e36fbbb54a20d3afaa69e2090b3a59b1e93bf25067`  
		Last Modified: Wed, 25 Dec 2024 03:28:59 GMT  
		Size: 4.9 MB (4880401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c13ef05b160d3362c6c826f740b9767e4308a41b09f72e0d685c89355ee776`  
		Last Modified: Wed, 25 Dec 2024 03:28:59 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197345a1fb9ad8e6138a397d8df5bc7d45ec166e6e184644bb752ad28b7b5bd0`  
		Last Modified: Wed, 25 Dec 2024 03:29:00 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2` - unknown; unknown

```console
$ docker pull spiped@sha256:eeaa7583a0a22f13495b38c77a31bf4d901a2495c1f9b48530daa385142eb131
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3500976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90fc682623c6de4b402365a3d369ab05ba6ebb046ebe8d29a563d598d97b1cae`

```dockerfile
```

-	Layers:
	-	`sha256:0b21e96fc1d27b03f925dc09a0800453ca5c69103cdc7292ff53064aca0701a3`  
		Last Modified: Wed, 25 Dec 2024 03:29:00 GMT  
		Size: 3.5 MB (3485835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbed3956028284093ae6a4a6b3d472e942fc6c36a001c85a509eb87710e78c96`  
		Last Modified: Wed, 25 Dec 2024 03:28:59 GMT  
		Size: 15.1 KB (15141 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:683cabe7e0eed7297111985eb6618a1960ad0847dc683136c0d994533c1b8696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35788363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f41a2307bf8709f5a95d5444cab15e3d95355c41c58ec6099d7f1ba6f57a2e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f769b1854757b5b4ae5743b8d429389bae7f0381b4be0aa48e86934db98748`  
		Last Modified: Wed, 25 Dec 2024 01:28:10 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9162f0dcd326913bb139c0781a3f428fded3f0baf7a48a0e56bbf8888d8607`  
		Last Modified: Wed, 25 Dec 2024 01:28:10 GMT  
		Size: 2.2 MB (2247004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b572a3c9e43b9eb92754465fbc7cdce3e8618940970c40887e91b1af73f6f933`  
		Last Modified: Wed, 25 Dec 2024 01:28:10 GMT  
		Size: 5.5 MB (5481100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af2cae35c937b304605d6a2d691806a3d816c7f2e32109c5b779e858f5d4cbe`  
		Last Modified: Wed, 25 Dec 2024 01:28:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32afe8fd289c0f8521d68cf2b4f2e1c650e34bc7a288beeb7fe2591ea223d3f0`  
		Last Modified: Wed, 25 Dec 2024 01:28:11 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2` - unknown; unknown

```console
$ docker pull spiped@sha256:b223557fee24382404079822852eba4258babd849ae1e1fbea690ee9f0f74396
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3502216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36302ad039f457150bc5b5ef223e749f9f31cc12131f2bcfbcfab37635663f6a`

```dockerfile
```

-	Layers:
	-	`sha256:479e2b82d5ed62e0627a20bcf029de82590c35225fc11641db3f69c4723440e4`  
		Last Modified: Wed, 25 Dec 2024 01:28:10 GMT  
		Size: 3.5 MB (3487042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e21ed0a3ae7d4cb9c6d7d5e8f71fabcc40673cde1f3c45025b5694a723e26c4`  
		Last Modified: Wed, 25 Dec 2024 01:28:10 GMT  
		Size: 15.2 KB (15174 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2` - linux; 386

```console
$ docker pull spiped@sha256:d3bad81148a63f9e65b6a8e5edb28b22407f9870ac1b9daddb8dd62fb89eaa4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37547000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:381f29b36739ed9815e40d19ed03aef86c4c05e189b507ae287e9c56285da723`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:fba9c0797a7b5bba079e0fd9d815a8878aea58430ea12c84047010f98fbe34d7`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 29.2 MB (29205387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b1e932b36b88542e04dada12c3f21f0f34b8d16e96a07d2182f0ceb3cfc52a`  
		Last Modified: Tue, 24 Dec 2024 22:14:41 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a49d5b20f552856ebdc1f91a1818ed41a9a9c5b31b7191cf1e6f0fc09c95916`  
		Last Modified: Tue, 24 Dec 2024 22:14:41 GMT  
		Size: 2.4 MB (2398659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb97d01b24b3952ed0462f79f171d4926106395407dc96963a036f27f041bee`  
		Last Modified: Tue, 24 Dec 2024 22:14:41 GMT  
		Size: 5.9 MB (5941415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956df477ffa74406f5801dbb1143462f11d46d675392b087e13191d2810bf2d3`  
		Last Modified: Tue, 24 Dec 2024 22:14:41 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e154e0ef38fb7a31b609c417e6eca590c4cd2d87d656d7080a5a92c051be3d86`  
		Last Modified: Tue, 24 Dec 2024 22:14:42 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2` - unknown; unknown

```console
$ docker pull spiped@sha256:094af1deb53cda626632725ba7f785a3213f615908d1a27b653d88e399c296e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67332a7e6a2833848d5d47240f969c1fcbf987e8ddbe6ac3739f79b812e9260d`

```dockerfile
```

-	Layers:
	-	`sha256:e9b7f1f48aad35bf0976821f09af4acdc310a8d7795f1eab0893279d31f5f028`  
		Last Modified: Tue, 24 Dec 2024 22:14:41 GMT  
		Size: 3.5 MB (3509741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa8ea9d57c1c96e289bc572430f49d54b1289bd2768065d0e9d7626693bef7f3`  
		Last Modified: Tue, 24 Dec 2024 22:14:41 GMT  
		Size: 15.0 KB (15004 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2` - linux; mips64le

```console
$ docker pull spiped@sha256:d89a09b29a3053b1374ac6c3b197938d6f41e4c00d5bb716fd65e61d7c97975a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36152100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d8acb258cdf976c86134a73453ccf189b3ecbe6040145d37d213c14ad71531`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1733097600'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:29ac4ae2849b0c84c0ef17659082268617abeb406402ef46b6fa9140e6d2064d`  
		Last Modified: Tue, 03 Dec 2024 01:28:15 GMT  
		Size: 28.5 MB (28505909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2a37d1c3544aae9cf855e4f9d96754f7d5aad9c9a3f7d42a3eb8987d04b10a`  
		Last Modified: Tue, 03 Dec 2024 15:43:23 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687c3b1191976c7d74198e8e57529daabebefb487799f83eb7d8681422ef72b8`  
		Last Modified: Tue, 03 Dec 2024 15:43:24 GMT  
		Size: 1.8 MB (1841107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71cc921943a3967383a50f905dd8868956c3ac63ebb385d9cec2f3cb34a9f87e`  
		Last Modified: Tue, 03 Dec 2024 15:43:24 GMT  
		Size: 5.8 MB (5803545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c26a9ead4b058916305bb6fd71d2599865275170bdb57724c307edf3509f326`  
		Last Modified: Tue, 03 Dec 2024 15:43:23 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9104292331624763e6d460ca187a0f85b64d1f486b86284c07c95592b8e94da1`  
		Last Modified: Tue, 03 Dec 2024 15:43:24 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2` - unknown; unknown

```console
$ docker pull spiped@sha256:ee8a92a1ad8cafc8ea99877f6bfd0d92dc91949f54b840b48821ce544aa9bcda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ab156a72eff661cd8aed8bf33e1b225c9f5f2c967cb69cf1c020b44d53b44d`

```dockerfile
```

-	Layers:
	-	`sha256:2bd3fbc5d440f518558673839c4fcba7382ea6d548360ed2c57eb7bd0f049a65`  
		Last Modified: Tue, 03 Dec 2024 15:43:23 GMT  
		Size: 14.9 KB (14897 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2` - linux; ppc64le

```console
$ docker pull spiped@sha256:fa1c0e0ca44831854510e672c54f19e7f6f438f1b478e6e12eb6fc349cb6036e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41069658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:badc1dcf78bdd756328e48de377c9ac83765d7fd252f4f6aed46a14bd58061e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4a1ea4d3c9e0863e99d27aae6dac9a4b908a6413e758c7785d8fefe555b0e760`  
		Last Modified: Wed, 25 Dec 2024 00:32:48 GMT  
		Size: 32.1 MB (32063240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a10da46285624ad419bea829c84e2e283422614dc35af1abbcae2a21f755880`  
		Last Modified: Wed, 25 Dec 2024 06:00:22 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a18aaec69dfb91f7d658b963b1908aea3dd52a5d0ca1bd2882ce20e4891f72`  
		Last Modified: Wed, 25 Dec 2024 06:00:22 GMT  
		Size: 2.6 MB (2582060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944f472562e3088d879887732f39ea7cd0325819e2e8a179e0bb9564d18b57bb`  
		Last Modified: Wed, 25 Dec 2024 06:00:22 GMT  
		Size: 6.4 MB (6422816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df99d607fa9056ce8bb98db90549b7cbb6134b22361fc8c6293e8b883590d69`  
		Last Modified: Wed, 25 Dec 2024 06:00:22 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a6e26267e78fc9b2b7d66526922f89447996b9b8966d139452965d17fe008d`  
		Last Modified: Wed, 25 Dec 2024 06:00:23 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2` - unknown; unknown

```console
$ docker pull spiped@sha256:39bf9515ccb9ec3a1513b875efcfece99ec844387b12732b93639b1c4dd870c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3516571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ca2573bd1e1ca8bceff7576088a8e2dcc6308a088e8fdc6c45ca47102b82647`

```dockerfile
```

-	Layers:
	-	`sha256:eee07c1e01812a3751985b1f438d18380d58d390e5da5ae1e3bbdca47c05c113`  
		Last Modified: Wed, 25 Dec 2024 06:00:22 GMT  
		Size: 3.5 MB (3501483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb349bf5733a427d8d67d73d6730d8117ab8dc2f68442180e877e7a53062a071`  
		Last Modified: Wed, 25 Dec 2024 06:00:22 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2` - linux; s390x

```console
$ docker pull spiped@sha256:6c8b9b684784fd7e276e9642a6f67e29c09b10a5e70c83ce74be972322034cdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34334969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8363621faa6e61fe5ffedc99a0ac820582911b3efb820dd5c5e56288cfdca21d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:0e7e84bd4cca9e29f08dfac96d436e65bdd31929520e73147137b382fbc89b70`  
		Last Modified: Tue, 24 Dec 2024 21:33:49 GMT  
		Size: 26.9 MB (26878901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc416ec43cf7816408db05f15f973105968e740cadc2d8bf781d0f18b1662e2`  
		Last Modified: Wed, 25 Dec 2024 00:06:46 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43bde2f7b43f7809ecb4a99fef725c7668af05efd43fab2b2de7d0e9cdeed7df`  
		Last Modified: Wed, 25 Dec 2024 00:06:46 GMT  
		Size: 2.1 MB (2068729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c405c4f3d636ce991eec1df48ab2acbafb141f057b012887daeac232eeae8852`  
		Last Modified: Wed, 25 Dec 2024 00:06:46 GMT  
		Size: 5.4 MB (5385800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb5fd31da13e128253de1c3be9f0eaccc9791741f2ddbd7f64c404738ccfceb`  
		Last Modified: Wed, 25 Dec 2024 00:06:46 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67aa610193b9571e7f56cc25183b12debeda63c2b610cd66c4e3029c6fb31fb4`  
		Last Modified: Wed, 25 Dec 2024 00:06:46 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2` - unknown; unknown

```console
$ docker pull spiped@sha256:3d6bf018776d6e6d237fde4d2f785340bcd6e32728626dba860c50d1995f0203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3519040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:054b3ee947046ff8f0f3b14b7e50d2f17b81f1ba09225a49e6d135180a585d01`

```dockerfile
```

-	Layers:
	-	`sha256:be1536a048742b7927962b19f3ec187b33b5f53d994d3883fb3398e0cc303f31`  
		Last Modified: Wed, 25 Dec 2024 00:06:46 GMT  
		Size: 3.5 MB (3504000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3dec620d34fc6d656f7478c968b406037c961f5f26c3e0b72bdd506d2fdceac`  
		Last Modified: Wed, 25 Dec 2024 00:06:46 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6.2-alpine`

```console
$ docker pull spiped@sha256:e32b4b32ec1bebd57bcef51d51943394d621e20004e559d74d0a5fadbb262fc5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `spiped:1.6.2-alpine` - linux; amd64

```console
$ docker pull spiped@sha256:daefb5299ff2e9476112aa9c609b5264e2c34f92126f0bb20e29d5c14ef90fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6132905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29aab44abfc742685430558f3458335cf0cd806c6d386b3eed8c756a4666be89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44372b8a42e415e28022098de7f58892719831ddb3b69d1982475c01e1ebcee9`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4d3d0195931e82893a059b29aa5e09859b561a5699199003caa76db025a103`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 7.6 KB (7552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faaff9889bcd7686a7e389188c9b1da11b944593c3f367ce73321c9cd1f9f4d3`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 2.5 MB (2500052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742ceb23f0c29b5b00035c6ae582d5ff76d9120d036d2c2963228c0b95b636c1`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcda00b0c3a86b025e7acc0393e7b903b2a7e0174aa346d91d7ec0647b02082d`  
		Last Modified: Tue, 12 Nov 2024 02:37:27 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:dd862b700b2f279233f9ae16d5c25154680ee1dfcd86f522a853623380c7e63f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 KB (88486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60c4488d7285be9cc92fe8c34981fd09686e9eece95b44097621805a9422d86`

```dockerfile
```

-	Layers:
	-	`sha256:0c0c153d8884f2d689fb54feef58d5b3f507c9257a4da7ef17c63cc34edfbab7`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 74.2 KB (74181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f273e32436d0f59afb7e53948d572f8c2a58adad3690545a558a4a9074424b5`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 14.3 KB (14305 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:5b42c6f2c6f6d4daf16d2b7f02566b892213498a607898ec86fe4f13ba174433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5530602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae2a9c2c8102d9dfaf0e25652471e9e17f0128392eb62b35fd98ecf2ae3a790b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2124325dc5cb0e691b81062d52602d82e66cf4a54d05d890bdf506e6eb914835`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8bc56b9fe431e43e990d6ce1df319af96d7a3c550c23870b2c1051a27fbe06`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 7.6 KB (7555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4007f0c3a790e3d7107168b4005f37de82f1c1c5d974f34ba3933bbc0419ea4a`  
		Last Modified: Tue, 12 Nov 2024 06:29:08 GMT  
		Size: 2.2 MB (2155051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11376d8ca4651e301f66a4e1203da53694eb1be5d78239a60c000768c941525`  
		Last Modified: Tue, 12 Nov 2024 06:29:08 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a2a3ed2d5ea66800cdf4bb8bb04faca0e1725b756688c0d63daf5bcca2d310`  
		Last Modified: Tue, 12 Nov 2024 06:29:08 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:66e0dc5536fdbd525be5c4d9f9f3ae6c4cffce04ff577a831143d54d7876dc1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cf059becbf5ff9f78307636057df7a043c0d5e6d27cb25c8d761b7fba67b075`

```dockerfile
```

-	Layers:
	-	`sha256:2e10f6bc35866f5a553ae9a114eafa57e88f05f4423cbac2a76088422ce325c0`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 14.2 KB (14192 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:f1b28e18aa159ad4b27d738d0e6271ba9f7f14fea5025db3ead37944a1c1d38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5104726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f5914ed409d7a9b8d1d4b37a7f11dafe085591b60fe58b70ea028c271c80290`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3f756621e1fede5561bf3c8b16df49f95f70f146e0dcf052b5be6ab859f7ad`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a57661377f6134602ff6bb1e331bb44ffa59d55b34e7f1afc7758704aa905f`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17e1750441e507ad7e1f0363aabe05175114a5764b1e7ab139af0e89e3e8ae2`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 2.0 MB (2000280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db3501f51148e9fbda41edee3f07843a542820b52626ecebc0d123cff9f86f0`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c83efd7947156d56b945c49da1d15a267824161f7cbb06f182a19f951d46eb`  
		Last Modified: Tue, 12 Nov 2024 15:31:29 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f8e99759c16c5acd111b0a4c9cd95892c25016f5ee89821b4b3146e5fb36a615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 KB (88624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a9f2d3ac23f0f25dd218dfc12896c53ce47fc6066ee717cb9a9a1d076cf976`

```dockerfile
```

-	Layers:
	-	`sha256:f93fe0699906bc92245e1be0751778f7df38efd418fdd621e6f0a882f7176f1d`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 74.2 KB (74217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1987893a490fa099b5341b220483d8eff205a754295987430790b44538df2716`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 14.4 KB (14407 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:53804ac33977b62680e560b74ba5b5d22713391963530048538f60555cfdefeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7006326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90940b6c3a5d028791331563f8e8ed1afdd05d1d06aee6494da2e04dd2b1ffe6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a88c0f1cd0fd5f6079c67eac729ff5a805c5a469e26e47e580751968b7f372`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd36a7367ed608d19a699ca4c0a2062ff5094acc1d3815baf34a01aa293c2714`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 7.6 KB (7563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a95d0832d1bc79736bef4c10b336d5f18b8b548b754a6753537e54c463a1a3`  
		Last Modified: Tue, 12 Nov 2024 10:30:10 GMT  
		Size: 2.9 MB (2909644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9945356ed175181e01d175895b560aaf6dbe437550ce277dd031a8348f84876f`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198174201e9ff5bde070dcb1468a1be3c27943e332be9207cbf99edd10b46552`  
		Last Modified: Tue, 12 Nov 2024 10:30:10 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:0673de50fe1b90d9eba54ceb48d9f764a97f6d383426370685df181b70f7cc63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 KB (88676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6fa5047039d1fadd0ae7378601b830022268a3ada3f00c912dbcdabf45cdea0`

```dockerfile
```

-	Layers:
	-	`sha256:b7546d292551cf31ac3bd93e1e6e162b689c94b9443030c420887493a945351d`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 74.2 KB (74237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95d4514b51e612f28c127e3cff2d26e19284f01ad6b7f8ee94cea702f485a8e0`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 14.4 KB (14439 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2-alpine` - linux; 386

```console
$ docker pull spiped@sha256:6d46f04e30a3105fc3141267e91ffb5ba3050aa7be87148dcc59dd960122b8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5825462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bbcb7b0f29ba9dab0f0c1726527e43ed4016181bd95ab9debba9300da8dad8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97a6fd63828fbfe315eb146a6e09131a00451eb6df7364f89b2838fc8967506`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71549e122188c29598764406aede3a2d7f39ee116980cb024522fa714099248e`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 7.6 KB (7562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9082d20944f15111e92d68546d0843fef30343a5d20401f9dbbbaa559107f7`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 2.3 MB (2347284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a12d1f809df9acb5e86279c66f9f620f87d4359dd8b552217833aabf984c725`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565e15916b0ca46193b8a9e1c83bc74904a8fd5ac8d51710d11a9cd1974c67f2`  
		Last Modified: Tue, 12 Nov 2024 02:10:45 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:ae024814f19ccf108f4c49012d543026dcebbcda6cf432b72e679e80eac307c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 KB (88425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f85c7eb8498f8dab641cf09ac2320681a6bfeb6471034d0b8f17c0413c26f96`

```dockerfile
```

-	Layers:
	-	`sha256:c338f2f328277430db1def5c4614e72997853bf84529ed6d44202ce3949aad37`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 74.2 KB (74156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5902723b69c008d179c3e0da07749f803cb6ad90ba97a9c3feb151d76dadba00`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 14.3 KB (14269 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:8afb3bf99c94a591d0eba15d96253b003415424195f369f761365ded0250911e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5946540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c165f7c09f005647071973ca64009e4fcfbb357266bce909503a70125b3cc603`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acff226d267e2f526a684557f036f58a914c59247be39068651a3bbb5be99c8`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8522a836c3199ccf9b49cd625b0801b4893ca92b819606a20a60eef862d763fa`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0aca5aa27b0c34935f8383d3017c2e1b574336e405b6e683e2fd18f0544bc9d`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 2.4 MB (2365118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39730da67a08ee98eba5461d059c4ae17310847df8147206ae9dd3c915a2a053`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1466bf84e7abe5d6dc8431df5577ea2e1eb5767f85402df0d10e38bd9b21175`  
		Last Modified: Tue, 12 Nov 2024 08:08:13 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:68986bada3dc3e301441051f41dd84386659fa6521bcfba1865e24368e919451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 KB (86614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbbad23dc8d88c7da7f63057b1a78301962cad8edf146f8c53a7fdcd9a7b558`

```dockerfile
```

-	Layers:
	-	`sha256:8af705f7ad2b931357ae0f8d34cff42c83b9ea58f0a34298a04cbebcab791e59`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 72.3 KB (72261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90553d9dcd0f0a8f53c333aed2eed7edd767d790498bd322ce254e64fa3dd8cb`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 14.4 KB (14353 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:da6591d15c86f3bf43fab6ccc0035a0650a5756859870abdd3276d24eedff6a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5551193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b8476d53de131526ad9562517c1b099c24ce9385a5730746d1e83247619389c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46aa88ab9b012a876209b14e6deee5c7982f819f8de6d7b9ed357459d28c597e`  
		Last Modified: Wed, 13 Nov 2024 01:24:28 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5bdf98d05f4226e17074c09dea718e6191052243811401bf5891cdfb4f1005a`  
		Last Modified: Wed, 13 Nov 2024 01:24:28 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1cc53836a810c0768e9eb515600a82be8862a3129239035de56d851625f2890`  
		Last Modified: Wed, 13 Nov 2024 01:24:29 GMT  
		Size: 2.2 MB (2170750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd669ab852fa6faffdff5b54301703ace4f36faf005d628470fcef6f3ba9296`  
		Last Modified: Wed, 13 Nov 2024 01:24:29 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31ad710654b9957b395b764e0751fb8ceb335cd3970bee0870c731d0c9d1631`  
		Last Modified: Wed, 13 Nov 2024 01:24:30 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:35c0217a072785ece237b37268cd30f7410f423b96bd889e56db03a674044795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 KB (86610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21f8f74486982bdb4f701b16321ebb5b430c4a06622f6960273f474bfbb2188e`

```dockerfile
```

-	Layers:
	-	`sha256:88a28221c4fd9d156a4ebf0935fa189d8524bb92c8fdc1d76981cf7435c2056e`  
		Last Modified: Wed, 13 Nov 2024 01:24:28 GMT  
		Size: 72.3 KB (72257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a28652304d303135a92cbe69570122aaa332626746b8080a921073de8775bb3`  
		Last Modified: Wed, 13 Nov 2024 01:24:28 GMT  
		Size: 14.4 KB (14353 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:30464ff5097e65f47e6a755c9c779d3075ff07a1e9de556d11e7c96a7a94bd7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5713802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eb33bd33066b8fc5173e375f27f7f9452ab4ccf03a15c2a86c9ee2c7b389d04`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8899981d6f06508315b3001ebf4f1bde53ab20235caaa013f5ba8c77a73e8adb`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6687c63f48eb23b685aac39d34fd10d946be39a35d263efb7f96ab22c27e5540`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acea042cc930aa404c9b71350854bad5f8f7641916069b37d0d586596d4bbd2d`  
		Last Modified: Tue, 12 Nov 2024 08:43:36 GMT  
		Size: 2.2 MB (2243236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43854f54c63f7333c81ead906bd289eb4a3559aed20097234270a6b9ac8a472c`  
		Last Modified: Tue, 12 Nov 2024 08:43:36 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d137c29c807dddaad7226bf07aa3e0a203dd1839e595b93c07975336ff0379`  
		Last Modified: Tue, 12 Nov 2024 08:43:36 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:0eae92830e9bc1adf13eac44f18f428cde18ca2b63aae15579bcf3fef67941d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 KB (86532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23d8e6d1cfce745a53aeb2213c583ad2b0372bccd118edc86a78c30b8dc0d5b8`

```dockerfile
```

-	Layers:
	-	`sha256:511653a9b9e8708d56eb05048ec62f75f94b92d11463839efcc6c8f9d950ddbd`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 72.2 KB (72227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23d284526c8ef1bc8f766ba9f4b30d40ffacde5f0411805933554ef0edf6dc33`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 14.3 KB (14305 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:alpine`

```console
$ docker pull spiped@sha256:e32b4b32ec1bebd57bcef51d51943394d621e20004e559d74d0a5fadbb262fc5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `spiped:alpine` - linux; amd64

```console
$ docker pull spiped@sha256:daefb5299ff2e9476112aa9c609b5264e2c34f92126f0bb20e29d5c14ef90fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6132905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29aab44abfc742685430558f3458335cf0cd806c6d386b3eed8c756a4666be89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44372b8a42e415e28022098de7f58892719831ddb3b69d1982475c01e1ebcee9`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4d3d0195931e82893a059b29aa5e09859b561a5699199003caa76db025a103`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 7.6 KB (7552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faaff9889bcd7686a7e389188c9b1da11b944593c3f367ce73321c9cd1f9f4d3`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 2.5 MB (2500052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742ceb23f0c29b5b00035c6ae582d5ff76d9120d036d2c2963228c0b95b636c1`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcda00b0c3a86b025e7acc0393e7b903b2a7e0174aa346d91d7ec0647b02082d`  
		Last Modified: Tue, 12 Nov 2024 02:37:27 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:dd862b700b2f279233f9ae16d5c25154680ee1dfcd86f522a853623380c7e63f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 KB (88486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60c4488d7285be9cc92fe8c34981fd09686e9eece95b44097621805a9422d86`

```dockerfile
```

-	Layers:
	-	`sha256:0c0c153d8884f2d689fb54feef58d5b3f507c9257a4da7ef17c63cc34edfbab7`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 74.2 KB (74181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f273e32436d0f59afb7e53948d572f8c2a58adad3690545a558a4a9074424b5`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 14.3 KB (14305 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:5b42c6f2c6f6d4daf16d2b7f02566b892213498a607898ec86fe4f13ba174433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5530602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae2a9c2c8102d9dfaf0e25652471e9e17f0128392eb62b35fd98ecf2ae3a790b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2124325dc5cb0e691b81062d52602d82e66cf4a54d05d890bdf506e6eb914835`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8bc56b9fe431e43e990d6ce1df319af96d7a3c550c23870b2c1051a27fbe06`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 7.6 KB (7555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4007f0c3a790e3d7107168b4005f37de82f1c1c5d974f34ba3933bbc0419ea4a`  
		Last Modified: Tue, 12 Nov 2024 06:29:08 GMT  
		Size: 2.2 MB (2155051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11376d8ca4651e301f66a4e1203da53694eb1be5d78239a60c000768c941525`  
		Last Modified: Tue, 12 Nov 2024 06:29:08 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a2a3ed2d5ea66800cdf4bb8bb04faca0e1725b756688c0d63daf5bcca2d310`  
		Last Modified: Tue, 12 Nov 2024 06:29:08 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:66e0dc5536fdbd525be5c4d9f9f3ae6c4cffce04ff577a831143d54d7876dc1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cf059becbf5ff9f78307636057df7a043c0d5e6d27cb25c8d761b7fba67b075`

```dockerfile
```

-	Layers:
	-	`sha256:2e10f6bc35866f5a553ae9a114eafa57e88f05f4423cbac2a76088422ce325c0`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 14.2 KB (14192 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:f1b28e18aa159ad4b27d738d0e6271ba9f7f14fea5025db3ead37944a1c1d38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5104726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f5914ed409d7a9b8d1d4b37a7f11dafe085591b60fe58b70ea028c271c80290`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3f756621e1fede5561bf3c8b16df49f95f70f146e0dcf052b5be6ab859f7ad`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a57661377f6134602ff6bb1e331bb44ffa59d55b34e7f1afc7758704aa905f`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17e1750441e507ad7e1f0363aabe05175114a5764b1e7ab139af0e89e3e8ae2`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 2.0 MB (2000280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db3501f51148e9fbda41edee3f07843a542820b52626ecebc0d123cff9f86f0`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c83efd7947156d56b945c49da1d15a267824161f7cbb06f182a19f951d46eb`  
		Last Modified: Tue, 12 Nov 2024 15:31:29 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f8e99759c16c5acd111b0a4c9cd95892c25016f5ee89821b4b3146e5fb36a615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 KB (88624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a9f2d3ac23f0f25dd218dfc12896c53ce47fc6066ee717cb9a9a1d076cf976`

```dockerfile
```

-	Layers:
	-	`sha256:f93fe0699906bc92245e1be0751778f7df38efd418fdd621e6f0a882f7176f1d`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 74.2 KB (74217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1987893a490fa099b5341b220483d8eff205a754295987430790b44538df2716`  
		Last Modified: Tue, 12 Nov 2024 15:31:28 GMT  
		Size: 14.4 KB (14407 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:53804ac33977b62680e560b74ba5b5d22713391963530048538f60555cfdefeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7006326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90940b6c3a5d028791331563f8e8ed1afdd05d1d06aee6494da2e04dd2b1ffe6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a88c0f1cd0fd5f6079c67eac729ff5a805c5a469e26e47e580751968b7f372`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd36a7367ed608d19a699ca4c0a2062ff5094acc1d3815baf34a01aa293c2714`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 7.6 KB (7563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a95d0832d1bc79736bef4c10b336d5f18b8b548b754a6753537e54c463a1a3`  
		Last Modified: Tue, 12 Nov 2024 10:30:10 GMT  
		Size: 2.9 MB (2909644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9945356ed175181e01d175895b560aaf6dbe437550ce277dd031a8348f84876f`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198174201e9ff5bde070dcb1468a1be3c27943e332be9207cbf99edd10b46552`  
		Last Modified: Tue, 12 Nov 2024 10:30:10 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:0673de50fe1b90d9eba54ceb48d9f764a97f6d383426370685df181b70f7cc63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 KB (88676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6fa5047039d1fadd0ae7378601b830022268a3ada3f00c912dbcdabf45cdea0`

```dockerfile
```

-	Layers:
	-	`sha256:b7546d292551cf31ac3bd93e1e6e162b689c94b9443030c420887493a945351d`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 74.2 KB (74237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95d4514b51e612f28c127e3cff2d26e19284f01ad6b7f8ee94cea702f485a8e0`  
		Last Modified: Tue, 12 Nov 2024 10:30:09 GMT  
		Size: 14.4 KB (14439 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; 386

```console
$ docker pull spiped@sha256:6d46f04e30a3105fc3141267e91ffb5ba3050aa7be87148dcc59dd960122b8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5825462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bbcb7b0f29ba9dab0f0c1726527e43ed4016181bd95ab9debba9300da8dad8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97a6fd63828fbfe315eb146a6e09131a00451eb6df7364f89b2838fc8967506`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71549e122188c29598764406aede3a2d7f39ee116980cb024522fa714099248e`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 7.6 KB (7562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9082d20944f15111e92d68546d0843fef30343a5d20401f9dbbbaa559107f7`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 2.3 MB (2347284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a12d1f809df9acb5e86279c66f9f620f87d4359dd8b552217833aabf984c725`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565e15916b0ca46193b8a9e1c83bc74904a8fd5ac8d51710d11a9cd1974c67f2`  
		Last Modified: Tue, 12 Nov 2024 02:10:45 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:ae024814f19ccf108f4c49012d543026dcebbcda6cf432b72e679e80eac307c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 KB (88425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f85c7eb8498f8dab641cf09ac2320681a6bfeb6471034d0b8f17c0413c26f96`

```dockerfile
```

-	Layers:
	-	`sha256:c338f2f328277430db1def5c4614e72997853bf84529ed6d44202ce3949aad37`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 74.2 KB (74156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5902723b69c008d179c3e0da07749f803cb6ad90ba97a9c3feb151d76dadba00`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 14.3 KB (14269 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:8afb3bf99c94a591d0eba15d96253b003415424195f369f761365ded0250911e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5946540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c165f7c09f005647071973ca64009e4fcfbb357266bce909503a70125b3cc603`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acff226d267e2f526a684557f036f58a914c59247be39068651a3bbb5be99c8`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8522a836c3199ccf9b49cd625b0801b4893ca92b819606a20a60eef862d763fa`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0aca5aa27b0c34935f8383d3017c2e1b574336e405b6e683e2fd18f0544bc9d`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 2.4 MB (2365118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39730da67a08ee98eba5461d059c4ae17310847df8147206ae9dd3c915a2a053`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1466bf84e7abe5d6dc8431df5577ea2e1eb5767f85402df0d10e38bd9b21175`  
		Last Modified: Tue, 12 Nov 2024 08:08:13 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:68986bada3dc3e301441051f41dd84386659fa6521bcfba1865e24368e919451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 KB (86614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbbad23dc8d88c7da7f63057b1a78301962cad8edf146f8c53a7fdcd9a7b558`

```dockerfile
```

-	Layers:
	-	`sha256:8af705f7ad2b931357ae0f8d34cff42c83b9ea58f0a34298a04cbebcab791e59`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 72.3 KB (72261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90553d9dcd0f0a8f53c333aed2eed7edd767d790498bd322ce254e64fa3dd8cb`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 14.4 KB (14353 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:da6591d15c86f3bf43fab6ccc0035a0650a5756859870abdd3276d24eedff6a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5551193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b8476d53de131526ad9562517c1b099c24ce9385a5730746d1e83247619389c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46aa88ab9b012a876209b14e6deee5c7982f819f8de6d7b9ed357459d28c597e`  
		Last Modified: Wed, 13 Nov 2024 01:24:28 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5bdf98d05f4226e17074c09dea718e6191052243811401bf5891cdfb4f1005a`  
		Last Modified: Wed, 13 Nov 2024 01:24:28 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1cc53836a810c0768e9eb515600a82be8862a3129239035de56d851625f2890`  
		Last Modified: Wed, 13 Nov 2024 01:24:29 GMT  
		Size: 2.2 MB (2170750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd669ab852fa6faffdff5b54301703ace4f36faf005d628470fcef6f3ba9296`  
		Last Modified: Wed, 13 Nov 2024 01:24:29 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31ad710654b9957b395b764e0751fb8ceb335cd3970bee0870c731d0c9d1631`  
		Last Modified: Wed, 13 Nov 2024 01:24:30 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:35c0217a072785ece237b37268cd30f7410f423b96bd889e56db03a674044795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 KB (86610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21f8f74486982bdb4f701b16321ebb5b430c4a06622f6960273f474bfbb2188e`

```dockerfile
```

-	Layers:
	-	`sha256:88a28221c4fd9d156a4ebf0935fa189d8524bb92c8fdc1d76981cf7435c2056e`  
		Last Modified: Wed, 13 Nov 2024 01:24:28 GMT  
		Size: 72.3 KB (72257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a28652304d303135a92cbe69570122aaa332626746b8080a921073de8775bb3`  
		Last Modified: Wed, 13 Nov 2024 01:24:28 GMT  
		Size: 14.4 KB (14353 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; s390x

```console
$ docker pull spiped@sha256:30464ff5097e65f47e6a755c9c779d3075ff07a1e9de556d11e7c96a7a94bd7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5713802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eb33bd33066b8fc5173e375f27f7f9452ab4ccf03a15c2a86c9ee2c7b389d04`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8899981d6f06508315b3001ebf4f1bde53ab20235caaa013f5ba8c77a73e8adb`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6687c63f48eb23b685aac39d34fd10d946be39a35d263efb7f96ab22c27e5540`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acea042cc930aa404c9b71350854bad5f8f7641916069b37d0d586596d4bbd2d`  
		Last Modified: Tue, 12 Nov 2024 08:43:36 GMT  
		Size: 2.2 MB (2243236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43854f54c63f7333c81ead906bd289eb4a3559aed20097234270a6b9ac8a472c`  
		Last Modified: Tue, 12 Nov 2024 08:43:36 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d137c29c807dddaad7226bf07aa3e0a203dd1839e595b93c07975336ff0379`  
		Last Modified: Tue, 12 Nov 2024 08:43:36 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:0eae92830e9bc1adf13eac44f18f428cde18ca2b63aae15579bcf3fef67941d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 KB (86532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23d8e6d1cfce745a53aeb2213c583ad2b0372bccd118edc86a78c30b8dc0d5b8`

```dockerfile
```

-	Layers:
	-	`sha256:511653a9b9e8708d56eb05048ec62f75f94b92d11463839efcc6c8f9d950ddbd`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 72.2 KB (72227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23d284526c8ef1bc8f766ba9f4b30d40ffacde5f0411805933554ef0edf6dc33`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 14.3 KB (14305 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:latest`

```console
$ docker pull spiped@sha256:7677d10bae50eab7bce723d61c919ef49c2c23d9c8c623a799b235047d821d84
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `spiped:latest` - linux; amd64

```console
$ docker pull spiped@sha256:a7dd97a20081470a35cadd6169785d86caf3bf93d4987ebc5a4ae955bf303419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37105291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b451eb143d5594952a98dae1b0b0ef55ef97e913b3a344634368967860ca265e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd767aded3e0e4a452f4aa3ac09696385e71487127ca9739d1024c9ba463dd6e`  
		Last Modified: Tue, 24 Dec 2024 22:15:30 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9838d1339bbeadb079dd51218b3aade84cf88d1d115d999a4e4a3b1390c6fd4d`  
		Last Modified: Tue, 24 Dec 2024 22:15:30 GMT  
		Size: 2.4 MB (2401313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc193ce4740ac330677795e51eadea142972081c95fb4aee71923f4bce5243a6`  
		Last Modified: Tue, 24 Dec 2024 22:15:30 GMT  
		Size: 6.5 MB (6470860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5809551b454860f1e4058c63d28c028953b2e2ed893867755dfad49a923b71b`  
		Last Modified: Tue, 24 Dec 2024 22:15:30 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf961f7ac0e0eac310dd1632c7de4baf508b1b42e304b43c676e6b0d87003251`  
		Last Modified: Tue, 24 Dec 2024 22:15:31 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:3c0a59ebccbc3c7ef4acba7e77ca62ad7fd18b73c0c346cca42e8c285ef812e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3530854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c03182376f3f3fc440c34bcd0513b7114b779c642cdfaddfd78510e6a4cbc26d`

```dockerfile
```

-	Layers:
	-	`sha256:3ce4c62fb5412f9b49941e62f081b29f85902c6d533daaeaa4a008b619e31115`  
		Last Modified: Tue, 24 Dec 2024 22:15:30 GMT  
		Size: 3.5 MB (3515814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8736e4f073ce4ba6ce28e2b8fd9ac45b95124e6b3f5d7e229a8d4e5cc5fe38f0`  
		Last Modified: Tue, 24 Dec 2024 22:15:30 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v5

```console
$ docker pull spiped@sha256:5a0ff595b4809d9f657cd755f82afad83a5400ebed7098e1c9e1d4485c696680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32891708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51914d90458025639148f873fa2737154d95a4acf426a39d1531c3a28bd9d634`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1734912000'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:61230a432de02dc9fd57340d88179517d7f651caeb2a5e2fa6ec333d17ed65c5`  
		Last Modified: Tue, 24 Dec 2024 21:33:31 GMT  
		Size: 25.8 MB (25754907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff406d9a466b89f1ee0d62de835144d8a20f4e4090e34b1f99d314c32300fa6`  
		Last Modified: Wed, 25 Dec 2024 01:30:01 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594b7318a0e87718e415649e74ad23b30870383adb319e8129e2e6357cbdffb5`  
		Last Modified: Wed, 25 Dec 2024 01:30:01 GMT  
		Size: 2.0 MB (1997182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9516f1676319d8b0d371e636fabf37d16151918abd539b6e6ac36b86503e6d`  
		Last Modified: Wed, 25 Dec 2024 01:30:01 GMT  
		Size: 5.1 MB (5138080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bfb3f5aa819cbf256ea5483de4b098613c94f4a25dd3ed8178e207ec003c48`  
		Last Modified: Wed, 25 Dec 2024 01:30:01 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e148c2154289a52718590456f627dfcd48b0419ce7ddee43087b88c75cd869f1`  
		Last Modified: Wed, 25 Dec 2024 01:30:01 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:69d4d0d616215b625bef7a1c0b1514bf42fac5c0e5d1b41de1c4711e04a42b77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3501486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f06323f57f358722230b775cbb482532200f4955cf8da6065825b11122ff47f`

```dockerfile
```

-	Layers:
	-	`sha256:6ecc6ea63b5f6f3da3546e6b73304075502f588e6acc90ef3a8e171576b48316`  
		Last Modified: Wed, 25 Dec 2024 01:30:01 GMT  
		Size: 3.5 MB (3486344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85a19088103eac42e407f88234f0df6a4a43a3b22b502e66b2e4a90f8715b1ac`  
		Last Modified: Wed, 25 Dec 2024 01:30:00 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v7

```console
$ docker pull spiped@sha256:ede738edc1dd3664cdc2056ab1070988ba5b5d5b50c94c0e1c426873eb1fe883
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 MB (30671063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb2b65bc9e81bf68c58ab1fdd7fa057c179c5b191be2380bba0e61fdd126632f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:24f0da30a772db626789cda3e7b0911098d07574c40b30be943d43dec3ed685f`  
		Last Modified: Tue, 24 Dec 2024 21:33:51 GMT  
		Size: 23.9 MB (23933522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381ee1c72da2fe25de158dc79f791a4e5f2640cce1929d519a43ded3ea5e8a90`  
		Last Modified: Wed, 25 Dec 2024 03:28:59 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3dd3a794351508157cfcb738934464fb3ef893c8545d3be6205d6fec4dbbb0`  
		Last Modified: Wed, 25 Dec 2024 03:28:59 GMT  
		Size: 1.9 MB (1855604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c52c57bab55640fb8a84e36fbbb54a20d3afaa69e2090b3a59b1e93bf25067`  
		Last Modified: Wed, 25 Dec 2024 03:28:59 GMT  
		Size: 4.9 MB (4880401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c13ef05b160d3362c6c826f740b9767e4308a41b09f72e0d685c89355ee776`  
		Last Modified: Wed, 25 Dec 2024 03:28:59 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197345a1fb9ad8e6138a397d8df5bc7d45ec166e6e184644bb752ad28b7b5bd0`  
		Last Modified: Wed, 25 Dec 2024 03:29:00 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:eeaa7583a0a22f13495b38c77a31bf4d901a2495c1f9b48530daa385142eb131
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3500976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90fc682623c6de4b402365a3d369ab05ba6ebb046ebe8d29a563d598d97b1cae`

```dockerfile
```

-	Layers:
	-	`sha256:0b21e96fc1d27b03f925dc09a0800453ca5c69103cdc7292ff53064aca0701a3`  
		Last Modified: Wed, 25 Dec 2024 03:29:00 GMT  
		Size: 3.5 MB (3485835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbed3956028284093ae6a4a6b3d472e942fc6c36a001c85a509eb87710e78c96`  
		Last Modified: Wed, 25 Dec 2024 03:28:59 GMT  
		Size: 15.1 KB (15141 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:683cabe7e0eed7297111985eb6618a1960ad0847dc683136c0d994533c1b8696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35788363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f41a2307bf8709f5a95d5444cab15e3d95355c41c58ec6099d7f1ba6f57a2e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f769b1854757b5b4ae5743b8d429389bae7f0381b4be0aa48e86934db98748`  
		Last Modified: Wed, 25 Dec 2024 01:28:10 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9162f0dcd326913bb139c0781a3f428fded3f0baf7a48a0e56bbf8888d8607`  
		Last Modified: Wed, 25 Dec 2024 01:28:10 GMT  
		Size: 2.2 MB (2247004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b572a3c9e43b9eb92754465fbc7cdce3e8618940970c40887e91b1af73f6f933`  
		Last Modified: Wed, 25 Dec 2024 01:28:10 GMT  
		Size: 5.5 MB (5481100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af2cae35c937b304605d6a2d691806a3d816c7f2e32109c5b779e858f5d4cbe`  
		Last Modified: Wed, 25 Dec 2024 01:28:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32afe8fd289c0f8521d68cf2b4f2e1c650e34bc7a288beeb7fe2591ea223d3f0`  
		Last Modified: Wed, 25 Dec 2024 01:28:11 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:b223557fee24382404079822852eba4258babd849ae1e1fbea690ee9f0f74396
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3502216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36302ad039f457150bc5b5ef223e749f9f31cc12131f2bcfbcfab37635663f6a`

```dockerfile
```

-	Layers:
	-	`sha256:479e2b82d5ed62e0627a20bcf029de82590c35225fc11641db3f69c4723440e4`  
		Last Modified: Wed, 25 Dec 2024 01:28:10 GMT  
		Size: 3.5 MB (3487042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e21ed0a3ae7d4cb9c6d7d5e8f71fabcc40673cde1f3c45025b5694a723e26c4`  
		Last Modified: Wed, 25 Dec 2024 01:28:10 GMT  
		Size: 15.2 KB (15174 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; 386

```console
$ docker pull spiped@sha256:d3bad81148a63f9e65b6a8e5edb28b22407f9870ac1b9daddb8dd62fb89eaa4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37547000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:381f29b36739ed9815e40d19ed03aef86c4c05e189b507ae287e9c56285da723`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:fba9c0797a7b5bba079e0fd9d815a8878aea58430ea12c84047010f98fbe34d7`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 29.2 MB (29205387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b1e932b36b88542e04dada12c3f21f0f34b8d16e96a07d2182f0ceb3cfc52a`  
		Last Modified: Tue, 24 Dec 2024 22:14:41 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a49d5b20f552856ebdc1f91a1818ed41a9a9c5b31b7191cf1e6f0fc09c95916`  
		Last Modified: Tue, 24 Dec 2024 22:14:41 GMT  
		Size: 2.4 MB (2398659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb97d01b24b3952ed0462f79f171d4926106395407dc96963a036f27f041bee`  
		Last Modified: Tue, 24 Dec 2024 22:14:41 GMT  
		Size: 5.9 MB (5941415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956df477ffa74406f5801dbb1143462f11d46d675392b087e13191d2810bf2d3`  
		Last Modified: Tue, 24 Dec 2024 22:14:41 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e154e0ef38fb7a31b609c417e6eca590c4cd2d87d656d7080a5a92c051be3d86`  
		Last Modified: Tue, 24 Dec 2024 22:14:42 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:094af1deb53cda626632725ba7f785a3213f615908d1a27b653d88e399c296e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67332a7e6a2833848d5d47240f969c1fcbf987e8ddbe6ac3739f79b812e9260d`

```dockerfile
```

-	Layers:
	-	`sha256:e9b7f1f48aad35bf0976821f09af4acdc310a8d7795f1eab0893279d31f5f028`  
		Last Modified: Tue, 24 Dec 2024 22:14:41 GMT  
		Size: 3.5 MB (3509741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa8ea9d57c1c96e289bc572430f49d54b1289bd2768065d0e9d7626693bef7f3`  
		Last Modified: Tue, 24 Dec 2024 22:14:41 GMT  
		Size: 15.0 KB (15004 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; mips64le

```console
$ docker pull spiped@sha256:d89a09b29a3053b1374ac6c3b197938d6f41e4c00d5bb716fd65e61d7c97975a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36152100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d8acb258cdf976c86134a73453ccf189b3ecbe6040145d37d213c14ad71531`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1733097600'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:29ac4ae2849b0c84c0ef17659082268617abeb406402ef46b6fa9140e6d2064d`  
		Last Modified: Tue, 03 Dec 2024 01:28:15 GMT  
		Size: 28.5 MB (28505909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2a37d1c3544aae9cf855e4f9d96754f7d5aad9c9a3f7d42a3eb8987d04b10a`  
		Last Modified: Tue, 03 Dec 2024 15:43:23 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687c3b1191976c7d74198e8e57529daabebefb487799f83eb7d8681422ef72b8`  
		Last Modified: Tue, 03 Dec 2024 15:43:24 GMT  
		Size: 1.8 MB (1841107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71cc921943a3967383a50f905dd8868956c3ac63ebb385d9cec2f3cb34a9f87e`  
		Last Modified: Tue, 03 Dec 2024 15:43:24 GMT  
		Size: 5.8 MB (5803545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c26a9ead4b058916305bb6fd71d2599865275170bdb57724c307edf3509f326`  
		Last Modified: Tue, 03 Dec 2024 15:43:23 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9104292331624763e6d460ca187a0f85b64d1f486b86284c07c95592b8e94da1`  
		Last Modified: Tue, 03 Dec 2024 15:43:24 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:ee8a92a1ad8cafc8ea99877f6bfd0d92dc91949f54b840b48821ce544aa9bcda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ab156a72eff661cd8aed8bf33e1b225c9f5f2c967cb69cf1c020b44d53b44d`

```dockerfile
```

-	Layers:
	-	`sha256:2bd3fbc5d440f518558673839c4fcba7382ea6d548360ed2c57eb7bd0f049a65`  
		Last Modified: Tue, 03 Dec 2024 15:43:23 GMT  
		Size: 14.9 KB (14897 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; ppc64le

```console
$ docker pull spiped@sha256:fa1c0e0ca44831854510e672c54f19e7f6f438f1b478e6e12eb6fc349cb6036e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41069658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:badc1dcf78bdd756328e48de377c9ac83765d7fd252f4f6aed46a14bd58061e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:4a1ea4d3c9e0863e99d27aae6dac9a4b908a6413e758c7785d8fefe555b0e760`  
		Last Modified: Wed, 25 Dec 2024 00:32:48 GMT  
		Size: 32.1 MB (32063240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a10da46285624ad419bea829c84e2e283422614dc35af1abbcae2a21f755880`  
		Last Modified: Wed, 25 Dec 2024 06:00:22 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a18aaec69dfb91f7d658b963b1908aea3dd52a5d0ca1bd2882ce20e4891f72`  
		Last Modified: Wed, 25 Dec 2024 06:00:22 GMT  
		Size: 2.6 MB (2582060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944f472562e3088d879887732f39ea7cd0325819e2e8a179e0bb9564d18b57bb`  
		Last Modified: Wed, 25 Dec 2024 06:00:22 GMT  
		Size: 6.4 MB (6422816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df99d607fa9056ce8bb98db90549b7cbb6134b22361fc8c6293e8b883590d69`  
		Last Modified: Wed, 25 Dec 2024 06:00:22 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a6e26267e78fc9b2b7d66526922f89447996b9b8966d139452965d17fe008d`  
		Last Modified: Wed, 25 Dec 2024 06:00:23 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:39bf9515ccb9ec3a1513b875efcfece99ec844387b12732b93639b1c4dd870c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3516571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ca2573bd1e1ca8bceff7576088a8e2dcc6308a088e8fdc6c45ca47102b82647`

```dockerfile
```

-	Layers:
	-	`sha256:eee07c1e01812a3751985b1f438d18380d58d390e5da5ae1e3bbdca47c05c113`  
		Last Modified: Wed, 25 Dec 2024 06:00:22 GMT  
		Size: 3.5 MB (3501483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb349bf5733a427d8d67d73d6730d8117ab8dc2f68442180e877e7a53062a071`  
		Last Modified: Wed, 25 Dec 2024 06:00:22 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; s390x

```console
$ docker pull spiped@sha256:6c8b9b684784fd7e276e9642a6f67e29c09b10a5e70c83ce74be972322034cdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34334969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8363621faa6e61fe5ffedc99a0ac820582911b3efb820dd5c5e56288cfdca21d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:0e7e84bd4cca9e29f08dfac96d436e65bdd31929520e73147137b382fbc89b70`  
		Last Modified: Tue, 24 Dec 2024 21:33:49 GMT  
		Size: 26.9 MB (26878901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc416ec43cf7816408db05f15f973105968e740cadc2d8bf781d0f18b1662e2`  
		Last Modified: Wed, 25 Dec 2024 00:06:46 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43bde2f7b43f7809ecb4a99fef725c7668af05efd43fab2b2de7d0e9cdeed7df`  
		Last Modified: Wed, 25 Dec 2024 00:06:46 GMT  
		Size: 2.1 MB (2068729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c405c4f3d636ce991eec1df48ab2acbafb141f057b012887daeac232eeae8852`  
		Last Modified: Wed, 25 Dec 2024 00:06:46 GMT  
		Size: 5.4 MB (5385800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb5fd31da13e128253de1c3be9f0eaccc9791741f2ddbd7f64c404738ccfceb`  
		Last Modified: Wed, 25 Dec 2024 00:06:46 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67aa610193b9571e7f56cc25183b12debeda63c2b610cd66c4e3029c6fb31fb4`  
		Last Modified: Wed, 25 Dec 2024 00:06:46 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:3d6bf018776d6e6d237fde4d2f785340bcd6e32728626dba860c50d1995f0203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3519040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:054b3ee947046ff8f0f3b14b7e50d2f17b81f1ba09225a49e6d135180a585d01`

```dockerfile
```

-	Layers:
	-	`sha256:be1536a048742b7927962b19f3ec187b33b5f53d994d3883fb3398e0cc303f31`  
		Last Modified: Wed, 25 Dec 2024 00:06:46 GMT  
		Size: 3.5 MB (3504000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3dec620d34fc6d656f7478c968b406037c961f5f26c3e0b72bdd506d2fdceac`  
		Last Modified: Wed, 25 Dec 2024 00:06:46 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json
