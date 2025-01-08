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
$ docker pull spiped@sha256:8d5c2be4b38e4dd0d2977de6a557dd1217c481b131092d2fc86b58aec32a2d01
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
$ docker pull spiped@sha256:40db27aa7bf41fa2069cb38a42c91f16e30afb71ecc98638aeb354525b6d295d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36152050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edccfe05ee79919ba17983ac76fb9b5e424f36b911bd78de0806bdfe94cf6c8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1734912000'
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
	-	`sha256:8a9f899eb883b68bbb36209214842bc927b7c446aa0471f0b241ae7e76adb6e5`  
		Last Modified: Tue, 24 Dec 2024 21:33:38 GMT  
		Size: 28.5 MB (28505873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1093361a7499794781b2579c11586abdbe5d3f2df6a47f37fac74efdfb68893`  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ac298b930dd94b2f9f52f24c80e05e67f1be3672276c85ad399c351032b087`  
		Last Modified: Wed, 25 Dec 2024 11:44:14 GMT  
		Size: 1.8 MB (1841056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872acbbc9e0c74dace76c2b05e8da8b3a8f7ecca12f50cff8bf687f1140f2e0a`  
		Last Modified: Wed, 25 Dec 2024 11:44:14 GMT  
		Size: 5.8 MB (5803579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d315c1ce1440d3be213f517aeb12ae5ef02ea5957a47b00aa7a2547e289395`  
		Last Modified: Wed, 25 Dec 2024 11:44:13 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed324a48a7751ab39997d72129fbb399275395ae6b9757f266299bf3a79e75b3`  
		Last Modified: Wed, 25 Dec 2024 11:44:14 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:f16b2264f8ef7c6f87eeb6e5be9c173d4b31873535eb434e99b9b35d2caed80f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a1a0d891081762c3f095d847e238aa5e22867bf1dbc1b48683b36ad6cfb5433`

```dockerfile
```

-	Layers:
	-	`sha256:f429d0a19254f7d3db7b8d2eb84831d6f0bf02d100dfd38c2092442567ddc27d`  
		Last Modified: Wed, 25 Dec 2024 11:44:13 GMT  
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
		Last Modified: Wed, 08 Jan 2025 00:29:06 GMT  
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
$ docker pull spiped@sha256:f18720de28f93ecd77081a09f9fb50ef7b27e1b2f0ddd9e2a702e6547d67f8db
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
$ docker pull spiped@sha256:a2437bb32549fb26b2c5e2352337fa9b828b4529ac7c6d698d6dc35dfa6c4e39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3841253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e22840a5a70c56a7afdbbe563875d46c463af08f3803e89b942525fc8553dce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
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
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 23:53:52 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e7a51a2a61e8030d5392bd6a2f988a691d4bdd152f66dfcd44181b00fcffa5`  
		Last Modified: Tue, 07 Jan 2025 03:15:40 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e91285f9d5b26051e2a5c1577356ac3ca99ebc076b31c3d56c9af3687a0555`  
		Last Modified: Tue, 07 Jan 2025 03:15:40 GMT  
		Size: 7.5 KB (7549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b26d557ad63db6871840245fed75a25551bf86d6c43769731af10cec4e6556e5`  
		Last Modified: Tue, 07 Jan 2025 03:15:40 GMT  
		Size: 218.3 KB (218313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa628faafccfe7536bfe0751f2d14ba2361149efff1e1a40c3cdff322f7c7466`  
		Last Modified: Tue, 07 Jan 2025 03:15:40 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce3140b85b696b66b837bafaca07b043ce407975ddb7b5bfb9032d1eee2fd8e`  
		Last Modified: Tue, 07 Jan 2025 03:15:41 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:2dc54027609990d392a8ababdc4bbd5d0ce43886bfce0f58e9972886a290177b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 KB (88398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49d05c704ccdb0f5140bcd26d76d07e9aeb4e5e96c5fb973908352ba7aabb28b`

```dockerfile
```

-	Layers:
	-	`sha256:7bf8d5ef28bf164279c555c22ae6c52f2225df777335b6865fd4369badb65cd8`  
		Last Modified: Tue, 07 Jan 2025 03:15:40 GMT  
		Size: 74.1 KB (74096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a26a64c8c305fb0782b665571a4094d4c1d054b88078ffc8ec545539d2f771b8`  
		Last Modified: Tue, 07 Jan 2025 03:15:40 GMT  
		Size: 14.3 KB (14302 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:9b4d16f259f74f7ae9b1c1ecddaffcc30b885797ab1d60f0477cc840a52ce65f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3575623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:652d5f62598bd5ffe8ddc89e0d92496adc12ba2ca526ec27ba1fb42776b21137`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.4-armhf.tar.gz / # buildkit
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
	-	`sha256:9327c400cc7c63bc8696a8da86f21db1ffdb7ce43885aa521a67ab8105dd2af9`  
		Last Modified: Tue, 07 Jan 2025 02:29:49 GMT  
		Size: 3.4 MB (3363944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a29b8b207ad9555db0164f2c351570fbf0a53ccb093bd193b087063577055c1`  
		Last Modified: Tue, 07 Jan 2025 06:42:40 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f5a64d59e5b0c8f034f770c9eca85ca71ba9a73e463212f81d6e6a4462dbd5`  
		Last Modified: Wed, 08 Jan 2025 00:02:53 GMT  
		Size: 7.6 KB (7552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd01fb3f9a09a2dd08b845b169987bfb7853b6ee5808101bae8ca74c86a2e88`  
		Last Modified: Tue, 07 Jan 2025 06:42:41 GMT  
		Size: 202.7 KB (202728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927b498d6513dfddba82a6b7f7cdf3c87b13b7bf2fc3c425847c78fc33910be4`  
		Last Modified: Tue, 07 Jan 2025 06:42:41 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cbc736b391c47cbc09e98e86a9c513f62c662bbac310ec71e3e20bac5605cbf`  
		Last Modified: Tue, 07 Jan 2025 06:42:41 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:66c25ca1517901b4b08905893052a2fed202aae0879a1de61d38a727e133a02d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:772f571d35c16879a7ff3fa8f100987a1e571aab44cb51f62b75ee3555bd9b3c`

```dockerfile
```

-	Layers:
	-	`sha256:cd8b30cb15f8d9de66e419a8094744867e4734a5cc4d08a37d7d9f575bae5486`  
		Last Modified: Tue, 07 Jan 2025 06:42:40 GMT  
		Size: 14.2 KB (14189 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:317f548279e1c85c7ac74344b71832b8588d763e18e76af3950b2dbfce0c2e66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3296467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:816d532b96ad48e2d8eb9c9d3ceb60c51d8d8ca5ea971981c2741297c77b4e38`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.4-armv7.tar.gz / # buildkit
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
	-	`sha256:0695ed689d581197c59573cee0b2f2ef2c3a332e0d52bbb8f0e7e0865c2d5b23`  
		Last Modified: Tue, 07 Jan 2025 02:55:40 GMT  
		Size: 3.1 MB (3091288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05dfd721334f5542e7031dc7e4d8c1295bc566abdada8cd729209f7a0048138f`  
		Last Modified: Tue, 07 Jan 2025 06:20:20 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341cd5baaaebac2c76dbb23327031ffd02bbcde8f31957ed2e093dc0a3d7cae0`  
		Last Modified: Tue, 07 Jan 2025 06:20:20 GMT  
		Size: 7.6 KB (7562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1c1aefb60d120aa4f15d645553a6c856b198ec71d52178b5750253d9682292`  
		Last Modified: Tue, 07 Jan 2025 06:20:21 GMT  
		Size: 196.2 KB (196222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f0471c8ff4a4830446446ac80595a67a7b3327fe46ce8083fbd00d3aac033a`  
		Last Modified: Tue, 07 Jan 2025 06:20:21 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d68cacf6fe4b54bc857a69776b0078df52e4b0edb50d4b9595ae47e97e2af5`  
		Last Modified: Tue, 07 Jan 2025 06:20:21 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:de9af5cb4485d7e53d223c2f2e5a7e7e62118e1f0f7f6c28e6d9d869673c723d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 KB (88536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:559fda02f71cbfaaa9934ec5b65f7a0c1de405e28468932e9dd21880a7f2aa6d`

```dockerfile
```

-	Layers:
	-	`sha256:20ed53337aa7afa648a3c2e36917ab1caff5c7803ea2fce77cf6e24884021bf8`  
		Last Modified: Tue, 07 Jan 2025 06:20:20 GMT  
		Size: 74.1 KB (74132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2c7ed91d6c6346126e45e47f5808ea8bfee2c51ef4ca4f1f5da160550f611da`  
		Last Modified: Tue, 07 Jan 2025 06:20:20 GMT  
		Size: 14.4 KB (14404 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:fdbb12824b88c7b18859c04cc8fbd31d6ccc84c135af3e8a2df261b38a10057f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4308713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c767cc3f98c29c28297080fd7c1d27c661584beb88a486df47d28053b48a455b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
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
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b19e3d04ec2b9d3001f2787d68b4b449f3e689a0d6f2f471a0386c4cfec4b1e`  
		Last Modified: Tue, 07 Jan 2025 07:09:34 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc909cbe9bc37ee1c83cc781499991aaf16f74091b8b3dc10087ccdb9cd8bbc1`  
		Last Modified: Tue, 07 Jan 2025 07:09:35 GMT  
		Size: 7.6 KB (7555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b65ae735ee44407b76890196851e37d2728197b6a257a567737116e76a178885`  
		Last Modified: Tue, 07 Jan 2025 07:09:35 GMT  
		Size: 213.1 KB (213077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac91bc929cadefcfdb1a75a0f2f5c44be39a2a126e2316a777d34e777cf25c0`  
		Last Modified: Tue, 07 Jan 2025 07:09:35 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b00577687504dcf1da7210e90b7144500242cd716a98cd945aee7317ff2b853`  
		Last Modified: Tue, 07 Jan 2025 07:09:35 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:278cb7494adb7b010caaa0fc5a6d18b19dde2a17677fef36fc1ba4852e0163a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 KB (88587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63b31a8595fc81a7abeaa1742e609cb7d6ddfa29e8382e0f625ebf7511d3679`

```dockerfile
```

-	Layers:
	-	`sha256:62af3aeae92f48ea868503a424e93b9c08260ae07dca8e88bddfca56b1593592`  
		Last Modified: Tue, 07 Jan 2025 07:09:35 GMT  
		Size: 74.2 KB (74152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3ca283b7fa2827d2d9cde0670b6d868f61d5adc4b68bc70bafc06cf1935e83b`  
		Last Modified: Tue, 07 Jan 2025 07:09:35 GMT  
		Size: 14.4 KB (14435 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; 386

```console
$ docker pull spiped@sha256:78bc42e6a96585db8bdd8556e294d69b9ed44e4f789631e260b190a14e162735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3700771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:998f961e80b642a56013e83879523113a861992b529b3ff7b5767bc7cc7a628b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.4-x86.tar.gz / # buildkit
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
	-	`sha256:a48310298946cd9150f3929f2f8cebe3709f1c7ecd0e99ff2b0c9b6502172586`  
		Last Modified: Tue, 07 Jan 2025 02:28:41 GMT  
		Size: 3.5 MB (3463189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8423b800688f39626883f31d6f6e28c792f7b2c2b38eff3660b37b8f5985948a`  
		Last Modified: Tue, 07 Jan 2025 03:14:53 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc601454882a7f688874ee7eb6db905a8a1fd66fd8f74839f2616d43ffdbc60`  
		Last Modified: Tue, 07 Jan 2025 03:14:53 GMT  
		Size: 7.6 KB (7560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc540e07a100bef5d0924a05e52558c7723fdcadd6b9985563c7939ecd22f78`  
		Last Modified: Tue, 07 Jan 2025 03:14:53 GMT  
		Size: 228.6 KB (228627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:983f177c9f56963e5413b0628afb23e7b581d7f0e7829632fb472dee1d43e532`  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1d8a9e4cbb12b01b9a10d87658320bc01979d3f2709a0dd5613974a2270a64`  
		Last Modified: Tue, 07 Jan 2025 03:14:54 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:d94b06b62806c406a02f830533f8e5b1d274a4ec7af0a886324cb8b8033a8a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 KB (88337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6073d4c32fc43315273812b7e6dead1b7421f3d92e2abea2c62600438f9f7b9c`

```dockerfile
```

-	Layers:
	-	`sha256:d88073ad75f69f0118fa3fac91a25e5cfe758dcfc9b8933775ad48751cda23d8`  
		Last Modified: Tue, 07 Jan 2025 03:14:53 GMT  
		Size: 74.1 KB (74071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c93a63055383835cd30affb3ac53a708d8659bc3a31268b5bece883d901e9a75`  
		Last Modified: Tue, 07 Jan 2025 03:14:53 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:acf12ae1c612b3d71f4f4ba5eba9457c016eb0ffd7656079ecc6efec2d93d42a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3794399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28e53576b17bd09a0639a34556eac32bfd9a6c24b843678abbb73f14b018d01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.4-ppc64le.tar.gz / # buildkit
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
	-	`sha256:c96bc34ea0111931eae2007b7db67b205ebd3c8a096d711e1be59e48f25006a3`  
		Last Modified: Tue, 07 Jan 2025 02:32:24 GMT  
		Size: 3.6 MB (3568727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f58b562e7456d04a8a4485e9c2074a9e970f91fc0c31c84417492a091fb0d9`  
		Last Modified: Tue, 07 Jan 2025 06:13:44 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ecaa236d35dff0d883b4e1df8af1896bed049f98eb2ebf06b4d3abe1175285`  
		Last Modified: Tue, 07 Jan 2025 06:13:44 GMT  
		Size: 7.6 KB (7560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5452c07f1c981726006484a86ee19ada2152fc861cbf7fa64f93607f4c722ec8`  
		Size: 216.7 KB (216715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c840be9d9960807fda71ec5277170b84d7a4f1f302a40a60c6a58aa5d0e26b5`  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6cb66e59e31eb74643da37a8a614d258f5e133d1be21972cea66400c55efe2`  
		Last Modified: Tue, 07 Jan 2025 06:13:45 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:15bddc3596ae063a10a0f93e806478f1eabaeaeeb04e6c16767d5bf3a5aca278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 KB (86529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d84439a9043cd5c314ae04d742cc069d7ac73bb9250ed8097468189c63d97e`

```dockerfile
```

-	Layers:
	-	`sha256:f1d0853fb999d7e046e8fb680844a6937030b6d9961660dd42283d594427994d`  
		Last Modified: Tue, 07 Jan 2025 06:13:45 GMT  
		Size: 72.2 KB (72179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b05b1e01cb4427d75c873721837d33c9d94909ed405e90f19dbc76425fb45db`  
		Last Modified: Tue, 07 Jan 2025 06:13:44 GMT  
		Size: 14.3 KB (14350 bytes)  
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
$ docker pull spiped@sha256:2b056e84c73867952da7b22052f17a7df808b47516a5bb83b8ee13395dc5923d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3674138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3595de50a5f32e15b6db59451eae6913f4aba96c241c1107b30e84d282d1c841`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.4-s390x.tar.gz / # buildkit
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
	-	`sha256:2ed16bdf68dac880df118dfa3d21d44652bc18382729359f97297fa5998086cd`  
		Last Modified: Tue, 07 Jan 2025 02:32:49 GMT  
		Size: 3.5 MB (3459179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc1c58e04de4e903d567e58827a257047fc49b0eef9f83f28092313f82cbde8`  
		Last Modified: Tue, 07 Jan 2025 06:19:19 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797ce336a1e875ccc1cd81f71aff2122e82a35cc94121592994a0335577d072f`  
		Last Modified: Tue, 07 Jan 2025 06:19:19 GMT  
		Size: 7.6 KB (7562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876bf37cceecc9d224e361a1ad76cf766d3c66622e6bf682fed3bb15bb73ca6b`  
		Last Modified: Tue, 07 Jan 2025 06:19:19 GMT  
		Size: 206.0 KB (206006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef3d29125754db1b1c388a568ccaa80fa40fc0c2b9078aaae244b5a314eaa96`  
		Last Modified: Tue, 07 Jan 2025 06:19:19 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8bb164b00a2b113f38d85168412b681bebb59d60c7cd5639f5d336feb07d30`  
		Last Modified: Tue, 07 Jan 2025 06:19:20 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:dfa792f46cacda3f23b902f295f4c89e1405c9ecbbf35d3dc361b490cb5d2bd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 KB (86446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a50a77b62b00200a0d22583cee5739c50ef87fac5617e6a874a57b6ab43071bd`

```dockerfile
```

-	Layers:
	-	`sha256:2f8c8e6e444fb4067b5793ed502feadffb90b238f975366fb53d0618681dca0c`  
		Last Modified: Tue, 07 Jan 2025 06:19:19 GMT  
		Size: 72.1 KB (72145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0ae978c3bffb1c7f0cad075aee069f572a9513bee2ea6a85ca5f5f145836bc1`  
		Last Modified: Tue, 07 Jan 2025 06:19:19 GMT  
		Size: 14.3 KB (14301 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6`

```console
$ docker pull spiped@sha256:8d5c2be4b38e4dd0d2977de6a557dd1217c481b131092d2fc86b58aec32a2d01
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
$ docker pull spiped@sha256:40db27aa7bf41fa2069cb38a42c91f16e30afb71ecc98638aeb354525b6d295d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36152050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edccfe05ee79919ba17983ac76fb9b5e424f36b911bd78de0806bdfe94cf6c8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1734912000'
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
	-	`sha256:8a9f899eb883b68bbb36209214842bc927b7c446aa0471f0b241ae7e76adb6e5`  
		Last Modified: Tue, 24 Dec 2024 21:33:38 GMT  
		Size: 28.5 MB (28505873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1093361a7499794781b2579c11586abdbe5d3f2df6a47f37fac74efdfb68893`  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ac298b930dd94b2f9f52f24c80e05e67f1be3672276c85ad399c351032b087`  
		Last Modified: Wed, 25 Dec 2024 11:44:14 GMT  
		Size: 1.8 MB (1841056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872acbbc9e0c74dace76c2b05e8da8b3a8f7ecca12f50cff8bf687f1140f2e0a`  
		Last Modified: Wed, 25 Dec 2024 11:44:14 GMT  
		Size: 5.8 MB (5803579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d315c1ce1440d3be213f517aeb12ae5ef02ea5957a47b00aa7a2547e289395`  
		Last Modified: Wed, 25 Dec 2024 11:44:13 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed324a48a7751ab39997d72129fbb399275395ae6b9757f266299bf3a79e75b3`  
		Last Modified: Wed, 25 Dec 2024 11:44:14 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:f16b2264f8ef7c6f87eeb6e5be9c173d4b31873535eb434e99b9b35d2caed80f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a1a0d891081762c3f095d847e238aa5e22867bf1dbc1b48683b36ad6cfb5433`

```dockerfile
```

-	Layers:
	-	`sha256:f429d0a19254f7d3db7b8d2eb84831d6f0bf02d100dfd38c2092442567ddc27d`  
		Last Modified: Wed, 25 Dec 2024 11:44:13 GMT  
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
		Last Modified: Wed, 08 Jan 2025 00:29:06 GMT  
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
$ docker pull spiped@sha256:f18720de28f93ecd77081a09f9fb50ef7b27e1b2f0ddd9e2a702e6547d67f8db
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
$ docker pull spiped@sha256:a2437bb32549fb26b2c5e2352337fa9b828b4529ac7c6d698d6dc35dfa6c4e39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3841253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e22840a5a70c56a7afdbbe563875d46c463af08f3803e89b942525fc8553dce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
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
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 23:53:52 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e7a51a2a61e8030d5392bd6a2f988a691d4bdd152f66dfcd44181b00fcffa5`  
		Last Modified: Tue, 07 Jan 2025 03:15:40 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e91285f9d5b26051e2a5c1577356ac3ca99ebc076b31c3d56c9af3687a0555`  
		Last Modified: Tue, 07 Jan 2025 03:15:40 GMT  
		Size: 7.5 KB (7549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b26d557ad63db6871840245fed75a25551bf86d6c43769731af10cec4e6556e5`  
		Last Modified: Tue, 07 Jan 2025 03:15:40 GMT  
		Size: 218.3 KB (218313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa628faafccfe7536bfe0751f2d14ba2361149efff1e1a40c3cdff322f7c7466`  
		Last Modified: Tue, 07 Jan 2025 03:15:40 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce3140b85b696b66b837bafaca07b043ce407975ddb7b5bfb9032d1eee2fd8e`  
		Last Modified: Tue, 07 Jan 2025 03:15:41 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:2dc54027609990d392a8ababdc4bbd5d0ce43886bfce0f58e9972886a290177b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 KB (88398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49d05c704ccdb0f5140bcd26d76d07e9aeb4e5e96c5fb973908352ba7aabb28b`

```dockerfile
```

-	Layers:
	-	`sha256:7bf8d5ef28bf164279c555c22ae6c52f2225df777335b6865fd4369badb65cd8`  
		Last Modified: Tue, 07 Jan 2025 03:15:40 GMT  
		Size: 74.1 KB (74096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a26a64c8c305fb0782b665571a4094d4c1d054b88078ffc8ec545539d2f771b8`  
		Last Modified: Tue, 07 Jan 2025 03:15:40 GMT  
		Size: 14.3 KB (14302 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:9b4d16f259f74f7ae9b1c1ecddaffcc30b885797ab1d60f0477cc840a52ce65f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3575623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:652d5f62598bd5ffe8ddc89e0d92496adc12ba2ca526ec27ba1fb42776b21137`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.4-armhf.tar.gz / # buildkit
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
	-	`sha256:9327c400cc7c63bc8696a8da86f21db1ffdb7ce43885aa521a67ab8105dd2af9`  
		Last Modified: Tue, 07 Jan 2025 02:29:49 GMT  
		Size: 3.4 MB (3363944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a29b8b207ad9555db0164f2c351570fbf0a53ccb093bd193b087063577055c1`  
		Last Modified: Tue, 07 Jan 2025 06:42:40 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f5a64d59e5b0c8f034f770c9eca85ca71ba9a73e463212f81d6e6a4462dbd5`  
		Last Modified: Wed, 08 Jan 2025 00:02:53 GMT  
		Size: 7.6 KB (7552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd01fb3f9a09a2dd08b845b169987bfb7853b6ee5808101bae8ca74c86a2e88`  
		Last Modified: Tue, 07 Jan 2025 06:42:41 GMT  
		Size: 202.7 KB (202728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927b498d6513dfddba82a6b7f7cdf3c87b13b7bf2fc3c425847c78fc33910be4`  
		Last Modified: Tue, 07 Jan 2025 06:42:41 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cbc736b391c47cbc09e98e86a9c513f62c662bbac310ec71e3e20bac5605cbf`  
		Last Modified: Tue, 07 Jan 2025 06:42:41 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:66c25ca1517901b4b08905893052a2fed202aae0879a1de61d38a727e133a02d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:772f571d35c16879a7ff3fa8f100987a1e571aab44cb51f62b75ee3555bd9b3c`

```dockerfile
```

-	Layers:
	-	`sha256:cd8b30cb15f8d9de66e419a8094744867e4734a5cc4d08a37d7d9f575bae5486`  
		Last Modified: Tue, 07 Jan 2025 06:42:40 GMT  
		Size: 14.2 KB (14189 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:317f548279e1c85c7ac74344b71832b8588d763e18e76af3950b2dbfce0c2e66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3296467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:816d532b96ad48e2d8eb9c9d3ceb60c51d8d8ca5ea971981c2741297c77b4e38`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.4-armv7.tar.gz / # buildkit
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
	-	`sha256:0695ed689d581197c59573cee0b2f2ef2c3a332e0d52bbb8f0e7e0865c2d5b23`  
		Last Modified: Tue, 07 Jan 2025 02:55:40 GMT  
		Size: 3.1 MB (3091288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05dfd721334f5542e7031dc7e4d8c1295bc566abdada8cd729209f7a0048138f`  
		Last Modified: Tue, 07 Jan 2025 06:20:20 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341cd5baaaebac2c76dbb23327031ffd02bbcde8f31957ed2e093dc0a3d7cae0`  
		Last Modified: Tue, 07 Jan 2025 06:20:20 GMT  
		Size: 7.6 KB (7562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1c1aefb60d120aa4f15d645553a6c856b198ec71d52178b5750253d9682292`  
		Last Modified: Tue, 07 Jan 2025 06:20:21 GMT  
		Size: 196.2 KB (196222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f0471c8ff4a4830446446ac80595a67a7b3327fe46ce8083fbd00d3aac033a`  
		Last Modified: Tue, 07 Jan 2025 06:20:21 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d68cacf6fe4b54bc857a69776b0078df52e4b0edb50d4b9595ae47e97e2af5`  
		Last Modified: Tue, 07 Jan 2025 06:20:21 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:de9af5cb4485d7e53d223c2f2e5a7e7e62118e1f0f7f6c28e6d9d869673c723d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 KB (88536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:559fda02f71cbfaaa9934ec5b65f7a0c1de405e28468932e9dd21880a7f2aa6d`

```dockerfile
```

-	Layers:
	-	`sha256:20ed53337aa7afa648a3c2e36917ab1caff5c7803ea2fce77cf6e24884021bf8`  
		Last Modified: Tue, 07 Jan 2025 06:20:20 GMT  
		Size: 74.1 KB (74132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2c7ed91d6c6346126e45e47f5808ea8bfee2c51ef4ca4f1f5da160550f611da`  
		Last Modified: Tue, 07 Jan 2025 06:20:20 GMT  
		Size: 14.4 KB (14404 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:fdbb12824b88c7b18859c04cc8fbd31d6ccc84c135af3e8a2df261b38a10057f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4308713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c767cc3f98c29c28297080fd7c1d27c661584beb88a486df47d28053b48a455b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
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
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b19e3d04ec2b9d3001f2787d68b4b449f3e689a0d6f2f471a0386c4cfec4b1e`  
		Last Modified: Tue, 07 Jan 2025 07:09:34 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc909cbe9bc37ee1c83cc781499991aaf16f74091b8b3dc10087ccdb9cd8bbc1`  
		Last Modified: Tue, 07 Jan 2025 07:09:35 GMT  
		Size: 7.6 KB (7555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b65ae735ee44407b76890196851e37d2728197b6a257a567737116e76a178885`  
		Last Modified: Tue, 07 Jan 2025 07:09:35 GMT  
		Size: 213.1 KB (213077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac91bc929cadefcfdb1a75a0f2f5c44be39a2a126e2316a777d34e777cf25c0`  
		Last Modified: Tue, 07 Jan 2025 07:09:35 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b00577687504dcf1da7210e90b7144500242cd716a98cd945aee7317ff2b853`  
		Last Modified: Tue, 07 Jan 2025 07:09:35 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:278cb7494adb7b010caaa0fc5a6d18b19dde2a17677fef36fc1ba4852e0163a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 KB (88587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63b31a8595fc81a7abeaa1742e609cb7d6ddfa29e8382e0f625ebf7511d3679`

```dockerfile
```

-	Layers:
	-	`sha256:62af3aeae92f48ea868503a424e93b9c08260ae07dca8e88bddfca56b1593592`  
		Last Modified: Tue, 07 Jan 2025 07:09:35 GMT  
		Size: 74.2 KB (74152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3ca283b7fa2827d2d9cde0670b6d868f61d5adc4b68bc70bafc06cf1935e83b`  
		Last Modified: Tue, 07 Jan 2025 07:09:35 GMT  
		Size: 14.4 KB (14435 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; 386

```console
$ docker pull spiped@sha256:78bc42e6a96585db8bdd8556e294d69b9ed44e4f789631e260b190a14e162735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3700771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:998f961e80b642a56013e83879523113a861992b529b3ff7b5767bc7cc7a628b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.4-x86.tar.gz / # buildkit
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
	-	`sha256:a48310298946cd9150f3929f2f8cebe3709f1c7ecd0e99ff2b0c9b6502172586`  
		Last Modified: Tue, 07 Jan 2025 02:28:41 GMT  
		Size: 3.5 MB (3463189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8423b800688f39626883f31d6f6e28c792f7b2c2b38eff3660b37b8f5985948a`  
		Last Modified: Tue, 07 Jan 2025 03:14:53 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc601454882a7f688874ee7eb6db905a8a1fd66fd8f74839f2616d43ffdbc60`  
		Last Modified: Tue, 07 Jan 2025 03:14:53 GMT  
		Size: 7.6 KB (7560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc540e07a100bef5d0924a05e52558c7723fdcadd6b9985563c7939ecd22f78`  
		Last Modified: Tue, 07 Jan 2025 03:14:53 GMT  
		Size: 228.6 KB (228627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:983f177c9f56963e5413b0628afb23e7b581d7f0e7829632fb472dee1d43e532`  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1d8a9e4cbb12b01b9a10d87658320bc01979d3f2709a0dd5613974a2270a64`  
		Last Modified: Tue, 07 Jan 2025 03:14:54 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:d94b06b62806c406a02f830533f8e5b1d274a4ec7af0a886324cb8b8033a8a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 KB (88337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6073d4c32fc43315273812b7e6dead1b7421f3d92e2abea2c62600438f9f7b9c`

```dockerfile
```

-	Layers:
	-	`sha256:d88073ad75f69f0118fa3fac91a25e5cfe758dcfc9b8933775ad48751cda23d8`  
		Last Modified: Tue, 07 Jan 2025 03:14:53 GMT  
		Size: 74.1 KB (74071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c93a63055383835cd30affb3ac53a708d8659bc3a31268b5bece883d901e9a75`  
		Last Modified: Tue, 07 Jan 2025 03:14:53 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:acf12ae1c612b3d71f4f4ba5eba9457c016eb0ffd7656079ecc6efec2d93d42a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3794399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28e53576b17bd09a0639a34556eac32bfd9a6c24b843678abbb73f14b018d01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.4-ppc64le.tar.gz / # buildkit
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
	-	`sha256:c96bc34ea0111931eae2007b7db67b205ebd3c8a096d711e1be59e48f25006a3`  
		Last Modified: Tue, 07 Jan 2025 02:32:24 GMT  
		Size: 3.6 MB (3568727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f58b562e7456d04a8a4485e9c2074a9e970f91fc0c31c84417492a091fb0d9`  
		Last Modified: Tue, 07 Jan 2025 06:13:44 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ecaa236d35dff0d883b4e1df8af1896bed049f98eb2ebf06b4d3abe1175285`  
		Last Modified: Tue, 07 Jan 2025 06:13:44 GMT  
		Size: 7.6 KB (7560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5452c07f1c981726006484a86ee19ada2152fc861cbf7fa64f93607f4c722ec8`  
		Size: 216.7 KB (216715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c840be9d9960807fda71ec5277170b84d7a4f1f302a40a60c6a58aa5d0e26b5`  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6cb66e59e31eb74643da37a8a614d258f5e133d1be21972cea66400c55efe2`  
		Last Modified: Tue, 07 Jan 2025 06:13:45 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:15bddc3596ae063a10a0f93e806478f1eabaeaeeb04e6c16767d5bf3a5aca278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 KB (86529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d84439a9043cd5c314ae04d742cc069d7ac73bb9250ed8097468189c63d97e`

```dockerfile
```

-	Layers:
	-	`sha256:f1d0853fb999d7e046e8fb680844a6937030b6d9961660dd42283d594427994d`  
		Last Modified: Tue, 07 Jan 2025 06:13:45 GMT  
		Size: 72.2 KB (72179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b05b1e01cb4427d75c873721837d33c9d94909ed405e90f19dbc76425fb45db`  
		Last Modified: Tue, 07 Jan 2025 06:13:44 GMT  
		Size: 14.3 KB (14350 bytes)  
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
$ docker pull spiped@sha256:2b056e84c73867952da7b22052f17a7df808b47516a5bb83b8ee13395dc5923d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3674138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3595de50a5f32e15b6db59451eae6913f4aba96c241c1107b30e84d282d1c841`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.4-s390x.tar.gz / # buildkit
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
	-	`sha256:2ed16bdf68dac880df118dfa3d21d44652bc18382729359f97297fa5998086cd`  
		Last Modified: Tue, 07 Jan 2025 02:32:49 GMT  
		Size: 3.5 MB (3459179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc1c58e04de4e903d567e58827a257047fc49b0eef9f83f28092313f82cbde8`  
		Last Modified: Tue, 07 Jan 2025 06:19:19 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797ce336a1e875ccc1cd81f71aff2122e82a35cc94121592994a0335577d072f`  
		Last Modified: Tue, 07 Jan 2025 06:19:19 GMT  
		Size: 7.6 KB (7562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876bf37cceecc9d224e361a1ad76cf766d3c66622e6bf682fed3bb15bb73ca6b`  
		Last Modified: Tue, 07 Jan 2025 06:19:19 GMT  
		Size: 206.0 KB (206006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef3d29125754db1b1c388a568ccaa80fa40fc0c2b9078aaae244b5a314eaa96`  
		Last Modified: Tue, 07 Jan 2025 06:19:19 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8bb164b00a2b113f38d85168412b681bebb59d60c7cd5639f5d336feb07d30`  
		Last Modified: Tue, 07 Jan 2025 06:19:20 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:dfa792f46cacda3f23b902f295f4c89e1405c9ecbbf35d3dc361b490cb5d2bd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 KB (86446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a50a77b62b00200a0d22583cee5739c50ef87fac5617e6a874a57b6ab43071bd`

```dockerfile
```

-	Layers:
	-	`sha256:2f8c8e6e444fb4067b5793ed502feadffb90b238f975366fb53d0618681dca0c`  
		Last Modified: Tue, 07 Jan 2025 06:19:19 GMT  
		Size: 72.1 KB (72145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0ae978c3bffb1c7f0cad075aee069f572a9513bee2ea6a85ca5f5f145836bc1`  
		Last Modified: Tue, 07 Jan 2025 06:19:19 GMT  
		Size: 14.3 KB (14301 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6.2`

```console
$ docker pull spiped@sha256:8d5c2be4b38e4dd0d2977de6a557dd1217c481b131092d2fc86b58aec32a2d01
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
$ docker pull spiped@sha256:40db27aa7bf41fa2069cb38a42c91f16e30afb71ecc98638aeb354525b6d295d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36152050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edccfe05ee79919ba17983ac76fb9b5e424f36b911bd78de0806bdfe94cf6c8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1734912000'
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
	-	`sha256:8a9f899eb883b68bbb36209214842bc927b7c446aa0471f0b241ae7e76adb6e5`  
		Last Modified: Tue, 24 Dec 2024 21:33:38 GMT  
		Size: 28.5 MB (28505873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1093361a7499794781b2579c11586abdbe5d3f2df6a47f37fac74efdfb68893`  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ac298b930dd94b2f9f52f24c80e05e67f1be3672276c85ad399c351032b087`  
		Last Modified: Wed, 25 Dec 2024 11:44:14 GMT  
		Size: 1.8 MB (1841056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872acbbc9e0c74dace76c2b05e8da8b3a8f7ecca12f50cff8bf687f1140f2e0a`  
		Last Modified: Wed, 25 Dec 2024 11:44:14 GMT  
		Size: 5.8 MB (5803579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d315c1ce1440d3be213f517aeb12ae5ef02ea5957a47b00aa7a2547e289395`  
		Last Modified: Wed, 25 Dec 2024 11:44:13 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed324a48a7751ab39997d72129fbb399275395ae6b9757f266299bf3a79e75b3`  
		Last Modified: Wed, 25 Dec 2024 11:44:14 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2` - unknown; unknown

```console
$ docker pull spiped@sha256:f16b2264f8ef7c6f87eeb6e5be9c173d4b31873535eb434e99b9b35d2caed80f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a1a0d891081762c3f095d847e238aa5e22867bf1dbc1b48683b36ad6cfb5433`

```dockerfile
```

-	Layers:
	-	`sha256:f429d0a19254f7d3db7b8d2eb84831d6f0bf02d100dfd38c2092442567ddc27d`  
		Last Modified: Wed, 25 Dec 2024 11:44:13 GMT  
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
		Last Modified: Wed, 08 Jan 2025 00:29:06 GMT  
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
$ docker pull spiped@sha256:f18720de28f93ecd77081a09f9fb50ef7b27e1b2f0ddd9e2a702e6547d67f8db
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
$ docker pull spiped@sha256:a2437bb32549fb26b2c5e2352337fa9b828b4529ac7c6d698d6dc35dfa6c4e39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3841253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e22840a5a70c56a7afdbbe563875d46c463af08f3803e89b942525fc8553dce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
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
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 23:53:52 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e7a51a2a61e8030d5392bd6a2f988a691d4bdd152f66dfcd44181b00fcffa5`  
		Last Modified: Tue, 07 Jan 2025 03:15:40 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e91285f9d5b26051e2a5c1577356ac3ca99ebc076b31c3d56c9af3687a0555`  
		Last Modified: Tue, 07 Jan 2025 03:15:40 GMT  
		Size: 7.5 KB (7549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b26d557ad63db6871840245fed75a25551bf86d6c43769731af10cec4e6556e5`  
		Last Modified: Tue, 07 Jan 2025 03:15:40 GMT  
		Size: 218.3 KB (218313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa628faafccfe7536bfe0751f2d14ba2361149efff1e1a40c3cdff322f7c7466`  
		Last Modified: Tue, 07 Jan 2025 03:15:40 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce3140b85b696b66b837bafaca07b043ce407975ddb7b5bfb9032d1eee2fd8e`  
		Last Modified: Tue, 07 Jan 2025 03:15:41 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:2dc54027609990d392a8ababdc4bbd5d0ce43886bfce0f58e9972886a290177b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 KB (88398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49d05c704ccdb0f5140bcd26d76d07e9aeb4e5e96c5fb973908352ba7aabb28b`

```dockerfile
```

-	Layers:
	-	`sha256:7bf8d5ef28bf164279c555c22ae6c52f2225df777335b6865fd4369badb65cd8`  
		Last Modified: Tue, 07 Jan 2025 03:15:40 GMT  
		Size: 74.1 KB (74096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a26a64c8c305fb0782b665571a4094d4c1d054b88078ffc8ec545539d2f771b8`  
		Last Modified: Tue, 07 Jan 2025 03:15:40 GMT  
		Size: 14.3 KB (14302 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:9b4d16f259f74f7ae9b1c1ecddaffcc30b885797ab1d60f0477cc840a52ce65f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3575623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:652d5f62598bd5ffe8ddc89e0d92496adc12ba2ca526ec27ba1fb42776b21137`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.4-armhf.tar.gz / # buildkit
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
	-	`sha256:9327c400cc7c63bc8696a8da86f21db1ffdb7ce43885aa521a67ab8105dd2af9`  
		Last Modified: Tue, 07 Jan 2025 02:29:49 GMT  
		Size: 3.4 MB (3363944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a29b8b207ad9555db0164f2c351570fbf0a53ccb093bd193b087063577055c1`  
		Last Modified: Tue, 07 Jan 2025 06:42:40 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f5a64d59e5b0c8f034f770c9eca85ca71ba9a73e463212f81d6e6a4462dbd5`  
		Last Modified: Wed, 08 Jan 2025 00:02:53 GMT  
		Size: 7.6 KB (7552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd01fb3f9a09a2dd08b845b169987bfb7853b6ee5808101bae8ca74c86a2e88`  
		Last Modified: Tue, 07 Jan 2025 06:42:41 GMT  
		Size: 202.7 KB (202728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927b498d6513dfddba82a6b7f7cdf3c87b13b7bf2fc3c425847c78fc33910be4`  
		Last Modified: Tue, 07 Jan 2025 06:42:41 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cbc736b391c47cbc09e98e86a9c513f62c662bbac310ec71e3e20bac5605cbf`  
		Last Modified: Tue, 07 Jan 2025 06:42:41 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:66c25ca1517901b4b08905893052a2fed202aae0879a1de61d38a727e133a02d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:772f571d35c16879a7ff3fa8f100987a1e571aab44cb51f62b75ee3555bd9b3c`

```dockerfile
```

-	Layers:
	-	`sha256:cd8b30cb15f8d9de66e419a8094744867e4734a5cc4d08a37d7d9f575bae5486`  
		Last Modified: Tue, 07 Jan 2025 06:42:40 GMT  
		Size: 14.2 KB (14189 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:317f548279e1c85c7ac74344b71832b8588d763e18e76af3950b2dbfce0c2e66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3296467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:816d532b96ad48e2d8eb9c9d3ceb60c51d8d8ca5ea971981c2741297c77b4e38`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.4-armv7.tar.gz / # buildkit
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
	-	`sha256:0695ed689d581197c59573cee0b2f2ef2c3a332e0d52bbb8f0e7e0865c2d5b23`  
		Last Modified: Tue, 07 Jan 2025 02:55:40 GMT  
		Size: 3.1 MB (3091288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05dfd721334f5542e7031dc7e4d8c1295bc566abdada8cd729209f7a0048138f`  
		Last Modified: Tue, 07 Jan 2025 06:20:20 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341cd5baaaebac2c76dbb23327031ffd02bbcde8f31957ed2e093dc0a3d7cae0`  
		Last Modified: Tue, 07 Jan 2025 06:20:20 GMT  
		Size: 7.6 KB (7562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1c1aefb60d120aa4f15d645553a6c856b198ec71d52178b5750253d9682292`  
		Last Modified: Tue, 07 Jan 2025 06:20:21 GMT  
		Size: 196.2 KB (196222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f0471c8ff4a4830446446ac80595a67a7b3327fe46ce8083fbd00d3aac033a`  
		Last Modified: Tue, 07 Jan 2025 06:20:21 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d68cacf6fe4b54bc857a69776b0078df52e4b0edb50d4b9595ae47e97e2af5`  
		Last Modified: Tue, 07 Jan 2025 06:20:21 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:de9af5cb4485d7e53d223c2f2e5a7e7e62118e1f0f7f6c28e6d9d869673c723d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 KB (88536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:559fda02f71cbfaaa9934ec5b65f7a0c1de405e28468932e9dd21880a7f2aa6d`

```dockerfile
```

-	Layers:
	-	`sha256:20ed53337aa7afa648a3c2e36917ab1caff5c7803ea2fce77cf6e24884021bf8`  
		Last Modified: Tue, 07 Jan 2025 06:20:20 GMT  
		Size: 74.1 KB (74132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2c7ed91d6c6346126e45e47f5808ea8bfee2c51ef4ca4f1f5da160550f611da`  
		Last Modified: Tue, 07 Jan 2025 06:20:20 GMT  
		Size: 14.4 KB (14404 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:fdbb12824b88c7b18859c04cc8fbd31d6ccc84c135af3e8a2df261b38a10057f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4308713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c767cc3f98c29c28297080fd7c1d27c661584beb88a486df47d28053b48a455b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
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
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b19e3d04ec2b9d3001f2787d68b4b449f3e689a0d6f2f471a0386c4cfec4b1e`  
		Last Modified: Tue, 07 Jan 2025 07:09:34 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc909cbe9bc37ee1c83cc781499991aaf16f74091b8b3dc10087ccdb9cd8bbc1`  
		Last Modified: Tue, 07 Jan 2025 07:09:35 GMT  
		Size: 7.6 KB (7555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b65ae735ee44407b76890196851e37d2728197b6a257a567737116e76a178885`  
		Last Modified: Tue, 07 Jan 2025 07:09:35 GMT  
		Size: 213.1 KB (213077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac91bc929cadefcfdb1a75a0f2f5c44be39a2a126e2316a777d34e777cf25c0`  
		Last Modified: Tue, 07 Jan 2025 07:09:35 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b00577687504dcf1da7210e90b7144500242cd716a98cd945aee7317ff2b853`  
		Last Modified: Tue, 07 Jan 2025 07:09:35 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:278cb7494adb7b010caaa0fc5a6d18b19dde2a17677fef36fc1ba4852e0163a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 KB (88587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63b31a8595fc81a7abeaa1742e609cb7d6ddfa29e8382e0f625ebf7511d3679`

```dockerfile
```

-	Layers:
	-	`sha256:62af3aeae92f48ea868503a424e93b9c08260ae07dca8e88bddfca56b1593592`  
		Last Modified: Tue, 07 Jan 2025 07:09:35 GMT  
		Size: 74.2 KB (74152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3ca283b7fa2827d2d9cde0670b6d868f61d5adc4b68bc70bafc06cf1935e83b`  
		Last Modified: Tue, 07 Jan 2025 07:09:35 GMT  
		Size: 14.4 KB (14435 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2-alpine` - linux; 386

```console
$ docker pull spiped@sha256:78bc42e6a96585db8bdd8556e294d69b9ed44e4f789631e260b190a14e162735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3700771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:998f961e80b642a56013e83879523113a861992b529b3ff7b5767bc7cc7a628b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.4-x86.tar.gz / # buildkit
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
	-	`sha256:a48310298946cd9150f3929f2f8cebe3709f1c7ecd0e99ff2b0c9b6502172586`  
		Last Modified: Tue, 07 Jan 2025 02:28:41 GMT  
		Size: 3.5 MB (3463189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8423b800688f39626883f31d6f6e28c792f7b2c2b38eff3660b37b8f5985948a`  
		Last Modified: Tue, 07 Jan 2025 03:14:53 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc601454882a7f688874ee7eb6db905a8a1fd66fd8f74839f2616d43ffdbc60`  
		Last Modified: Tue, 07 Jan 2025 03:14:53 GMT  
		Size: 7.6 KB (7560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc540e07a100bef5d0924a05e52558c7723fdcadd6b9985563c7939ecd22f78`  
		Last Modified: Tue, 07 Jan 2025 03:14:53 GMT  
		Size: 228.6 KB (228627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:983f177c9f56963e5413b0628afb23e7b581d7f0e7829632fb472dee1d43e532`  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1d8a9e4cbb12b01b9a10d87658320bc01979d3f2709a0dd5613974a2270a64`  
		Last Modified: Tue, 07 Jan 2025 03:14:54 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:d94b06b62806c406a02f830533f8e5b1d274a4ec7af0a886324cb8b8033a8a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 KB (88337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6073d4c32fc43315273812b7e6dead1b7421f3d92e2abea2c62600438f9f7b9c`

```dockerfile
```

-	Layers:
	-	`sha256:d88073ad75f69f0118fa3fac91a25e5cfe758dcfc9b8933775ad48751cda23d8`  
		Last Modified: Tue, 07 Jan 2025 03:14:53 GMT  
		Size: 74.1 KB (74071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c93a63055383835cd30affb3ac53a708d8659bc3a31268b5bece883d901e9a75`  
		Last Modified: Tue, 07 Jan 2025 03:14:53 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:acf12ae1c612b3d71f4f4ba5eba9457c016eb0ffd7656079ecc6efec2d93d42a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3794399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28e53576b17bd09a0639a34556eac32bfd9a6c24b843678abbb73f14b018d01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.4-ppc64le.tar.gz / # buildkit
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
	-	`sha256:c96bc34ea0111931eae2007b7db67b205ebd3c8a096d711e1be59e48f25006a3`  
		Last Modified: Tue, 07 Jan 2025 02:32:24 GMT  
		Size: 3.6 MB (3568727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f58b562e7456d04a8a4485e9c2074a9e970f91fc0c31c84417492a091fb0d9`  
		Last Modified: Tue, 07 Jan 2025 06:13:44 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ecaa236d35dff0d883b4e1df8af1896bed049f98eb2ebf06b4d3abe1175285`  
		Last Modified: Tue, 07 Jan 2025 06:13:44 GMT  
		Size: 7.6 KB (7560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5452c07f1c981726006484a86ee19ada2152fc861cbf7fa64f93607f4c722ec8`  
		Size: 216.7 KB (216715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c840be9d9960807fda71ec5277170b84d7a4f1f302a40a60c6a58aa5d0e26b5`  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6cb66e59e31eb74643da37a8a614d258f5e133d1be21972cea66400c55efe2`  
		Last Modified: Tue, 07 Jan 2025 06:13:45 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:15bddc3596ae063a10a0f93e806478f1eabaeaeeb04e6c16767d5bf3a5aca278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 KB (86529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d84439a9043cd5c314ae04d742cc069d7ac73bb9250ed8097468189c63d97e`

```dockerfile
```

-	Layers:
	-	`sha256:f1d0853fb999d7e046e8fb680844a6937030b6d9961660dd42283d594427994d`  
		Last Modified: Tue, 07 Jan 2025 06:13:45 GMT  
		Size: 72.2 KB (72179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b05b1e01cb4427d75c873721837d33c9d94909ed405e90f19dbc76425fb45db`  
		Last Modified: Tue, 07 Jan 2025 06:13:44 GMT  
		Size: 14.3 KB (14350 bytes)  
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
$ docker pull spiped@sha256:2b056e84c73867952da7b22052f17a7df808b47516a5bb83b8ee13395dc5923d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3674138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3595de50a5f32e15b6db59451eae6913f4aba96c241c1107b30e84d282d1c841`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.4-s390x.tar.gz / # buildkit
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
	-	`sha256:2ed16bdf68dac880df118dfa3d21d44652bc18382729359f97297fa5998086cd`  
		Last Modified: Tue, 07 Jan 2025 02:32:49 GMT  
		Size: 3.5 MB (3459179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc1c58e04de4e903d567e58827a257047fc49b0eef9f83f28092313f82cbde8`  
		Last Modified: Tue, 07 Jan 2025 06:19:19 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797ce336a1e875ccc1cd81f71aff2122e82a35cc94121592994a0335577d072f`  
		Last Modified: Tue, 07 Jan 2025 06:19:19 GMT  
		Size: 7.6 KB (7562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876bf37cceecc9d224e361a1ad76cf766d3c66622e6bf682fed3bb15bb73ca6b`  
		Last Modified: Tue, 07 Jan 2025 06:19:19 GMT  
		Size: 206.0 KB (206006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef3d29125754db1b1c388a568ccaa80fa40fc0c2b9078aaae244b5a314eaa96`  
		Last Modified: Tue, 07 Jan 2025 06:19:19 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8bb164b00a2b113f38d85168412b681bebb59d60c7cd5639f5d336feb07d30`  
		Last Modified: Tue, 07 Jan 2025 06:19:20 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:dfa792f46cacda3f23b902f295f4c89e1405c9ecbbf35d3dc361b490cb5d2bd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 KB (86446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a50a77b62b00200a0d22583cee5739c50ef87fac5617e6a874a57b6ab43071bd`

```dockerfile
```

-	Layers:
	-	`sha256:2f8c8e6e444fb4067b5793ed502feadffb90b238f975366fb53d0618681dca0c`  
		Last Modified: Tue, 07 Jan 2025 06:19:19 GMT  
		Size: 72.1 KB (72145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0ae978c3bffb1c7f0cad075aee069f572a9513bee2ea6a85ca5f5f145836bc1`  
		Last Modified: Tue, 07 Jan 2025 06:19:19 GMT  
		Size: 14.3 KB (14301 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:alpine`

```console
$ docker pull spiped@sha256:f18720de28f93ecd77081a09f9fb50ef7b27e1b2f0ddd9e2a702e6547d67f8db
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
$ docker pull spiped@sha256:a2437bb32549fb26b2c5e2352337fa9b828b4529ac7c6d698d6dc35dfa6c4e39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3841253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e22840a5a70c56a7afdbbe563875d46c463af08f3803e89b942525fc8553dce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
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
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 23:53:52 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e7a51a2a61e8030d5392bd6a2f988a691d4bdd152f66dfcd44181b00fcffa5`  
		Last Modified: Tue, 07 Jan 2025 03:15:40 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e91285f9d5b26051e2a5c1577356ac3ca99ebc076b31c3d56c9af3687a0555`  
		Last Modified: Tue, 07 Jan 2025 03:15:40 GMT  
		Size: 7.5 KB (7549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b26d557ad63db6871840245fed75a25551bf86d6c43769731af10cec4e6556e5`  
		Last Modified: Tue, 07 Jan 2025 03:15:40 GMT  
		Size: 218.3 KB (218313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa628faafccfe7536bfe0751f2d14ba2361149efff1e1a40c3cdff322f7c7466`  
		Last Modified: Tue, 07 Jan 2025 03:15:40 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce3140b85b696b66b837bafaca07b043ce407975ddb7b5bfb9032d1eee2fd8e`  
		Last Modified: Tue, 07 Jan 2025 03:15:41 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:2dc54027609990d392a8ababdc4bbd5d0ce43886bfce0f58e9972886a290177b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 KB (88398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49d05c704ccdb0f5140bcd26d76d07e9aeb4e5e96c5fb973908352ba7aabb28b`

```dockerfile
```

-	Layers:
	-	`sha256:7bf8d5ef28bf164279c555c22ae6c52f2225df777335b6865fd4369badb65cd8`  
		Last Modified: Tue, 07 Jan 2025 03:15:40 GMT  
		Size: 74.1 KB (74096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a26a64c8c305fb0782b665571a4094d4c1d054b88078ffc8ec545539d2f771b8`  
		Last Modified: Tue, 07 Jan 2025 03:15:40 GMT  
		Size: 14.3 KB (14302 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:9b4d16f259f74f7ae9b1c1ecddaffcc30b885797ab1d60f0477cc840a52ce65f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3575623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:652d5f62598bd5ffe8ddc89e0d92496adc12ba2ca526ec27ba1fb42776b21137`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.4-armhf.tar.gz / # buildkit
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
	-	`sha256:9327c400cc7c63bc8696a8da86f21db1ffdb7ce43885aa521a67ab8105dd2af9`  
		Last Modified: Tue, 07 Jan 2025 02:29:49 GMT  
		Size: 3.4 MB (3363944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a29b8b207ad9555db0164f2c351570fbf0a53ccb093bd193b087063577055c1`  
		Last Modified: Tue, 07 Jan 2025 06:42:40 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f5a64d59e5b0c8f034f770c9eca85ca71ba9a73e463212f81d6e6a4462dbd5`  
		Last Modified: Wed, 08 Jan 2025 00:02:53 GMT  
		Size: 7.6 KB (7552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd01fb3f9a09a2dd08b845b169987bfb7853b6ee5808101bae8ca74c86a2e88`  
		Last Modified: Tue, 07 Jan 2025 06:42:41 GMT  
		Size: 202.7 KB (202728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927b498d6513dfddba82a6b7f7cdf3c87b13b7bf2fc3c425847c78fc33910be4`  
		Last Modified: Tue, 07 Jan 2025 06:42:41 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cbc736b391c47cbc09e98e86a9c513f62c662bbac310ec71e3e20bac5605cbf`  
		Last Modified: Tue, 07 Jan 2025 06:42:41 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:66c25ca1517901b4b08905893052a2fed202aae0879a1de61d38a727e133a02d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:772f571d35c16879a7ff3fa8f100987a1e571aab44cb51f62b75ee3555bd9b3c`

```dockerfile
```

-	Layers:
	-	`sha256:cd8b30cb15f8d9de66e419a8094744867e4734a5cc4d08a37d7d9f575bae5486`  
		Last Modified: Tue, 07 Jan 2025 06:42:40 GMT  
		Size: 14.2 KB (14189 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:317f548279e1c85c7ac74344b71832b8588d763e18e76af3950b2dbfce0c2e66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3296467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:816d532b96ad48e2d8eb9c9d3ceb60c51d8d8ca5ea971981c2741297c77b4e38`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.4-armv7.tar.gz / # buildkit
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
	-	`sha256:0695ed689d581197c59573cee0b2f2ef2c3a332e0d52bbb8f0e7e0865c2d5b23`  
		Last Modified: Tue, 07 Jan 2025 02:55:40 GMT  
		Size: 3.1 MB (3091288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05dfd721334f5542e7031dc7e4d8c1295bc566abdada8cd729209f7a0048138f`  
		Last Modified: Tue, 07 Jan 2025 06:20:20 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341cd5baaaebac2c76dbb23327031ffd02bbcde8f31957ed2e093dc0a3d7cae0`  
		Last Modified: Tue, 07 Jan 2025 06:20:20 GMT  
		Size: 7.6 KB (7562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1c1aefb60d120aa4f15d645553a6c856b198ec71d52178b5750253d9682292`  
		Last Modified: Tue, 07 Jan 2025 06:20:21 GMT  
		Size: 196.2 KB (196222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f0471c8ff4a4830446446ac80595a67a7b3327fe46ce8083fbd00d3aac033a`  
		Last Modified: Tue, 07 Jan 2025 06:20:21 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d68cacf6fe4b54bc857a69776b0078df52e4b0edb50d4b9595ae47e97e2af5`  
		Last Modified: Tue, 07 Jan 2025 06:20:21 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:de9af5cb4485d7e53d223c2f2e5a7e7e62118e1f0f7f6c28e6d9d869673c723d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 KB (88536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:559fda02f71cbfaaa9934ec5b65f7a0c1de405e28468932e9dd21880a7f2aa6d`

```dockerfile
```

-	Layers:
	-	`sha256:20ed53337aa7afa648a3c2e36917ab1caff5c7803ea2fce77cf6e24884021bf8`  
		Last Modified: Tue, 07 Jan 2025 06:20:20 GMT  
		Size: 74.1 KB (74132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2c7ed91d6c6346126e45e47f5808ea8bfee2c51ef4ca4f1f5da160550f611da`  
		Last Modified: Tue, 07 Jan 2025 06:20:20 GMT  
		Size: 14.4 KB (14404 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:fdbb12824b88c7b18859c04cc8fbd31d6ccc84c135af3e8a2df261b38a10057f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4308713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c767cc3f98c29c28297080fd7c1d27c661584beb88a486df47d28053b48a455b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
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
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b19e3d04ec2b9d3001f2787d68b4b449f3e689a0d6f2f471a0386c4cfec4b1e`  
		Last Modified: Tue, 07 Jan 2025 07:09:34 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc909cbe9bc37ee1c83cc781499991aaf16f74091b8b3dc10087ccdb9cd8bbc1`  
		Last Modified: Tue, 07 Jan 2025 07:09:35 GMT  
		Size: 7.6 KB (7555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b65ae735ee44407b76890196851e37d2728197b6a257a567737116e76a178885`  
		Last Modified: Tue, 07 Jan 2025 07:09:35 GMT  
		Size: 213.1 KB (213077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac91bc929cadefcfdb1a75a0f2f5c44be39a2a126e2316a777d34e777cf25c0`  
		Last Modified: Tue, 07 Jan 2025 07:09:35 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b00577687504dcf1da7210e90b7144500242cd716a98cd945aee7317ff2b853`  
		Last Modified: Tue, 07 Jan 2025 07:09:35 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:278cb7494adb7b010caaa0fc5a6d18b19dde2a17677fef36fc1ba4852e0163a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 KB (88587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63b31a8595fc81a7abeaa1742e609cb7d6ddfa29e8382e0f625ebf7511d3679`

```dockerfile
```

-	Layers:
	-	`sha256:62af3aeae92f48ea868503a424e93b9c08260ae07dca8e88bddfca56b1593592`  
		Last Modified: Tue, 07 Jan 2025 07:09:35 GMT  
		Size: 74.2 KB (74152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3ca283b7fa2827d2d9cde0670b6d868f61d5adc4b68bc70bafc06cf1935e83b`  
		Last Modified: Tue, 07 Jan 2025 07:09:35 GMT  
		Size: 14.4 KB (14435 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; 386

```console
$ docker pull spiped@sha256:78bc42e6a96585db8bdd8556e294d69b9ed44e4f789631e260b190a14e162735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3700771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:998f961e80b642a56013e83879523113a861992b529b3ff7b5767bc7cc7a628b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.4-x86.tar.gz / # buildkit
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
	-	`sha256:a48310298946cd9150f3929f2f8cebe3709f1c7ecd0e99ff2b0c9b6502172586`  
		Last Modified: Tue, 07 Jan 2025 02:28:41 GMT  
		Size: 3.5 MB (3463189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8423b800688f39626883f31d6f6e28c792f7b2c2b38eff3660b37b8f5985948a`  
		Last Modified: Tue, 07 Jan 2025 03:14:53 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc601454882a7f688874ee7eb6db905a8a1fd66fd8f74839f2616d43ffdbc60`  
		Last Modified: Tue, 07 Jan 2025 03:14:53 GMT  
		Size: 7.6 KB (7560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc540e07a100bef5d0924a05e52558c7723fdcadd6b9985563c7939ecd22f78`  
		Last Modified: Tue, 07 Jan 2025 03:14:53 GMT  
		Size: 228.6 KB (228627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:983f177c9f56963e5413b0628afb23e7b581d7f0e7829632fb472dee1d43e532`  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1d8a9e4cbb12b01b9a10d87658320bc01979d3f2709a0dd5613974a2270a64`  
		Last Modified: Tue, 07 Jan 2025 03:14:54 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:d94b06b62806c406a02f830533f8e5b1d274a4ec7af0a886324cb8b8033a8a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 KB (88337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6073d4c32fc43315273812b7e6dead1b7421f3d92e2abea2c62600438f9f7b9c`

```dockerfile
```

-	Layers:
	-	`sha256:d88073ad75f69f0118fa3fac91a25e5cfe758dcfc9b8933775ad48751cda23d8`  
		Last Modified: Tue, 07 Jan 2025 03:14:53 GMT  
		Size: 74.1 KB (74071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c93a63055383835cd30affb3ac53a708d8659bc3a31268b5bece883d901e9a75`  
		Last Modified: Tue, 07 Jan 2025 03:14:53 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:acf12ae1c612b3d71f4f4ba5eba9457c016eb0ffd7656079ecc6efec2d93d42a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3794399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28e53576b17bd09a0639a34556eac32bfd9a6c24b843678abbb73f14b018d01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.4-ppc64le.tar.gz / # buildkit
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
	-	`sha256:c96bc34ea0111931eae2007b7db67b205ebd3c8a096d711e1be59e48f25006a3`  
		Last Modified: Tue, 07 Jan 2025 02:32:24 GMT  
		Size: 3.6 MB (3568727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f58b562e7456d04a8a4485e9c2074a9e970f91fc0c31c84417492a091fb0d9`  
		Last Modified: Tue, 07 Jan 2025 06:13:44 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ecaa236d35dff0d883b4e1df8af1896bed049f98eb2ebf06b4d3abe1175285`  
		Last Modified: Tue, 07 Jan 2025 06:13:44 GMT  
		Size: 7.6 KB (7560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5452c07f1c981726006484a86ee19ada2152fc861cbf7fa64f93607f4c722ec8`  
		Size: 216.7 KB (216715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c840be9d9960807fda71ec5277170b84d7a4f1f302a40a60c6a58aa5d0e26b5`  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6cb66e59e31eb74643da37a8a614d258f5e133d1be21972cea66400c55efe2`  
		Last Modified: Tue, 07 Jan 2025 06:13:45 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:15bddc3596ae063a10a0f93e806478f1eabaeaeeb04e6c16767d5bf3a5aca278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 KB (86529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d84439a9043cd5c314ae04d742cc069d7ac73bb9250ed8097468189c63d97e`

```dockerfile
```

-	Layers:
	-	`sha256:f1d0853fb999d7e046e8fb680844a6937030b6d9961660dd42283d594427994d`  
		Last Modified: Tue, 07 Jan 2025 06:13:45 GMT  
		Size: 72.2 KB (72179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b05b1e01cb4427d75c873721837d33c9d94909ed405e90f19dbc76425fb45db`  
		Last Modified: Tue, 07 Jan 2025 06:13:44 GMT  
		Size: 14.3 KB (14350 bytes)  
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
$ docker pull spiped@sha256:2b056e84c73867952da7b22052f17a7df808b47516a5bb83b8ee13395dc5923d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3674138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3595de50a5f32e15b6db59451eae6913f4aba96c241c1107b30e84d282d1c841`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.4-s390x.tar.gz / # buildkit
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
	-	`sha256:2ed16bdf68dac880df118dfa3d21d44652bc18382729359f97297fa5998086cd`  
		Last Modified: Tue, 07 Jan 2025 02:32:49 GMT  
		Size: 3.5 MB (3459179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc1c58e04de4e903d567e58827a257047fc49b0eef9f83f28092313f82cbde8`  
		Last Modified: Tue, 07 Jan 2025 06:19:19 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797ce336a1e875ccc1cd81f71aff2122e82a35cc94121592994a0335577d072f`  
		Last Modified: Tue, 07 Jan 2025 06:19:19 GMT  
		Size: 7.6 KB (7562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876bf37cceecc9d224e361a1ad76cf766d3c66622e6bf682fed3bb15bb73ca6b`  
		Last Modified: Tue, 07 Jan 2025 06:19:19 GMT  
		Size: 206.0 KB (206006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef3d29125754db1b1c388a568ccaa80fa40fc0c2b9078aaae244b5a314eaa96`  
		Last Modified: Tue, 07 Jan 2025 06:19:19 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8bb164b00a2b113f38d85168412b681bebb59d60c7cd5639f5d336feb07d30`  
		Last Modified: Tue, 07 Jan 2025 06:19:20 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:dfa792f46cacda3f23b902f295f4c89e1405c9ecbbf35d3dc361b490cb5d2bd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 KB (86446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a50a77b62b00200a0d22583cee5739c50ef87fac5617e6a874a57b6ab43071bd`

```dockerfile
```

-	Layers:
	-	`sha256:2f8c8e6e444fb4067b5793ed502feadffb90b238f975366fb53d0618681dca0c`  
		Last Modified: Tue, 07 Jan 2025 06:19:19 GMT  
		Size: 72.1 KB (72145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0ae978c3bffb1c7f0cad075aee069f572a9513bee2ea6a85ca5f5f145836bc1`  
		Last Modified: Tue, 07 Jan 2025 06:19:19 GMT  
		Size: 14.3 KB (14301 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:latest`

```console
$ docker pull spiped@sha256:8d5c2be4b38e4dd0d2977de6a557dd1217c481b131092d2fc86b58aec32a2d01
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
$ docker pull spiped@sha256:40db27aa7bf41fa2069cb38a42c91f16e30afb71ecc98638aeb354525b6d295d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36152050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edccfe05ee79919ba17983ac76fb9b5e424f36b911bd78de0806bdfe94cf6c8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1734912000'
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
	-	`sha256:8a9f899eb883b68bbb36209214842bc927b7c446aa0471f0b241ae7e76adb6e5`  
		Last Modified: Tue, 24 Dec 2024 21:33:38 GMT  
		Size: 28.5 MB (28505873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1093361a7499794781b2579c11586abdbe5d3f2df6a47f37fac74efdfb68893`  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ac298b930dd94b2f9f52f24c80e05e67f1be3672276c85ad399c351032b087`  
		Last Modified: Wed, 25 Dec 2024 11:44:14 GMT  
		Size: 1.8 MB (1841056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872acbbc9e0c74dace76c2b05e8da8b3a8f7ecca12f50cff8bf687f1140f2e0a`  
		Last Modified: Wed, 25 Dec 2024 11:44:14 GMT  
		Size: 5.8 MB (5803579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d315c1ce1440d3be213f517aeb12ae5ef02ea5957a47b00aa7a2547e289395`  
		Last Modified: Wed, 25 Dec 2024 11:44:13 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed324a48a7751ab39997d72129fbb399275395ae6b9757f266299bf3a79e75b3`  
		Last Modified: Wed, 25 Dec 2024 11:44:14 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:f16b2264f8ef7c6f87eeb6e5be9c173d4b31873535eb434e99b9b35d2caed80f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a1a0d891081762c3f095d847e238aa5e22867bf1dbc1b48683b36ad6cfb5433`

```dockerfile
```

-	Layers:
	-	`sha256:f429d0a19254f7d3db7b8d2eb84831d6f0bf02d100dfd38c2092442567ddc27d`  
		Last Modified: Wed, 25 Dec 2024 11:44:13 GMT  
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
		Last Modified: Wed, 08 Jan 2025 00:29:06 GMT  
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
