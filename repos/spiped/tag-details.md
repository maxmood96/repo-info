<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `spiped`

-	[`spiped:1`](#spiped1)
-	[`spiped:1-alpine`](#spiped1-alpine)
-	[`spiped:1.6`](#spiped16)
-	[`spiped:1.6-alpine`](#spiped16-alpine)
-	[`spiped:1.6.3`](#spiped163)
-	[`spiped:1.6.3-alpine`](#spiped163-alpine)
-	[`spiped:alpine`](#spipedalpine)
-	[`spiped:latest`](#spipedlatest)

## `spiped:1`

```console
$ docker pull spiped@sha256:8f77956d848c5f3eb11bee20026e0d9a843af8a30b2c0310b669c658468127e3
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
$ docker pull spiped@sha256:536ab474df09e03eac6134fbad4dd27c18a9135fbd86911f2ea7ad690cd04c33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37097837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61f9190e48c091c3f1a4bb917ae20281a709f4394fe1e013004350789b909d3d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297bb720785ed556393334ee818634585f1264385e1193c7cb9a6c139bc65e14`  
		Last Modified: Tue, 28 Jan 2025 01:28:12 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf32c2751d5f872e24f5ed59e217dfd7f84f720367f3076380ff4715073f8266`  
		Last Modified: Tue, 28 Jan 2025 01:28:12 GMT  
		Size: 2.4 MB (2401375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52ec02d46ad29a364ad7f54bb7579493738fab77fe07703d1e53490f14ada4d`  
		Last Modified: Tue, 28 Jan 2025 01:28:12 GMT  
		Size: 6.5 MB (6482502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e904725dea08f9faf2a31328c10f1398468e995b0d27eadb03ed85a22210d22`  
		Last Modified: Tue, 28 Jan 2025 01:28:12 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60b6b0ce2ec5b5eba3960efaa100171ec619e02ea4145fe1925f0376dafadbc`  
		Last Modified: Tue, 28 Jan 2025 01:28:12 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:8a092ebcd3079b2fbc9871bcd444705cac06810db040b4d55c3479865935afcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3530854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f58c8d654972c43b6abb062eb1922573a9f104695000577382138c422a961791`

```dockerfile
```

-	Layers:
	-	`sha256:68928954d7e34be1617a4df1c97a0aab4efc8c72ae02be92a38358bb07437fec`  
		Last Modified: Tue, 28 Jan 2025 01:28:12 GMT  
		Size: 3.5 MB (3515814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8da9ca933cbc0022cfb2d34616b0a64c0d373dd8393666ef7c6e9adc16a5e722`  
		Last Modified: Tue, 28 Jan 2025 01:28:12 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm variant v5

```console
$ docker pull spiped@sha256:0e5c7e178a60719668836afaff3ff67125afee9e3d03accd4401cab3bf3aea23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32882141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d77ac67695453c5d4fc89a848dee8a8392d8bc72b52ea81b468257f78768ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1736726400'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7a3fc1134bc1af98e13c0b7ea743c863d5a17f830a5fbd5a7002f750500e76c2`  
		Last Modified: Tue, 14 Jan 2025 01:33:27 GMT  
		Size: 25.7 MB (25736665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d02c24549d50cc08f67dd0716935f9fa89992a0a0c1150357bba3bd55a0c1e7`  
		Last Modified: Tue, 14 Jan 2025 06:07:49 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3c5e73b2f407694f10795c56fde8bcb539c9e2933731585f42dca1b1ace55f`  
		Last Modified: Tue, 14 Jan 2025 06:07:49 GMT  
		Size: 2.0 MB (1997177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e30adfe160215d6c7902f37ebf94ac563be9c6fccb4a395277b1aa3818607b7`  
		Last Modified: Tue, 28 Jan 2025 01:31:03 GMT  
		Size: 5.1 MB (5146757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27aac59a43177421679bd0226f35aab3ba9fa205c1b5d6c67dafa249b4e83cfd`  
		Last Modified: Tue, 28 Jan 2025 01:31:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9448be81708fcc8741ac6f43584de6ba475c3536046bde4f7c2191a0870c19b`  
		Last Modified: Tue, 28 Jan 2025 01:31:03 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:23079fe3fffca7762fa71b01d0411f8384596126fe153c023b09dc5660eeaf82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3501486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eeb887a5a783665797ba8dc1fdd892d0261c16063f2c97462d2de3fcb591a5e`

```dockerfile
```

-	Layers:
	-	`sha256:22e1c45058e14bd513fd59735994785f69dca0da45c2043c929cd60ab6ee6712`  
		Last Modified: Tue, 28 Jan 2025 01:31:03 GMT  
		Size: 3.5 MB (3486344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b83aa6e8691e60672de940db65cf58f8168cc03800c9df896f0392230faef68d`  
		Last Modified: Tue, 28 Jan 2025 01:31:03 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm variant v7

```console
$ docker pull spiped@sha256:ccbdcef0387e5cc6e9d060a7cb6251eab74ea58109617ddfb00ae7dfbadec466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 MB (30659580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:531150a8da7eb7ecbbdd6e1044330fae803c4f7a5e6fd062da86e8c1d4b96829`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 01:35:15 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f82d2a6f73f55cbf1d37fd27277b02bccaab05b4f4566fba3f60d3414b02ee`  
		Last Modified: Tue, 28 Jan 2025 01:37:09 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbd4fec55999df669ac552c8a8a36d23d8968fc0384aa8e416b1c891eaf20ae`  
		Last Modified: Tue, 28 Jan 2025 01:37:10 GMT  
		Size: 1.9 MB (1855576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82cb6e6723fd5a0ef75b0dd184cf799af3ed260e21af13ab1c2e506822b2fa70`  
		Last Modified: Tue, 28 Jan 2025 01:37:10 GMT  
		Size: 4.9 MB (4887862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d26fd234d491740cb625280d39e623f8d839377ffc0b57cb3504d8de911c3a`  
		Last Modified: Tue, 28 Jan 2025 01:37:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901f496578fbc184fc4790a1b4c0bab2352fb6e530beea188e4b0ba08046ce2a`  
		Last Modified: Tue, 28 Jan 2025 01:37:10 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:1033931b8488d45445247954b4346c2ab38a753e8b906a66b9bf16352c819acd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3500977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd5b75d5b44c4854ab926811600353150aa50de74119e06dddbb73d084581421`

```dockerfile
```

-	Layers:
	-	`sha256:9fa27b21622f0eccb462ea952ab0228e3f904ac0ba741c3b32b2127f45ef179c`  
		Last Modified: Tue, 28 Jan 2025 01:37:09 GMT  
		Size: 3.5 MB (3485835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53bbd1b214a94134a85adbc419d7fc676232db4a3b9e14631c713a43a5060e11`  
		Last Modified: Tue, 28 Jan 2025 01:37:09 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:f2a66012e502dbb68d83b8806cce2a21cb04c84f8e8095bbc2ce736123fb1c20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35780523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3cecf8e2ff2652a6faf516302f17aaa5e8c690b4d97abc9d701160260cd09df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611fe6e9d63e5acb1e7209441d4b6f53839cdb499ce56c53d0a30b18127308af`  
		Last Modified: Tue, 28 Jan 2025 01:41:01 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92430745938fc1ad04a384084859a1779a798bfb2a43cb5e04624d43cd1c7acb`  
		Last Modified: Tue, 28 Jan 2025 01:41:02 GMT  
		Size: 2.2 MB (2247010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369b9862e0933ebe96fc5bda017bd6683b320f8a4d289e80aeed978512cfd255`  
		Last Modified: Tue, 28 Jan 2025 01:41:02 GMT  
		Size: 5.5 MB (5490939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44aa3faa85b28c389faec240ea702de4afa507e7ae685e53314bbdbdff04e80`  
		Last Modified: Tue, 28 Jan 2025 01:41:02 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0a4dc5911186cef9e82bc70ce35d467f950380c65a8d1b0250e0cc206e281e`  
		Last Modified: Tue, 28 Jan 2025 01:41:02 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:47baf7f47236cf831a26ca76d55a8157b116d3dda5925ce8dbbd41d52567069c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3502215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a52acd09d735182eaae4ccffd45c06b9c79bda50a540013e3d691be3da2f431b`

```dockerfile
```

-	Layers:
	-	`sha256:f37345f4dbabaa7e656ed0a75816887fbcfe4951dd41a63d2740bd6ed26f51db`  
		Last Modified: Tue, 28 Jan 2025 01:41:01 GMT  
		Size: 3.5 MB (3487042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:843f601a405007c9da76c3218d51fb2452dc29660928c0893ae7a93703c06e25`  
		Last Modified: Tue, 28 Jan 2025 01:41:01 GMT  
		Size: 15.2 KB (15173 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; 386

```console
$ docker pull spiped@sha256:98ef029814d34d405160b8cd8774b36e1d4075a55db56c75216503f239694141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37544183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d67702ad5748bfe47a10731422eb415fdfc7806bb9184783f769026d4b749a5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 01:33:46 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:990933e5818dac2477379a6c22c8ff156aac80a847271355d54aa7f84e4047c9`  
		Last Modified: Tue, 28 Jan 2025 01:28:36 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec82207d2d5f8c5aee844ce2e9965b1200e45e37009b0bd27d9c3669dd80982`  
		Last Modified: Tue, 28 Jan 2025 01:28:36 GMT  
		Size: 2.4 MB (2398647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de33615d1d4298ca4d90a730d18b76eeab9221bd569fb9925d296300b3597612`  
		Last Modified: Tue, 28 Jan 2025 01:28:36 GMT  
		Size: 6.0 MB (5956398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f9dbd3c5360bd8b3e00e28ec6bfa6f27a97b4b5be2b628a808617b72108df9`  
		Last Modified: Tue, 28 Jan 2025 01:28:36 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf9571f1b17fff32d6a9adffafb32ad8904d04b3f7156f083697132e0b29725`  
		Last Modified: Tue, 28 Jan 2025 01:28:37 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:15d6e0b7e94089abdc57fd1f30df3fc0de016254b2559e656bd0a497b9f74ab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f402ca8235399d4eaacdc1a9831b9d0fea4707fb82e628c7b5e5b32eada091cd`

```dockerfile
```

-	Layers:
	-	`sha256:4f281e15904f5ac0cd9177326f1d676beae6635dd8abbb81371af8c165adc9a9`  
		Last Modified: Tue, 28 Jan 2025 01:28:36 GMT  
		Size: 3.5 MB (3509741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:092229d42c4fa5b9eeb6f986ac672c68620fbb93f0b803f6bc734339f807e88d`  
		Last Modified: Tue, 28 Jan 2025 01:28:36 GMT  
		Size: 15.0 KB (15004 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; mips64le

```console
$ docker pull spiped@sha256:6bf1b2934b50bc37036f47c176307572e04ff3a865286a7cccb291a8c555bf59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36142417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e18f14eeb0958c9f235ad5a0e8476007640d4ed876a873b66b364a4e51c9b9b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1736726400'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b08d7e697b04bda8cef97763765ebbbc16790e22945b5ab31d97d448a15c8650`  
		Last Modified: Tue, 14 Jan 2025 01:38:32 GMT  
		Size: 28.5 MB (28486647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252230c34678f565279955a422dad63275a16eeef208147f154e13e5647df2ed`  
		Last Modified: Tue, 14 Jan 2025 18:08:24 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f980dd5eb6de9195670967164c2a6d21dfc4bd270afc766fc82f7303fcea879a`  
		Last Modified: Tue, 14 Jan 2025 18:08:25 GMT  
		Size: 1.8 MB (1841121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336f4b90f8852da9787d9b302a76c1c166e886091303a5004535e9cb73fd632d`  
		Last Modified: Tue, 28 Jan 2025 01:32:12 GMT  
		Size: 5.8 MB (5813106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5512c8a48481cf94715c1506c2c4e1ff9f6d805efb3b0338118b5689e3c21079`  
		Last Modified: Tue, 28 Jan 2025 01:32:11 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c228f3bd07cbcd06c100e65d713148abb7e018c7025c9b9d6484049c0a2146a9`  
		Last Modified: Tue, 28 Jan 2025 01:32:12 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:249deaaff0d1784a18b6797030367453d08714a64db8712ca45edd7df3073b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbab1862f923b3499782eb1f960684b595f083d0fe2345bd5a6e2c53ae83acd0`

```dockerfile
```

-	Layers:
	-	`sha256:7c6c6f098c793c8847f89582fbc460774fcad941d2a4ed4ded37e75f6dcf7622`  
		Last Modified: Tue, 28 Jan 2025 01:32:11 GMT  
		Size: 14.9 KB (14896 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; ppc64le

```console
$ docker pull spiped@sha256:d18399db45255851ae8ddbad4e7b5c900d55f4e43695efd3981135d67341765b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41069257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d445aa64495f4c7fdb2a32b492a68d159b909988abb7b61737e38b5345a0b8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2904017eed57b6a379aba91f659af48ec8d1305525c46625a955313f2f21e7a9`  
		Last Modified: Tue, 28 Jan 2025 01:42:23 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170c8da9f5a98720edaa9345e098b778f3682abcc6a559d512c35d465ed68eb1`  
		Last Modified: Tue, 28 Jan 2025 01:42:24 GMT  
		Size: 2.6 MB (2582109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf6e585af2ae045254fc980b05067c3829832933e9228997d7b38860b66ec72`  
		Last Modified: Tue, 28 Jan 2025 01:42:24 GMT  
		Size: 6.4 MB (6440760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839630c4aa5ab3314108a0e90bc3ef41c6d874dbf2195903468542b67df10b19`  
		Last Modified: Tue, 28 Jan 2025 01:42:24 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1bd1225ed7d385f9ccd07a3e86a10eecb6f5aceb0d21253d66059f25cc10f76`  
		Last Modified: Tue, 28 Jan 2025 01:42:24 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:635959fa2681a25dc8179b535939238e6dedf3b4407e4b61c265dcaef89b8b0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3516571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7a5467d6b5e70429f77b5ecc51c24454e72e2a4bec50c2ce6d2c38b6d6ceda`

```dockerfile
```

-	Layers:
	-	`sha256:058f9b63cb6c662558bc2dc672de21d6e7f0b7686ae208b7d53a9ed320429272`  
		Last Modified: Tue, 28 Jan 2025 01:42:24 GMT  
		Size: 3.5 MB (3501483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58bba2fecafbd5b0fec43540d380620c8286e345af289a079b69e2ac6bc4556c`  
		Last Modified: Tue, 28 Jan 2025 01:42:23 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; s390x

```console
$ docker pull spiped@sha256:1360a16741b1d8479ba95a46e1eba44e5a1865a9b32409d5461808606b6b823b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34320664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a19118972ca2e46f28001e2d3152e846d353428043b8bd5449cf0659847072d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9e408aef4b499eef3c5a232610cdb9528eac0555c35a861721e1b66e887bce`  
		Last Modified: Tue, 28 Jan 2025 01:56:55 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9cb1363f3ebb86bcd48ad2dfee1768ef18362d453c9befc1470291d84150aaf`  
		Last Modified: Tue, 28 Jan 2025 01:56:56 GMT  
		Size: 2.1 MB (2068705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca8f083cf8abe1b1441f2edc74b5257b41d3ce228131595d258c42c95bb6074`  
		Last Modified: Tue, 28 Jan 2025 01:56:56 GMT  
		Size: 5.4 MB (5391679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445668117981bb081001c5c8686393d3ea7269a2c19c1a02123c111d4ea71388`  
		Last Modified: Tue, 28 Jan 2025 01:56:56 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b87d689b7d650c827b31ea84b35647df1ba39ce7d24b0700f17a0d97decba3`  
		Last Modified: Tue, 28 Jan 2025 01:56:56 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:d14b17075dae6fdb16fc48d6774f8fcadaa06b728ba5478747afec1ccbcb1614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3519040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d01e321bd685e686da98fa6db440fc0736d29b352be36b6b89c8c977200c6299`

```dockerfile
```

-	Layers:
	-	`sha256:0f886e33ca85512f04d777aad824fda2adcbe9e19a9c3e19518644f51adf168b`  
		Last Modified: Tue, 28 Jan 2025 01:56:56 GMT  
		Size: 3.5 MB (3504000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daa4df4848c5169cbffc9300f9d2ac12ef5ce68655c6423c6432a1533d3d1899`  
		Last Modified: Tue, 28 Jan 2025 01:56:55 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1-alpine`

```console
$ docker pull spiped@sha256:cff1ff69fc6f8904043ef5d9bb654e468a38fc671dedcecd1f568a1d61f1d634
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
$ docker pull spiped@sha256:2715ebbc20690dda6d438989f61f4eb4fb11162e932ba70cedc0c7f12b3c26f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3758631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ec86461245d72383c5662f686c25016cc299d589def9478af4205b484492be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b181c716ebe4d13478b33f2488cb40b954ba24081d61c5bc9d7f0605ba9d113`  
		Last Modified: Tue, 28 Jan 2025 01:28:04 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ded10ce7d7c8e5d5eb05c5a7d5246a6a045996ee4f18dcc322d6600e68cd81`  
		Last Modified: Tue, 28 Jan 2025 01:28:04 GMT  
		Size: 7.9 KB (7907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d46a15f052086577ecb502311cd9f4d176cd407ad00862e11dd7d6f8c2a868`  
		Last Modified: Tue, 28 Jan 2025 01:28:04 GMT  
		Size: 107.6 KB (107614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b34221300809a19087f5d67a70e8167a72247feb52faa8c58a878f5af671d3`  
		Last Modified: Tue, 28 Jan 2025 01:28:04 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c89b10c18fcccf667446750b679723f2821a55bf5612caacbb8c510578e77e1`  
		Last Modified: Tue, 28 Jan 2025 01:28:05 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:6a640be7b02114db4704050ac59d1be28b1b8f1a10f0ce877865a41933bc6d1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24283cd9a878c00f69d37c768fc27af4fe97d6fa56a0174f6b441c10746770b0`

```dockerfile
```

-	Layers:
	-	`sha256:f6e7df028e10774143b75638cf9a91ae4484ad9be9705a3ab7de160bfbeab308`  
		Last Modified: Tue, 28 Jan 2025 01:28:04 GMT  
		Size: 79.8 KB (79816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:307857c2fc1847cc55f2ad19b9b6647658c5135c8b20a447ca114dfaf6cdb9b3`  
		Last Modified: Tue, 28 Jan 2025 01:28:04 GMT  
		Size: 14.3 KB (14301 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:6f9bbe66f9f9620c0aad2b8b464d5f0912510b5fbbcce31e1458c51d8bdc36a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3462325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24b357cad96475791645ca664e952dfc2be3a80db4daa6ebc50db2cdb2426d71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee72c2b1876a0156b7d396caf2dc29a0f8081b2b7a6733a3ff64d9527f586ea`  
		Last Modified: Tue, 21 Jan 2025 19:29:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1da6fb0facd6416135ae0db69e959ecf3e75cab6ea327aabb4ead163825dfc7`  
		Last Modified: Tue, 21 Jan 2025 19:29:40 GMT  
		Size: 7.9 KB (7914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0919c3817d8379bb41e1be06c4a9ce8b781a7c46fd9a118114bab8de444770a2`  
		Last Modified: Tue, 28 Jan 2025 01:40:36 GMT  
		Size: 89.1 KB (89138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995e0d0ce3aa2cc891355694b9f4548ada6aa0f587ac1f8f95ff08b62f092ca3`  
		Last Modified: Tue, 28 Jan 2025 01:40:36 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6048abcd79b046de58bebf91b3eb0b6d1d3cdef973e93188a86da2ad1ffe65`  
		Last Modified: Tue, 28 Jan 2025 01:40:36 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:3f840c3a9d83f847e5bb8879ed8d0fae64e2ab7849ae389421052f6925264c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71a31c54f0008afb75dde7c016b9771c6f37268270d33d98c57f6d4c46be550c`

```dockerfile
```

-	Layers:
	-	`sha256:e415d942102ceb25c19c03d57e7aad5f3e309c6a8aebe7422ef678a4f6a8c3c4`  
		Last Modified: Tue, 28 Jan 2025 01:40:36 GMT  
		Size: 14.2 KB (14186 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:12817cd6117bed3cdf9e7e4b52de247dd1a87d2876d8dc7434e5115f0fc9a549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3188067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1cba0ff108ef4a8e8108d49bf7ccd596afac4a82110a7c14e80a001be5fa5bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ae962cfc489c298278551ba32bca1e0ed1f67cd05192848331b7c3ee926a77`  
		Last Modified: Tue, 21 Jan 2025 19:30:37 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1114d274ac423361940bdd6b0c7904acc23cb9903e6f1a2904b32a6b89f331c4`  
		Last Modified: Tue, 21 Jan 2025 19:30:37 GMT  
		Size: 7.9 KB (7915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51637362b800c4f96d7abb05ca7529a770947ee4b1e9623b35af4b936195f4a9`  
		Last Modified: Tue, 28 Jan 2025 01:37:32 GMT  
		Size: 81.6 KB (81648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b15074482593cb5d5f416eda5eadebe75a10ba5005975523c4c34e81f46e618`  
		Last Modified: Tue, 28 Jan 2025 01:37:33 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db71199d0efb2f82ed5530667b5595dd7a34230b43f8dd94dbe9c99654b1b9ae`  
		Last Modified: Tue, 28 Jan 2025 01:37:33 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b5a94554ddb9da6514578c1b09075a2b4ab9c4410f3e3e231bae96919d45f4b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2f515b3bed3192db05a2ad5b870421a369f4a33d6b7164dac00142ecf5bc150`

```dockerfile
```

-	Layers:
	-	`sha256:49f4a9e142d4f0bbdb2b6f12f002efa4735f8926b13589ba3a9a5a9ce1a027ef`  
		Last Modified: Tue, 28 Jan 2025 01:37:32 GMT  
		Size: 79.9 KB (79852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c72de5bccb3b20f12aaba84aa22f33c24e0ef214459867af7cbe28470672cb2`  
		Last Modified: Tue, 28 Jan 2025 01:37:32 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:7bd7eff848bd7ecb4ebeafabcab07a01e40580fc27ad865b3b7dc5c3e8307bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4102233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46380b40fc8cf495b0e4fe6bb439caf833e2bbaf42e79ccbccacbd21456f38f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987e71ee6cc5ab416ed1f0e49bb9a1696b4b5656b4d3fcc1feca517c7bbe5030`  
		Last Modified: Tue, 21 Jan 2025 19:50:56 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5faf545dafdf63442f66bf2d829b8ba0c5dd8fe81240a3298cbf9fee767c891`  
		Last Modified: Tue, 21 Jan 2025 19:50:56 GMT  
		Size: 7.9 KB (7921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7966823473fa57bd0c6c045474918109f56a52c519aa3ff2bbeb53a9bd43f890`  
		Last Modified: Tue, 28 Jan 2025 01:41:34 GMT  
		Size: 100.6 KB (100555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5487e20745df540295ba2a7d5c3230edfbc1657b671f349f920b261416279acc`  
		Last Modified: Tue, 28 Jan 2025 01:41:34 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9477716625dcd64617f5279d092cb746cef8275524ced557b548fac120fd1e9d`  
		Last Modified: Tue, 28 Jan 2025 01:41:35 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:bf674933baf7156a187fcab52df270880af433ca3e590a2d21c400137e505bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e08d169c62b2f76c8f3d4eae8033be48d397c61a9f6edf7ecbdff2e94987c6`

```dockerfile
```

-	Layers:
	-	`sha256:c463f59b08554468e33ec7d67e5bf358a4422df9ba9c9e8a5c85545acbf01205`  
		Last Modified: Tue, 28 Jan 2025 01:41:34 GMT  
		Size: 79.9 KB (79872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55be9c8a835f959acbc00acf5a1a31119a99c2d3a92aba2088b8f3f0b9b7f56c`  
		Last Modified: Tue, 28 Jan 2025 01:41:34 GMT  
		Size: 14.4 KB (14436 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; 386

```console
$ docker pull spiped@sha256:b310c392ab6f14391fb45b5af6ea15dbcbd23076e497d3d94c110d7b2087f4a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3592537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cbcf6cf269492e27066e7c7bbcb967e81247f0f3f3d09284672b28db7077ed8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551001421d38a34944d1a96a5df258e75c389ab10abd35456cbb26915537f7fd`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f72f77ecf249ccd9496811e0eb3c0cf489c7b7fdbfa9b09a800fc23ce9a5b86`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 7.9 KB (7906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78fa624f51e7a9f83ca9c71b40f866f13ab95ae1d6fb7f7fb39888ee08b23f5`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 120.1 KB (120111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b172e6f71ba4a3cd0b9d569cc026414ab5ff72c2c999047269348e63b5abaf`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102f42fb7496f67e41461243ea1a96721d75c60e36c3fc0bc0cc31f4a05a0a3f`  
		Last Modified: Tue, 28 Jan 2025 01:28:29 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:9927a6df5d8b7dbdb338658808aeddad5564ef5897b94b692df5dfa29b9abdef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d905998f2bfd41e52ca5677826d1ba128880dee6ab953a307411406c31b587`

```dockerfile
```

-	Layers:
	-	`sha256:aef24c41d2f2fe02d3f60245a4d8614488af106b27f1694638bb0aa63affdeec`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 79.8 KB (79791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e634c06318ef153f0dea3d1996b85ebfa8b5d1ae392ac0ae4aba4ce249a2d7ee`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 14.3 KB (14265 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:884a0eb6ba4f64c3edda016b28d4bd99dba5200f5af5ac9cb6b72f18cb3a3a60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3695562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18a09f14f9a1c5c8a4bc39f97cc1d4dfc2da04ebc3eb0e1c14ee25ecf135a583`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2937ae7bb7a53c30739164fd8d6b1af5449b91bdeaacb11c09da360a795e967b`  
		Last Modified: Tue, 21 Jan 2025 19:31:28 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbed2b37b3a36511a8f8cde15ac74df12676c707a75cac7400604b533817a57b`  
		Last Modified: Tue, 21 Jan 2025 19:31:28 GMT  
		Size: 7.9 KB (7918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2bb56ba626edfb899d02de6e190e018998d7573a673f6db87d5ef30de0a050`  
		Last Modified: Tue, 28 Jan 2025 01:43:33 GMT  
		Size: 112.6 KB (112648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e93d7242196ad9ca14b560ce78c345dfa536c1a35de8044919beffdf4eb97a`  
		Last Modified: Tue, 28 Jan 2025 01:43:33 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9e06feef4b6941cffa38f96ec7bf4e23040ea0baf7cf6f0a7345c46675eff3`  
		Last Modified: Tue, 28 Jan 2025 01:43:33 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:02029f95376d43c51ccddf3f8c8bbebb0671c8774aacfa19d44aee40f4773161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4efe04e204e62e8c95b99341d61fcd033d068bcbce5868ae0ec1685e9f9da3e`

```dockerfile
```

-	Layers:
	-	`sha256:f198a76291582efc4f722539762e32a43b96a2acfb2de57f18adfa903c9b3c57`  
		Last Modified: Tue, 28 Jan 2025 01:43:33 GMT  
		Size: 77.9 KB (77899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c32d956ebf079b702220519e8a308783736857197d7766e995bfbcd8c71dbf2c`  
		Last Modified: Tue, 28 Jan 2025 01:43:33 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:756e00d72198e903bfd6356e80496c2936c64fa26149b3662c09c044393ac715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3458360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef3b076b4ea8c2964765a22bf8c5d8b2fb8141f171e1f335b628572524c3ab7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Wed, 08 Jan 2025 17:48:43 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410676c340782e10ad961429d12c4fc7bc22fe42e602f44af8fe4564583fa790`  
		Last Modified: Tue, 21 Jan 2025 19:47:10 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb03e5e951a5c0dc5098e3f3712ba683716c2830cd781627b8c589f37e35d49e`  
		Last Modified: Tue, 21 Jan 2025 19:47:10 GMT  
		Size: 7.9 KB (7900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d4da436692d4ab0fd5035ee54eac03b05bf24df9aa3304a4cbb3e6bb7fb7de`  
		Last Modified: Tue, 28 Jan 2025 02:22:45 GMT  
		Size: 98.8 KB (98808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b11f3813ff058c0963785dcdc5c5f860f00840874673c02d724b273f844d53c`  
		Last Modified: Tue, 28 Jan 2025 02:22:45 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d897b6a73cbb856ebfd058f311b8f0e39512fdede0d33460f38db93bb89b6c`  
		Last Modified: Tue, 28 Jan 2025 02:22:45 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:877a9cd3fe26f402674032844c26b7149200267a47a431963b72e3b4563d519c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b37c1a9028694f866e7acc219fbf431ce5b97965a6f5489a14f064c84a12b1`

```dockerfile
```

-	Layers:
	-	`sha256:40546cca6e89cde845ebe9184ed940f3b4f38ba1e18049e3b36b047821e42722`  
		Last Modified: Tue, 28 Jan 2025 02:22:45 GMT  
		Size: 77.9 KB (77895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12a0377ea7376b0115517894b6c6f3d26482dcf699f270a21454fd463c994114`  
		Last Modified: Tue, 28 Jan 2025 02:22:45 GMT  
		Size: 14.3 KB (14347 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:496d1116424a4c78bad3fdd46c2db89305089a904ff0d42fcd07ffca4576a0b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32ae085c92ecf8421e7f161ab96951c317b5e771993504a3e09c8db10414930`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2d0ea9a1061fe840c13a046b93faaeb9dbcf4357f53a37b83747a395c05279`  
		Last Modified: Tue, 21 Jan 2025 19:32:37 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068b14e90f05cd3c9537d5988b4bbe6abead4cac15a8b25d1959964036cdbb13`  
		Last Modified: Tue, 21 Jan 2025 19:32:37 GMT  
		Size: 7.9 KB (7909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3398f6409117bd2a57c6b304f740badcea613c5def606a7c072bcd0c73b061e0`  
		Last Modified: Tue, 28 Jan 2025 01:57:36 GMT  
		Size: 96.9 KB (96911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32ed7682792c020e13d8b547fdbb8c43a4956cb69969b8f5a2724202bbcb39d`  
		Last Modified: Tue, 28 Jan 2025 01:57:37 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff53239a6486b270ef8a57e32718cefe901786526573b780eb054d1ac053dc6e`  
		Last Modified: Tue, 28 Jan 2025 01:57:37 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:d66b26cdcd77f8b4437bcb47a340f63d583e754a794e2a822931eafa72152360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6cdd7bbb43e56276987d1ae0048a6f92a4bca0ccdee9e8e670ddb9ea5e16cb9`

```dockerfile
```

-	Layers:
	-	`sha256:6fe581f275230ca3b53c4a9c2f8f4690c4edf45359ead5089d277953f8872d2a`  
		Last Modified: Tue, 28 Jan 2025 01:57:36 GMT  
		Size: 77.9 KB (77865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0280df9fd96cadb1c6e05a657e4d4caa094e820e2a85ddd2df85b36c0363d18`  
		Last Modified: Tue, 28 Jan 2025 01:57:36 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6`

```console
$ docker pull spiped@sha256:8f77956d848c5f3eb11bee20026e0d9a843af8a30b2c0310b669c658468127e3
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
$ docker pull spiped@sha256:536ab474df09e03eac6134fbad4dd27c18a9135fbd86911f2ea7ad690cd04c33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37097837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61f9190e48c091c3f1a4bb917ae20281a709f4394fe1e013004350789b909d3d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297bb720785ed556393334ee818634585f1264385e1193c7cb9a6c139bc65e14`  
		Last Modified: Tue, 28 Jan 2025 01:28:12 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf32c2751d5f872e24f5ed59e217dfd7f84f720367f3076380ff4715073f8266`  
		Last Modified: Tue, 28 Jan 2025 01:28:12 GMT  
		Size: 2.4 MB (2401375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52ec02d46ad29a364ad7f54bb7579493738fab77fe07703d1e53490f14ada4d`  
		Last Modified: Tue, 28 Jan 2025 01:28:12 GMT  
		Size: 6.5 MB (6482502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e904725dea08f9faf2a31328c10f1398468e995b0d27eadb03ed85a22210d22`  
		Last Modified: Tue, 28 Jan 2025 01:28:12 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60b6b0ce2ec5b5eba3960efaa100171ec619e02ea4145fe1925f0376dafadbc`  
		Last Modified: Tue, 28 Jan 2025 01:28:12 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:8a092ebcd3079b2fbc9871bcd444705cac06810db040b4d55c3479865935afcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3530854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f58c8d654972c43b6abb062eb1922573a9f104695000577382138c422a961791`

```dockerfile
```

-	Layers:
	-	`sha256:68928954d7e34be1617a4df1c97a0aab4efc8c72ae02be92a38358bb07437fec`  
		Last Modified: Tue, 28 Jan 2025 01:28:12 GMT  
		Size: 3.5 MB (3515814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8da9ca933cbc0022cfb2d34616b0a64c0d373dd8393666ef7c6e9adc16a5e722`  
		Last Modified: Tue, 28 Jan 2025 01:28:12 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm variant v5

```console
$ docker pull spiped@sha256:0e5c7e178a60719668836afaff3ff67125afee9e3d03accd4401cab3bf3aea23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32882141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d77ac67695453c5d4fc89a848dee8a8392d8bc72b52ea81b468257f78768ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1736726400'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7a3fc1134bc1af98e13c0b7ea743c863d5a17f830a5fbd5a7002f750500e76c2`  
		Last Modified: Tue, 14 Jan 2025 01:33:27 GMT  
		Size: 25.7 MB (25736665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d02c24549d50cc08f67dd0716935f9fa89992a0a0c1150357bba3bd55a0c1e7`  
		Last Modified: Tue, 14 Jan 2025 06:07:49 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3c5e73b2f407694f10795c56fde8bcb539c9e2933731585f42dca1b1ace55f`  
		Last Modified: Tue, 14 Jan 2025 06:07:49 GMT  
		Size: 2.0 MB (1997177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e30adfe160215d6c7902f37ebf94ac563be9c6fccb4a395277b1aa3818607b7`  
		Last Modified: Tue, 28 Jan 2025 01:31:03 GMT  
		Size: 5.1 MB (5146757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27aac59a43177421679bd0226f35aab3ba9fa205c1b5d6c67dafa249b4e83cfd`  
		Last Modified: Tue, 28 Jan 2025 01:31:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9448be81708fcc8741ac6f43584de6ba475c3536046bde4f7c2191a0870c19b`  
		Last Modified: Tue, 28 Jan 2025 01:31:03 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:23079fe3fffca7762fa71b01d0411f8384596126fe153c023b09dc5660eeaf82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3501486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eeb887a5a783665797ba8dc1fdd892d0261c16063f2c97462d2de3fcb591a5e`

```dockerfile
```

-	Layers:
	-	`sha256:22e1c45058e14bd513fd59735994785f69dca0da45c2043c929cd60ab6ee6712`  
		Last Modified: Tue, 28 Jan 2025 01:31:03 GMT  
		Size: 3.5 MB (3486344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b83aa6e8691e60672de940db65cf58f8168cc03800c9df896f0392230faef68d`  
		Last Modified: Tue, 28 Jan 2025 01:31:03 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm variant v7

```console
$ docker pull spiped@sha256:ccbdcef0387e5cc6e9d060a7cb6251eab74ea58109617ddfb00ae7dfbadec466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 MB (30659580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:531150a8da7eb7ecbbdd6e1044330fae803c4f7a5e6fd062da86e8c1d4b96829`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 01:35:15 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f82d2a6f73f55cbf1d37fd27277b02bccaab05b4f4566fba3f60d3414b02ee`  
		Last Modified: Tue, 28 Jan 2025 01:37:09 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbd4fec55999df669ac552c8a8a36d23d8968fc0384aa8e416b1c891eaf20ae`  
		Last Modified: Tue, 28 Jan 2025 01:37:10 GMT  
		Size: 1.9 MB (1855576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82cb6e6723fd5a0ef75b0dd184cf799af3ed260e21af13ab1c2e506822b2fa70`  
		Last Modified: Tue, 28 Jan 2025 01:37:10 GMT  
		Size: 4.9 MB (4887862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d26fd234d491740cb625280d39e623f8d839377ffc0b57cb3504d8de911c3a`  
		Last Modified: Tue, 28 Jan 2025 01:37:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901f496578fbc184fc4790a1b4c0bab2352fb6e530beea188e4b0ba08046ce2a`  
		Last Modified: Tue, 28 Jan 2025 01:37:10 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:1033931b8488d45445247954b4346c2ab38a753e8b906a66b9bf16352c819acd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3500977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd5b75d5b44c4854ab926811600353150aa50de74119e06dddbb73d084581421`

```dockerfile
```

-	Layers:
	-	`sha256:9fa27b21622f0eccb462ea952ab0228e3f904ac0ba741c3b32b2127f45ef179c`  
		Last Modified: Tue, 28 Jan 2025 01:37:09 GMT  
		Size: 3.5 MB (3485835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53bbd1b214a94134a85adbc419d7fc676232db4a3b9e14631c713a43a5060e11`  
		Last Modified: Tue, 28 Jan 2025 01:37:09 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:f2a66012e502dbb68d83b8806cce2a21cb04c84f8e8095bbc2ce736123fb1c20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35780523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3cecf8e2ff2652a6faf516302f17aaa5e8c690b4d97abc9d701160260cd09df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611fe6e9d63e5acb1e7209441d4b6f53839cdb499ce56c53d0a30b18127308af`  
		Last Modified: Tue, 28 Jan 2025 01:41:01 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92430745938fc1ad04a384084859a1779a798bfb2a43cb5e04624d43cd1c7acb`  
		Last Modified: Tue, 28 Jan 2025 01:41:02 GMT  
		Size: 2.2 MB (2247010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369b9862e0933ebe96fc5bda017bd6683b320f8a4d289e80aeed978512cfd255`  
		Last Modified: Tue, 28 Jan 2025 01:41:02 GMT  
		Size: 5.5 MB (5490939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44aa3faa85b28c389faec240ea702de4afa507e7ae685e53314bbdbdff04e80`  
		Last Modified: Tue, 28 Jan 2025 01:41:02 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0a4dc5911186cef9e82bc70ce35d467f950380c65a8d1b0250e0cc206e281e`  
		Last Modified: Tue, 28 Jan 2025 01:41:02 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:47baf7f47236cf831a26ca76d55a8157b116d3dda5925ce8dbbd41d52567069c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3502215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a52acd09d735182eaae4ccffd45c06b9c79bda50a540013e3d691be3da2f431b`

```dockerfile
```

-	Layers:
	-	`sha256:f37345f4dbabaa7e656ed0a75816887fbcfe4951dd41a63d2740bd6ed26f51db`  
		Last Modified: Tue, 28 Jan 2025 01:41:01 GMT  
		Size: 3.5 MB (3487042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:843f601a405007c9da76c3218d51fb2452dc29660928c0893ae7a93703c06e25`  
		Last Modified: Tue, 28 Jan 2025 01:41:01 GMT  
		Size: 15.2 KB (15173 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; 386

```console
$ docker pull spiped@sha256:98ef029814d34d405160b8cd8774b36e1d4075a55db56c75216503f239694141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37544183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d67702ad5748bfe47a10731422eb415fdfc7806bb9184783f769026d4b749a5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 01:33:46 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:990933e5818dac2477379a6c22c8ff156aac80a847271355d54aa7f84e4047c9`  
		Last Modified: Tue, 28 Jan 2025 01:28:36 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec82207d2d5f8c5aee844ce2e9965b1200e45e37009b0bd27d9c3669dd80982`  
		Last Modified: Tue, 28 Jan 2025 01:28:36 GMT  
		Size: 2.4 MB (2398647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de33615d1d4298ca4d90a730d18b76eeab9221bd569fb9925d296300b3597612`  
		Last Modified: Tue, 28 Jan 2025 01:28:36 GMT  
		Size: 6.0 MB (5956398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f9dbd3c5360bd8b3e00e28ec6bfa6f27a97b4b5be2b628a808617b72108df9`  
		Last Modified: Tue, 28 Jan 2025 01:28:36 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf9571f1b17fff32d6a9adffafb32ad8904d04b3f7156f083697132e0b29725`  
		Last Modified: Tue, 28 Jan 2025 01:28:37 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:15d6e0b7e94089abdc57fd1f30df3fc0de016254b2559e656bd0a497b9f74ab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f402ca8235399d4eaacdc1a9831b9d0fea4707fb82e628c7b5e5b32eada091cd`

```dockerfile
```

-	Layers:
	-	`sha256:4f281e15904f5ac0cd9177326f1d676beae6635dd8abbb81371af8c165adc9a9`  
		Last Modified: Tue, 28 Jan 2025 01:28:36 GMT  
		Size: 3.5 MB (3509741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:092229d42c4fa5b9eeb6f986ac672c68620fbb93f0b803f6bc734339f807e88d`  
		Last Modified: Tue, 28 Jan 2025 01:28:36 GMT  
		Size: 15.0 KB (15004 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; mips64le

```console
$ docker pull spiped@sha256:6bf1b2934b50bc37036f47c176307572e04ff3a865286a7cccb291a8c555bf59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36142417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e18f14eeb0958c9f235ad5a0e8476007640d4ed876a873b66b364a4e51c9b9b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1736726400'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b08d7e697b04bda8cef97763765ebbbc16790e22945b5ab31d97d448a15c8650`  
		Last Modified: Tue, 14 Jan 2025 01:38:32 GMT  
		Size: 28.5 MB (28486647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252230c34678f565279955a422dad63275a16eeef208147f154e13e5647df2ed`  
		Last Modified: Tue, 14 Jan 2025 18:08:24 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f980dd5eb6de9195670967164c2a6d21dfc4bd270afc766fc82f7303fcea879a`  
		Last Modified: Tue, 14 Jan 2025 18:08:25 GMT  
		Size: 1.8 MB (1841121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336f4b90f8852da9787d9b302a76c1c166e886091303a5004535e9cb73fd632d`  
		Last Modified: Tue, 28 Jan 2025 01:32:12 GMT  
		Size: 5.8 MB (5813106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5512c8a48481cf94715c1506c2c4e1ff9f6d805efb3b0338118b5689e3c21079`  
		Last Modified: Tue, 28 Jan 2025 01:32:11 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c228f3bd07cbcd06c100e65d713148abb7e018c7025c9b9d6484049c0a2146a9`  
		Last Modified: Tue, 28 Jan 2025 01:32:12 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:249deaaff0d1784a18b6797030367453d08714a64db8712ca45edd7df3073b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbab1862f923b3499782eb1f960684b595f083d0fe2345bd5a6e2c53ae83acd0`

```dockerfile
```

-	Layers:
	-	`sha256:7c6c6f098c793c8847f89582fbc460774fcad941d2a4ed4ded37e75f6dcf7622`  
		Last Modified: Tue, 28 Jan 2025 01:32:11 GMT  
		Size: 14.9 KB (14896 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; ppc64le

```console
$ docker pull spiped@sha256:d18399db45255851ae8ddbad4e7b5c900d55f4e43695efd3981135d67341765b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41069257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d445aa64495f4c7fdb2a32b492a68d159b909988abb7b61737e38b5345a0b8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2904017eed57b6a379aba91f659af48ec8d1305525c46625a955313f2f21e7a9`  
		Last Modified: Tue, 28 Jan 2025 01:42:23 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170c8da9f5a98720edaa9345e098b778f3682abcc6a559d512c35d465ed68eb1`  
		Last Modified: Tue, 28 Jan 2025 01:42:24 GMT  
		Size: 2.6 MB (2582109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf6e585af2ae045254fc980b05067c3829832933e9228997d7b38860b66ec72`  
		Last Modified: Tue, 28 Jan 2025 01:42:24 GMT  
		Size: 6.4 MB (6440760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839630c4aa5ab3314108a0e90bc3ef41c6d874dbf2195903468542b67df10b19`  
		Last Modified: Tue, 28 Jan 2025 01:42:24 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1bd1225ed7d385f9ccd07a3e86a10eecb6f5aceb0d21253d66059f25cc10f76`  
		Last Modified: Tue, 28 Jan 2025 01:42:24 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:635959fa2681a25dc8179b535939238e6dedf3b4407e4b61c265dcaef89b8b0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3516571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7a5467d6b5e70429f77b5ecc51c24454e72e2a4bec50c2ce6d2c38b6d6ceda`

```dockerfile
```

-	Layers:
	-	`sha256:058f9b63cb6c662558bc2dc672de21d6e7f0b7686ae208b7d53a9ed320429272`  
		Last Modified: Tue, 28 Jan 2025 01:42:24 GMT  
		Size: 3.5 MB (3501483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58bba2fecafbd5b0fec43540d380620c8286e345af289a079b69e2ac6bc4556c`  
		Last Modified: Tue, 28 Jan 2025 01:42:23 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; s390x

```console
$ docker pull spiped@sha256:1360a16741b1d8479ba95a46e1eba44e5a1865a9b32409d5461808606b6b823b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34320664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a19118972ca2e46f28001e2d3152e846d353428043b8bd5449cf0659847072d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9e408aef4b499eef3c5a232610cdb9528eac0555c35a861721e1b66e887bce`  
		Last Modified: Tue, 28 Jan 2025 01:56:55 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9cb1363f3ebb86bcd48ad2dfee1768ef18362d453c9befc1470291d84150aaf`  
		Last Modified: Tue, 28 Jan 2025 01:56:56 GMT  
		Size: 2.1 MB (2068705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca8f083cf8abe1b1441f2edc74b5257b41d3ce228131595d258c42c95bb6074`  
		Last Modified: Tue, 28 Jan 2025 01:56:56 GMT  
		Size: 5.4 MB (5391679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445668117981bb081001c5c8686393d3ea7269a2c19c1a02123c111d4ea71388`  
		Last Modified: Tue, 28 Jan 2025 01:56:56 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b87d689b7d650c827b31ea84b35647df1ba39ce7d24b0700f17a0d97decba3`  
		Last Modified: Tue, 28 Jan 2025 01:56:56 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:d14b17075dae6fdb16fc48d6774f8fcadaa06b728ba5478747afec1ccbcb1614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3519040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d01e321bd685e686da98fa6db440fc0736d29b352be36b6b89c8c977200c6299`

```dockerfile
```

-	Layers:
	-	`sha256:0f886e33ca85512f04d777aad824fda2adcbe9e19a9c3e19518644f51adf168b`  
		Last Modified: Tue, 28 Jan 2025 01:56:56 GMT  
		Size: 3.5 MB (3504000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daa4df4848c5169cbffc9300f9d2ac12ef5ce68655c6423c6432a1533d3d1899`  
		Last Modified: Tue, 28 Jan 2025 01:56:55 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6-alpine`

```console
$ docker pull spiped@sha256:cff1ff69fc6f8904043ef5d9bb654e468a38fc671dedcecd1f568a1d61f1d634
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
$ docker pull spiped@sha256:2715ebbc20690dda6d438989f61f4eb4fb11162e932ba70cedc0c7f12b3c26f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3758631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ec86461245d72383c5662f686c25016cc299d589def9478af4205b484492be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b181c716ebe4d13478b33f2488cb40b954ba24081d61c5bc9d7f0605ba9d113`  
		Last Modified: Tue, 28 Jan 2025 01:28:04 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ded10ce7d7c8e5d5eb05c5a7d5246a6a045996ee4f18dcc322d6600e68cd81`  
		Last Modified: Tue, 28 Jan 2025 01:28:04 GMT  
		Size: 7.9 KB (7907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d46a15f052086577ecb502311cd9f4d176cd407ad00862e11dd7d6f8c2a868`  
		Last Modified: Tue, 28 Jan 2025 01:28:04 GMT  
		Size: 107.6 KB (107614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b34221300809a19087f5d67a70e8167a72247feb52faa8c58a878f5af671d3`  
		Last Modified: Tue, 28 Jan 2025 01:28:04 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c89b10c18fcccf667446750b679723f2821a55bf5612caacbb8c510578e77e1`  
		Last Modified: Tue, 28 Jan 2025 01:28:05 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:6a640be7b02114db4704050ac59d1be28b1b8f1a10f0ce877865a41933bc6d1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24283cd9a878c00f69d37c768fc27af4fe97d6fa56a0174f6b441c10746770b0`

```dockerfile
```

-	Layers:
	-	`sha256:f6e7df028e10774143b75638cf9a91ae4484ad9be9705a3ab7de160bfbeab308`  
		Last Modified: Tue, 28 Jan 2025 01:28:04 GMT  
		Size: 79.8 KB (79816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:307857c2fc1847cc55f2ad19b9b6647658c5135c8b20a447ca114dfaf6cdb9b3`  
		Last Modified: Tue, 28 Jan 2025 01:28:04 GMT  
		Size: 14.3 KB (14301 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:6f9bbe66f9f9620c0aad2b8b464d5f0912510b5fbbcce31e1458c51d8bdc36a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3462325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24b357cad96475791645ca664e952dfc2be3a80db4daa6ebc50db2cdb2426d71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee72c2b1876a0156b7d396caf2dc29a0f8081b2b7a6733a3ff64d9527f586ea`  
		Last Modified: Tue, 21 Jan 2025 19:29:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1da6fb0facd6416135ae0db69e959ecf3e75cab6ea327aabb4ead163825dfc7`  
		Last Modified: Tue, 21 Jan 2025 19:29:40 GMT  
		Size: 7.9 KB (7914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0919c3817d8379bb41e1be06c4a9ce8b781a7c46fd9a118114bab8de444770a2`  
		Last Modified: Tue, 28 Jan 2025 01:40:36 GMT  
		Size: 89.1 KB (89138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995e0d0ce3aa2cc891355694b9f4548ada6aa0f587ac1f8f95ff08b62f092ca3`  
		Last Modified: Tue, 28 Jan 2025 01:40:36 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6048abcd79b046de58bebf91b3eb0b6d1d3cdef973e93188a86da2ad1ffe65`  
		Last Modified: Tue, 28 Jan 2025 01:40:36 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:3f840c3a9d83f847e5bb8879ed8d0fae64e2ab7849ae389421052f6925264c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71a31c54f0008afb75dde7c016b9771c6f37268270d33d98c57f6d4c46be550c`

```dockerfile
```

-	Layers:
	-	`sha256:e415d942102ceb25c19c03d57e7aad5f3e309c6a8aebe7422ef678a4f6a8c3c4`  
		Last Modified: Tue, 28 Jan 2025 01:40:36 GMT  
		Size: 14.2 KB (14186 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:12817cd6117bed3cdf9e7e4b52de247dd1a87d2876d8dc7434e5115f0fc9a549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3188067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1cba0ff108ef4a8e8108d49bf7ccd596afac4a82110a7c14e80a001be5fa5bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ae962cfc489c298278551ba32bca1e0ed1f67cd05192848331b7c3ee926a77`  
		Last Modified: Tue, 21 Jan 2025 19:30:37 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1114d274ac423361940bdd6b0c7904acc23cb9903e6f1a2904b32a6b89f331c4`  
		Last Modified: Tue, 21 Jan 2025 19:30:37 GMT  
		Size: 7.9 KB (7915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51637362b800c4f96d7abb05ca7529a770947ee4b1e9623b35af4b936195f4a9`  
		Last Modified: Tue, 28 Jan 2025 01:37:32 GMT  
		Size: 81.6 KB (81648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b15074482593cb5d5f416eda5eadebe75a10ba5005975523c4c34e81f46e618`  
		Last Modified: Tue, 28 Jan 2025 01:37:33 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db71199d0efb2f82ed5530667b5595dd7a34230b43f8dd94dbe9c99654b1b9ae`  
		Last Modified: Tue, 28 Jan 2025 01:37:33 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b5a94554ddb9da6514578c1b09075a2b4ab9c4410f3e3e231bae96919d45f4b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2f515b3bed3192db05a2ad5b870421a369f4a33d6b7164dac00142ecf5bc150`

```dockerfile
```

-	Layers:
	-	`sha256:49f4a9e142d4f0bbdb2b6f12f002efa4735f8926b13589ba3a9a5a9ce1a027ef`  
		Last Modified: Tue, 28 Jan 2025 01:37:32 GMT  
		Size: 79.9 KB (79852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c72de5bccb3b20f12aaba84aa22f33c24e0ef214459867af7cbe28470672cb2`  
		Last Modified: Tue, 28 Jan 2025 01:37:32 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:7bd7eff848bd7ecb4ebeafabcab07a01e40580fc27ad865b3b7dc5c3e8307bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4102233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46380b40fc8cf495b0e4fe6bb439caf833e2bbaf42e79ccbccacbd21456f38f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987e71ee6cc5ab416ed1f0e49bb9a1696b4b5656b4d3fcc1feca517c7bbe5030`  
		Last Modified: Tue, 21 Jan 2025 19:50:56 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5faf545dafdf63442f66bf2d829b8ba0c5dd8fe81240a3298cbf9fee767c891`  
		Last Modified: Tue, 21 Jan 2025 19:50:56 GMT  
		Size: 7.9 KB (7921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7966823473fa57bd0c6c045474918109f56a52c519aa3ff2bbeb53a9bd43f890`  
		Last Modified: Tue, 28 Jan 2025 01:41:34 GMT  
		Size: 100.6 KB (100555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5487e20745df540295ba2a7d5c3230edfbc1657b671f349f920b261416279acc`  
		Last Modified: Tue, 28 Jan 2025 01:41:34 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9477716625dcd64617f5279d092cb746cef8275524ced557b548fac120fd1e9d`  
		Last Modified: Tue, 28 Jan 2025 01:41:35 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:bf674933baf7156a187fcab52df270880af433ca3e590a2d21c400137e505bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e08d169c62b2f76c8f3d4eae8033be48d397c61a9f6edf7ecbdff2e94987c6`

```dockerfile
```

-	Layers:
	-	`sha256:c463f59b08554468e33ec7d67e5bf358a4422df9ba9c9e8a5c85545acbf01205`  
		Last Modified: Tue, 28 Jan 2025 01:41:34 GMT  
		Size: 79.9 KB (79872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55be9c8a835f959acbc00acf5a1a31119a99c2d3a92aba2088b8f3f0b9b7f56c`  
		Last Modified: Tue, 28 Jan 2025 01:41:34 GMT  
		Size: 14.4 KB (14436 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; 386

```console
$ docker pull spiped@sha256:b310c392ab6f14391fb45b5af6ea15dbcbd23076e497d3d94c110d7b2087f4a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3592537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cbcf6cf269492e27066e7c7bbcb967e81247f0f3f3d09284672b28db7077ed8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551001421d38a34944d1a96a5df258e75c389ab10abd35456cbb26915537f7fd`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f72f77ecf249ccd9496811e0eb3c0cf489c7b7fdbfa9b09a800fc23ce9a5b86`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 7.9 KB (7906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78fa624f51e7a9f83ca9c71b40f866f13ab95ae1d6fb7f7fb39888ee08b23f5`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 120.1 KB (120111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b172e6f71ba4a3cd0b9d569cc026414ab5ff72c2c999047269348e63b5abaf`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102f42fb7496f67e41461243ea1a96721d75c60e36c3fc0bc0cc31f4a05a0a3f`  
		Last Modified: Tue, 28 Jan 2025 01:28:29 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:9927a6df5d8b7dbdb338658808aeddad5564ef5897b94b692df5dfa29b9abdef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d905998f2bfd41e52ca5677826d1ba128880dee6ab953a307411406c31b587`

```dockerfile
```

-	Layers:
	-	`sha256:aef24c41d2f2fe02d3f60245a4d8614488af106b27f1694638bb0aa63affdeec`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 79.8 KB (79791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e634c06318ef153f0dea3d1996b85ebfa8b5d1ae392ac0ae4aba4ce249a2d7ee`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 14.3 KB (14265 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:884a0eb6ba4f64c3edda016b28d4bd99dba5200f5af5ac9cb6b72f18cb3a3a60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3695562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18a09f14f9a1c5c8a4bc39f97cc1d4dfc2da04ebc3eb0e1c14ee25ecf135a583`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2937ae7bb7a53c30739164fd8d6b1af5449b91bdeaacb11c09da360a795e967b`  
		Last Modified: Tue, 21 Jan 2025 19:31:28 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbed2b37b3a36511a8f8cde15ac74df12676c707a75cac7400604b533817a57b`  
		Last Modified: Tue, 21 Jan 2025 19:31:28 GMT  
		Size: 7.9 KB (7918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2bb56ba626edfb899d02de6e190e018998d7573a673f6db87d5ef30de0a050`  
		Last Modified: Tue, 28 Jan 2025 01:43:33 GMT  
		Size: 112.6 KB (112648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e93d7242196ad9ca14b560ce78c345dfa536c1a35de8044919beffdf4eb97a`  
		Last Modified: Tue, 28 Jan 2025 01:43:33 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9e06feef4b6941cffa38f96ec7bf4e23040ea0baf7cf6f0a7345c46675eff3`  
		Last Modified: Tue, 28 Jan 2025 01:43:33 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:02029f95376d43c51ccddf3f8c8bbebb0671c8774aacfa19d44aee40f4773161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4efe04e204e62e8c95b99341d61fcd033d068bcbce5868ae0ec1685e9f9da3e`

```dockerfile
```

-	Layers:
	-	`sha256:f198a76291582efc4f722539762e32a43b96a2acfb2de57f18adfa903c9b3c57`  
		Last Modified: Tue, 28 Jan 2025 01:43:33 GMT  
		Size: 77.9 KB (77899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c32d956ebf079b702220519e8a308783736857197d7766e995bfbcd8c71dbf2c`  
		Last Modified: Tue, 28 Jan 2025 01:43:33 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:756e00d72198e903bfd6356e80496c2936c64fa26149b3662c09c044393ac715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3458360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef3b076b4ea8c2964765a22bf8c5d8b2fb8141f171e1f335b628572524c3ab7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Wed, 08 Jan 2025 17:48:43 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410676c340782e10ad961429d12c4fc7bc22fe42e602f44af8fe4564583fa790`  
		Last Modified: Tue, 21 Jan 2025 19:47:10 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb03e5e951a5c0dc5098e3f3712ba683716c2830cd781627b8c589f37e35d49e`  
		Last Modified: Tue, 21 Jan 2025 19:47:10 GMT  
		Size: 7.9 KB (7900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d4da436692d4ab0fd5035ee54eac03b05bf24df9aa3304a4cbb3e6bb7fb7de`  
		Last Modified: Tue, 28 Jan 2025 02:22:45 GMT  
		Size: 98.8 KB (98808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b11f3813ff058c0963785dcdc5c5f860f00840874673c02d724b273f844d53c`  
		Last Modified: Tue, 28 Jan 2025 02:22:45 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d897b6a73cbb856ebfd058f311b8f0e39512fdede0d33460f38db93bb89b6c`  
		Last Modified: Tue, 28 Jan 2025 02:22:45 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:877a9cd3fe26f402674032844c26b7149200267a47a431963b72e3b4563d519c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b37c1a9028694f866e7acc219fbf431ce5b97965a6f5489a14f064c84a12b1`

```dockerfile
```

-	Layers:
	-	`sha256:40546cca6e89cde845ebe9184ed940f3b4f38ba1e18049e3b36b047821e42722`  
		Last Modified: Tue, 28 Jan 2025 02:22:45 GMT  
		Size: 77.9 KB (77895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12a0377ea7376b0115517894b6c6f3d26482dcf699f270a21454fd463c994114`  
		Last Modified: Tue, 28 Jan 2025 02:22:45 GMT  
		Size: 14.3 KB (14347 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:496d1116424a4c78bad3fdd46c2db89305089a904ff0d42fcd07ffca4576a0b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32ae085c92ecf8421e7f161ab96951c317b5e771993504a3e09c8db10414930`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2d0ea9a1061fe840c13a046b93faaeb9dbcf4357f53a37b83747a395c05279`  
		Last Modified: Tue, 21 Jan 2025 19:32:37 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068b14e90f05cd3c9537d5988b4bbe6abead4cac15a8b25d1959964036cdbb13`  
		Last Modified: Tue, 21 Jan 2025 19:32:37 GMT  
		Size: 7.9 KB (7909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3398f6409117bd2a57c6b304f740badcea613c5def606a7c072bcd0c73b061e0`  
		Last Modified: Tue, 28 Jan 2025 01:57:36 GMT  
		Size: 96.9 KB (96911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32ed7682792c020e13d8b547fdbb8c43a4956cb69969b8f5a2724202bbcb39d`  
		Last Modified: Tue, 28 Jan 2025 01:57:37 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff53239a6486b270ef8a57e32718cefe901786526573b780eb054d1ac053dc6e`  
		Last Modified: Tue, 28 Jan 2025 01:57:37 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:d66b26cdcd77f8b4437bcb47a340f63d583e754a794e2a822931eafa72152360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6cdd7bbb43e56276987d1ae0048a6f92a4bca0ccdee9e8e670ddb9ea5e16cb9`

```dockerfile
```

-	Layers:
	-	`sha256:6fe581f275230ca3b53c4a9c2f8f4690c4edf45359ead5089d277953f8872d2a`  
		Last Modified: Tue, 28 Jan 2025 01:57:36 GMT  
		Size: 77.9 KB (77865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0280df9fd96cadb1c6e05a657e4d4caa094e820e2a85ddd2df85b36c0363d18`  
		Last Modified: Tue, 28 Jan 2025 01:57:36 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6.3`

```console
$ docker pull spiped@sha256:8f77956d848c5f3eb11bee20026e0d9a843af8a30b2c0310b669c658468127e3
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

### `spiped:1.6.3` - linux; amd64

```console
$ docker pull spiped@sha256:536ab474df09e03eac6134fbad4dd27c18a9135fbd86911f2ea7ad690cd04c33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37097837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61f9190e48c091c3f1a4bb917ae20281a709f4394fe1e013004350789b909d3d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297bb720785ed556393334ee818634585f1264385e1193c7cb9a6c139bc65e14`  
		Last Modified: Tue, 28 Jan 2025 01:28:12 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf32c2751d5f872e24f5ed59e217dfd7f84f720367f3076380ff4715073f8266`  
		Last Modified: Tue, 28 Jan 2025 01:28:12 GMT  
		Size: 2.4 MB (2401375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52ec02d46ad29a364ad7f54bb7579493738fab77fe07703d1e53490f14ada4d`  
		Last Modified: Tue, 28 Jan 2025 01:28:12 GMT  
		Size: 6.5 MB (6482502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e904725dea08f9faf2a31328c10f1398468e995b0d27eadb03ed85a22210d22`  
		Last Modified: Tue, 28 Jan 2025 01:28:12 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60b6b0ce2ec5b5eba3960efaa100171ec619e02ea4145fe1925f0376dafadbc`  
		Last Modified: Tue, 28 Jan 2025 01:28:12 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3` - unknown; unknown

```console
$ docker pull spiped@sha256:8a092ebcd3079b2fbc9871bcd444705cac06810db040b4d55c3479865935afcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3530854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f58c8d654972c43b6abb062eb1922573a9f104695000577382138c422a961791`

```dockerfile
```

-	Layers:
	-	`sha256:68928954d7e34be1617a4df1c97a0aab4efc8c72ae02be92a38358bb07437fec`  
		Last Modified: Tue, 28 Jan 2025 01:28:12 GMT  
		Size: 3.5 MB (3515814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8da9ca933cbc0022cfb2d34616b0a64c0d373dd8393666ef7c6e9adc16a5e722`  
		Last Modified: Tue, 28 Jan 2025 01:28:12 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.3` - linux; arm variant v5

```console
$ docker pull spiped@sha256:0e5c7e178a60719668836afaff3ff67125afee9e3d03accd4401cab3bf3aea23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32882141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d77ac67695453c5d4fc89a848dee8a8392d8bc72b52ea81b468257f78768ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1736726400'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7a3fc1134bc1af98e13c0b7ea743c863d5a17f830a5fbd5a7002f750500e76c2`  
		Last Modified: Tue, 14 Jan 2025 01:33:27 GMT  
		Size: 25.7 MB (25736665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d02c24549d50cc08f67dd0716935f9fa89992a0a0c1150357bba3bd55a0c1e7`  
		Last Modified: Tue, 14 Jan 2025 06:07:49 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3c5e73b2f407694f10795c56fde8bcb539c9e2933731585f42dca1b1ace55f`  
		Last Modified: Tue, 14 Jan 2025 06:07:49 GMT  
		Size: 2.0 MB (1997177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e30adfe160215d6c7902f37ebf94ac563be9c6fccb4a395277b1aa3818607b7`  
		Last Modified: Tue, 28 Jan 2025 01:31:03 GMT  
		Size: 5.1 MB (5146757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27aac59a43177421679bd0226f35aab3ba9fa205c1b5d6c67dafa249b4e83cfd`  
		Last Modified: Tue, 28 Jan 2025 01:31:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9448be81708fcc8741ac6f43584de6ba475c3536046bde4f7c2191a0870c19b`  
		Last Modified: Tue, 28 Jan 2025 01:31:03 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3` - unknown; unknown

```console
$ docker pull spiped@sha256:23079fe3fffca7762fa71b01d0411f8384596126fe153c023b09dc5660eeaf82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3501486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eeb887a5a783665797ba8dc1fdd892d0261c16063f2c97462d2de3fcb591a5e`

```dockerfile
```

-	Layers:
	-	`sha256:22e1c45058e14bd513fd59735994785f69dca0da45c2043c929cd60ab6ee6712`  
		Last Modified: Tue, 28 Jan 2025 01:31:03 GMT  
		Size: 3.5 MB (3486344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b83aa6e8691e60672de940db65cf58f8168cc03800c9df896f0392230faef68d`  
		Last Modified: Tue, 28 Jan 2025 01:31:03 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.3` - linux; arm variant v7

```console
$ docker pull spiped@sha256:ccbdcef0387e5cc6e9d060a7cb6251eab74ea58109617ddfb00ae7dfbadec466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 MB (30659580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:531150a8da7eb7ecbbdd6e1044330fae803c4f7a5e6fd062da86e8c1d4b96829`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 01:35:15 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f82d2a6f73f55cbf1d37fd27277b02bccaab05b4f4566fba3f60d3414b02ee`  
		Last Modified: Tue, 28 Jan 2025 01:37:09 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbd4fec55999df669ac552c8a8a36d23d8968fc0384aa8e416b1c891eaf20ae`  
		Last Modified: Tue, 28 Jan 2025 01:37:10 GMT  
		Size: 1.9 MB (1855576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82cb6e6723fd5a0ef75b0dd184cf799af3ed260e21af13ab1c2e506822b2fa70`  
		Last Modified: Tue, 28 Jan 2025 01:37:10 GMT  
		Size: 4.9 MB (4887862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d26fd234d491740cb625280d39e623f8d839377ffc0b57cb3504d8de911c3a`  
		Last Modified: Tue, 28 Jan 2025 01:37:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901f496578fbc184fc4790a1b4c0bab2352fb6e530beea188e4b0ba08046ce2a`  
		Last Modified: Tue, 28 Jan 2025 01:37:10 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3` - unknown; unknown

```console
$ docker pull spiped@sha256:1033931b8488d45445247954b4346c2ab38a753e8b906a66b9bf16352c819acd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3500977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd5b75d5b44c4854ab926811600353150aa50de74119e06dddbb73d084581421`

```dockerfile
```

-	Layers:
	-	`sha256:9fa27b21622f0eccb462ea952ab0228e3f904ac0ba741c3b32b2127f45ef179c`  
		Last Modified: Tue, 28 Jan 2025 01:37:09 GMT  
		Size: 3.5 MB (3485835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53bbd1b214a94134a85adbc419d7fc676232db4a3b9e14631c713a43a5060e11`  
		Last Modified: Tue, 28 Jan 2025 01:37:09 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.3` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:f2a66012e502dbb68d83b8806cce2a21cb04c84f8e8095bbc2ce736123fb1c20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35780523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3cecf8e2ff2652a6faf516302f17aaa5e8c690b4d97abc9d701160260cd09df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611fe6e9d63e5acb1e7209441d4b6f53839cdb499ce56c53d0a30b18127308af`  
		Last Modified: Tue, 28 Jan 2025 01:41:01 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92430745938fc1ad04a384084859a1779a798bfb2a43cb5e04624d43cd1c7acb`  
		Last Modified: Tue, 28 Jan 2025 01:41:02 GMT  
		Size: 2.2 MB (2247010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369b9862e0933ebe96fc5bda017bd6683b320f8a4d289e80aeed978512cfd255`  
		Last Modified: Tue, 28 Jan 2025 01:41:02 GMT  
		Size: 5.5 MB (5490939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44aa3faa85b28c389faec240ea702de4afa507e7ae685e53314bbdbdff04e80`  
		Last Modified: Tue, 28 Jan 2025 01:41:02 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0a4dc5911186cef9e82bc70ce35d467f950380c65a8d1b0250e0cc206e281e`  
		Last Modified: Tue, 28 Jan 2025 01:41:02 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3` - unknown; unknown

```console
$ docker pull spiped@sha256:47baf7f47236cf831a26ca76d55a8157b116d3dda5925ce8dbbd41d52567069c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3502215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a52acd09d735182eaae4ccffd45c06b9c79bda50a540013e3d691be3da2f431b`

```dockerfile
```

-	Layers:
	-	`sha256:f37345f4dbabaa7e656ed0a75816887fbcfe4951dd41a63d2740bd6ed26f51db`  
		Last Modified: Tue, 28 Jan 2025 01:41:01 GMT  
		Size: 3.5 MB (3487042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:843f601a405007c9da76c3218d51fb2452dc29660928c0893ae7a93703c06e25`  
		Last Modified: Tue, 28 Jan 2025 01:41:01 GMT  
		Size: 15.2 KB (15173 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.3` - linux; 386

```console
$ docker pull spiped@sha256:98ef029814d34d405160b8cd8774b36e1d4075a55db56c75216503f239694141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37544183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d67702ad5748bfe47a10731422eb415fdfc7806bb9184783f769026d4b749a5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 01:33:46 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:990933e5818dac2477379a6c22c8ff156aac80a847271355d54aa7f84e4047c9`  
		Last Modified: Tue, 28 Jan 2025 01:28:36 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec82207d2d5f8c5aee844ce2e9965b1200e45e37009b0bd27d9c3669dd80982`  
		Last Modified: Tue, 28 Jan 2025 01:28:36 GMT  
		Size: 2.4 MB (2398647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de33615d1d4298ca4d90a730d18b76eeab9221bd569fb9925d296300b3597612`  
		Last Modified: Tue, 28 Jan 2025 01:28:36 GMT  
		Size: 6.0 MB (5956398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f9dbd3c5360bd8b3e00e28ec6bfa6f27a97b4b5be2b628a808617b72108df9`  
		Last Modified: Tue, 28 Jan 2025 01:28:36 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf9571f1b17fff32d6a9adffafb32ad8904d04b3f7156f083697132e0b29725`  
		Last Modified: Tue, 28 Jan 2025 01:28:37 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3` - unknown; unknown

```console
$ docker pull spiped@sha256:15d6e0b7e94089abdc57fd1f30df3fc0de016254b2559e656bd0a497b9f74ab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f402ca8235399d4eaacdc1a9831b9d0fea4707fb82e628c7b5e5b32eada091cd`

```dockerfile
```

-	Layers:
	-	`sha256:4f281e15904f5ac0cd9177326f1d676beae6635dd8abbb81371af8c165adc9a9`  
		Last Modified: Tue, 28 Jan 2025 01:28:36 GMT  
		Size: 3.5 MB (3509741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:092229d42c4fa5b9eeb6f986ac672c68620fbb93f0b803f6bc734339f807e88d`  
		Last Modified: Tue, 28 Jan 2025 01:28:36 GMT  
		Size: 15.0 KB (15004 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.3` - linux; mips64le

```console
$ docker pull spiped@sha256:6bf1b2934b50bc37036f47c176307572e04ff3a865286a7cccb291a8c555bf59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36142417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e18f14eeb0958c9f235ad5a0e8476007640d4ed876a873b66b364a4e51c9b9b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1736726400'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b08d7e697b04bda8cef97763765ebbbc16790e22945b5ab31d97d448a15c8650`  
		Last Modified: Tue, 14 Jan 2025 01:38:32 GMT  
		Size: 28.5 MB (28486647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252230c34678f565279955a422dad63275a16eeef208147f154e13e5647df2ed`  
		Last Modified: Tue, 14 Jan 2025 18:08:24 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f980dd5eb6de9195670967164c2a6d21dfc4bd270afc766fc82f7303fcea879a`  
		Last Modified: Tue, 14 Jan 2025 18:08:25 GMT  
		Size: 1.8 MB (1841121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336f4b90f8852da9787d9b302a76c1c166e886091303a5004535e9cb73fd632d`  
		Last Modified: Tue, 28 Jan 2025 01:32:12 GMT  
		Size: 5.8 MB (5813106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5512c8a48481cf94715c1506c2c4e1ff9f6d805efb3b0338118b5689e3c21079`  
		Last Modified: Tue, 28 Jan 2025 01:32:11 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c228f3bd07cbcd06c100e65d713148abb7e018c7025c9b9d6484049c0a2146a9`  
		Last Modified: Tue, 28 Jan 2025 01:32:12 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3` - unknown; unknown

```console
$ docker pull spiped@sha256:249deaaff0d1784a18b6797030367453d08714a64db8712ca45edd7df3073b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbab1862f923b3499782eb1f960684b595f083d0fe2345bd5a6e2c53ae83acd0`

```dockerfile
```

-	Layers:
	-	`sha256:7c6c6f098c793c8847f89582fbc460774fcad941d2a4ed4ded37e75f6dcf7622`  
		Last Modified: Tue, 28 Jan 2025 01:32:11 GMT  
		Size: 14.9 KB (14896 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.3` - linux; ppc64le

```console
$ docker pull spiped@sha256:d18399db45255851ae8ddbad4e7b5c900d55f4e43695efd3981135d67341765b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41069257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d445aa64495f4c7fdb2a32b492a68d159b909988abb7b61737e38b5345a0b8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2904017eed57b6a379aba91f659af48ec8d1305525c46625a955313f2f21e7a9`  
		Last Modified: Tue, 28 Jan 2025 01:42:23 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170c8da9f5a98720edaa9345e098b778f3682abcc6a559d512c35d465ed68eb1`  
		Last Modified: Tue, 28 Jan 2025 01:42:24 GMT  
		Size: 2.6 MB (2582109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf6e585af2ae045254fc980b05067c3829832933e9228997d7b38860b66ec72`  
		Last Modified: Tue, 28 Jan 2025 01:42:24 GMT  
		Size: 6.4 MB (6440760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839630c4aa5ab3314108a0e90bc3ef41c6d874dbf2195903468542b67df10b19`  
		Last Modified: Tue, 28 Jan 2025 01:42:24 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1bd1225ed7d385f9ccd07a3e86a10eecb6f5aceb0d21253d66059f25cc10f76`  
		Last Modified: Tue, 28 Jan 2025 01:42:24 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3` - unknown; unknown

```console
$ docker pull spiped@sha256:635959fa2681a25dc8179b535939238e6dedf3b4407e4b61c265dcaef89b8b0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3516571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7a5467d6b5e70429f77b5ecc51c24454e72e2a4bec50c2ce6d2c38b6d6ceda`

```dockerfile
```

-	Layers:
	-	`sha256:058f9b63cb6c662558bc2dc672de21d6e7f0b7686ae208b7d53a9ed320429272`  
		Last Modified: Tue, 28 Jan 2025 01:42:24 GMT  
		Size: 3.5 MB (3501483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58bba2fecafbd5b0fec43540d380620c8286e345af289a079b69e2ac6bc4556c`  
		Last Modified: Tue, 28 Jan 2025 01:42:23 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.3` - linux; s390x

```console
$ docker pull spiped@sha256:1360a16741b1d8479ba95a46e1eba44e5a1865a9b32409d5461808606b6b823b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34320664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a19118972ca2e46f28001e2d3152e846d353428043b8bd5449cf0659847072d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9e408aef4b499eef3c5a232610cdb9528eac0555c35a861721e1b66e887bce`  
		Last Modified: Tue, 28 Jan 2025 01:56:55 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9cb1363f3ebb86bcd48ad2dfee1768ef18362d453c9befc1470291d84150aaf`  
		Last Modified: Tue, 28 Jan 2025 01:56:56 GMT  
		Size: 2.1 MB (2068705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca8f083cf8abe1b1441f2edc74b5257b41d3ce228131595d258c42c95bb6074`  
		Last Modified: Tue, 28 Jan 2025 01:56:56 GMT  
		Size: 5.4 MB (5391679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445668117981bb081001c5c8686393d3ea7269a2c19c1a02123c111d4ea71388`  
		Last Modified: Tue, 28 Jan 2025 01:56:56 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b87d689b7d650c827b31ea84b35647df1ba39ce7d24b0700f17a0d97decba3`  
		Last Modified: Tue, 28 Jan 2025 01:56:56 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3` - unknown; unknown

```console
$ docker pull spiped@sha256:d14b17075dae6fdb16fc48d6774f8fcadaa06b728ba5478747afec1ccbcb1614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3519040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d01e321bd685e686da98fa6db440fc0736d29b352be36b6b89c8c977200c6299`

```dockerfile
```

-	Layers:
	-	`sha256:0f886e33ca85512f04d777aad824fda2adcbe9e19a9c3e19518644f51adf168b`  
		Last Modified: Tue, 28 Jan 2025 01:56:56 GMT  
		Size: 3.5 MB (3504000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daa4df4848c5169cbffc9300f9d2ac12ef5ce68655c6423c6432a1533d3d1899`  
		Last Modified: Tue, 28 Jan 2025 01:56:55 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6.3-alpine`

```console
$ docker pull spiped@sha256:cff1ff69fc6f8904043ef5d9bb654e468a38fc671dedcecd1f568a1d61f1d634
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

### `spiped:1.6.3-alpine` - linux; amd64

```console
$ docker pull spiped@sha256:2715ebbc20690dda6d438989f61f4eb4fb11162e932ba70cedc0c7f12b3c26f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3758631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ec86461245d72383c5662f686c25016cc299d589def9478af4205b484492be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b181c716ebe4d13478b33f2488cb40b954ba24081d61c5bc9d7f0605ba9d113`  
		Last Modified: Tue, 28 Jan 2025 01:28:04 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ded10ce7d7c8e5d5eb05c5a7d5246a6a045996ee4f18dcc322d6600e68cd81`  
		Last Modified: Tue, 28 Jan 2025 01:28:04 GMT  
		Size: 7.9 KB (7907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d46a15f052086577ecb502311cd9f4d176cd407ad00862e11dd7d6f8c2a868`  
		Last Modified: Tue, 28 Jan 2025 01:28:04 GMT  
		Size: 107.6 KB (107614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b34221300809a19087f5d67a70e8167a72247feb52faa8c58a878f5af671d3`  
		Last Modified: Tue, 28 Jan 2025 01:28:04 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c89b10c18fcccf667446750b679723f2821a55bf5612caacbb8c510578e77e1`  
		Last Modified: Tue, 28 Jan 2025 01:28:05 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:6a640be7b02114db4704050ac59d1be28b1b8f1a10f0ce877865a41933bc6d1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24283cd9a878c00f69d37c768fc27af4fe97d6fa56a0174f6b441c10746770b0`

```dockerfile
```

-	Layers:
	-	`sha256:f6e7df028e10774143b75638cf9a91ae4484ad9be9705a3ab7de160bfbeab308`  
		Last Modified: Tue, 28 Jan 2025 01:28:04 GMT  
		Size: 79.8 KB (79816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:307857c2fc1847cc55f2ad19b9b6647658c5135c8b20a447ca114dfaf6cdb9b3`  
		Last Modified: Tue, 28 Jan 2025 01:28:04 GMT  
		Size: 14.3 KB (14301 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.3-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:6f9bbe66f9f9620c0aad2b8b464d5f0912510b5fbbcce31e1458c51d8bdc36a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3462325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24b357cad96475791645ca664e952dfc2be3a80db4daa6ebc50db2cdb2426d71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee72c2b1876a0156b7d396caf2dc29a0f8081b2b7a6733a3ff64d9527f586ea`  
		Last Modified: Tue, 21 Jan 2025 19:29:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1da6fb0facd6416135ae0db69e959ecf3e75cab6ea327aabb4ead163825dfc7`  
		Last Modified: Tue, 21 Jan 2025 19:29:40 GMT  
		Size: 7.9 KB (7914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0919c3817d8379bb41e1be06c4a9ce8b781a7c46fd9a118114bab8de444770a2`  
		Last Modified: Tue, 28 Jan 2025 01:40:36 GMT  
		Size: 89.1 KB (89138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995e0d0ce3aa2cc891355694b9f4548ada6aa0f587ac1f8f95ff08b62f092ca3`  
		Last Modified: Tue, 28 Jan 2025 01:40:36 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6048abcd79b046de58bebf91b3eb0b6d1d3cdef973e93188a86da2ad1ffe65`  
		Last Modified: Tue, 28 Jan 2025 01:40:36 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:3f840c3a9d83f847e5bb8879ed8d0fae64e2ab7849ae389421052f6925264c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71a31c54f0008afb75dde7c016b9771c6f37268270d33d98c57f6d4c46be550c`

```dockerfile
```

-	Layers:
	-	`sha256:e415d942102ceb25c19c03d57e7aad5f3e309c6a8aebe7422ef678a4f6a8c3c4`  
		Last Modified: Tue, 28 Jan 2025 01:40:36 GMT  
		Size: 14.2 KB (14186 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.3-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:12817cd6117bed3cdf9e7e4b52de247dd1a87d2876d8dc7434e5115f0fc9a549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3188067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1cba0ff108ef4a8e8108d49bf7ccd596afac4a82110a7c14e80a001be5fa5bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ae962cfc489c298278551ba32bca1e0ed1f67cd05192848331b7c3ee926a77`  
		Last Modified: Tue, 21 Jan 2025 19:30:37 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1114d274ac423361940bdd6b0c7904acc23cb9903e6f1a2904b32a6b89f331c4`  
		Last Modified: Tue, 21 Jan 2025 19:30:37 GMT  
		Size: 7.9 KB (7915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51637362b800c4f96d7abb05ca7529a770947ee4b1e9623b35af4b936195f4a9`  
		Last Modified: Tue, 28 Jan 2025 01:37:32 GMT  
		Size: 81.6 KB (81648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b15074482593cb5d5f416eda5eadebe75a10ba5005975523c4c34e81f46e618`  
		Last Modified: Tue, 28 Jan 2025 01:37:33 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db71199d0efb2f82ed5530667b5595dd7a34230b43f8dd94dbe9c99654b1b9ae`  
		Last Modified: Tue, 28 Jan 2025 01:37:33 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b5a94554ddb9da6514578c1b09075a2b4ab9c4410f3e3e231bae96919d45f4b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2f515b3bed3192db05a2ad5b870421a369f4a33d6b7164dac00142ecf5bc150`

```dockerfile
```

-	Layers:
	-	`sha256:49f4a9e142d4f0bbdb2b6f12f002efa4735f8926b13589ba3a9a5a9ce1a027ef`  
		Last Modified: Tue, 28 Jan 2025 01:37:32 GMT  
		Size: 79.9 KB (79852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c72de5bccb3b20f12aaba84aa22f33c24e0ef214459867af7cbe28470672cb2`  
		Last Modified: Tue, 28 Jan 2025 01:37:32 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.3-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:7bd7eff848bd7ecb4ebeafabcab07a01e40580fc27ad865b3b7dc5c3e8307bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4102233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46380b40fc8cf495b0e4fe6bb439caf833e2bbaf42e79ccbccacbd21456f38f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987e71ee6cc5ab416ed1f0e49bb9a1696b4b5656b4d3fcc1feca517c7bbe5030`  
		Last Modified: Tue, 21 Jan 2025 19:50:56 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5faf545dafdf63442f66bf2d829b8ba0c5dd8fe81240a3298cbf9fee767c891`  
		Last Modified: Tue, 21 Jan 2025 19:50:56 GMT  
		Size: 7.9 KB (7921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7966823473fa57bd0c6c045474918109f56a52c519aa3ff2bbeb53a9bd43f890`  
		Last Modified: Tue, 28 Jan 2025 01:41:34 GMT  
		Size: 100.6 KB (100555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5487e20745df540295ba2a7d5c3230edfbc1657b671f349f920b261416279acc`  
		Last Modified: Tue, 28 Jan 2025 01:41:34 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9477716625dcd64617f5279d092cb746cef8275524ced557b548fac120fd1e9d`  
		Last Modified: Tue, 28 Jan 2025 01:41:35 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:bf674933baf7156a187fcab52df270880af433ca3e590a2d21c400137e505bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e08d169c62b2f76c8f3d4eae8033be48d397c61a9f6edf7ecbdff2e94987c6`

```dockerfile
```

-	Layers:
	-	`sha256:c463f59b08554468e33ec7d67e5bf358a4422df9ba9c9e8a5c85545acbf01205`  
		Last Modified: Tue, 28 Jan 2025 01:41:34 GMT  
		Size: 79.9 KB (79872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55be9c8a835f959acbc00acf5a1a31119a99c2d3a92aba2088b8f3f0b9b7f56c`  
		Last Modified: Tue, 28 Jan 2025 01:41:34 GMT  
		Size: 14.4 KB (14436 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.3-alpine` - linux; 386

```console
$ docker pull spiped@sha256:b310c392ab6f14391fb45b5af6ea15dbcbd23076e497d3d94c110d7b2087f4a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3592537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cbcf6cf269492e27066e7c7bbcb967e81247f0f3f3d09284672b28db7077ed8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551001421d38a34944d1a96a5df258e75c389ab10abd35456cbb26915537f7fd`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f72f77ecf249ccd9496811e0eb3c0cf489c7b7fdbfa9b09a800fc23ce9a5b86`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 7.9 KB (7906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78fa624f51e7a9f83ca9c71b40f866f13ab95ae1d6fb7f7fb39888ee08b23f5`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 120.1 KB (120111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b172e6f71ba4a3cd0b9d569cc026414ab5ff72c2c999047269348e63b5abaf`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102f42fb7496f67e41461243ea1a96721d75c60e36c3fc0bc0cc31f4a05a0a3f`  
		Last Modified: Tue, 28 Jan 2025 01:28:29 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:9927a6df5d8b7dbdb338658808aeddad5564ef5897b94b692df5dfa29b9abdef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d905998f2bfd41e52ca5677826d1ba128880dee6ab953a307411406c31b587`

```dockerfile
```

-	Layers:
	-	`sha256:aef24c41d2f2fe02d3f60245a4d8614488af106b27f1694638bb0aa63affdeec`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 79.8 KB (79791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e634c06318ef153f0dea3d1996b85ebfa8b5d1ae392ac0ae4aba4ce249a2d7ee`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 14.3 KB (14265 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.3-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:884a0eb6ba4f64c3edda016b28d4bd99dba5200f5af5ac9cb6b72f18cb3a3a60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3695562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18a09f14f9a1c5c8a4bc39f97cc1d4dfc2da04ebc3eb0e1c14ee25ecf135a583`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2937ae7bb7a53c30739164fd8d6b1af5449b91bdeaacb11c09da360a795e967b`  
		Last Modified: Tue, 21 Jan 2025 19:31:28 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbed2b37b3a36511a8f8cde15ac74df12676c707a75cac7400604b533817a57b`  
		Last Modified: Tue, 21 Jan 2025 19:31:28 GMT  
		Size: 7.9 KB (7918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2bb56ba626edfb899d02de6e190e018998d7573a673f6db87d5ef30de0a050`  
		Last Modified: Tue, 28 Jan 2025 01:43:33 GMT  
		Size: 112.6 KB (112648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e93d7242196ad9ca14b560ce78c345dfa536c1a35de8044919beffdf4eb97a`  
		Last Modified: Tue, 28 Jan 2025 01:43:33 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9e06feef4b6941cffa38f96ec7bf4e23040ea0baf7cf6f0a7345c46675eff3`  
		Last Modified: Tue, 28 Jan 2025 01:43:33 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:02029f95376d43c51ccddf3f8c8bbebb0671c8774aacfa19d44aee40f4773161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4efe04e204e62e8c95b99341d61fcd033d068bcbce5868ae0ec1685e9f9da3e`

```dockerfile
```

-	Layers:
	-	`sha256:f198a76291582efc4f722539762e32a43b96a2acfb2de57f18adfa903c9b3c57`  
		Last Modified: Tue, 28 Jan 2025 01:43:33 GMT  
		Size: 77.9 KB (77899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c32d956ebf079b702220519e8a308783736857197d7766e995bfbcd8c71dbf2c`  
		Last Modified: Tue, 28 Jan 2025 01:43:33 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.3-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:756e00d72198e903bfd6356e80496c2936c64fa26149b3662c09c044393ac715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3458360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef3b076b4ea8c2964765a22bf8c5d8b2fb8141f171e1f335b628572524c3ab7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Wed, 08 Jan 2025 17:48:43 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410676c340782e10ad961429d12c4fc7bc22fe42e602f44af8fe4564583fa790`  
		Last Modified: Tue, 21 Jan 2025 19:47:10 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb03e5e951a5c0dc5098e3f3712ba683716c2830cd781627b8c589f37e35d49e`  
		Last Modified: Tue, 21 Jan 2025 19:47:10 GMT  
		Size: 7.9 KB (7900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d4da436692d4ab0fd5035ee54eac03b05bf24df9aa3304a4cbb3e6bb7fb7de`  
		Last Modified: Tue, 28 Jan 2025 02:22:45 GMT  
		Size: 98.8 KB (98808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b11f3813ff058c0963785dcdc5c5f860f00840874673c02d724b273f844d53c`  
		Last Modified: Tue, 28 Jan 2025 02:22:45 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d897b6a73cbb856ebfd058f311b8f0e39512fdede0d33460f38db93bb89b6c`  
		Last Modified: Tue, 28 Jan 2025 02:22:45 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:877a9cd3fe26f402674032844c26b7149200267a47a431963b72e3b4563d519c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b37c1a9028694f866e7acc219fbf431ce5b97965a6f5489a14f064c84a12b1`

```dockerfile
```

-	Layers:
	-	`sha256:40546cca6e89cde845ebe9184ed940f3b4f38ba1e18049e3b36b047821e42722`  
		Last Modified: Tue, 28 Jan 2025 02:22:45 GMT  
		Size: 77.9 KB (77895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12a0377ea7376b0115517894b6c6f3d26482dcf699f270a21454fd463c994114`  
		Last Modified: Tue, 28 Jan 2025 02:22:45 GMT  
		Size: 14.3 KB (14347 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.3-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:496d1116424a4c78bad3fdd46c2db89305089a904ff0d42fcd07ffca4576a0b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32ae085c92ecf8421e7f161ab96951c317b5e771993504a3e09c8db10414930`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2d0ea9a1061fe840c13a046b93faaeb9dbcf4357f53a37b83747a395c05279`  
		Last Modified: Tue, 21 Jan 2025 19:32:37 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068b14e90f05cd3c9537d5988b4bbe6abead4cac15a8b25d1959964036cdbb13`  
		Last Modified: Tue, 21 Jan 2025 19:32:37 GMT  
		Size: 7.9 KB (7909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3398f6409117bd2a57c6b304f740badcea613c5def606a7c072bcd0c73b061e0`  
		Last Modified: Tue, 28 Jan 2025 01:57:36 GMT  
		Size: 96.9 KB (96911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32ed7682792c020e13d8b547fdbb8c43a4956cb69969b8f5a2724202bbcb39d`  
		Last Modified: Tue, 28 Jan 2025 01:57:37 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff53239a6486b270ef8a57e32718cefe901786526573b780eb054d1ac053dc6e`  
		Last Modified: Tue, 28 Jan 2025 01:57:37 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.3-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:d66b26cdcd77f8b4437bcb47a340f63d583e754a794e2a822931eafa72152360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6cdd7bbb43e56276987d1ae0048a6f92a4bca0ccdee9e8e670ddb9ea5e16cb9`

```dockerfile
```

-	Layers:
	-	`sha256:6fe581f275230ca3b53c4a9c2f8f4690c4edf45359ead5089d277953f8872d2a`  
		Last Modified: Tue, 28 Jan 2025 01:57:36 GMT  
		Size: 77.9 KB (77865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0280df9fd96cadb1c6e05a657e4d4caa094e820e2a85ddd2df85b36c0363d18`  
		Last Modified: Tue, 28 Jan 2025 01:57:36 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:alpine`

```console
$ docker pull spiped@sha256:cff1ff69fc6f8904043ef5d9bb654e468a38fc671dedcecd1f568a1d61f1d634
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
$ docker pull spiped@sha256:2715ebbc20690dda6d438989f61f4eb4fb11162e932ba70cedc0c7f12b3c26f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3758631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ec86461245d72383c5662f686c25016cc299d589def9478af4205b484492be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b181c716ebe4d13478b33f2488cb40b954ba24081d61c5bc9d7f0605ba9d113`  
		Last Modified: Tue, 28 Jan 2025 01:28:04 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ded10ce7d7c8e5d5eb05c5a7d5246a6a045996ee4f18dcc322d6600e68cd81`  
		Last Modified: Tue, 28 Jan 2025 01:28:04 GMT  
		Size: 7.9 KB (7907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d46a15f052086577ecb502311cd9f4d176cd407ad00862e11dd7d6f8c2a868`  
		Last Modified: Tue, 28 Jan 2025 01:28:04 GMT  
		Size: 107.6 KB (107614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b34221300809a19087f5d67a70e8167a72247feb52faa8c58a878f5af671d3`  
		Last Modified: Tue, 28 Jan 2025 01:28:04 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c89b10c18fcccf667446750b679723f2821a55bf5612caacbb8c510578e77e1`  
		Last Modified: Tue, 28 Jan 2025 01:28:05 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:6a640be7b02114db4704050ac59d1be28b1b8f1a10f0ce877865a41933bc6d1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24283cd9a878c00f69d37c768fc27af4fe97d6fa56a0174f6b441c10746770b0`

```dockerfile
```

-	Layers:
	-	`sha256:f6e7df028e10774143b75638cf9a91ae4484ad9be9705a3ab7de160bfbeab308`  
		Last Modified: Tue, 28 Jan 2025 01:28:04 GMT  
		Size: 79.8 KB (79816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:307857c2fc1847cc55f2ad19b9b6647658c5135c8b20a447ca114dfaf6cdb9b3`  
		Last Modified: Tue, 28 Jan 2025 01:28:04 GMT  
		Size: 14.3 KB (14301 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:6f9bbe66f9f9620c0aad2b8b464d5f0912510b5fbbcce31e1458c51d8bdc36a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3462325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24b357cad96475791645ca664e952dfc2be3a80db4daa6ebc50db2cdb2426d71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee72c2b1876a0156b7d396caf2dc29a0f8081b2b7a6733a3ff64d9527f586ea`  
		Last Modified: Tue, 21 Jan 2025 19:29:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1da6fb0facd6416135ae0db69e959ecf3e75cab6ea327aabb4ead163825dfc7`  
		Last Modified: Tue, 21 Jan 2025 19:29:40 GMT  
		Size: 7.9 KB (7914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0919c3817d8379bb41e1be06c4a9ce8b781a7c46fd9a118114bab8de444770a2`  
		Last Modified: Tue, 28 Jan 2025 01:40:36 GMT  
		Size: 89.1 KB (89138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995e0d0ce3aa2cc891355694b9f4548ada6aa0f587ac1f8f95ff08b62f092ca3`  
		Last Modified: Tue, 28 Jan 2025 01:40:36 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6048abcd79b046de58bebf91b3eb0b6d1d3cdef973e93188a86da2ad1ffe65`  
		Last Modified: Tue, 28 Jan 2025 01:40:36 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:3f840c3a9d83f847e5bb8879ed8d0fae64e2ab7849ae389421052f6925264c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71a31c54f0008afb75dde7c016b9771c6f37268270d33d98c57f6d4c46be550c`

```dockerfile
```

-	Layers:
	-	`sha256:e415d942102ceb25c19c03d57e7aad5f3e309c6a8aebe7422ef678a4f6a8c3c4`  
		Last Modified: Tue, 28 Jan 2025 01:40:36 GMT  
		Size: 14.2 KB (14186 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:12817cd6117bed3cdf9e7e4b52de247dd1a87d2876d8dc7434e5115f0fc9a549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3188067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1cba0ff108ef4a8e8108d49bf7ccd596afac4a82110a7c14e80a001be5fa5bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ae962cfc489c298278551ba32bca1e0ed1f67cd05192848331b7c3ee926a77`  
		Last Modified: Tue, 21 Jan 2025 19:30:37 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1114d274ac423361940bdd6b0c7904acc23cb9903e6f1a2904b32a6b89f331c4`  
		Last Modified: Tue, 21 Jan 2025 19:30:37 GMT  
		Size: 7.9 KB (7915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51637362b800c4f96d7abb05ca7529a770947ee4b1e9623b35af4b936195f4a9`  
		Last Modified: Tue, 28 Jan 2025 01:37:32 GMT  
		Size: 81.6 KB (81648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b15074482593cb5d5f416eda5eadebe75a10ba5005975523c4c34e81f46e618`  
		Last Modified: Tue, 28 Jan 2025 01:37:33 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db71199d0efb2f82ed5530667b5595dd7a34230b43f8dd94dbe9c99654b1b9ae`  
		Last Modified: Tue, 28 Jan 2025 01:37:33 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b5a94554ddb9da6514578c1b09075a2b4ab9c4410f3e3e231bae96919d45f4b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2f515b3bed3192db05a2ad5b870421a369f4a33d6b7164dac00142ecf5bc150`

```dockerfile
```

-	Layers:
	-	`sha256:49f4a9e142d4f0bbdb2b6f12f002efa4735f8926b13589ba3a9a5a9ce1a027ef`  
		Last Modified: Tue, 28 Jan 2025 01:37:32 GMT  
		Size: 79.9 KB (79852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c72de5bccb3b20f12aaba84aa22f33c24e0ef214459867af7cbe28470672cb2`  
		Last Modified: Tue, 28 Jan 2025 01:37:32 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:7bd7eff848bd7ecb4ebeafabcab07a01e40580fc27ad865b3b7dc5c3e8307bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4102233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46380b40fc8cf495b0e4fe6bb439caf833e2bbaf42e79ccbccacbd21456f38f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987e71ee6cc5ab416ed1f0e49bb9a1696b4b5656b4d3fcc1feca517c7bbe5030`  
		Last Modified: Tue, 21 Jan 2025 19:50:56 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5faf545dafdf63442f66bf2d829b8ba0c5dd8fe81240a3298cbf9fee767c891`  
		Last Modified: Tue, 21 Jan 2025 19:50:56 GMT  
		Size: 7.9 KB (7921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7966823473fa57bd0c6c045474918109f56a52c519aa3ff2bbeb53a9bd43f890`  
		Last Modified: Tue, 28 Jan 2025 01:41:34 GMT  
		Size: 100.6 KB (100555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5487e20745df540295ba2a7d5c3230edfbc1657b671f349f920b261416279acc`  
		Last Modified: Tue, 28 Jan 2025 01:41:34 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9477716625dcd64617f5279d092cb746cef8275524ced557b548fac120fd1e9d`  
		Last Modified: Tue, 28 Jan 2025 01:41:35 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:bf674933baf7156a187fcab52df270880af433ca3e590a2d21c400137e505bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e08d169c62b2f76c8f3d4eae8033be48d397c61a9f6edf7ecbdff2e94987c6`

```dockerfile
```

-	Layers:
	-	`sha256:c463f59b08554468e33ec7d67e5bf358a4422df9ba9c9e8a5c85545acbf01205`  
		Last Modified: Tue, 28 Jan 2025 01:41:34 GMT  
		Size: 79.9 KB (79872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55be9c8a835f959acbc00acf5a1a31119a99c2d3a92aba2088b8f3f0b9b7f56c`  
		Last Modified: Tue, 28 Jan 2025 01:41:34 GMT  
		Size: 14.4 KB (14436 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; 386

```console
$ docker pull spiped@sha256:b310c392ab6f14391fb45b5af6ea15dbcbd23076e497d3d94c110d7b2087f4a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3592537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cbcf6cf269492e27066e7c7bbcb967e81247f0f3f3d09284672b28db7077ed8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551001421d38a34944d1a96a5df258e75c389ab10abd35456cbb26915537f7fd`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f72f77ecf249ccd9496811e0eb3c0cf489c7b7fdbfa9b09a800fc23ce9a5b86`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 7.9 KB (7906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78fa624f51e7a9f83ca9c71b40f866f13ab95ae1d6fb7f7fb39888ee08b23f5`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 120.1 KB (120111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b172e6f71ba4a3cd0b9d569cc026414ab5ff72c2c999047269348e63b5abaf`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102f42fb7496f67e41461243ea1a96721d75c60e36c3fc0bc0cc31f4a05a0a3f`  
		Last Modified: Tue, 28 Jan 2025 01:28:29 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:9927a6df5d8b7dbdb338658808aeddad5564ef5897b94b692df5dfa29b9abdef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d905998f2bfd41e52ca5677826d1ba128880dee6ab953a307411406c31b587`

```dockerfile
```

-	Layers:
	-	`sha256:aef24c41d2f2fe02d3f60245a4d8614488af106b27f1694638bb0aa63affdeec`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 79.8 KB (79791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e634c06318ef153f0dea3d1996b85ebfa8b5d1ae392ac0ae4aba4ce249a2d7ee`  
		Last Modified: Tue, 28 Jan 2025 01:28:28 GMT  
		Size: 14.3 KB (14265 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:884a0eb6ba4f64c3edda016b28d4bd99dba5200f5af5ac9cb6b72f18cb3a3a60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3695562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18a09f14f9a1c5c8a4bc39f97cc1d4dfc2da04ebc3eb0e1c14ee25ecf135a583`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2937ae7bb7a53c30739164fd8d6b1af5449b91bdeaacb11c09da360a795e967b`  
		Last Modified: Tue, 21 Jan 2025 19:31:28 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbed2b37b3a36511a8f8cde15ac74df12676c707a75cac7400604b533817a57b`  
		Last Modified: Tue, 21 Jan 2025 19:31:28 GMT  
		Size: 7.9 KB (7918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2bb56ba626edfb899d02de6e190e018998d7573a673f6db87d5ef30de0a050`  
		Last Modified: Tue, 28 Jan 2025 01:43:33 GMT  
		Size: 112.6 KB (112648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e93d7242196ad9ca14b560ce78c345dfa536c1a35de8044919beffdf4eb97a`  
		Last Modified: Tue, 28 Jan 2025 01:43:33 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9e06feef4b6941cffa38f96ec7bf4e23040ea0baf7cf6f0a7345c46675eff3`  
		Last Modified: Tue, 28 Jan 2025 01:43:33 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:02029f95376d43c51ccddf3f8c8bbebb0671c8774aacfa19d44aee40f4773161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4efe04e204e62e8c95b99341d61fcd033d068bcbce5868ae0ec1685e9f9da3e`

```dockerfile
```

-	Layers:
	-	`sha256:f198a76291582efc4f722539762e32a43b96a2acfb2de57f18adfa903c9b3c57`  
		Last Modified: Tue, 28 Jan 2025 01:43:33 GMT  
		Size: 77.9 KB (77899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c32d956ebf079b702220519e8a308783736857197d7766e995bfbcd8c71dbf2c`  
		Last Modified: Tue, 28 Jan 2025 01:43:33 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:756e00d72198e903bfd6356e80496c2936c64fa26149b3662c09c044393ac715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3458360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef3b076b4ea8c2964765a22bf8c5d8b2fb8141f171e1f335b628572524c3ab7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Wed, 08 Jan 2025 17:48:43 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410676c340782e10ad961429d12c4fc7bc22fe42e602f44af8fe4564583fa790`  
		Last Modified: Tue, 21 Jan 2025 19:47:10 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb03e5e951a5c0dc5098e3f3712ba683716c2830cd781627b8c589f37e35d49e`  
		Last Modified: Tue, 21 Jan 2025 19:47:10 GMT  
		Size: 7.9 KB (7900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d4da436692d4ab0fd5035ee54eac03b05bf24df9aa3304a4cbb3e6bb7fb7de`  
		Last Modified: Tue, 28 Jan 2025 02:22:45 GMT  
		Size: 98.8 KB (98808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b11f3813ff058c0963785dcdc5c5f860f00840874673c02d724b273f844d53c`  
		Last Modified: Tue, 28 Jan 2025 02:22:45 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d897b6a73cbb856ebfd058f311b8f0e39512fdede0d33460f38db93bb89b6c`  
		Last Modified: Tue, 28 Jan 2025 02:22:45 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:877a9cd3fe26f402674032844c26b7149200267a47a431963b72e3b4563d519c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b37c1a9028694f866e7acc219fbf431ce5b97965a6f5489a14f064c84a12b1`

```dockerfile
```

-	Layers:
	-	`sha256:40546cca6e89cde845ebe9184ed940f3b4f38ba1e18049e3b36b047821e42722`  
		Last Modified: Tue, 28 Jan 2025 02:22:45 GMT  
		Size: 77.9 KB (77895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12a0377ea7376b0115517894b6c6f3d26482dcf699f270a21454fd463c994114`  
		Last Modified: Tue, 28 Jan 2025 02:22:45 GMT  
		Size: 14.3 KB (14347 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; s390x

```console
$ docker pull spiped@sha256:496d1116424a4c78bad3fdd46c2db89305089a904ff0d42fcd07ffca4576a0b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32ae085c92ecf8421e7f161ab96951c317b5e771993504a3e09c8db10414930`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2d0ea9a1061fe840c13a046b93faaeb9dbcf4357f53a37b83747a395c05279`  
		Last Modified: Tue, 21 Jan 2025 19:32:37 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068b14e90f05cd3c9537d5988b4bbe6abead4cac15a8b25d1959964036cdbb13`  
		Last Modified: Tue, 21 Jan 2025 19:32:37 GMT  
		Size: 7.9 KB (7909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3398f6409117bd2a57c6b304f740badcea613c5def606a7c072bcd0c73b061e0`  
		Last Modified: Tue, 28 Jan 2025 01:57:36 GMT  
		Size: 96.9 KB (96911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32ed7682792c020e13d8b547fdbb8c43a4956cb69969b8f5a2724202bbcb39d`  
		Last Modified: Tue, 28 Jan 2025 01:57:37 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff53239a6486b270ef8a57e32718cefe901786526573b780eb054d1ac053dc6e`  
		Last Modified: Tue, 28 Jan 2025 01:57:37 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:d66b26cdcd77f8b4437bcb47a340f63d583e754a794e2a822931eafa72152360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6cdd7bbb43e56276987d1ae0048a6f92a4bca0ccdee9e8e670ddb9ea5e16cb9`

```dockerfile
```

-	Layers:
	-	`sha256:6fe581f275230ca3b53c4a9c2f8f4690c4edf45359ead5089d277953f8872d2a`  
		Last Modified: Tue, 28 Jan 2025 01:57:36 GMT  
		Size: 77.9 KB (77865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0280df9fd96cadb1c6e05a657e4d4caa094e820e2a85ddd2df85b36c0363d18`  
		Last Modified: Tue, 28 Jan 2025 01:57:36 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:latest`

```console
$ docker pull spiped@sha256:8f77956d848c5f3eb11bee20026e0d9a843af8a30b2c0310b669c658468127e3
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
$ docker pull spiped@sha256:536ab474df09e03eac6134fbad4dd27c18a9135fbd86911f2ea7ad690cd04c33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37097837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61f9190e48c091c3f1a4bb917ae20281a709f4394fe1e013004350789b909d3d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297bb720785ed556393334ee818634585f1264385e1193c7cb9a6c139bc65e14`  
		Last Modified: Tue, 28 Jan 2025 01:28:12 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf32c2751d5f872e24f5ed59e217dfd7f84f720367f3076380ff4715073f8266`  
		Last Modified: Tue, 28 Jan 2025 01:28:12 GMT  
		Size: 2.4 MB (2401375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52ec02d46ad29a364ad7f54bb7579493738fab77fe07703d1e53490f14ada4d`  
		Last Modified: Tue, 28 Jan 2025 01:28:12 GMT  
		Size: 6.5 MB (6482502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e904725dea08f9faf2a31328c10f1398468e995b0d27eadb03ed85a22210d22`  
		Last Modified: Tue, 28 Jan 2025 01:28:12 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60b6b0ce2ec5b5eba3960efaa100171ec619e02ea4145fe1925f0376dafadbc`  
		Last Modified: Tue, 28 Jan 2025 01:28:12 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:8a092ebcd3079b2fbc9871bcd444705cac06810db040b4d55c3479865935afcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3530854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f58c8d654972c43b6abb062eb1922573a9f104695000577382138c422a961791`

```dockerfile
```

-	Layers:
	-	`sha256:68928954d7e34be1617a4df1c97a0aab4efc8c72ae02be92a38358bb07437fec`  
		Last Modified: Tue, 28 Jan 2025 01:28:12 GMT  
		Size: 3.5 MB (3515814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8da9ca933cbc0022cfb2d34616b0a64c0d373dd8393666ef7c6e9adc16a5e722`  
		Last Modified: Tue, 28 Jan 2025 01:28:12 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v5

```console
$ docker pull spiped@sha256:0e5c7e178a60719668836afaff3ff67125afee9e3d03accd4401cab3bf3aea23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32882141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d77ac67695453c5d4fc89a848dee8a8392d8bc72b52ea81b468257f78768ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1736726400'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7a3fc1134bc1af98e13c0b7ea743c863d5a17f830a5fbd5a7002f750500e76c2`  
		Last Modified: Tue, 14 Jan 2025 01:33:27 GMT  
		Size: 25.7 MB (25736665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d02c24549d50cc08f67dd0716935f9fa89992a0a0c1150357bba3bd55a0c1e7`  
		Last Modified: Tue, 14 Jan 2025 06:07:49 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3c5e73b2f407694f10795c56fde8bcb539c9e2933731585f42dca1b1ace55f`  
		Last Modified: Tue, 14 Jan 2025 06:07:49 GMT  
		Size: 2.0 MB (1997177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e30adfe160215d6c7902f37ebf94ac563be9c6fccb4a395277b1aa3818607b7`  
		Last Modified: Tue, 28 Jan 2025 01:31:03 GMT  
		Size: 5.1 MB (5146757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27aac59a43177421679bd0226f35aab3ba9fa205c1b5d6c67dafa249b4e83cfd`  
		Last Modified: Tue, 28 Jan 2025 01:31:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9448be81708fcc8741ac6f43584de6ba475c3536046bde4f7c2191a0870c19b`  
		Last Modified: Tue, 28 Jan 2025 01:31:03 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:23079fe3fffca7762fa71b01d0411f8384596126fe153c023b09dc5660eeaf82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3501486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eeb887a5a783665797ba8dc1fdd892d0261c16063f2c97462d2de3fcb591a5e`

```dockerfile
```

-	Layers:
	-	`sha256:22e1c45058e14bd513fd59735994785f69dca0da45c2043c929cd60ab6ee6712`  
		Last Modified: Tue, 28 Jan 2025 01:31:03 GMT  
		Size: 3.5 MB (3486344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b83aa6e8691e60672de940db65cf58f8168cc03800c9df896f0392230faef68d`  
		Last Modified: Tue, 28 Jan 2025 01:31:03 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v7

```console
$ docker pull spiped@sha256:ccbdcef0387e5cc6e9d060a7cb6251eab74ea58109617ddfb00ae7dfbadec466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 MB (30659580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:531150a8da7eb7ecbbdd6e1044330fae803c4f7a5e6fd062da86e8c1d4b96829`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 01:35:15 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f82d2a6f73f55cbf1d37fd27277b02bccaab05b4f4566fba3f60d3414b02ee`  
		Last Modified: Tue, 28 Jan 2025 01:37:09 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbd4fec55999df669ac552c8a8a36d23d8968fc0384aa8e416b1c891eaf20ae`  
		Last Modified: Tue, 28 Jan 2025 01:37:10 GMT  
		Size: 1.9 MB (1855576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82cb6e6723fd5a0ef75b0dd184cf799af3ed260e21af13ab1c2e506822b2fa70`  
		Last Modified: Tue, 28 Jan 2025 01:37:10 GMT  
		Size: 4.9 MB (4887862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d26fd234d491740cb625280d39e623f8d839377ffc0b57cb3504d8de911c3a`  
		Last Modified: Tue, 28 Jan 2025 01:37:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901f496578fbc184fc4790a1b4c0bab2352fb6e530beea188e4b0ba08046ce2a`  
		Last Modified: Tue, 28 Jan 2025 01:37:10 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:1033931b8488d45445247954b4346c2ab38a753e8b906a66b9bf16352c819acd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3500977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd5b75d5b44c4854ab926811600353150aa50de74119e06dddbb73d084581421`

```dockerfile
```

-	Layers:
	-	`sha256:9fa27b21622f0eccb462ea952ab0228e3f904ac0ba741c3b32b2127f45ef179c`  
		Last Modified: Tue, 28 Jan 2025 01:37:09 GMT  
		Size: 3.5 MB (3485835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53bbd1b214a94134a85adbc419d7fc676232db4a3b9e14631c713a43a5060e11`  
		Last Modified: Tue, 28 Jan 2025 01:37:09 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:f2a66012e502dbb68d83b8806cce2a21cb04c84f8e8095bbc2ce736123fb1c20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35780523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3cecf8e2ff2652a6faf516302f17aaa5e8c690b4d97abc9d701160260cd09df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611fe6e9d63e5acb1e7209441d4b6f53839cdb499ce56c53d0a30b18127308af`  
		Last Modified: Tue, 28 Jan 2025 01:41:01 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92430745938fc1ad04a384084859a1779a798bfb2a43cb5e04624d43cd1c7acb`  
		Last Modified: Tue, 28 Jan 2025 01:41:02 GMT  
		Size: 2.2 MB (2247010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369b9862e0933ebe96fc5bda017bd6683b320f8a4d289e80aeed978512cfd255`  
		Last Modified: Tue, 28 Jan 2025 01:41:02 GMT  
		Size: 5.5 MB (5490939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44aa3faa85b28c389faec240ea702de4afa507e7ae685e53314bbdbdff04e80`  
		Last Modified: Tue, 28 Jan 2025 01:41:02 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0a4dc5911186cef9e82bc70ce35d467f950380c65a8d1b0250e0cc206e281e`  
		Last Modified: Tue, 28 Jan 2025 01:41:02 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:47baf7f47236cf831a26ca76d55a8157b116d3dda5925ce8dbbd41d52567069c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3502215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a52acd09d735182eaae4ccffd45c06b9c79bda50a540013e3d691be3da2f431b`

```dockerfile
```

-	Layers:
	-	`sha256:f37345f4dbabaa7e656ed0a75816887fbcfe4951dd41a63d2740bd6ed26f51db`  
		Last Modified: Tue, 28 Jan 2025 01:41:01 GMT  
		Size: 3.5 MB (3487042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:843f601a405007c9da76c3218d51fb2452dc29660928c0893ae7a93703c06e25`  
		Last Modified: Tue, 28 Jan 2025 01:41:01 GMT  
		Size: 15.2 KB (15173 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; 386

```console
$ docker pull spiped@sha256:98ef029814d34d405160b8cd8774b36e1d4075a55db56c75216503f239694141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37544183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d67702ad5748bfe47a10731422eb415fdfc7806bb9184783f769026d4b749a5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 01:33:46 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:990933e5818dac2477379a6c22c8ff156aac80a847271355d54aa7f84e4047c9`  
		Last Modified: Tue, 28 Jan 2025 01:28:36 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec82207d2d5f8c5aee844ce2e9965b1200e45e37009b0bd27d9c3669dd80982`  
		Last Modified: Tue, 28 Jan 2025 01:28:36 GMT  
		Size: 2.4 MB (2398647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de33615d1d4298ca4d90a730d18b76eeab9221bd569fb9925d296300b3597612`  
		Last Modified: Tue, 28 Jan 2025 01:28:36 GMT  
		Size: 6.0 MB (5956398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f9dbd3c5360bd8b3e00e28ec6bfa6f27a97b4b5be2b628a808617b72108df9`  
		Last Modified: Tue, 28 Jan 2025 01:28:36 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf9571f1b17fff32d6a9adffafb32ad8904d04b3f7156f083697132e0b29725`  
		Last Modified: Tue, 28 Jan 2025 01:28:37 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:15d6e0b7e94089abdc57fd1f30df3fc0de016254b2559e656bd0a497b9f74ab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3524745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f402ca8235399d4eaacdc1a9831b9d0fea4707fb82e628c7b5e5b32eada091cd`

```dockerfile
```

-	Layers:
	-	`sha256:4f281e15904f5ac0cd9177326f1d676beae6635dd8abbb81371af8c165adc9a9`  
		Last Modified: Tue, 28 Jan 2025 01:28:36 GMT  
		Size: 3.5 MB (3509741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:092229d42c4fa5b9eeb6f986ac672c68620fbb93f0b803f6bc734339f807e88d`  
		Last Modified: Tue, 28 Jan 2025 01:28:36 GMT  
		Size: 15.0 KB (15004 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; mips64le

```console
$ docker pull spiped@sha256:6bf1b2934b50bc37036f47c176307572e04ff3a865286a7cccb291a8c555bf59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36142417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e18f14eeb0958c9f235ad5a0e8476007640d4ed876a873b66b364a4e51c9b9b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1736726400'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b08d7e697b04bda8cef97763765ebbbc16790e22945b5ab31d97d448a15c8650`  
		Last Modified: Tue, 14 Jan 2025 01:38:32 GMT  
		Size: 28.5 MB (28486647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252230c34678f565279955a422dad63275a16eeef208147f154e13e5647df2ed`  
		Last Modified: Tue, 14 Jan 2025 18:08:24 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f980dd5eb6de9195670967164c2a6d21dfc4bd270afc766fc82f7303fcea879a`  
		Last Modified: Tue, 14 Jan 2025 18:08:25 GMT  
		Size: 1.8 MB (1841121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336f4b90f8852da9787d9b302a76c1c166e886091303a5004535e9cb73fd632d`  
		Last Modified: Tue, 28 Jan 2025 01:32:12 GMT  
		Size: 5.8 MB (5813106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5512c8a48481cf94715c1506c2c4e1ff9f6d805efb3b0338118b5689e3c21079`  
		Last Modified: Tue, 28 Jan 2025 01:32:11 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c228f3bd07cbcd06c100e65d713148abb7e018c7025c9b9d6484049c0a2146a9`  
		Last Modified: Tue, 28 Jan 2025 01:32:12 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:249deaaff0d1784a18b6797030367453d08714a64db8712ca45edd7df3073b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbab1862f923b3499782eb1f960684b595f083d0fe2345bd5a6e2c53ae83acd0`

```dockerfile
```

-	Layers:
	-	`sha256:7c6c6f098c793c8847f89582fbc460774fcad941d2a4ed4ded37e75f6dcf7622`  
		Last Modified: Tue, 28 Jan 2025 01:32:11 GMT  
		Size: 14.9 KB (14896 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; ppc64le

```console
$ docker pull spiped@sha256:d18399db45255851ae8ddbad4e7b5c900d55f4e43695efd3981135d67341765b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41069257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d445aa64495f4c7fdb2a32b492a68d159b909988abb7b61737e38b5345a0b8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2904017eed57b6a379aba91f659af48ec8d1305525c46625a955313f2f21e7a9`  
		Last Modified: Tue, 28 Jan 2025 01:42:23 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170c8da9f5a98720edaa9345e098b778f3682abcc6a559d512c35d465ed68eb1`  
		Last Modified: Tue, 28 Jan 2025 01:42:24 GMT  
		Size: 2.6 MB (2582109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf6e585af2ae045254fc980b05067c3829832933e9228997d7b38860b66ec72`  
		Last Modified: Tue, 28 Jan 2025 01:42:24 GMT  
		Size: 6.4 MB (6440760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839630c4aa5ab3314108a0e90bc3ef41c6d874dbf2195903468542b67df10b19`  
		Last Modified: Tue, 28 Jan 2025 01:42:24 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1bd1225ed7d385f9ccd07a3e86a10eecb6f5aceb0d21253d66059f25cc10f76`  
		Last Modified: Tue, 28 Jan 2025 01:42:24 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:635959fa2681a25dc8179b535939238e6dedf3b4407e4b61c265dcaef89b8b0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3516571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7a5467d6b5e70429f77b5ecc51c24454e72e2a4bec50c2ce6d2c38b6d6ceda`

```dockerfile
```

-	Layers:
	-	`sha256:058f9b63cb6c662558bc2dc672de21d6e7f0b7686ae208b7d53a9ed320429272`  
		Last Modified: Tue, 28 Jan 2025 01:42:24 GMT  
		Size: 3.5 MB (3501483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58bba2fecafbd5b0fec43540d380620c8286e345af289a079b69e2ac6bc4556c`  
		Last Modified: Tue, 28 Jan 2025 01:42:23 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; s390x

```console
$ docker pull spiped@sha256:1360a16741b1d8479ba95a46e1eba44e5a1865a9b32409d5461808606b6b823b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34320664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a19118972ca2e46f28001e2d3152e846d353428043b8bd5449cf0659847072d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9e408aef4b499eef3c5a232610cdb9528eac0555c35a861721e1b66e887bce`  
		Last Modified: Tue, 28 Jan 2025 01:56:55 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9cb1363f3ebb86bcd48ad2dfee1768ef18362d453c9befc1470291d84150aaf`  
		Last Modified: Tue, 28 Jan 2025 01:56:56 GMT  
		Size: 2.1 MB (2068705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca8f083cf8abe1b1441f2edc74b5257b41d3ce228131595d258c42c95bb6074`  
		Last Modified: Tue, 28 Jan 2025 01:56:56 GMT  
		Size: 5.4 MB (5391679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445668117981bb081001c5c8686393d3ea7269a2c19c1a02123c111d4ea71388`  
		Last Modified: Tue, 28 Jan 2025 01:56:56 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b87d689b7d650c827b31ea84b35647df1ba39ce7d24b0700f17a0d97decba3`  
		Last Modified: Tue, 28 Jan 2025 01:56:56 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:d14b17075dae6fdb16fc48d6774f8fcadaa06b728ba5478747afec1ccbcb1614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3519040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d01e321bd685e686da98fa6db440fc0736d29b352be36b6b89c8c977200c6299`

```dockerfile
```

-	Layers:
	-	`sha256:0f886e33ca85512f04d777aad824fda2adcbe9e19a9c3e19518644f51adf168b`  
		Last Modified: Tue, 28 Jan 2025 01:56:56 GMT  
		Size: 3.5 MB (3504000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daa4df4848c5169cbffc9300f9d2ac12ef5ce68655c6423c6432a1533d3d1899`  
		Last Modified: Tue, 28 Jan 2025 01:56:55 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json
