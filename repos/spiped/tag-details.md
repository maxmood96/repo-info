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
$ docker pull spiped@sha256:11ce1ac8b2718d4bf53335a88287d47f4d7de92a7d96639e822d8b5bf5a4b013
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
$ docker pull spiped@sha256:0807efe8e57e7a74993be6066b8c4d4917a1f6e3611dd0833309a2f48e69d189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37086272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43af49e196ea5b3803a09fb654b9f3a31809b1d63db50efadc92753d2a5ea1b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb387415fb818a8b4d56b6c4b1981b2212e57ec6addac3a80cfb2b9d9331b50`  
		Last Modified: Tue, 14 Jan 2025 02:17:46 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228fe3a70b06fc8ca22481663a32d8b20b71b4a1cc2ef6bad63851b3cddc6a02`  
		Last Modified: Tue, 14 Jan 2025 02:17:46 GMT  
		Size: 2.4 MB (2401340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bdc698a91b053c8c6c8793884aeb21f069855e2f35ceaf6d354563a622ec60`  
		Last Modified: Tue, 14 Jan 2025 02:17:47 GMT  
		Size: 6.5 MB (6470976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562950f9b4e1da298d9932319a15c677ac7b1072f4a6218a62318ec083a438bf`  
		Last Modified: Tue, 14 Jan 2025 02:17:46 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d26d7b3a2a6d5bfa2d8845580756d251c7acbb85868393a8dc4b15857a936c`  
		Last Modified: Tue, 14 Jan 2025 02:17:47 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:4596a995a081e15712ce75ccbd6382c0362bbb99730c9b479c48fb6deb3de184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3530854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb27c549da9cd3fd74e3b201a56fe8440fe2368fbba1fa80abc7dac9262ff93`

```dockerfile
```

-	Layers:
	-	`sha256:d833741283a7f0cc036493894e91aa8f599339f065480034207be52408751f12`  
		Last Modified: Tue, 14 Jan 2025 02:17:47 GMT  
		Size: 3.5 MB (3515814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ab16c690e615571a539221290f9c7154ed500a5de18d47dfbe3d130daff486f`  
		Last Modified: Tue, 14 Jan 2025 02:17:46 GMT  
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
$ docker pull spiped@sha256:50dc383a39b7bbf8bc7274000476568ef19f00fa47f5e77a3b945e542d602e87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37529245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff3adfb5bcb041fd776f222523c7e5f7d316c3a84275c48f8a469520e3cf670`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
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
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 01:33:46 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9757c47c7f65469fabaf649c24c76e71b0ee344186b7378388e73b9ff3584956`  
		Last Modified: Tue, 14 Jan 2025 02:17:03 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41f696ea1cea6b748d59acb3f0e93feb73a67b208dc03bdd8d489b78b8c4c1c`  
		Last Modified: Tue, 14 Jan 2025 02:17:04 GMT  
		Size: 2.4 MB (2398649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241faa93dbe7603d3ddfe8143dbc5f7e9990a80036efae46f8147ce9b8e684d7`  
		Last Modified: Tue, 14 Jan 2025 02:17:04 GMT  
		Size: 5.9 MB (5941461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac324e1750c72f49ee4d4c3b000ae242266e9e9b1946584a5a221c6d4b01bbe9`  
		Last Modified: Tue, 14 Jan 2025 02:17:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6f5c66d701ad1b4e0469df5595f673c4d111557d936709a7c5ab15e2ca0f378`  
		Last Modified: Tue, 14 Jan 2025 02:17:04 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:78318e0a0bae94e38b3a5d9c7578f6751580c7038fd2e2660d4d7cc768105076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed705c7a2f1d4214425c51ed536dd3d3ab550dfbe9a1b50c38de8bba85e59791`

```dockerfile
```

-	Layers:
	-	`sha256:b0eb158509e496490a1fa281c429ec733f8201538a8ead508644c888a4a09018`  
		Last Modified: Tue, 14 Jan 2025 02:17:04 GMT  
		Size: 3.5 MB (3509741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08e8230d3f815bb664e5eda60129ff633bc7d34854e10e52903d538454410d33`  
		Last Modified: Tue, 14 Jan 2025 02:17:03 GMT  
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
		Last Modified: Wed, 25 Dec 2024 11:44:13 GMT  
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
$ docker pull spiped@sha256:3defbc7042c9287d78d336478981bdf2410928e48fd8a9504755509633620376
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
$ docker pull spiped@sha256:924e7f71ff8a6210c218250cadec128119d344f463da73b7435727f3b79f8b8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3860004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:002ee6ce7d381016e688df520b2d8e452892442cc9dd7d7fe4f2fd27e10bd9cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
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
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4d648a75810ee71e4a811a07ea0f0ac2c721e73e72187e9a1516d4c4c5ee6f`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe07a72f4be9ce0f108da046cf545981624f6b49403d76321af17c0c395f286d`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 7.5 KB (7550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda92c005435cc07d0f9aeede336b39adeacb3d2b63892bd145844c2ffdee52b`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 224.8 KB (224801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d408faf96bb5ca591f0228176fd9fe8fcadf008b4a1d270852fc8c6e4ba93ef1`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403e29defa7a55825f8f61eda130cb04ee394d66bd712f70709ac7053a248548`  
		Last Modified: Wed, 08 Jan 2025 18:12:48 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:bbb6e45e7eb3500533fd5eb9b6e02cbb71696097c25c94d70ad5011ff89719b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 KB (88397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ed9b89a1c4bf4f119be92f17b9244feb5432b0aa95a99a543b91711e64d2ff`

```dockerfile
```

-	Layers:
	-	`sha256:d6dbec5f27c384596dd421778e731d1e085e3759f6d847458fe59a756fb7ac42`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 74.1 KB (74096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb9a321a7ee93632ee08168238d08c393bd8977dc0b90058743b7578fd3ffc57`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 14.3 KB (14301 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:3b33305e723d928de0ceb007a192d635fbcead1966adcef42495013c151ab1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3589779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3908b8302a74d29d2ba4f9fad53ec5dae4d694c59ef5e425f9d3b4ae6f8e82c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-armhf.tar.gz / # buildkit
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
	-	`sha256:27a1f2308f194d2c8cfe617a324e0078d055d65032c6c342eae11afb7a8d38c0`  
		Last Modified: Wed, 08 Jan 2025 17:23:56 GMT  
		Size: 3.4 MB (3371473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af3f0630555eb148818822fb59b573ef21353f360d8de1a31a9d923807ee4cd`  
		Last Modified: Wed, 08 Jan 2025 21:50:16 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779a48568101672a32588570e7ceef7c0674397cbfa25ee720cde2859ab94873`  
		Last Modified: Wed, 08 Jan 2025 21:50:16 GMT  
		Size: 7.5 KB (7549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a21818ff816934f603fcd2d4cba9f12db282bab07e3069da21d7578259ccec`  
		Last Modified: Wed, 08 Jan 2025 21:50:17 GMT  
		Size: 209.4 KB (209360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908425f61ccde4470882b7fc3250f120af7e457373de37561ca1bc2c428156fb`  
		Last Modified: Wed, 08 Jan 2025 21:50:16 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d99959ccf8e07e46905c21480b4a1efde735673420d31417427ecef2146095`  
		Last Modified: Wed, 08 Jan 2025 21:50:17 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b7cb53f249d979d695f81563768605e871ddd1ea8a0819dd8dd81dc4987a573f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:755f963c27fded64f7e3f6ff08da27dc1fd056f8030a81de4cb41f27e65d037b`

```dockerfile
```

-	Layers:
	-	`sha256:696c936ae51f846bce7be1a6d2dde5c03aa3b71ffda41e1e6b2cf2a621f6cd97`  
		Last Modified: Wed, 08 Jan 2025 21:50:16 GMT  
		Size: 14.2 KB (14189 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:ae8dad9afbb0cc8a3d199d4f081244152b6bb25a314d1c1b53d2015cb7a3148c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3307454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db4e1533dc661a40478a134b3fe58301335db42d8f87ae18e6918ff38e81ae91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-armv7.tar.gz / # buildkit
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
	-	`sha256:c8a32ed454e751770c0976636b8d0d0fccc4f778a2dd26c428067d613be1a299`  
		Last Modified: Wed, 08 Jan 2025 17:34:15 GMT  
		Size: 3.1 MB (3095514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7fdb315d3c34eb6935e1b7deb703093f5317800ff4d8b3936d5f771137cb79`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3360ef971eae752027c0ac2e924cac0c91b7f45b5099026b2a8f4be3279f6b5`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 7.6 KB (7566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70480e7090e82ed5e217b413501ec1d1ac188d14349be7aa351d6ebc4bfa572b`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 203.0 KB (202981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa024b8e7a4dcd96a95ba7c408a6b6bf086e89742d975c9ce4fdfcfc7cabc1b`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4350bd55dee2c6c0b00a05b33f36a79b911cbfa491acf490c5bdc593d8e3e547`  
		Last Modified: Wed, 08 Jan 2025 21:55:30 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:374da430416cd603b6845710a7b6b98de8856fb9d596f167daa655438d68910f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 KB (88536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddfb7685b3853e3be4a1172afeae58a3bd43dbc7f6bf21565a8d6843e6b79559`

```dockerfile
```

-	Layers:
	-	`sha256:d4af9f6a3307489ccc6bd25b80644c322c26bf5739a42dab919b2dc03edff9ab`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 74.1 KB (74132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d585d482698adea511246e8d288a1602e3c63dc4f235cfa0915b12ae4b080f64`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 14.4 KB (14404 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:3565ca7a9021c033aa2f9aa3fa95ec43241003635fa8669990453c55ff55e1e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4319245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aa0a984328f7027e356ee0aa46ff85666d4fdeec5eb2d5343a30a9dbe998445`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
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
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3f2d3fc3adfdd301f5e24f24c5392b9879a1b61f182e7752a21cb03e6aeb04`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d972687789bff098d9b33d09c024319254bdf8dcd29abb2bf072809733c79f49`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 7.6 KB (7561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37195bfd737aa3f22ef0dd56d792afbe7e88b9c83db3bf0e69cb557d04d0d152`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 219.5 KB (219522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9420b682506ca5859fc3f4af6d59a5ca6fb329a69a869e8d7d0766374eb87ae7`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f38e672eaca427117d78c3580183cebdd51913b95165f7a4fecbb7219aeb29`  
		Last Modified: Wed, 08 Jan 2025 22:06:49 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:c1545d907101296a82932a434f77b80a720493d1f158f28037a360c849c6b869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 KB (88588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af58e3c42e72d2f836cf482efb095b5869000f90e0fd8c744622051f65cbeb6`

```dockerfile
```

-	Layers:
	-	`sha256:802dad5a525c4dc8453a7af1d74e5f8e0f8e9db9e0b53075b1abb70ebcbcac58`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 74.2 KB (74152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f31d587a383d8f42361fc2623919a7a23e16261c7eb1f51cb4aa140497be4935`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 14.4 KB (14436 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; 386

```console
$ docker pull spiped@sha256:92342ba21763b953dae5124e2470d7b310cdec0e1aa1c278c715dda9eb6c5a0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3715310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a710174a0b36bde4dc08b5531a97264b1a956e7b607e3cb81fa4ed42446333`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-x86.tar.gz / # buildkit
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
	-	`sha256:6d632fc6244662e41ee3b3f29090684a520e615dc5c282638a7587366dcd4fb9`  
		Last Modified: Wed, 08 Jan 2025 17:23:34 GMT  
		Size: 3.5 MB (3470969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01646177e05c873338d049d0058c8cd923326812215a3897564adbd669ee56f`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf3460ecbeac950e26287d1cf9fdf47918bf993988d851835f852bbd5707856`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 7.6 KB (7563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69044b34b50595fbdc42e577dc79e206d3962968154ec6fbf18024dfe607c6cd`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 235.4 KB (235383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e2fe84ec006ef02b90eb19d8de0f72b59b1f5d3cad78ef6d043f1ea320d121`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8feb2512bb10b2b05cf6ac1f623ac53ae1aaaf4d759aa98618bf0a96439d0c`  
		Last Modified: Wed, 08 Jan 2025 18:07:24 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f82eea4e46a614570a5475a2c2999ebdb44416593095c39bfe597dfb70954205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 KB (88337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c43d43c6b18f013ddf9e79c05395cc1213c96194b62e9231a34602566ed737c`

```dockerfile
```

-	Layers:
	-	`sha256:662bb99fc24ff68d14f1e276dc7da9f11ef9f56131659d2a511578d1c4547a4e`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 74.1 KB (74071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ab4679badb23f30ba84ac1e7ab274f8693e730ac87dbfac78c97707c071c360`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:62a8529f4a88431c2c8453c2198b9f19f5027af08967a818ceb2e9f5485a2d10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3806729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b6428f7bf466f0e03b157ec2507c547f21126e87e9b2e288213771e8ccfd2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
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
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Wed, 08 Jan 2025 17:24:56 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d50e862e95a905933f50b6440c968976a25afd06a9808138b7b662be556076`  
		Last Modified: Wed, 08 Jan 2025 21:29:14 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca1e9dba23dfea2ee87d2657bcd8e5e57a74b668b777c31cdf12a5a688c9e23`  
		Last Modified: Wed, 08 Jan 2025 21:29:14 GMT  
		Size: 7.6 KB (7562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b2864e003337f2f79f0ebbd5d8f47c821a711805de5ac4aac9a3f02a5d06b3`  
		Last Modified: Wed, 08 Jan 2025 21:29:15 GMT  
		Size: 223.4 KB (223364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b04a1708fbc0147d4ef6fdeb564449a7a41b7b0e5df2aa27a1441946c81598c`  
		Last Modified: Wed, 08 Jan 2025 21:29:14 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66b8e9453e2d649488c8d053b0d1d4ae5e3740489586c6bb32f7eae7a3ec003`  
		Last Modified: Wed, 08 Jan 2025 21:29:15 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:641f93fddb6e6a668353356d78a708a17b7271ab06e13c5d2d1645d499c65794
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 KB (86529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1511f0eb48159856515b99abf8dee3e56263f52094148ce660d713454d210ec3`

```dockerfile
```

-	Layers:
	-	`sha256:55e5c3dc4287df2df2d9e20c08f5cd46d57a5616350e241f492bf844c18956d1`  
		Last Modified: Wed, 08 Jan 2025 21:29:14 GMT  
		Size: 72.2 KB (72179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9f348d15a848da4a767fe70750751a3015a5b347ab3175554ad77137d71526a`  
		Last Modified: Wed, 08 Jan 2025 21:29:14 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:79982546d0bed357c3b7f570dab84958af0f189249fe28e89577d41749385d17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3596676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84f4d20594fd72e32a00a9feabc004f2a01714cd681f91d6012c8315cb905ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-riscv64.tar.gz / # buildkit
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
	-	`sha256:34b7590cc8ea3b21e8c3a0d69270b822d3ba63bc58c6cf0e36c987c95b18eb8d`  
		Last Modified: Wed, 08 Jan 2025 17:49:41 GMT  
		Size: 3.4 MB (3371926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afdd5abd6a9641f814dc31398b1f41f1208ca3c43eafd4a1c8885cb772431cc5`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473a53dcc89c2068574226fb084968b4ffe7be1af4300f024b632369f8a8c233`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 7.6 KB (7561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113dcefb1595560f60660ee7a991d2b59509bc30e01ceddb44741db3ef240384`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 215.8 KB (215788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659fa19d2020016e65ba76874ea424e5842bf892ef9cbb0fb225538f1e187cf7`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecff65919c3bd12f584108c1e36a3685a85470a54c58c385eb56d95175f5ab8c`  
		Last Modified: Fri, 10 Jan 2025 16:34:52 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:1fe29fb7531300754b92edf6a17cb43bbf6bdccf3669dda2f135e21ecd7bc35d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 KB (86525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d832c44e71bd3c5c8e4af761656415c7160b797f2992b90ae6ccd9ad1d3bae`

```dockerfile
```

-	Layers:
	-	`sha256:22ce3c1ef9750e4e84284967ee5eccca34b598a38edbca4cd170feb5ca477190`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 72.2 KB (72175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aff322ae82649ec4042d09e767199a7e60414c2658b767de2a09545e6bc998d`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:8e65076fea6d36aa50870267c91ec6d95243f1fb11c28be61a1d14cc261f1cdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3684480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3f24babcb5d8bb3f6840a272a25b4d6bdcfcea3fcb3a940801065c5753d9538`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-s390x.tar.gz / # buildkit
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
	-	`sha256:3e71c43ed556c3ed564b517d9141db651f4134655f96c8731767c14c6dedc4d0`  
		Last Modified: Wed, 08 Jan 2025 17:25:57 GMT  
		Size: 3.5 MB (3463322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe78366bb027e03c42216a6e1d382df7a3ee78f1471f4c62ff2d535ec78d8ce`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644fc493adbda1d67b109c8285fbc4e3c1d916ad0fdd4e52b1d30d0c3b5a8b83`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 7.6 KB (7558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b5aca5c5549a3999391bdaf9bfdf23ae037d07dd0278bcc20a847480979e45`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 212.2 KB (212205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:176ea9af669d43767bfdf3ce63602addb4cf802565986d5dc091d471acc30fe8`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d93146a4a9bfc5584cd3df6a564e1f4ed3da6472cd8f41e6e08d7031d0c8114`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:93f271bcfc043724cd8ed10b5a81e091db12c7c9d2e449003a555df7b3164e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 KB (86446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e388d85c4a8c82382bf1c9f50c1c9b6f983abffb8517c5e88afc7ecb4b51d7af`

```dockerfile
```

-	Layers:
	-	`sha256:2f690c178f9bae18125b1de0d54e1b4493b26e2f974141f5f5fd3c9d3a20c6cb`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 72.1 KB (72145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8043e5e2fb4d14db768fcedf2f5c98e22493faee4d4820a99c0fb644ece380fc`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 14.3 KB (14301 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6`

```console
$ docker pull spiped@sha256:11ce1ac8b2718d4bf53335a88287d47f4d7de92a7d96639e822d8b5bf5a4b013
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
$ docker pull spiped@sha256:0807efe8e57e7a74993be6066b8c4d4917a1f6e3611dd0833309a2f48e69d189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37086272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43af49e196ea5b3803a09fb654b9f3a31809b1d63db50efadc92753d2a5ea1b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb387415fb818a8b4d56b6c4b1981b2212e57ec6addac3a80cfb2b9d9331b50`  
		Last Modified: Tue, 14 Jan 2025 02:17:46 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228fe3a70b06fc8ca22481663a32d8b20b71b4a1cc2ef6bad63851b3cddc6a02`  
		Last Modified: Tue, 14 Jan 2025 02:17:46 GMT  
		Size: 2.4 MB (2401340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bdc698a91b053c8c6c8793884aeb21f069855e2f35ceaf6d354563a622ec60`  
		Last Modified: Tue, 14 Jan 2025 02:17:47 GMT  
		Size: 6.5 MB (6470976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562950f9b4e1da298d9932319a15c677ac7b1072f4a6218a62318ec083a438bf`  
		Last Modified: Tue, 14 Jan 2025 02:17:46 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d26d7b3a2a6d5bfa2d8845580756d251c7acbb85868393a8dc4b15857a936c`  
		Last Modified: Tue, 14 Jan 2025 02:17:47 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:4596a995a081e15712ce75ccbd6382c0362bbb99730c9b479c48fb6deb3de184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3530854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb27c549da9cd3fd74e3b201a56fe8440fe2368fbba1fa80abc7dac9262ff93`

```dockerfile
```

-	Layers:
	-	`sha256:d833741283a7f0cc036493894e91aa8f599339f065480034207be52408751f12`  
		Last Modified: Tue, 14 Jan 2025 02:17:47 GMT  
		Size: 3.5 MB (3515814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ab16c690e615571a539221290f9c7154ed500a5de18d47dfbe3d130daff486f`  
		Last Modified: Tue, 14 Jan 2025 02:17:46 GMT  
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
$ docker pull spiped@sha256:50dc383a39b7bbf8bc7274000476568ef19f00fa47f5e77a3b945e542d602e87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37529245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff3adfb5bcb041fd776f222523c7e5f7d316c3a84275c48f8a469520e3cf670`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
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
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 01:33:46 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9757c47c7f65469fabaf649c24c76e71b0ee344186b7378388e73b9ff3584956`  
		Last Modified: Tue, 14 Jan 2025 02:17:03 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41f696ea1cea6b748d59acb3f0e93feb73a67b208dc03bdd8d489b78b8c4c1c`  
		Last Modified: Tue, 14 Jan 2025 02:17:04 GMT  
		Size: 2.4 MB (2398649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241faa93dbe7603d3ddfe8143dbc5f7e9990a80036efae46f8147ce9b8e684d7`  
		Last Modified: Tue, 14 Jan 2025 02:17:04 GMT  
		Size: 5.9 MB (5941461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac324e1750c72f49ee4d4c3b000ae242266e9e9b1946584a5a221c6d4b01bbe9`  
		Last Modified: Tue, 14 Jan 2025 02:17:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6f5c66d701ad1b4e0469df5595f673c4d111557d936709a7c5ab15e2ca0f378`  
		Last Modified: Tue, 14 Jan 2025 02:17:04 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:78318e0a0bae94e38b3a5d9c7578f6751580c7038fd2e2660d4d7cc768105076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed705c7a2f1d4214425c51ed536dd3d3ab550dfbe9a1b50c38de8bba85e59791`

```dockerfile
```

-	Layers:
	-	`sha256:b0eb158509e496490a1fa281c429ec733f8201538a8ead508644c888a4a09018`  
		Last Modified: Tue, 14 Jan 2025 02:17:04 GMT  
		Size: 3.5 MB (3509741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08e8230d3f815bb664e5eda60129ff633bc7d34854e10e52903d538454410d33`  
		Last Modified: Tue, 14 Jan 2025 02:17:03 GMT  
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
		Last Modified: Wed, 25 Dec 2024 11:44:13 GMT  
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
$ docker pull spiped@sha256:3defbc7042c9287d78d336478981bdf2410928e48fd8a9504755509633620376
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
$ docker pull spiped@sha256:924e7f71ff8a6210c218250cadec128119d344f463da73b7435727f3b79f8b8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3860004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:002ee6ce7d381016e688df520b2d8e452892442cc9dd7d7fe4f2fd27e10bd9cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
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
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4d648a75810ee71e4a811a07ea0f0ac2c721e73e72187e9a1516d4c4c5ee6f`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe07a72f4be9ce0f108da046cf545981624f6b49403d76321af17c0c395f286d`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 7.5 KB (7550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda92c005435cc07d0f9aeede336b39adeacb3d2b63892bd145844c2ffdee52b`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 224.8 KB (224801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d408faf96bb5ca591f0228176fd9fe8fcadf008b4a1d270852fc8c6e4ba93ef1`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403e29defa7a55825f8f61eda130cb04ee394d66bd712f70709ac7053a248548`  
		Last Modified: Wed, 08 Jan 2025 18:12:48 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:bbb6e45e7eb3500533fd5eb9b6e02cbb71696097c25c94d70ad5011ff89719b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 KB (88397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ed9b89a1c4bf4f119be92f17b9244feb5432b0aa95a99a543b91711e64d2ff`

```dockerfile
```

-	Layers:
	-	`sha256:d6dbec5f27c384596dd421778e731d1e085e3759f6d847458fe59a756fb7ac42`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 74.1 KB (74096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb9a321a7ee93632ee08168238d08c393bd8977dc0b90058743b7578fd3ffc57`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 14.3 KB (14301 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:3b33305e723d928de0ceb007a192d635fbcead1966adcef42495013c151ab1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3589779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3908b8302a74d29d2ba4f9fad53ec5dae4d694c59ef5e425f9d3b4ae6f8e82c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-armhf.tar.gz / # buildkit
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
	-	`sha256:27a1f2308f194d2c8cfe617a324e0078d055d65032c6c342eae11afb7a8d38c0`  
		Last Modified: Wed, 08 Jan 2025 17:23:56 GMT  
		Size: 3.4 MB (3371473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af3f0630555eb148818822fb59b573ef21353f360d8de1a31a9d923807ee4cd`  
		Last Modified: Wed, 08 Jan 2025 21:50:16 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779a48568101672a32588570e7ceef7c0674397cbfa25ee720cde2859ab94873`  
		Last Modified: Wed, 08 Jan 2025 21:50:16 GMT  
		Size: 7.5 KB (7549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a21818ff816934f603fcd2d4cba9f12db282bab07e3069da21d7578259ccec`  
		Last Modified: Wed, 08 Jan 2025 21:50:17 GMT  
		Size: 209.4 KB (209360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908425f61ccde4470882b7fc3250f120af7e457373de37561ca1bc2c428156fb`  
		Last Modified: Wed, 08 Jan 2025 21:50:16 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d99959ccf8e07e46905c21480b4a1efde735673420d31417427ecef2146095`  
		Last Modified: Wed, 08 Jan 2025 21:50:17 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b7cb53f249d979d695f81563768605e871ddd1ea8a0819dd8dd81dc4987a573f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:755f963c27fded64f7e3f6ff08da27dc1fd056f8030a81de4cb41f27e65d037b`

```dockerfile
```

-	Layers:
	-	`sha256:696c936ae51f846bce7be1a6d2dde5c03aa3b71ffda41e1e6b2cf2a621f6cd97`  
		Last Modified: Wed, 08 Jan 2025 21:50:16 GMT  
		Size: 14.2 KB (14189 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:ae8dad9afbb0cc8a3d199d4f081244152b6bb25a314d1c1b53d2015cb7a3148c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3307454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db4e1533dc661a40478a134b3fe58301335db42d8f87ae18e6918ff38e81ae91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-armv7.tar.gz / # buildkit
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
	-	`sha256:c8a32ed454e751770c0976636b8d0d0fccc4f778a2dd26c428067d613be1a299`  
		Last Modified: Wed, 08 Jan 2025 17:34:15 GMT  
		Size: 3.1 MB (3095514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7fdb315d3c34eb6935e1b7deb703093f5317800ff4d8b3936d5f771137cb79`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3360ef971eae752027c0ac2e924cac0c91b7f45b5099026b2a8f4be3279f6b5`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 7.6 KB (7566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70480e7090e82ed5e217b413501ec1d1ac188d14349be7aa351d6ebc4bfa572b`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 203.0 KB (202981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa024b8e7a4dcd96a95ba7c408a6b6bf086e89742d975c9ce4fdfcfc7cabc1b`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4350bd55dee2c6c0b00a05b33f36a79b911cbfa491acf490c5bdc593d8e3e547`  
		Last Modified: Wed, 08 Jan 2025 21:55:30 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:374da430416cd603b6845710a7b6b98de8856fb9d596f167daa655438d68910f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 KB (88536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddfb7685b3853e3be4a1172afeae58a3bd43dbc7f6bf21565a8d6843e6b79559`

```dockerfile
```

-	Layers:
	-	`sha256:d4af9f6a3307489ccc6bd25b80644c322c26bf5739a42dab919b2dc03edff9ab`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 74.1 KB (74132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d585d482698adea511246e8d288a1602e3c63dc4f235cfa0915b12ae4b080f64`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 14.4 KB (14404 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:3565ca7a9021c033aa2f9aa3fa95ec43241003635fa8669990453c55ff55e1e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4319245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aa0a984328f7027e356ee0aa46ff85666d4fdeec5eb2d5343a30a9dbe998445`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
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
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3f2d3fc3adfdd301f5e24f24c5392b9879a1b61f182e7752a21cb03e6aeb04`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d972687789bff098d9b33d09c024319254bdf8dcd29abb2bf072809733c79f49`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 7.6 KB (7561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37195bfd737aa3f22ef0dd56d792afbe7e88b9c83db3bf0e69cb557d04d0d152`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 219.5 KB (219522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9420b682506ca5859fc3f4af6d59a5ca6fb329a69a869e8d7d0766374eb87ae7`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f38e672eaca427117d78c3580183cebdd51913b95165f7a4fecbb7219aeb29`  
		Last Modified: Wed, 08 Jan 2025 22:06:49 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:c1545d907101296a82932a434f77b80a720493d1f158f28037a360c849c6b869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 KB (88588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af58e3c42e72d2f836cf482efb095b5869000f90e0fd8c744622051f65cbeb6`

```dockerfile
```

-	Layers:
	-	`sha256:802dad5a525c4dc8453a7af1d74e5f8e0f8e9db9e0b53075b1abb70ebcbcac58`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 74.2 KB (74152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f31d587a383d8f42361fc2623919a7a23e16261c7eb1f51cb4aa140497be4935`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 14.4 KB (14436 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; 386

```console
$ docker pull spiped@sha256:92342ba21763b953dae5124e2470d7b310cdec0e1aa1c278c715dda9eb6c5a0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3715310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a710174a0b36bde4dc08b5531a97264b1a956e7b607e3cb81fa4ed42446333`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-x86.tar.gz / # buildkit
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
	-	`sha256:6d632fc6244662e41ee3b3f29090684a520e615dc5c282638a7587366dcd4fb9`  
		Last Modified: Wed, 08 Jan 2025 17:23:34 GMT  
		Size: 3.5 MB (3470969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01646177e05c873338d049d0058c8cd923326812215a3897564adbd669ee56f`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf3460ecbeac950e26287d1cf9fdf47918bf993988d851835f852bbd5707856`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 7.6 KB (7563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69044b34b50595fbdc42e577dc79e206d3962968154ec6fbf18024dfe607c6cd`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 235.4 KB (235383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e2fe84ec006ef02b90eb19d8de0f72b59b1f5d3cad78ef6d043f1ea320d121`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8feb2512bb10b2b05cf6ac1f623ac53ae1aaaf4d759aa98618bf0a96439d0c`  
		Last Modified: Wed, 08 Jan 2025 18:07:24 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f82eea4e46a614570a5475a2c2999ebdb44416593095c39bfe597dfb70954205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 KB (88337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c43d43c6b18f013ddf9e79c05395cc1213c96194b62e9231a34602566ed737c`

```dockerfile
```

-	Layers:
	-	`sha256:662bb99fc24ff68d14f1e276dc7da9f11ef9f56131659d2a511578d1c4547a4e`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 74.1 KB (74071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ab4679badb23f30ba84ac1e7ab274f8693e730ac87dbfac78c97707c071c360`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:62a8529f4a88431c2c8453c2198b9f19f5027af08967a818ceb2e9f5485a2d10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3806729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b6428f7bf466f0e03b157ec2507c547f21126e87e9b2e288213771e8ccfd2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
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
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Wed, 08 Jan 2025 17:24:56 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d50e862e95a905933f50b6440c968976a25afd06a9808138b7b662be556076`  
		Last Modified: Wed, 08 Jan 2025 21:29:14 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca1e9dba23dfea2ee87d2657bcd8e5e57a74b668b777c31cdf12a5a688c9e23`  
		Last Modified: Wed, 08 Jan 2025 21:29:14 GMT  
		Size: 7.6 KB (7562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b2864e003337f2f79f0ebbd5d8f47c821a711805de5ac4aac9a3f02a5d06b3`  
		Last Modified: Wed, 08 Jan 2025 21:29:15 GMT  
		Size: 223.4 KB (223364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b04a1708fbc0147d4ef6fdeb564449a7a41b7b0e5df2aa27a1441946c81598c`  
		Last Modified: Wed, 08 Jan 2025 21:29:14 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66b8e9453e2d649488c8d053b0d1d4ae5e3740489586c6bb32f7eae7a3ec003`  
		Last Modified: Wed, 08 Jan 2025 21:29:15 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:641f93fddb6e6a668353356d78a708a17b7271ab06e13c5d2d1645d499c65794
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 KB (86529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1511f0eb48159856515b99abf8dee3e56263f52094148ce660d713454d210ec3`

```dockerfile
```

-	Layers:
	-	`sha256:55e5c3dc4287df2df2d9e20c08f5cd46d57a5616350e241f492bf844c18956d1`  
		Last Modified: Wed, 08 Jan 2025 21:29:14 GMT  
		Size: 72.2 KB (72179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9f348d15a848da4a767fe70750751a3015a5b347ab3175554ad77137d71526a`  
		Last Modified: Wed, 08 Jan 2025 21:29:14 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:79982546d0bed357c3b7f570dab84958af0f189249fe28e89577d41749385d17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3596676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84f4d20594fd72e32a00a9feabc004f2a01714cd681f91d6012c8315cb905ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-riscv64.tar.gz / # buildkit
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
	-	`sha256:34b7590cc8ea3b21e8c3a0d69270b822d3ba63bc58c6cf0e36c987c95b18eb8d`  
		Last Modified: Wed, 08 Jan 2025 17:49:41 GMT  
		Size: 3.4 MB (3371926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afdd5abd6a9641f814dc31398b1f41f1208ca3c43eafd4a1c8885cb772431cc5`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473a53dcc89c2068574226fb084968b4ffe7be1af4300f024b632369f8a8c233`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 7.6 KB (7561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113dcefb1595560f60660ee7a991d2b59509bc30e01ceddb44741db3ef240384`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 215.8 KB (215788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659fa19d2020016e65ba76874ea424e5842bf892ef9cbb0fb225538f1e187cf7`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecff65919c3bd12f584108c1e36a3685a85470a54c58c385eb56d95175f5ab8c`  
		Last Modified: Fri, 10 Jan 2025 16:34:52 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:1fe29fb7531300754b92edf6a17cb43bbf6bdccf3669dda2f135e21ecd7bc35d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 KB (86525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d832c44e71bd3c5c8e4af761656415c7160b797f2992b90ae6ccd9ad1d3bae`

```dockerfile
```

-	Layers:
	-	`sha256:22ce3c1ef9750e4e84284967ee5eccca34b598a38edbca4cd170feb5ca477190`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 72.2 KB (72175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aff322ae82649ec4042d09e767199a7e60414c2658b767de2a09545e6bc998d`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:8e65076fea6d36aa50870267c91ec6d95243f1fb11c28be61a1d14cc261f1cdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3684480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3f24babcb5d8bb3f6840a272a25b4d6bdcfcea3fcb3a940801065c5753d9538`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-s390x.tar.gz / # buildkit
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
	-	`sha256:3e71c43ed556c3ed564b517d9141db651f4134655f96c8731767c14c6dedc4d0`  
		Last Modified: Wed, 08 Jan 2025 17:25:57 GMT  
		Size: 3.5 MB (3463322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe78366bb027e03c42216a6e1d382df7a3ee78f1471f4c62ff2d535ec78d8ce`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644fc493adbda1d67b109c8285fbc4e3c1d916ad0fdd4e52b1d30d0c3b5a8b83`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 7.6 KB (7558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b5aca5c5549a3999391bdaf9bfdf23ae037d07dd0278bcc20a847480979e45`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 212.2 KB (212205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:176ea9af669d43767bfdf3ce63602addb4cf802565986d5dc091d471acc30fe8`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d93146a4a9bfc5584cd3df6a564e1f4ed3da6472cd8f41e6e08d7031d0c8114`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:93f271bcfc043724cd8ed10b5a81e091db12c7c9d2e449003a555df7b3164e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 KB (86446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e388d85c4a8c82382bf1c9f50c1c9b6f983abffb8517c5e88afc7ecb4b51d7af`

```dockerfile
```

-	Layers:
	-	`sha256:2f690c178f9bae18125b1de0d54e1b4493b26e2f974141f5f5fd3c9d3a20c6cb`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 72.1 KB (72145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8043e5e2fb4d14db768fcedf2f5c98e22493faee4d4820a99c0fb644ece380fc`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 14.3 KB (14301 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6.2`

```console
$ docker pull spiped@sha256:11ce1ac8b2718d4bf53335a88287d47f4d7de92a7d96639e822d8b5bf5a4b013
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
$ docker pull spiped@sha256:0807efe8e57e7a74993be6066b8c4d4917a1f6e3611dd0833309a2f48e69d189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37086272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43af49e196ea5b3803a09fb654b9f3a31809b1d63db50efadc92753d2a5ea1b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb387415fb818a8b4d56b6c4b1981b2212e57ec6addac3a80cfb2b9d9331b50`  
		Last Modified: Tue, 14 Jan 2025 02:17:46 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228fe3a70b06fc8ca22481663a32d8b20b71b4a1cc2ef6bad63851b3cddc6a02`  
		Last Modified: Tue, 14 Jan 2025 02:17:46 GMT  
		Size: 2.4 MB (2401340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bdc698a91b053c8c6c8793884aeb21f069855e2f35ceaf6d354563a622ec60`  
		Last Modified: Tue, 14 Jan 2025 02:17:47 GMT  
		Size: 6.5 MB (6470976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562950f9b4e1da298d9932319a15c677ac7b1072f4a6218a62318ec083a438bf`  
		Last Modified: Tue, 14 Jan 2025 02:17:46 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d26d7b3a2a6d5bfa2d8845580756d251c7acbb85868393a8dc4b15857a936c`  
		Last Modified: Tue, 14 Jan 2025 02:17:47 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2` - unknown; unknown

```console
$ docker pull spiped@sha256:4596a995a081e15712ce75ccbd6382c0362bbb99730c9b479c48fb6deb3de184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3530854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb27c549da9cd3fd74e3b201a56fe8440fe2368fbba1fa80abc7dac9262ff93`

```dockerfile
```

-	Layers:
	-	`sha256:d833741283a7f0cc036493894e91aa8f599339f065480034207be52408751f12`  
		Last Modified: Tue, 14 Jan 2025 02:17:47 GMT  
		Size: 3.5 MB (3515814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ab16c690e615571a539221290f9c7154ed500a5de18d47dfbe3d130daff486f`  
		Last Modified: Tue, 14 Jan 2025 02:17:46 GMT  
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
$ docker pull spiped@sha256:50dc383a39b7bbf8bc7274000476568ef19f00fa47f5e77a3b945e542d602e87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37529245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff3adfb5bcb041fd776f222523c7e5f7d316c3a84275c48f8a469520e3cf670`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
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
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 01:33:46 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9757c47c7f65469fabaf649c24c76e71b0ee344186b7378388e73b9ff3584956`  
		Last Modified: Tue, 14 Jan 2025 02:17:03 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41f696ea1cea6b748d59acb3f0e93feb73a67b208dc03bdd8d489b78b8c4c1c`  
		Last Modified: Tue, 14 Jan 2025 02:17:04 GMT  
		Size: 2.4 MB (2398649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241faa93dbe7603d3ddfe8143dbc5f7e9990a80036efae46f8147ce9b8e684d7`  
		Last Modified: Tue, 14 Jan 2025 02:17:04 GMT  
		Size: 5.9 MB (5941461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac324e1750c72f49ee4d4c3b000ae242266e9e9b1946584a5a221c6d4b01bbe9`  
		Last Modified: Tue, 14 Jan 2025 02:17:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6f5c66d701ad1b4e0469df5595f673c4d111557d936709a7c5ab15e2ca0f378`  
		Last Modified: Tue, 14 Jan 2025 02:17:04 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2` - unknown; unknown

```console
$ docker pull spiped@sha256:78318e0a0bae94e38b3a5d9c7578f6751580c7038fd2e2660d4d7cc768105076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed705c7a2f1d4214425c51ed536dd3d3ab550dfbe9a1b50c38de8bba85e59791`

```dockerfile
```

-	Layers:
	-	`sha256:b0eb158509e496490a1fa281c429ec733f8201538a8ead508644c888a4a09018`  
		Last Modified: Tue, 14 Jan 2025 02:17:04 GMT  
		Size: 3.5 MB (3509741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08e8230d3f815bb664e5eda60129ff633bc7d34854e10e52903d538454410d33`  
		Last Modified: Tue, 14 Jan 2025 02:17:03 GMT  
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
		Last Modified: Wed, 25 Dec 2024 11:44:13 GMT  
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
$ docker pull spiped@sha256:3defbc7042c9287d78d336478981bdf2410928e48fd8a9504755509633620376
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
$ docker pull spiped@sha256:924e7f71ff8a6210c218250cadec128119d344f463da73b7435727f3b79f8b8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3860004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:002ee6ce7d381016e688df520b2d8e452892442cc9dd7d7fe4f2fd27e10bd9cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
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
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4d648a75810ee71e4a811a07ea0f0ac2c721e73e72187e9a1516d4c4c5ee6f`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe07a72f4be9ce0f108da046cf545981624f6b49403d76321af17c0c395f286d`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 7.5 KB (7550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda92c005435cc07d0f9aeede336b39adeacb3d2b63892bd145844c2ffdee52b`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 224.8 KB (224801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d408faf96bb5ca591f0228176fd9fe8fcadf008b4a1d270852fc8c6e4ba93ef1`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403e29defa7a55825f8f61eda130cb04ee394d66bd712f70709ac7053a248548`  
		Last Modified: Wed, 08 Jan 2025 18:12:48 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:bbb6e45e7eb3500533fd5eb9b6e02cbb71696097c25c94d70ad5011ff89719b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 KB (88397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ed9b89a1c4bf4f119be92f17b9244feb5432b0aa95a99a543b91711e64d2ff`

```dockerfile
```

-	Layers:
	-	`sha256:d6dbec5f27c384596dd421778e731d1e085e3759f6d847458fe59a756fb7ac42`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 74.1 KB (74096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb9a321a7ee93632ee08168238d08c393bd8977dc0b90058743b7578fd3ffc57`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 14.3 KB (14301 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:3b33305e723d928de0ceb007a192d635fbcead1966adcef42495013c151ab1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3589779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3908b8302a74d29d2ba4f9fad53ec5dae4d694c59ef5e425f9d3b4ae6f8e82c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-armhf.tar.gz / # buildkit
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
	-	`sha256:27a1f2308f194d2c8cfe617a324e0078d055d65032c6c342eae11afb7a8d38c0`  
		Last Modified: Wed, 08 Jan 2025 17:23:56 GMT  
		Size: 3.4 MB (3371473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af3f0630555eb148818822fb59b573ef21353f360d8de1a31a9d923807ee4cd`  
		Last Modified: Wed, 08 Jan 2025 21:50:16 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779a48568101672a32588570e7ceef7c0674397cbfa25ee720cde2859ab94873`  
		Last Modified: Wed, 08 Jan 2025 21:50:16 GMT  
		Size: 7.5 KB (7549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a21818ff816934f603fcd2d4cba9f12db282bab07e3069da21d7578259ccec`  
		Last Modified: Wed, 08 Jan 2025 21:50:17 GMT  
		Size: 209.4 KB (209360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908425f61ccde4470882b7fc3250f120af7e457373de37561ca1bc2c428156fb`  
		Last Modified: Wed, 08 Jan 2025 21:50:16 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d99959ccf8e07e46905c21480b4a1efde735673420d31417427ecef2146095`  
		Last Modified: Wed, 08 Jan 2025 21:50:17 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b7cb53f249d979d695f81563768605e871ddd1ea8a0819dd8dd81dc4987a573f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:755f963c27fded64f7e3f6ff08da27dc1fd056f8030a81de4cb41f27e65d037b`

```dockerfile
```

-	Layers:
	-	`sha256:696c936ae51f846bce7be1a6d2dde5c03aa3b71ffda41e1e6b2cf2a621f6cd97`  
		Last Modified: Wed, 08 Jan 2025 21:50:16 GMT  
		Size: 14.2 KB (14189 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:ae8dad9afbb0cc8a3d199d4f081244152b6bb25a314d1c1b53d2015cb7a3148c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3307454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db4e1533dc661a40478a134b3fe58301335db42d8f87ae18e6918ff38e81ae91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-armv7.tar.gz / # buildkit
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
	-	`sha256:c8a32ed454e751770c0976636b8d0d0fccc4f778a2dd26c428067d613be1a299`  
		Last Modified: Wed, 08 Jan 2025 17:34:15 GMT  
		Size: 3.1 MB (3095514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7fdb315d3c34eb6935e1b7deb703093f5317800ff4d8b3936d5f771137cb79`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3360ef971eae752027c0ac2e924cac0c91b7f45b5099026b2a8f4be3279f6b5`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 7.6 KB (7566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70480e7090e82ed5e217b413501ec1d1ac188d14349be7aa351d6ebc4bfa572b`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 203.0 KB (202981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa024b8e7a4dcd96a95ba7c408a6b6bf086e89742d975c9ce4fdfcfc7cabc1b`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4350bd55dee2c6c0b00a05b33f36a79b911cbfa491acf490c5bdc593d8e3e547`  
		Last Modified: Wed, 08 Jan 2025 21:55:30 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:374da430416cd603b6845710a7b6b98de8856fb9d596f167daa655438d68910f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 KB (88536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddfb7685b3853e3be4a1172afeae58a3bd43dbc7f6bf21565a8d6843e6b79559`

```dockerfile
```

-	Layers:
	-	`sha256:d4af9f6a3307489ccc6bd25b80644c322c26bf5739a42dab919b2dc03edff9ab`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 74.1 KB (74132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d585d482698adea511246e8d288a1602e3c63dc4f235cfa0915b12ae4b080f64`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 14.4 KB (14404 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:3565ca7a9021c033aa2f9aa3fa95ec43241003635fa8669990453c55ff55e1e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4319245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aa0a984328f7027e356ee0aa46ff85666d4fdeec5eb2d5343a30a9dbe998445`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
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
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3f2d3fc3adfdd301f5e24f24c5392b9879a1b61f182e7752a21cb03e6aeb04`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d972687789bff098d9b33d09c024319254bdf8dcd29abb2bf072809733c79f49`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 7.6 KB (7561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37195bfd737aa3f22ef0dd56d792afbe7e88b9c83db3bf0e69cb557d04d0d152`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 219.5 KB (219522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9420b682506ca5859fc3f4af6d59a5ca6fb329a69a869e8d7d0766374eb87ae7`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f38e672eaca427117d78c3580183cebdd51913b95165f7a4fecbb7219aeb29`  
		Last Modified: Wed, 08 Jan 2025 22:06:49 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:c1545d907101296a82932a434f77b80a720493d1f158f28037a360c849c6b869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 KB (88588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af58e3c42e72d2f836cf482efb095b5869000f90e0fd8c744622051f65cbeb6`

```dockerfile
```

-	Layers:
	-	`sha256:802dad5a525c4dc8453a7af1d74e5f8e0f8e9db9e0b53075b1abb70ebcbcac58`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 74.2 KB (74152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f31d587a383d8f42361fc2623919a7a23e16261c7eb1f51cb4aa140497be4935`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 14.4 KB (14436 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2-alpine` - linux; 386

```console
$ docker pull spiped@sha256:92342ba21763b953dae5124e2470d7b310cdec0e1aa1c278c715dda9eb6c5a0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3715310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a710174a0b36bde4dc08b5531a97264b1a956e7b607e3cb81fa4ed42446333`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-x86.tar.gz / # buildkit
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
	-	`sha256:6d632fc6244662e41ee3b3f29090684a520e615dc5c282638a7587366dcd4fb9`  
		Last Modified: Wed, 08 Jan 2025 17:23:34 GMT  
		Size: 3.5 MB (3470969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01646177e05c873338d049d0058c8cd923326812215a3897564adbd669ee56f`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf3460ecbeac950e26287d1cf9fdf47918bf993988d851835f852bbd5707856`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 7.6 KB (7563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69044b34b50595fbdc42e577dc79e206d3962968154ec6fbf18024dfe607c6cd`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 235.4 KB (235383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e2fe84ec006ef02b90eb19d8de0f72b59b1f5d3cad78ef6d043f1ea320d121`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8feb2512bb10b2b05cf6ac1f623ac53ae1aaaf4d759aa98618bf0a96439d0c`  
		Last Modified: Wed, 08 Jan 2025 18:07:24 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f82eea4e46a614570a5475a2c2999ebdb44416593095c39bfe597dfb70954205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 KB (88337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c43d43c6b18f013ddf9e79c05395cc1213c96194b62e9231a34602566ed737c`

```dockerfile
```

-	Layers:
	-	`sha256:662bb99fc24ff68d14f1e276dc7da9f11ef9f56131659d2a511578d1c4547a4e`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 74.1 KB (74071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ab4679badb23f30ba84ac1e7ab274f8693e730ac87dbfac78c97707c071c360`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:62a8529f4a88431c2c8453c2198b9f19f5027af08967a818ceb2e9f5485a2d10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3806729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b6428f7bf466f0e03b157ec2507c547f21126e87e9b2e288213771e8ccfd2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
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
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Wed, 08 Jan 2025 17:24:56 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d50e862e95a905933f50b6440c968976a25afd06a9808138b7b662be556076`  
		Last Modified: Wed, 08 Jan 2025 21:29:14 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca1e9dba23dfea2ee87d2657bcd8e5e57a74b668b777c31cdf12a5a688c9e23`  
		Last Modified: Wed, 08 Jan 2025 21:29:14 GMT  
		Size: 7.6 KB (7562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b2864e003337f2f79f0ebbd5d8f47c821a711805de5ac4aac9a3f02a5d06b3`  
		Last Modified: Wed, 08 Jan 2025 21:29:15 GMT  
		Size: 223.4 KB (223364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b04a1708fbc0147d4ef6fdeb564449a7a41b7b0e5df2aa27a1441946c81598c`  
		Last Modified: Wed, 08 Jan 2025 21:29:14 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66b8e9453e2d649488c8d053b0d1d4ae5e3740489586c6bb32f7eae7a3ec003`  
		Last Modified: Wed, 08 Jan 2025 21:29:15 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:641f93fddb6e6a668353356d78a708a17b7271ab06e13c5d2d1645d499c65794
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 KB (86529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1511f0eb48159856515b99abf8dee3e56263f52094148ce660d713454d210ec3`

```dockerfile
```

-	Layers:
	-	`sha256:55e5c3dc4287df2df2d9e20c08f5cd46d57a5616350e241f492bf844c18956d1`  
		Last Modified: Wed, 08 Jan 2025 21:29:14 GMT  
		Size: 72.2 KB (72179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9f348d15a848da4a767fe70750751a3015a5b347ab3175554ad77137d71526a`  
		Last Modified: Wed, 08 Jan 2025 21:29:14 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:79982546d0bed357c3b7f570dab84958af0f189249fe28e89577d41749385d17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3596676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84f4d20594fd72e32a00a9feabc004f2a01714cd681f91d6012c8315cb905ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-riscv64.tar.gz / # buildkit
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
	-	`sha256:34b7590cc8ea3b21e8c3a0d69270b822d3ba63bc58c6cf0e36c987c95b18eb8d`  
		Last Modified: Wed, 08 Jan 2025 17:49:41 GMT  
		Size: 3.4 MB (3371926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afdd5abd6a9641f814dc31398b1f41f1208ca3c43eafd4a1c8885cb772431cc5`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473a53dcc89c2068574226fb084968b4ffe7be1af4300f024b632369f8a8c233`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 7.6 KB (7561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113dcefb1595560f60660ee7a991d2b59509bc30e01ceddb44741db3ef240384`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 215.8 KB (215788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659fa19d2020016e65ba76874ea424e5842bf892ef9cbb0fb225538f1e187cf7`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecff65919c3bd12f584108c1e36a3685a85470a54c58c385eb56d95175f5ab8c`  
		Last Modified: Fri, 10 Jan 2025 16:34:52 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:1fe29fb7531300754b92edf6a17cb43bbf6bdccf3669dda2f135e21ecd7bc35d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 KB (86525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d832c44e71bd3c5c8e4af761656415c7160b797f2992b90ae6ccd9ad1d3bae`

```dockerfile
```

-	Layers:
	-	`sha256:22ce3c1ef9750e4e84284967ee5eccca34b598a38edbca4cd170feb5ca477190`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 72.2 KB (72175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aff322ae82649ec4042d09e767199a7e60414c2658b767de2a09545e6bc998d`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.2-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:8e65076fea6d36aa50870267c91ec6d95243f1fb11c28be61a1d14cc261f1cdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3684480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3f24babcb5d8bb3f6840a272a25b4d6bdcfcea3fcb3a940801065c5753d9538`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-s390x.tar.gz / # buildkit
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
	-	`sha256:3e71c43ed556c3ed564b517d9141db651f4134655f96c8731767c14c6dedc4d0`  
		Last Modified: Wed, 08 Jan 2025 17:25:57 GMT  
		Size: 3.5 MB (3463322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe78366bb027e03c42216a6e1d382df7a3ee78f1471f4c62ff2d535ec78d8ce`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644fc493adbda1d67b109c8285fbc4e3c1d916ad0fdd4e52b1d30d0c3b5a8b83`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 7.6 KB (7558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b5aca5c5549a3999391bdaf9bfdf23ae037d07dd0278bcc20a847480979e45`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 212.2 KB (212205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:176ea9af669d43767bfdf3ce63602addb4cf802565986d5dc091d471acc30fe8`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d93146a4a9bfc5584cd3df6a564e1f4ed3da6472cd8f41e6e08d7031d0c8114`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.2-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:93f271bcfc043724cd8ed10b5a81e091db12c7c9d2e449003a555df7b3164e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 KB (86446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e388d85c4a8c82382bf1c9f50c1c9b6f983abffb8517c5e88afc7ecb4b51d7af`

```dockerfile
```

-	Layers:
	-	`sha256:2f690c178f9bae18125b1de0d54e1b4493b26e2f974141f5f5fd3c9d3a20c6cb`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 72.1 KB (72145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8043e5e2fb4d14db768fcedf2f5c98e22493faee4d4820a99c0fb644ece380fc`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 14.3 KB (14301 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:alpine`

```console
$ docker pull spiped@sha256:3defbc7042c9287d78d336478981bdf2410928e48fd8a9504755509633620376
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
$ docker pull spiped@sha256:924e7f71ff8a6210c218250cadec128119d344f463da73b7435727f3b79f8b8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3860004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:002ee6ce7d381016e688df520b2d8e452892442cc9dd7d7fe4f2fd27e10bd9cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
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
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4d648a75810ee71e4a811a07ea0f0ac2c721e73e72187e9a1516d4c4c5ee6f`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe07a72f4be9ce0f108da046cf545981624f6b49403d76321af17c0c395f286d`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 7.5 KB (7550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda92c005435cc07d0f9aeede336b39adeacb3d2b63892bd145844c2ffdee52b`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 224.8 KB (224801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d408faf96bb5ca591f0228176fd9fe8fcadf008b4a1d270852fc8c6e4ba93ef1`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403e29defa7a55825f8f61eda130cb04ee394d66bd712f70709ac7053a248548`  
		Last Modified: Wed, 08 Jan 2025 18:12:48 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:bbb6e45e7eb3500533fd5eb9b6e02cbb71696097c25c94d70ad5011ff89719b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 KB (88397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ed9b89a1c4bf4f119be92f17b9244feb5432b0aa95a99a543b91711e64d2ff`

```dockerfile
```

-	Layers:
	-	`sha256:d6dbec5f27c384596dd421778e731d1e085e3759f6d847458fe59a756fb7ac42`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 74.1 KB (74096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb9a321a7ee93632ee08168238d08c393bd8977dc0b90058743b7578fd3ffc57`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 14.3 KB (14301 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:3b33305e723d928de0ceb007a192d635fbcead1966adcef42495013c151ab1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3589779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3908b8302a74d29d2ba4f9fad53ec5dae4d694c59ef5e425f9d3b4ae6f8e82c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-armhf.tar.gz / # buildkit
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
	-	`sha256:27a1f2308f194d2c8cfe617a324e0078d055d65032c6c342eae11afb7a8d38c0`  
		Last Modified: Wed, 08 Jan 2025 17:23:56 GMT  
		Size: 3.4 MB (3371473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af3f0630555eb148818822fb59b573ef21353f360d8de1a31a9d923807ee4cd`  
		Last Modified: Wed, 08 Jan 2025 21:50:16 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779a48568101672a32588570e7ceef7c0674397cbfa25ee720cde2859ab94873`  
		Last Modified: Wed, 08 Jan 2025 21:50:16 GMT  
		Size: 7.5 KB (7549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a21818ff816934f603fcd2d4cba9f12db282bab07e3069da21d7578259ccec`  
		Last Modified: Wed, 08 Jan 2025 21:50:17 GMT  
		Size: 209.4 KB (209360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908425f61ccde4470882b7fc3250f120af7e457373de37561ca1bc2c428156fb`  
		Last Modified: Wed, 08 Jan 2025 21:50:16 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d99959ccf8e07e46905c21480b4a1efde735673420d31417427ecef2146095`  
		Last Modified: Wed, 08 Jan 2025 21:50:17 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b7cb53f249d979d695f81563768605e871ddd1ea8a0819dd8dd81dc4987a573f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:755f963c27fded64f7e3f6ff08da27dc1fd056f8030a81de4cb41f27e65d037b`

```dockerfile
```

-	Layers:
	-	`sha256:696c936ae51f846bce7be1a6d2dde5c03aa3b71ffda41e1e6b2cf2a621f6cd97`  
		Last Modified: Wed, 08 Jan 2025 21:50:16 GMT  
		Size: 14.2 KB (14189 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:ae8dad9afbb0cc8a3d199d4f081244152b6bb25a314d1c1b53d2015cb7a3148c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3307454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db4e1533dc661a40478a134b3fe58301335db42d8f87ae18e6918ff38e81ae91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-armv7.tar.gz / # buildkit
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
	-	`sha256:c8a32ed454e751770c0976636b8d0d0fccc4f778a2dd26c428067d613be1a299`  
		Last Modified: Wed, 08 Jan 2025 17:34:15 GMT  
		Size: 3.1 MB (3095514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7fdb315d3c34eb6935e1b7deb703093f5317800ff4d8b3936d5f771137cb79`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3360ef971eae752027c0ac2e924cac0c91b7f45b5099026b2a8f4be3279f6b5`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 7.6 KB (7566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70480e7090e82ed5e217b413501ec1d1ac188d14349be7aa351d6ebc4bfa572b`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 203.0 KB (202981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa024b8e7a4dcd96a95ba7c408a6b6bf086e89742d975c9ce4fdfcfc7cabc1b`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4350bd55dee2c6c0b00a05b33f36a79b911cbfa491acf490c5bdc593d8e3e547`  
		Last Modified: Wed, 08 Jan 2025 21:55:30 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:374da430416cd603b6845710a7b6b98de8856fb9d596f167daa655438d68910f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 KB (88536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddfb7685b3853e3be4a1172afeae58a3bd43dbc7f6bf21565a8d6843e6b79559`

```dockerfile
```

-	Layers:
	-	`sha256:d4af9f6a3307489ccc6bd25b80644c322c26bf5739a42dab919b2dc03edff9ab`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 74.1 KB (74132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d585d482698adea511246e8d288a1602e3c63dc4f235cfa0915b12ae4b080f64`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 14.4 KB (14404 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:3565ca7a9021c033aa2f9aa3fa95ec43241003635fa8669990453c55ff55e1e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4319245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aa0a984328f7027e356ee0aa46ff85666d4fdeec5eb2d5343a30a9dbe998445`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
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
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3f2d3fc3adfdd301f5e24f24c5392b9879a1b61f182e7752a21cb03e6aeb04`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d972687789bff098d9b33d09c024319254bdf8dcd29abb2bf072809733c79f49`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 7.6 KB (7561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37195bfd737aa3f22ef0dd56d792afbe7e88b9c83db3bf0e69cb557d04d0d152`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 219.5 KB (219522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9420b682506ca5859fc3f4af6d59a5ca6fb329a69a869e8d7d0766374eb87ae7`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f38e672eaca427117d78c3580183cebdd51913b95165f7a4fecbb7219aeb29`  
		Last Modified: Wed, 08 Jan 2025 22:06:49 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:c1545d907101296a82932a434f77b80a720493d1f158f28037a360c849c6b869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 KB (88588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af58e3c42e72d2f836cf482efb095b5869000f90e0fd8c744622051f65cbeb6`

```dockerfile
```

-	Layers:
	-	`sha256:802dad5a525c4dc8453a7af1d74e5f8e0f8e9db9e0b53075b1abb70ebcbcac58`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 74.2 KB (74152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f31d587a383d8f42361fc2623919a7a23e16261c7eb1f51cb4aa140497be4935`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 14.4 KB (14436 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; 386

```console
$ docker pull spiped@sha256:92342ba21763b953dae5124e2470d7b310cdec0e1aa1c278c715dda9eb6c5a0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3715310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a710174a0b36bde4dc08b5531a97264b1a956e7b607e3cb81fa4ed42446333`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-x86.tar.gz / # buildkit
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
	-	`sha256:6d632fc6244662e41ee3b3f29090684a520e615dc5c282638a7587366dcd4fb9`  
		Last Modified: Wed, 08 Jan 2025 17:23:34 GMT  
		Size: 3.5 MB (3470969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01646177e05c873338d049d0058c8cd923326812215a3897564adbd669ee56f`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf3460ecbeac950e26287d1cf9fdf47918bf993988d851835f852bbd5707856`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 7.6 KB (7563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69044b34b50595fbdc42e577dc79e206d3962968154ec6fbf18024dfe607c6cd`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 235.4 KB (235383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e2fe84ec006ef02b90eb19d8de0f72b59b1f5d3cad78ef6d043f1ea320d121`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8feb2512bb10b2b05cf6ac1f623ac53ae1aaaf4d759aa98618bf0a96439d0c`  
		Last Modified: Wed, 08 Jan 2025 18:07:24 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f82eea4e46a614570a5475a2c2999ebdb44416593095c39bfe597dfb70954205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 KB (88337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c43d43c6b18f013ddf9e79c05395cc1213c96194b62e9231a34602566ed737c`

```dockerfile
```

-	Layers:
	-	`sha256:662bb99fc24ff68d14f1e276dc7da9f11ef9f56131659d2a511578d1c4547a4e`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 74.1 KB (74071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ab4679badb23f30ba84ac1e7ab274f8693e730ac87dbfac78c97707c071c360`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:62a8529f4a88431c2c8453c2198b9f19f5027af08967a818ceb2e9f5485a2d10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3806729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b6428f7bf466f0e03b157ec2507c547f21126e87e9b2e288213771e8ccfd2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
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
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Wed, 08 Jan 2025 17:24:56 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d50e862e95a905933f50b6440c968976a25afd06a9808138b7b662be556076`  
		Last Modified: Wed, 08 Jan 2025 21:29:14 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca1e9dba23dfea2ee87d2657bcd8e5e57a74b668b777c31cdf12a5a688c9e23`  
		Last Modified: Wed, 08 Jan 2025 21:29:14 GMT  
		Size: 7.6 KB (7562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b2864e003337f2f79f0ebbd5d8f47c821a711805de5ac4aac9a3f02a5d06b3`  
		Last Modified: Wed, 08 Jan 2025 21:29:15 GMT  
		Size: 223.4 KB (223364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b04a1708fbc0147d4ef6fdeb564449a7a41b7b0e5df2aa27a1441946c81598c`  
		Last Modified: Wed, 08 Jan 2025 21:29:14 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66b8e9453e2d649488c8d053b0d1d4ae5e3740489586c6bb32f7eae7a3ec003`  
		Last Modified: Wed, 08 Jan 2025 21:29:15 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:641f93fddb6e6a668353356d78a708a17b7271ab06e13c5d2d1645d499c65794
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 KB (86529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1511f0eb48159856515b99abf8dee3e56263f52094148ce660d713454d210ec3`

```dockerfile
```

-	Layers:
	-	`sha256:55e5c3dc4287df2df2d9e20c08f5cd46d57a5616350e241f492bf844c18956d1`  
		Last Modified: Wed, 08 Jan 2025 21:29:14 GMT  
		Size: 72.2 KB (72179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9f348d15a848da4a767fe70750751a3015a5b347ab3175554ad77137d71526a`  
		Last Modified: Wed, 08 Jan 2025 21:29:14 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:79982546d0bed357c3b7f570dab84958af0f189249fe28e89577d41749385d17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3596676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84f4d20594fd72e32a00a9feabc004f2a01714cd681f91d6012c8315cb905ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-riscv64.tar.gz / # buildkit
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
	-	`sha256:34b7590cc8ea3b21e8c3a0d69270b822d3ba63bc58c6cf0e36c987c95b18eb8d`  
		Last Modified: Wed, 08 Jan 2025 17:49:41 GMT  
		Size: 3.4 MB (3371926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afdd5abd6a9641f814dc31398b1f41f1208ca3c43eafd4a1c8885cb772431cc5`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473a53dcc89c2068574226fb084968b4ffe7be1af4300f024b632369f8a8c233`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 7.6 KB (7561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113dcefb1595560f60660ee7a991d2b59509bc30e01ceddb44741db3ef240384`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 215.8 KB (215788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659fa19d2020016e65ba76874ea424e5842bf892ef9cbb0fb225538f1e187cf7`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecff65919c3bd12f584108c1e36a3685a85470a54c58c385eb56d95175f5ab8c`  
		Last Modified: Fri, 10 Jan 2025 16:34:52 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:1fe29fb7531300754b92edf6a17cb43bbf6bdccf3669dda2f135e21ecd7bc35d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 KB (86525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d832c44e71bd3c5c8e4af761656415c7160b797f2992b90ae6ccd9ad1d3bae`

```dockerfile
```

-	Layers:
	-	`sha256:22ce3c1ef9750e4e84284967ee5eccca34b598a38edbca4cd170feb5ca477190`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 72.2 KB (72175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aff322ae82649ec4042d09e767199a7e60414c2658b767de2a09545e6bc998d`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; s390x

```console
$ docker pull spiped@sha256:8e65076fea6d36aa50870267c91ec6d95243f1fb11c28be61a1d14cc261f1cdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3684480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3f24babcb5d8bb3f6840a272a25b4d6bdcfcea3fcb3a940801065c5753d9538`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-s390x.tar.gz / # buildkit
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
	-	`sha256:3e71c43ed556c3ed564b517d9141db651f4134655f96c8731767c14c6dedc4d0`  
		Last Modified: Wed, 08 Jan 2025 17:25:57 GMT  
		Size: 3.5 MB (3463322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe78366bb027e03c42216a6e1d382df7a3ee78f1471f4c62ff2d535ec78d8ce`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644fc493adbda1d67b109c8285fbc4e3c1d916ad0fdd4e52b1d30d0c3b5a8b83`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 7.6 KB (7558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b5aca5c5549a3999391bdaf9bfdf23ae037d07dd0278bcc20a847480979e45`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 212.2 KB (212205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:176ea9af669d43767bfdf3ce63602addb4cf802565986d5dc091d471acc30fe8`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d93146a4a9bfc5584cd3df6a564e1f4ed3da6472cd8f41e6e08d7031d0c8114`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:93f271bcfc043724cd8ed10b5a81e091db12c7c9d2e449003a555df7b3164e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 KB (86446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e388d85c4a8c82382bf1c9f50c1c9b6f983abffb8517c5e88afc7ecb4b51d7af`

```dockerfile
```

-	Layers:
	-	`sha256:2f690c178f9bae18125b1de0d54e1b4493b26e2f974141f5f5fd3c9d3a20c6cb`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 72.1 KB (72145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8043e5e2fb4d14db768fcedf2f5c98e22493faee4d4820a99c0fb644ece380fc`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 14.3 KB (14301 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:latest`

```console
$ docker pull spiped@sha256:11ce1ac8b2718d4bf53335a88287d47f4d7de92a7d96639e822d8b5bf5a4b013
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
$ docker pull spiped@sha256:0807efe8e57e7a74993be6066b8c4d4917a1f6e3611dd0833309a2f48e69d189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37086272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43af49e196ea5b3803a09fb654b9f3a31809b1d63db50efadc92753d2a5ea1b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb387415fb818a8b4d56b6c4b1981b2212e57ec6addac3a80cfb2b9d9331b50`  
		Last Modified: Tue, 14 Jan 2025 02:17:46 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228fe3a70b06fc8ca22481663a32d8b20b71b4a1cc2ef6bad63851b3cddc6a02`  
		Last Modified: Tue, 14 Jan 2025 02:17:46 GMT  
		Size: 2.4 MB (2401340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bdc698a91b053c8c6c8793884aeb21f069855e2f35ceaf6d354563a622ec60`  
		Last Modified: Tue, 14 Jan 2025 02:17:47 GMT  
		Size: 6.5 MB (6470976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562950f9b4e1da298d9932319a15c677ac7b1072f4a6218a62318ec083a438bf`  
		Last Modified: Tue, 14 Jan 2025 02:17:46 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d26d7b3a2a6d5bfa2d8845580756d251c7acbb85868393a8dc4b15857a936c`  
		Last Modified: Tue, 14 Jan 2025 02:17:47 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:4596a995a081e15712ce75ccbd6382c0362bbb99730c9b479c48fb6deb3de184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3530854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb27c549da9cd3fd74e3b201a56fe8440fe2368fbba1fa80abc7dac9262ff93`

```dockerfile
```

-	Layers:
	-	`sha256:d833741283a7f0cc036493894e91aa8f599339f065480034207be52408751f12`  
		Last Modified: Tue, 14 Jan 2025 02:17:47 GMT  
		Size: 3.5 MB (3515814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ab16c690e615571a539221290f9c7154ed500a5de18d47dfbe3d130daff486f`  
		Last Modified: Tue, 14 Jan 2025 02:17:46 GMT  
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
$ docker pull spiped@sha256:50dc383a39b7bbf8bc7274000476568ef19f00fa47f5e77a3b945e542d602e87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37529245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff3adfb5bcb041fd776f222523c7e5f7d316c3a84275c48f8a469520e3cf670`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
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
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 01:33:46 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9757c47c7f65469fabaf649c24c76e71b0ee344186b7378388e73b9ff3584956`  
		Last Modified: Tue, 14 Jan 2025 02:17:03 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41f696ea1cea6b748d59acb3f0e93feb73a67b208dc03bdd8d489b78b8c4c1c`  
		Last Modified: Tue, 14 Jan 2025 02:17:04 GMT  
		Size: 2.4 MB (2398649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241faa93dbe7603d3ddfe8143dbc5f7e9990a80036efae46f8147ce9b8e684d7`  
		Last Modified: Tue, 14 Jan 2025 02:17:04 GMT  
		Size: 5.9 MB (5941461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac324e1750c72f49ee4d4c3b000ae242266e9e9b1946584a5a221c6d4b01bbe9`  
		Last Modified: Tue, 14 Jan 2025 02:17:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6f5c66d701ad1b4e0469df5595f673c4d111557d936709a7c5ab15e2ca0f378`  
		Last Modified: Tue, 14 Jan 2025 02:17:04 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:78318e0a0bae94e38b3a5d9c7578f6751580c7038fd2e2660d4d7cc768105076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed705c7a2f1d4214425c51ed536dd3d3ab550dfbe9a1b50c38de8bba85e59791`

```dockerfile
```

-	Layers:
	-	`sha256:b0eb158509e496490a1fa281c429ec733f8201538a8ead508644c888a4a09018`  
		Last Modified: Tue, 14 Jan 2025 02:17:04 GMT  
		Size: 3.5 MB (3509741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08e8230d3f815bb664e5eda60129ff633bc7d34854e10e52903d538454410d33`  
		Last Modified: Tue, 14 Jan 2025 02:17:03 GMT  
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
		Last Modified: Wed, 25 Dec 2024 11:44:13 GMT  
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
