<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rethinkdb`

-	[`rethinkdb:2`](#rethinkdb2)
-	[`rethinkdb:2-bookworm-slim`](#rethinkdb2-bookworm-slim)
-	[`rethinkdb:2.4`](#rethinkdb24)
-	[`rethinkdb:2.4-bookworm-slim`](#rethinkdb24-bookworm-slim)
-	[`rethinkdb:2.4.3`](#rethinkdb243)
-	[`rethinkdb:2.4.4-bookworm-slim`](#rethinkdb244-bookworm-slim)
-	[`rethinkdb:bookworm-slim`](#rethinkdbbookworm-slim)
-	[`rethinkdb:latest`](#rethinkdblatest)

## `rethinkdb:2`

```console
$ docker pull rethinkdb@sha256:b5ae14f8fcade00fd663f4498bc5026013d92c9b475e5182922077904ea7e79b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rethinkdb:2` - linux; amd64

```console
$ docker pull rethinkdb@sha256:3e88eb76a46002eeef88b164faa6214ba58e8796e263ce6748b937d27d4e4cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48021766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bc801ae82e54141c5e4875173e324f836a063d9ed95a78b94a62a1e15e0d1ee`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:05:25 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:05:26 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 08 Dec 2025 23:05:32 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 08 Dec 2025 23:05:32 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:05:32 GMT
VOLUME [/data]
# Mon, 08 Dec 2025 23:05:32 GMT
WORKDIR /data
# Mon, 08 Dec 2025 23:05:32 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 08 Dec 2025 23:05:32 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47deaed609a8c6d85b00259c5f7dafdc88bdf7ca3a7e5ea95f87a64f13342cfb`  
		Last Modified: Mon, 08 Dec 2025 23:05:45 GMT  
		Size: 9.8 MB (9797519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad52a063fe4edf29f56dde456c1c8fd53928e3f02531efde71c5e88fee550167`  
		Last Modified: Mon, 08 Dec 2025 23:05:45 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb9ec48a6a901e1cc82b3ef00ec6c01defee07b8f6f30dae03f9fafea8bb7fc`  
		Last Modified: Mon, 08 Dec 2025 23:05:45 GMT  
		Size: 10.0 MB (9993066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5007ff179ed89f1cc820e8d8ce410165075ce3760d4658105eeb10fa18450c48`  
		Last Modified: Mon, 08 Dec 2025 23:05:44 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:2cb94388e8da0e8b53d424d500a2c724191755ab68a8b6ec629ecc665a4a9b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b54dbc78ae710b1823a479ec4c065c6d34c6ecc7ff2101566ce16c41b5bc69`

```dockerfile
```

-	Layers:
	-	`sha256:411d89595f3becc7f76d0ab220416263d6843d4d2f8f4ef2523862d24ef5da95`  
		Last Modified: Tue, 09 Dec 2025 02:03:36 GMT  
		Size: 2.8 MB (2785036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa6b0d6bffafbb97ccbffe74ede6468d91d9e7f81ec0a68d23f456eadbbd8a8e`  
		Last Modified: Tue, 09 Dec 2025 02:03:37 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:24444aa0e413d3622b70bfeeb479bc6dba87b0f3078e7fe339220085d9f2cc4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47095882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:692b0aac704fba76b25ae9574851b8ee797bf9b877b6a063423d99ca920510f4`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:08:43 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:08:44 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 08 Dec 2025 23:08:50 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 08 Dec 2025 23:08:50 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:08:50 GMT
VOLUME [/data]
# Mon, 08 Dec 2025 23:08:50 GMT
WORKDIR /data
# Mon, 08 Dec 2025 23:08:50 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 08 Dec 2025 23:08:50 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf4a1715e7d3db37bfeaabec581958149da0ec49709d80a9d41e2605ea4e821`  
		Last Modified: Mon, 08 Dec 2025 23:09:04 GMT  
		Size: 9.6 MB (9627944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c4137c8a0abec58765b945616ba5551a63b37dea81f3db392e5d396dbcbbda`  
		Last Modified: Mon, 08 Dec 2025 23:09:03 GMT  
		Size: 2.7 KB (2665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408b28626690e82a6e8e40d5725e9f763d82cdf2b55107387081fcaa324e73eb`  
		Last Modified: Mon, 08 Dec 2025 23:09:09 GMT  
		Size: 9.4 MB (9362951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537b5947282899ce600a99cb69527b004e4fcc38305c2a049b17daee9a7f3380`  
		Last Modified: Mon, 08 Dec 2025 23:09:03 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:4e48908aef77b1144b67d89f17794eb955539038776a3cfe474b25bd7cf9dcd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa5518716542fa655e35f66634831d100a17e213c18f54db98ccb0f7d68cd59`

```dockerfile
```

-	Layers:
	-	`sha256:38897f13b16c0e987e9bba0072638d4414dd8efe107a4705fa4b4989ccf59304`  
		Last Modified: Tue, 09 Dec 2025 02:03:41 GMT  
		Size: 2.8 MB (2785371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eb9ee873592ccbfeee433924aabc25ee108c72d7c806ec17c97b633456ef409`  
		Last Modified: Tue, 09 Dec 2025 02:03:42 GMT  
		Size: 13.6 KB (13586 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2` - linux; s390x

```console
$ docker pull rethinkdb@sha256:a5662909b26f2d0165fb63b3612172978215afdaeae52ae1f4509443cfd9aa26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45487677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c8978f1ac9cc9cde7ef72628628fec0155e0d1a7796cae5e0b53b8e90ab0e8`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:01:27 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:01:28 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Tue, 18 Nov 2025 04:01:32 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 18 Nov 2025 04:01:32 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:01:32 GMT
VOLUME [/data]
# Tue, 18 Nov 2025 04:01:32 GMT
WORKDIR /data
# Tue, 18 Nov 2025 04:01:32 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 18 Nov 2025 04:01:32 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:9c38e4ef02fd030fdf68385dfbbfcada530597ca5203cf2638356502ae852f19`  
		Last Modified: Tue, 18 Nov 2025 01:11:11 GMT  
		Size: 26.9 MB (26884392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60efc471bf6acd5e67630925eb1db1aea89f52fd848d2040e71bcfb7fb758c0`  
		Last Modified: Tue, 18 Nov 2025 04:01:50 GMT  
		Size: 9.3 MB (9296831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab432923dd79e4f05c80e4b67a294bb6eb3ea59634c3d6e30040e6d6f59f27e`  
		Last Modified: Tue, 18 Nov 2025 04:01:49 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01d544b4b2ac409cbadb766f36aa053de0f213b5ee9f2612c57eb2ec229ca38`  
		Last Modified: Tue, 18 Nov 2025 04:01:50 GMT  
		Size: 9.3 MB (9303695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fce6638cfc1efdfb4b1ee1f956adaa8faa368ab875ae5f8f33491a701707653e`  
		Last Modified: Tue, 18 Nov 2025 04:01:49 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:8b6ffc3e672a0fb42ce24651684c47ad75df3bb754727b38bc59e4591a4fd358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daca7e2d3c6853ff6a1520ac7542a3472b4aa0a00b2bfd87b95ad31d105d81e8`

```dockerfile
```

-	Layers:
	-	`sha256:679dd2be8a4dd02248bc4a2ddadf0e860c1d71be186e539432b25f0fc1ede0c8`  
		Last Modified: Tue, 18 Nov 2025 05:04:30 GMT  
		Size: 2.8 MB (2781238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c342f999628120dac32c9ca5f59b00e340d96b16c43377d919bf2babdd36c1e`  
		Last Modified: Tue, 18 Nov 2025 05:04:30 GMT  
		Size: 13.4 KB (13403 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:2-bookworm-slim`

```console
$ docker pull rethinkdb@sha256:b5ae14f8fcade00fd663f4498bc5026013d92c9b475e5182922077904ea7e79b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rethinkdb:2-bookworm-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:3e88eb76a46002eeef88b164faa6214ba58e8796e263ce6748b937d27d4e4cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48021766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bc801ae82e54141c5e4875173e324f836a063d9ed95a78b94a62a1e15e0d1ee`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:05:25 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:05:26 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 08 Dec 2025 23:05:32 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 08 Dec 2025 23:05:32 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:05:32 GMT
VOLUME [/data]
# Mon, 08 Dec 2025 23:05:32 GMT
WORKDIR /data
# Mon, 08 Dec 2025 23:05:32 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 08 Dec 2025 23:05:32 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47deaed609a8c6d85b00259c5f7dafdc88bdf7ca3a7e5ea95f87a64f13342cfb`  
		Last Modified: Mon, 08 Dec 2025 23:05:45 GMT  
		Size: 9.8 MB (9797519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad52a063fe4edf29f56dde456c1c8fd53928e3f02531efde71c5e88fee550167`  
		Last Modified: Mon, 08 Dec 2025 23:05:45 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb9ec48a6a901e1cc82b3ef00ec6c01defee07b8f6f30dae03f9fafea8bb7fc`  
		Last Modified: Mon, 08 Dec 2025 23:05:45 GMT  
		Size: 10.0 MB (9993066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5007ff179ed89f1cc820e8d8ce410165075ce3760d4658105eeb10fa18450c48`  
		Last Modified: Mon, 08 Dec 2025 23:05:44 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:2cb94388e8da0e8b53d424d500a2c724191755ab68a8b6ec629ecc665a4a9b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b54dbc78ae710b1823a479ec4c065c6d34c6ecc7ff2101566ce16c41b5bc69`

```dockerfile
```

-	Layers:
	-	`sha256:411d89595f3becc7f76d0ab220416263d6843d4d2f8f4ef2523862d24ef5da95`  
		Last Modified: Tue, 09 Dec 2025 02:03:36 GMT  
		Size: 2.8 MB (2785036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa6b0d6bffafbb97ccbffe74ede6468d91d9e7f81ec0a68d23f456eadbbd8a8e`  
		Last Modified: Tue, 09 Dec 2025 02:03:37 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:24444aa0e413d3622b70bfeeb479bc6dba87b0f3078e7fe339220085d9f2cc4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47095882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:692b0aac704fba76b25ae9574851b8ee797bf9b877b6a063423d99ca920510f4`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:08:43 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:08:44 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 08 Dec 2025 23:08:50 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 08 Dec 2025 23:08:50 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:08:50 GMT
VOLUME [/data]
# Mon, 08 Dec 2025 23:08:50 GMT
WORKDIR /data
# Mon, 08 Dec 2025 23:08:50 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 08 Dec 2025 23:08:50 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf4a1715e7d3db37bfeaabec581958149da0ec49709d80a9d41e2605ea4e821`  
		Last Modified: Mon, 08 Dec 2025 23:09:04 GMT  
		Size: 9.6 MB (9627944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c4137c8a0abec58765b945616ba5551a63b37dea81f3db392e5d396dbcbbda`  
		Last Modified: Mon, 08 Dec 2025 23:09:03 GMT  
		Size: 2.7 KB (2665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408b28626690e82a6e8e40d5725e9f763d82cdf2b55107387081fcaa324e73eb`  
		Last Modified: Mon, 08 Dec 2025 23:09:09 GMT  
		Size: 9.4 MB (9362951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537b5947282899ce600a99cb69527b004e4fcc38305c2a049b17daee9a7f3380`  
		Last Modified: Mon, 08 Dec 2025 23:09:03 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:4e48908aef77b1144b67d89f17794eb955539038776a3cfe474b25bd7cf9dcd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa5518716542fa655e35f66634831d100a17e213c18f54db98ccb0f7d68cd59`

```dockerfile
```

-	Layers:
	-	`sha256:38897f13b16c0e987e9bba0072638d4414dd8efe107a4705fa4b4989ccf59304`  
		Last Modified: Tue, 09 Dec 2025 02:03:41 GMT  
		Size: 2.8 MB (2785371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eb9ee873592ccbfeee433924aabc25ee108c72d7c806ec17c97b633456ef409`  
		Last Modified: Tue, 09 Dec 2025 02:03:42 GMT  
		Size: 13.6 KB (13586 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2-bookworm-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:a5662909b26f2d0165fb63b3612172978215afdaeae52ae1f4509443cfd9aa26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45487677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c8978f1ac9cc9cde7ef72628628fec0155e0d1a7796cae5e0b53b8e90ab0e8`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:01:27 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:01:28 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Tue, 18 Nov 2025 04:01:32 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 18 Nov 2025 04:01:32 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:01:32 GMT
VOLUME [/data]
# Tue, 18 Nov 2025 04:01:32 GMT
WORKDIR /data
# Tue, 18 Nov 2025 04:01:32 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 18 Nov 2025 04:01:32 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:9c38e4ef02fd030fdf68385dfbbfcada530597ca5203cf2638356502ae852f19`  
		Last Modified: Tue, 18 Nov 2025 01:11:11 GMT  
		Size: 26.9 MB (26884392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60efc471bf6acd5e67630925eb1db1aea89f52fd848d2040e71bcfb7fb758c0`  
		Last Modified: Tue, 18 Nov 2025 04:01:50 GMT  
		Size: 9.3 MB (9296831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab432923dd79e4f05c80e4b67a294bb6eb3ea59634c3d6e30040e6d6f59f27e`  
		Last Modified: Tue, 18 Nov 2025 04:01:49 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01d544b4b2ac409cbadb766f36aa053de0f213b5ee9f2612c57eb2ec229ca38`  
		Last Modified: Tue, 18 Nov 2025 04:01:50 GMT  
		Size: 9.3 MB (9303695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fce6638cfc1efdfb4b1ee1f956adaa8faa368ab875ae5f8f33491a701707653e`  
		Last Modified: Tue, 18 Nov 2025 04:01:49 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:8b6ffc3e672a0fb42ce24651684c47ad75df3bb754727b38bc59e4591a4fd358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daca7e2d3c6853ff6a1520ac7542a3472b4aa0a00b2bfd87b95ad31d105d81e8`

```dockerfile
```

-	Layers:
	-	`sha256:679dd2be8a4dd02248bc4a2ddadf0e860c1d71be186e539432b25f0fc1ede0c8`  
		Last Modified: Tue, 18 Nov 2025 05:04:30 GMT  
		Size: 2.8 MB (2781238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c342f999628120dac32c9ca5f59b00e340d96b16c43377d919bf2babdd36c1e`  
		Last Modified: Tue, 18 Nov 2025 05:04:30 GMT  
		Size: 13.4 KB (13403 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:2.4`

```console
$ docker pull rethinkdb@sha256:b5ae14f8fcade00fd663f4498bc5026013d92c9b475e5182922077904ea7e79b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rethinkdb:2.4` - linux; amd64

```console
$ docker pull rethinkdb@sha256:3e88eb76a46002eeef88b164faa6214ba58e8796e263ce6748b937d27d4e4cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48021766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bc801ae82e54141c5e4875173e324f836a063d9ed95a78b94a62a1e15e0d1ee`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:05:25 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:05:26 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 08 Dec 2025 23:05:32 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 08 Dec 2025 23:05:32 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:05:32 GMT
VOLUME [/data]
# Mon, 08 Dec 2025 23:05:32 GMT
WORKDIR /data
# Mon, 08 Dec 2025 23:05:32 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 08 Dec 2025 23:05:32 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47deaed609a8c6d85b00259c5f7dafdc88bdf7ca3a7e5ea95f87a64f13342cfb`  
		Last Modified: Mon, 08 Dec 2025 23:05:45 GMT  
		Size: 9.8 MB (9797519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad52a063fe4edf29f56dde456c1c8fd53928e3f02531efde71c5e88fee550167`  
		Last Modified: Mon, 08 Dec 2025 23:05:45 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb9ec48a6a901e1cc82b3ef00ec6c01defee07b8f6f30dae03f9fafea8bb7fc`  
		Last Modified: Mon, 08 Dec 2025 23:05:45 GMT  
		Size: 10.0 MB (9993066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5007ff179ed89f1cc820e8d8ce410165075ce3760d4658105eeb10fa18450c48`  
		Last Modified: Mon, 08 Dec 2025 23:05:44 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:2cb94388e8da0e8b53d424d500a2c724191755ab68a8b6ec629ecc665a4a9b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b54dbc78ae710b1823a479ec4c065c6d34c6ecc7ff2101566ce16c41b5bc69`

```dockerfile
```

-	Layers:
	-	`sha256:411d89595f3becc7f76d0ab220416263d6843d4d2f8f4ef2523862d24ef5da95`  
		Last Modified: Tue, 09 Dec 2025 02:03:36 GMT  
		Size: 2.8 MB (2785036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa6b0d6bffafbb97ccbffe74ede6468d91d9e7f81ec0a68d23f456eadbbd8a8e`  
		Last Modified: Tue, 09 Dec 2025 02:03:37 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:24444aa0e413d3622b70bfeeb479bc6dba87b0f3078e7fe339220085d9f2cc4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47095882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:692b0aac704fba76b25ae9574851b8ee797bf9b877b6a063423d99ca920510f4`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:08:43 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:08:44 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 08 Dec 2025 23:08:50 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 08 Dec 2025 23:08:50 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:08:50 GMT
VOLUME [/data]
# Mon, 08 Dec 2025 23:08:50 GMT
WORKDIR /data
# Mon, 08 Dec 2025 23:08:50 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 08 Dec 2025 23:08:50 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf4a1715e7d3db37bfeaabec581958149da0ec49709d80a9d41e2605ea4e821`  
		Last Modified: Mon, 08 Dec 2025 23:09:04 GMT  
		Size: 9.6 MB (9627944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c4137c8a0abec58765b945616ba5551a63b37dea81f3db392e5d396dbcbbda`  
		Last Modified: Mon, 08 Dec 2025 23:09:03 GMT  
		Size: 2.7 KB (2665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408b28626690e82a6e8e40d5725e9f763d82cdf2b55107387081fcaa324e73eb`  
		Last Modified: Mon, 08 Dec 2025 23:09:09 GMT  
		Size: 9.4 MB (9362951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537b5947282899ce600a99cb69527b004e4fcc38305c2a049b17daee9a7f3380`  
		Last Modified: Mon, 08 Dec 2025 23:09:03 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:4e48908aef77b1144b67d89f17794eb955539038776a3cfe474b25bd7cf9dcd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa5518716542fa655e35f66634831d100a17e213c18f54db98ccb0f7d68cd59`

```dockerfile
```

-	Layers:
	-	`sha256:38897f13b16c0e987e9bba0072638d4414dd8efe107a4705fa4b4989ccf59304`  
		Last Modified: Tue, 09 Dec 2025 02:03:41 GMT  
		Size: 2.8 MB (2785371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eb9ee873592ccbfeee433924aabc25ee108c72d7c806ec17c97b633456ef409`  
		Last Modified: Tue, 09 Dec 2025 02:03:42 GMT  
		Size: 13.6 KB (13586 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4` - linux; s390x

```console
$ docker pull rethinkdb@sha256:a5662909b26f2d0165fb63b3612172978215afdaeae52ae1f4509443cfd9aa26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45487677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c8978f1ac9cc9cde7ef72628628fec0155e0d1a7796cae5e0b53b8e90ab0e8`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:01:27 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:01:28 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Tue, 18 Nov 2025 04:01:32 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 18 Nov 2025 04:01:32 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:01:32 GMT
VOLUME [/data]
# Tue, 18 Nov 2025 04:01:32 GMT
WORKDIR /data
# Tue, 18 Nov 2025 04:01:32 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 18 Nov 2025 04:01:32 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:9c38e4ef02fd030fdf68385dfbbfcada530597ca5203cf2638356502ae852f19`  
		Last Modified: Tue, 18 Nov 2025 01:11:11 GMT  
		Size: 26.9 MB (26884392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60efc471bf6acd5e67630925eb1db1aea89f52fd848d2040e71bcfb7fb758c0`  
		Last Modified: Tue, 18 Nov 2025 04:01:50 GMT  
		Size: 9.3 MB (9296831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab432923dd79e4f05c80e4b67a294bb6eb3ea59634c3d6e30040e6d6f59f27e`  
		Last Modified: Tue, 18 Nov 2025 04:01:49 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01d544b4b2ac409cbadb766f36aa053de0f213b5ee9f2612c57eb2ec229ca38`  
		Last Modified: Tue, 18 Nov 2025 04:01:50 GMT  
		Size: 9.3 MB (9303695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fce6638cfc1efdfb4b1ee1f956adaa8faa368ab875ae5f8f33491a701707653e`  
		Last Modified: Tue, 18 Nov 2025 04:01:49 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:8b6ffc3e672a0fb42ce24651684c47ad75df3bb754727b38bc59e4591a4fd358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daca7e2d3c6853ff6a1520ac7542a3472b4aa0a00b2bfd87b95ad31d105d81e8`

```dockerfile
```

-	Layers:
	-	`sha256:679dd2be8a4dd02248bc4a2ddadf0e860c1d71be186e539432b25f0fc1ede0c8`  
		Last Modified: Tue, 18 Nov 2025 05:04:30 GMT  
		Size: 2.8 MB (2781238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c342f999628120dac32c9ca5f59b00e340d96b16c43377d919bf2babdd36c1e`  
		Last Modified: Tue, 18 Nov 2025 05:04:30 GMT  
		Size: 13.4 KB (13403 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:2.4-bookworm-slim`

```console
$ docker pull rethinkdb@sha256:b5ae14f8fcade00fd663f4498bc5026013d92c9b475e5182922077904ea7e79b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rethinkdb:2.4-bookworm-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:3e88eb76a46002eeef88b164faa6214ba58e8796e263ce6748b937d27d4e4cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48021766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bc801ae82e54141c5e4875173e324f836a063d9ed95a78b94a62a1e15e0d1ee`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:05:25 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:05:26 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 08 Dec 2025 23:05:32 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 08 Dec 2025 23:05:32 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:05:32 GMT
VOLUME [/data]
# Mon, 08 Dec 2025 23:05:32 GMT
WORKDIR /data
# Mon, 08 Dec 2025 23:05:32 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 08 Dec 2025 23:05:32 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47deaed609a8c6d85b00259c5f7dafdc88bdf7ca3a7e5ea95f87a64f13342cfb`  
		Last Modified: Mon, 08 Dec 2025 23:05:45 GMT  
		Size: 9.8 MB (9797519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad52a063fe4edf29f56dde456c1c8fd53928e3f02531efde71c5e88fee550167`  
		Last Modified: Mon, 08 Dec 2025 23:05:45 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb9ec48a6a901e1cc82b3ef00ec6c01defee07b8f6f30dae03f9fafea8bb7fc`  
		Last Modified: Mon, 08 Dec 2025 23:05:45 GMT  
		Size: 10.0 MB (9993066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5007ff179ed89f1cc820e8d8ce410165075ce3760d4658105eeb10fa18450c48`  
		Last Modified: Mon, 08 Dec 2025 23:05:44 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:2cb94388e8da0e8b53d424d500a2c724191755ab68a8b6ec629ecc665a4a9b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b54dbc78ae710b1823a479ec4c065c6d34c6ecc7ff2101566ce16c41b5bc69`

```dockerfile
```

-	Layers:
	-	`sha256:411d89595f3becc7f76d0ab220416263d6843d4d2f8f4ef2523862d24ef5da95`  
		Last Modified: Tue, 09 Dec 2025 02:03:36 GMT  
		Size: 2.8 MB (2785036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa6b0d6bffafbb97ccbffe74ede6468d91d9e7f81ec0a68d23f456eadbbd8a8e`  
		Last Modified: Tue, 09 Dec 2025 02:03:37 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:24444aa0e413d3622b70bfeeb479bc6dba87b0f3078e7fe339220085d9f2cc4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47095882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:692b0aac704fba76b25ae9574851b8ee797bf9b877b6a063423d99ca920510f4`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:08:43 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:08:44 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 08 Dec 2025 23:08:50 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 08 Dec 2025 23:08:50 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:08:50 GMT
VOLUME [/data]
# Mon, 08 Dec 2025 23:08:50 GMT
WORKDIR /data
# Mon, 08 Dec 2025 23:08:50 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 08 Dec 2025 23:08:50 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf4a1715e7d3db37bfeaabec581958149da0ec49709d80a9d41e2605ea4e821`  
		Last Modified: Mon, 08 Dec 2025 23:09:04 GMT  
		Size: 9.6 MB (9627944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c4137c8a0abec58765b945616ba5551a63b37dea81f3db392e5d396dbcbbda`  
		Last Modified: Mon, 08 Dec 2025 23:09:03 GMT  
		Size: 2.7 KB (2665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408b28626690e82a6e8e40d5725e9f763d82cdf2b55107387081fcaa324e73eb`  
		Last Modified: Mon, 08 Dec 2025 23:09:09 GMT  
		Size: 9.4 MB (9362951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537b5947282899ce600a99cb69527b004e4fcc38305c2a049b17daee9a7f3380`  
		Last Modified: Mon, 08 Dec 2025 23:09:03 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:4e48908aef77b1144b67d89f17794eb955539038776a3cfe474b25bd7cf9dcd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa5518716542fa655e35f66634831d100a17e213c18f54db98ccb0f7d68cd59`

```dockerfile
```

-	Layers:
	-	`sha256:38897f13b16c0e987e9bba0072638d4414dd8efe107a4705fa4b4989ccf59304`  
		Last Modified: Tue, 09 Dec 2025 02:03:41 GMT  
		Size: 2.8 MB (2785371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eb9ee873592ccbfeee433924aabc25ee108c72d7c806ec17c97b633456ef409`  
		Last Modified: Tue, 09 Dec 2025 02:03:42 GMT  
		Size: 13.6 KB (13586 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4-bookworm-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:a5662909b26f2d0165fb63b3612172978215afdaeae52ae1f4509443cfd9aa26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45487677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c8978f1ac9cc9cde7ef72628628fec0155e0d1a7796cae5e0b53b8e90ab0e8`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:01:27 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:01:28 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Tue, 18 Nov 2025 04:01:32 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 18 Nov 2025 04:01:32 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:01:32 GMT
VOLUME [/data]
# Tue, 18 Nov 2025 04:01:32 GMT
WORKDIR /data
# Tue, 18 Nov 2025 04:01:32 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 18 Nov 2025 04:01:32 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:9c38e4ef02fd030fdf68385dfbbfcada530597ca5203cf2638356502ae852f19`  
		Last Modified: Tue, 18 Nov 2025 01:11:11 GMT  
		Size: 26.9 MB (26884392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60efc471bf6acd5e67630925eb1db1aea89f52fd848d2040e71bcfb7fb758c0`  
		Last Modified: Tue, 18 Nov 2025 04:01:50 GMT  
		Size: 9.3 MB (9296831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab432923dd79e4f05c80e4b67a294bb6eb3ea59634c3d6e30040e6d6f59f27e`  
		Last Modified: Tue, 18 Nov 2025 04:01:49 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01d544b4b2ac409cbadb766f36aa053de0f213b5ee9f2612c57eb2ec229ca38`  
		Last Modified: Tue, 18 Nov 2025 04:01:50 GMT  
		Size: 9.3 MB (9303695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fce6638cfc1efdfb4b1ee1f956adaa8faa368ab875ae5f8f33491a701707653e`  
		Last Modified: Tue, 18 Nov 2025 04:01:49 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:8b6ffc3e672a0fb42ce24651684c47ad75df3bb754727b38bc59e4591a4fd358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daca7e2d3c6853ff6a1520ac7542a3472b4aa0a00b2bfd87b95ad31d105d81e8`

```dockerfile
```

-	Layers:
	-	`sha256:679dd2be8a4dd02248bc4a2ddadf0e860c1d71be186e539432b25f0fc1ede0c8`  
		Last Modified: Tue, 18 Nov 2025 05:04:30 GMT  
		Size: 2.8 MB (2781238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c342f999628120dac32c9ca5f59b00e340d96b16c43377d919bf2babdd36c1e`  
		Last Modified: Tue, 18 Nov 2025 05:04:30 GMT  
		Size: 13.4 KB (13403 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:2.4.3`

```console
$ docker pull rethinkdb@sha256:b5ae14f8fcade00fd663f4498bc5026013d92c9b475e5182922077904ea7e79b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rethinkdb:2.4.3` - linux; amd64

```console
$ docker pull rethinkdb@sha256:3e88eb76a46002eeef88b164faa6214ba58e8796e263ce6748b937d27d4e4cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48021766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bc801ae82e54141c5e4875173e324f836a063d9ed95a78b94a62a1e15e0d1ee`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:05:25 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:05:26 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 08 Dec 2025 23:05:32 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 08 Dec 2025 23:05:32 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:05:32 GMT
VOLUME [/data]
# Mon, 08 Dec 2025 23:05:32 GMT
WORKDIR /data
# Mon, 08 Dec 2025 23:05:32 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 08 Dec 2025 23:05:32 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47deaed609a8c6d85b00259c5f7dafdc88bdf7ca3a7e5ea95f87a64f13342cfb`  
		Last Modified: Mon, 08 Dec 2025 23:05:45 GMT  
		Size: 9.8 MB (9797519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad52a063fe4edf29f56dde456c1c8fd53928e3f02531efde71c5e88fee550167`  
		Last Modified: Mon, 08 Dec 2025 23:05:45 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb9ec48a6a901e1cc82b3ef00ec6c01defee07b8f6f30dae03f9fafea8bb7fc`  
		Last Modified: Mon, 08 Dec 2025 23:05:45 GMT  
		Size: 10.0 MB (9993066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5007ff179ed89f1cc820e8d8ce410165075ce3760d4658105eeb10fa18450c48`  
		Last Modified: Mon, 08 Dec 2025 23:05:44 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.3` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:2cb94388e8da0e8b53d424d500a2c724191755ab68a8b6ec629ecc665a4a9b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b54dbc78ae710b1823a479ec4c065c6d34c6ecc7ff2101566ce16c41b5bc69`

```dockerfile
```

-	Layers:
	-	`sha256:411d89595f3becc7f76d0ab220416263d6843d4d2f8f4ef2523862d24ef5da95`  
		Last Modified: Tue, 09 Dec 2025 02:03:36 GMT  
		Size: 2.8 MB (2785036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa6b0d6bffafbb97ccbffe74ede6468d91d9e7f81ec0a68d23f456eadbbd8a8e`  
		Last Modified: Tue, 09 Dec 2025 02:03:37 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4.3` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:24444aa0e413d3622b70bfeeb479bc6dba87b0f3078e7fe339220085d9f2cc4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47095882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:692b0aac704fba76b25ae9574851b8ee797bf9b877b6a063423d99ca920510f4`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:08:43 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:08:44 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 08 Dec 2025 23:08:50 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 08 Dec 2025 23:08:50 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:08:50 GMT
VOLUME [/data]
# Mon, 08 Dec 2025 23:08:50 GMT
WORKDIR /data
# Mon, 08 Dec 2025 23:08:50 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 08 Dec 2025 23:08:50 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf4a1715e7d3db37bfeaabec581958149da0ec49709d80a9d41e2605ea4e821`  
		Last Modified: Mon, 08 Dec 2025 23:09:04 GMT  
		Size: 9.6 MB (9627944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c4137c8a0abec58765b945616ba5551a63b37dea81f3db392e5d396dbcbbda`  
		Last Modified: Mon, 08 Dec 2025 23:09:03 GMT  
		Size: 2.7 KB (2665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408b28626690e82a6e8e40d5725e9f763d82cdf2b55107387081fcaa324e73eb`  
		Last Modified: Mon, 08 Dec 2025 23:09:09 GMT  
		Size: 9.4 MB (9362951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537b5947282899ce600a99cb69527b004e4fcc38305c2a049b17daee9a7f3380`  
		Last Modified: Mon, 08 Dec 2025 23:09:03 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.3` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:4e48908aef77b1144b67d89f17794eb955539038776a3cfe474b25bd7cf9dcd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa5518716542fa655e35f66634831d100a17e213c18f54db98ccb0f7d68cd59`

```dockerfile
```

-	Layers:
	-	`sha256:38897f13b16c0e987e9bba0072638d4414dd8efe107a4705fa4b4989ccf59304`  
		Last Modified: Tue, 09 Dec 2025 02:03:41 GMT  
		Size: 2.8 MB (2785371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eb9ee873592ccbfeee433924aabc25ee108c72d7c806ec17c97b633456ef409`  
		Last Modified: Tue, 09 Dec 2025 02:03:42 GMT  
		Size: 13.6 KB (13586 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4.3` - linux; s390x

```console
$ docker pull rethinkdb@sha256:a5662909b26f2d0165fb63b3612172978215afdaeae52ae1f4509443cfd9aa26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45487677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c8978f1ac9cc9cde7ef72628628fec0155e0d1a7796cae5e0b53b8e90ab0e8`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:01:27 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:01:28 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Tue, 18 Nov 2025 04:01:32 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 18 Nov 2025 04:01:32 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:01:32 GMT
VOLUME [/data]
# Tue, 18 Nov 2025 04:01:32 GMT
WORKDIR /data
# Tue, 18 Nov 2025 04:01:32 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 18 Nov 2025 04:01:32 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:9c38e4ef02fd030fdf68385dfbbfcada530597ca5203cf2638356502ae852f19`  
		Last Modified: Tue, 18 Nov 2025 01:11:11 GMT  
		Size: 26.9 MB (26884392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60efc471bf6acd5e67630925eb1db1aea89f52fd848d2040e71bcfb7fb758c0`  
		Last Modified: Tue, 18 Nov 2025 04:01:50 GMT  
		Size: 9.3 MB (9296831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab432923dd79e4f05c80e4b67a294bb6eb3ea59634c3d6e30040e6d6f59f27e`  
		Last Modified: Tue, 18 Nov 2025 04:01:49 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01d544b4b2ac409cbadb766f36aa053de0f213b5ee9f2612c57eb2ec229ca38`  
		Last Modified: Tue, 18 Nov 2025 04:01:50 GMT  
		Size: 9.3 MB (9303695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fce6638cfc1efdfb4b1ee1f956adaa8faa368ab875ae5f8f33491a701707653e`  
		Last Modified: Tue, 18 Nov 2025 04:01:49 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.3` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:8b6ffc3e672a0fb42ce24651684c47ad75df3bb754727b38bc59e4591a4fd358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daca7e2d3c6853ff6a1520ac7542a3472b4aa0a00b2bfd87b95ad31d105d81e8`

```dockerfile
```

-	Layers:
	-	`sha256:679dd2be8a4dd02248bc4a2ddadf0e860c1d71be186e539432b25f0fc1ede0c8`  
		Last Modified: Tue, 18 Nov 2025 05:04:30 GMT  
		Size: 2.8 MB (2781238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c342f999628120dac32c9ca5f59b00e340d96b16c43377d919bf2babdd36c1e`  
		Last Modified: Tue, 18 Nov 2025 05:04:30 GMT  
		Size: 13.4 KB (13403 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:2.4.4-bookworm-slim`

```console
$ docker pull rethinkdb@sha256:b5ae14f8fcade00fd663f4498bc5026013d92c9b475e5182922077904ea7e79b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rethinkdb:2.4.4-bookworm-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:3e88eb76a46002eeef88b164faa6214ba58e8796e263ce6748b937d27d4e4cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48021766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bc801ae82e54141c5e4875173e324f836a063d9ed95a78b94a62a1e15e0d1ee`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:05:25 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:05:26 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 08 Dec 2025 23:05:32 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 08 Dec 2025 23:05:32 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:05:32 GMT
VOLUME [/data]
# Mon, 08 Dec 2025 23:05:32 GMT
WORKDIR /data
# Mon, 08 Dec 2025 23:05:32 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 08 Dec 2025 23:05:32 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47deaed609a8c6d85b00259c5f7dafdc88bdf7ca3a7e5ea95f87a64f13342cfb`  
		Last Modified: Mon, 08 Dec 2025 23:05:45 GMT  
		Size: 9.8 MB (9797519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad52a063fe4edf29f56dde456c1c8fd53928e3f02531efde71c5e88fee550167`  
		Last Modified: Mon, 08 Dec 2025 23:05:45 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb9ec48a6a901e1cc82b3ef00ec6c01defee07b8f6f30dae03f9fafea8bb7fc`  
		Last Modified: Mon, 08 Dec 2025 23:05:45 GMT  
		Size: 10.0 MB (9993066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5007ff179ed89f1cc820e8d8ce410165075ce3760d4658105eeb10fa18450c48`  
		Last Modified: Mon, 08 Dec 2025 23:05:44 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:2cb94388e8da0e8b53d424d500a2c724191755ab68a8b6ec629ecc665a4a9b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b54dbc78ae710b1823a479ec4c065c6d34c6ecc7ff2101566ce16c41b5bc69`

```dockerfile
```

-	Layers:
	-	`sha256:411d89595f3becc7f76d0ab220416263d6843d4d2f8f4ef2523862d24ef5da95`  
		Last Modified: Tue, 09 Dec 2025 02:03:36 GMT  
		Size: 2.8 MB (2785036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa6b0d6bffafbb97ccbffe74ede6468d91d9e7f81ec0a68d23f456eadbbd8a8e`  
		Last Modified: Tue, 09 Dec 2025 02:03:37 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4.4-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:24444aa0e413d3622b70bfeeb479bc6dba87b0f3078e7fe339220085d9f2cc4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47095882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:692b0aac704fba76b25ae9574851b8ee797bf9b877b6a063423d99ca920510f4`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:08:43 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:08:44 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 08 Dec 2025 23:08:50 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 08 Dec 2025 23:08:50 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:08:50 GMT
VOLUME [/data]
# Mon, 08 Dec 2025 23:08:50 GMT
WORKDIR /data
# Mon, 08 Dec 2025 23:08:50 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 08 Dec 2025 23:08:50 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf4a1715e7d3db37bfeaabec581958149da0ec49709d80a9d41e2605ea4e821`  
		Last Modified: Mon, 08 Dec 2025 23:09:04 GMT  
		Size: 9.6 MB (9627944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c4137c8a0abec58765b945616ba5551a63b37dea81f3db392e5d396dbcbbda`  
		Last Modified: Mon, 08 Dec 2025 23:09:03 GMT  
		Size: 2.7 KB (2665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408b28626690e82a6e8e40d5725e9f763d82cdf2b55107387081fcaa324e73eb`  
		Last Modified: Mon, 08 Dec 2025 23:09:09 GMT  
		Size: 9.4 MB (9362951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537b5947282899ce600a99cb69527b004e4fcc38305c2a049b17daee9a7f3380`  
		Last Modified: Mon, 08 Dec 2025 23:09:03 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:4e48908aef77b1144b67d89f17794eb955539038776a3cfe474b25bd7cf9dcd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa5518716542fa655e35f66634831d100a17e213c18f54db98ccb0f7d68cd59`

```dockerfile
```

-	Layers:
	-	`sha256:38897f13b16c0e987e9bba0072638d4414dd8efe107a4705fa4b4989ccf59304`  
		Last Modified: Tue, 09 Dec 2025 02:03:41 GMT  
		Size: 2.8 MB (2785371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eb9ee873592ccbfeee433924aabc25ee108c72d7c806ec17c97b633456ef409`  
		Last Modified: Tue, 09 Dec 2025 02:03:42 GMT  
		Size: 13.6 KB (13586 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4.4-bookworm-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:a5662909b26f2d0165fb63b3612172978215afdaeae52ae1f4509443cfd9aa26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45487677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c8978f1ac9cc9cde7ef72628628fec0155e0d1a7796cae5e0b53b8e90ab0e8`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:01:27 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:01:28 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Tue, 18 Nov 2025 04:01:32 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 18 Nov 2025 04:01:32 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:01:32 GMT
VOLUME [/data]
# Tue, 18 Nov 2025 04:01:32 GMT
WORKDIR /data
# Tue, 18 Nov 2025 04:01:32 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 18 Nov 2025 04:01:32 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:9c38e4ef02fd030fdf68385dfbbfcada530597ca5203cf2638356502ae852f19`  
		Last Modified: Tue, 18 Nov 2025 01:11:11 GMT  
		Size: 26.9 MB (26884392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60efc471bf6acd5e67630925eb1db1aea89f52fd848d2040e71bcfb7fb758c0`  
		Last Modified: Tue, 18 Nov 2025 04:01:50 GMT  
		Size: 9.3 MB (9296831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab432923dd79e4f05c80e4b67a294bb6eb3ea59634c3d6e30040e6d6f59f27e`  
		Last Modified: Tue, 18 Nov 2025 04:01:49 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01d544b4b2ac409cbadb766f36aa053de0f213b5ee9f2612c57eb2ec229ca38`  
		Last Modified: Tue, 18 Nov 2025 04:01:50 GMT  
		Size: 9.3 MB (9303695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fce6638cfc1efdfb4b1ee1f956adaa8faa368ab875ae5f8f33491a701707653e`  
		Last Modified: Tue, 18 Nov 2025 04:01:49 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:8b6ffc3e672a0fb42ce24651684c47ad75df3bb754727b38bc59e4591a4fd358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daca7e2d3c6853ff6a1520ac7542a3472b4aa0a00b2bfd87b95ad31d105d81e8`

```dockerfile
```

-	Layers:
	-	`sha256:679dd2be8a4dd02248bc4a2ddadf0e860c1d71be186e539432b25f0fc1ede0c8`  
		Last Modified: Tue, 18 Nov 2025 05:04:30 GMT  
		Size: 2.8 MB (2781238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c342f999628120dac32c9ca5f59b00e340d96b16c43377d919bf2babdd36c1e`  
		Last Modified: Tue, 18 Nov 2025 05:04:30 GMT  
		Size: 13.4 KB (13403 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:bookworm-slim`

```console
$ docker pull rethinkdb@sha256:b5ae14f8fcade00fd663f4498bc5026013d92c9b475e5182922077904ea7e79b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rethinkdb:bookworm-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:3e88eb76a46002eeef88b164faa6214ba58e8796e263ce6748b937d27d4e4cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48021766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bc801ae82e54141c5e4875173e324f836a063d9ed95a78b94a62a1e15e0d1ee`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:05:25 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:05:26 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 08 Dec 2025 23:05:32 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 08 Dec 2025 23:05:32 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:05:32 GMT
VOLUME [/data]
# Mon, 08 Dec 2025 23:05:32 GMT
WORKDIR /data
# Mon, 08 Dec 2025 23:05:32 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 08 Dec 2025 23:05:32 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47deaed609a8c6d85b00259c5f7dafdc88bdf7ca3a7e5ea95f87a64f13342cfb`  
		Last Modified: Mon, 08 Dec 2025 23:05:45 GMT  
		Size: 9.8 MB (9797519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad52a063fe4edf29f56dde456c1c8fd53928e3f02531efde71c5e88fee550167`  
		Last Modified: Mon, 08 Dec 2025 23:05:45 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb9ec48a6a901e1cc82b3ef00ec6c01defee07b8f6f30dae03f9fafea8bb7fc`  
		Last Modified: Mon, 08 Dec 2025 23:05:45 GMT  
		Size: 10.0 MB (9993066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5007ff179ed89f1cc820e8d8ce410165075ce3760d4658105eeb10fa18450c48`  
		Last Modified: Mon, 08 Dec 2025 23:05:44 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:2cb94388e8da0e8b53d424d500a2c724191755ab68a8b6ec629ecc665a4a9b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b54dbc78ae710b1823a479ec4c065c6d34c6ecc7ff2101566ce16c41b5bc69`

```dockerfile
```

-	Layers:
	-	`sha256:411d89595f3becc7f76d0ab220416263d6843d4d2f8f4ef2523862d24ef5da95`  
		Last Modified: Tue, 09 Dec 2025 02:03:36 GMT  
		Size: 2.8 MB (2785036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa6b0d6bffafbb97ccbffe74ede6468d91d9e7f81ec0a68d23f456eadbbd8a8e`  
		Last Modified: Tue, 09 Dec 2025 02:03:37 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:24444aa0e413d3622b70bfeeb479bc6dba87b0f3078e7fe339220085d9f2cc4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47095882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:692b0aac704fba76b25ae9574851b8ee797bf9b877b6a063423d99ca920510f4`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:08:43 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:08:44 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 08 Dec 2025 23:08:50 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 08 Dec 2025 23:08:50 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:08:50 GMT
VOLUME [/data]
# Mon, 08 Dec 2025 23:08:50 GMT
WORKDIR /data
# Mon, 08 Dec 2025 23:08:50 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 08 Dec 2025 23:08:50 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf4a1715e7d3db37bfeaabec581958149da0ec49709d80a9d41e2605ea4e821`  
		Last Modified: Mon, 08 Dec 2025 23:09:04 GMT  
		Size: 9.6 MB (9627944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c4137c8a0abec58765b945616ba5551a63b37dea81f3db392e5d396dbcbbda`  
		Last Modified: Mon, 08 Dec 2025 23:09:03 GMT  
		Size: 2.7 KB (2665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408b28626690e82a6e8e40d5725e9f763d82cdf2b55107387081fcaa324e73eb`  
		Last Modified: Mon, 08 Dec 2025 23:09:09 GMT  
		Size: 9.4 MB (9362951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537b5947282899ce600a99cb69527b004e4fcc38305c2a049b17daee9a7f3380`  
		Last Modified: Mon, 08 Dec 2025 23:09:03 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:4e48908aef77b1144b67d89f17794eb955539038776a3cfe474b25bd7cf9dcd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa5518716542fa655e35f66634831d100a17e213c18f54db98ccb0f7d68cd59`

```dockerfile
```

-	Layers:
	-	`sha256:38897f13b16c0e987e9bba0072638d4414dd8efe107a4705fa4b4989ccf59304`  
		Last Modified: Tue, 09 Dec 2025 02:03:41 GMT  
		Size: 2.8 MB (2785371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eb9ee873592ccbfeee433924aabc25ee108c72d7c806ec17c97b633456ef409`  
		Last Modified: Tue, 09 Dec 2025 02:03:42 GMT  
		Size: 13.6 KB (13586 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:bookworm-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:a5662909b26f2d0165fb63b3612172978215afdaeae52ae1f4509443cfd9aa26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45487677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c8978f1ac9cc9cde7ef72628628fec0155e0d1a7796cae5e0b53b8e90ab0e8`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:01:27 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:01:28 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Tue, 18 Nov 2025 04:01:32 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 18 Nov 2025 04:01:32 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:01:32 GMT
VOLUME [/data]
# Tue, 18 Nov 2025 04:01:32 GMT
WORKDIR /data
# Tue, 18 Nov 2025 04:01:32 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 18 Nov 2025 04:01:32 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:9c38e4ef02fd030fdf68385dfbbfcada530597ca5203cf2638356502ae852f19`  
		Last Modified: Tue, 18 Nov 2025 01:11:11 GMT  
		Size: 26.9 MB (26884392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60efc471bf6acd5e67630925eb1db1aea89f52fd848d2040e71bcfb7fb758c0`  
		Last Modified: Tue, 18 Nov 2025 04:01:50 GMT  
		Size: 9.3 MB (9296831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab432923dd79e4f05c80e4b67a294bb6eb3ea59634c3d6e30040e6d6f59f27e`  
		Last Modified: Tue, 18 Nov 2025 04:01:49 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01d544b4b2ac409cbadb766f36aa053de0f213b5ee9f2612c57eb2ec229ca38`  
		Last Modified: Tue, 18 Nov 2025 04:01:50 GMT  
		Size: 9.3 MB (9303695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fce6638cfc1efdfb4b1ee1f956adaa8faa368ab875ae5f8f33491a701707653e`  
		Last Modified: Tue, 18 Nov 2025 04:01:49 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:8b6ffc3e672a0fb42ce24651684c47ad75df3bb754727b38bc59e4591a4fd358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daca7e2d3c6853ff6a1520ac7542a3472b4aa0a00b2bfd87b95ad31d105d81e8`

```dockerfile
```

-	Layers:
	-	`sha256:679dd2be8a4dd02248bc4a2ddadf0e860c1d71be186e539432b25f0fc1ede0c8`  
		Last Modified: Tue, 18 Nov 2025 05:04:30 GMT  
		Size: 2.8 MB (2781238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c342f999628120dac32c9ca5f59b00e340d96b16c43377d919bf2babdd36c1e`  
		Last Modified: Tue, 18 Nov 2025 05:04:30 GMT  
		Size: 13.4 KB (13403 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:latest`

```console
$ docker pull rethinkdb@sha256:b5ae14f8fcade00fd663f4498bc5026013d92c9b475e5182922077904ea7e79b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rethinkdb:latest` - linux; amd64

```console
$ docker pull rethinkdb@sha256:3e88eb76a46002eeef88b164faa6214ba58e8796e263ce6748b937d27d4e4cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48021766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bc801ae82e54141c5e4875173e324f836a063d9ed95a78b94a62a1e15e0d1ee`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:05:25 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:05:26 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 08 Dec 2025 23:05:32 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 08 Dec 2025 23:05:32 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:05:32 GMT
VOLUME [/data]
# Mon, 08 Dec 2025 23:05:32 GMT
WORKDIR /data
# Mon, 08 Dec 2025 23:05:32 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 08 Dec 2025 23:05:32 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47deaed609a8c6d85b00259c5f7dafdc88bdf7ca3a7e5ea95f87a64f13342cfb`  
		Last Modified: Mon, 08 Dec 2025 23:05:45 GMT  
		Size: 9.8 MB (9797519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad52a063fe4edf29f56dde456c1c8fd53928e3f02531efde71c5e88fee550167`  
		Last Modified: Mon, 08 Dec 2025 23:05:45 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb9ec48a6a901e1cc82b3ef00ec6c01defee07b8f6f30dae03f9fafea8bb7fc`  
		Last Modified: Mon, 08 Dec 2025 23:05:45 GMT  
		Size: 10.0 MB (9993066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5007ff179ed89f1cc820e8d8ce410165075ce3760d4658105eeb10fa18450c48`  
		Last Modified: Mon, 08 Dec 2025 23:05:44 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:latest` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:2cb94388e8da0e8b53d424d500a2c724191755ab68a8b6ec629ecc665a4a9b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b54dbc78ae710b1823a479ec4c065c6d34c6ecc7ff2101566ce16c41b5bc69`

```dockerfile
```

-	Layers:
	-	`sha256:411d89595f3becc7f76d0ab220416263d6843d4d2f8f4ef2523862d24ef5da95`  
		Last Modified: Tue, 09 Dec 2025 02:03:36 GMT  
		Size: 2.8 MB (2785036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa6b0d6bffafbb97ccbffe74ede6468d91d9e7f81ec0a68d23f456eadbbd8a8e`  
		Last Modified: Tue, 09 Dec 2025 02:03:37 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:latest` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:24444aa0e413d3622b70bfeeb479bc6dba87b0f3078e7fe339220085d9f2cc4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47095882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:692b0aac704fba76b25ae9574851b8ee797bf9b877b6a063423d99ca920510f4`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:08:43 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:08:44 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 08 Dec 2025 23:08:50 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 08 Dec 2025 23:08:50 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:08:50 GMT
VOLUME [/data]
# Mon, 08 Dec 2025 23:08:50 GMT
WORKDIR /data
# Mon, 08 Dec 2025 23:08:50 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 08 Dec 2025 23:08:50 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf4a1715e7d3db37bfeaabec581958149da0ec49709d80a9d41e2605ea4e821`  
		Last Modified: Mon, 08 Dec 2025 23:09:04 GMT  
		Size: 9.6 MB (9627944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c4137c8a0abec58765b945616ba5551a63b37dea81f3db392e5d396dbcbbda`  
		Last Modified: Mon, 08 Dec 2025 23:09:03 GMT  
		Size: 2.7 KB (2665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408b28626690e82a6e8e40d5725e9f763d82cdf2b55107387081fcaa324e73eb`  
		Last Modified: Mon, 08 Dec 2025 23:09:09 GMT  
		Size: 9.4 MB (9362951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537b5947282899ce600a99cb69527b004e4fcc38305c2a049b17daee9a7f3380`  
		Last Modified: Mon, 08 Dec 2025 23:09:03 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:latest` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:4e48908aef77b1144b67d89f17794eb955539038776a3cfe474b25bd7cf9dcd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa5518716542fa655e35f66634831d100a17e213c18f54db98ccb0f7d68cd59`

```dockerfile
```

-	Layers:
	-	`sha256:38897f13b16c0e987e9bba0072638d4414dd8efe107a4705fa4b4989ccf59304`  
		Last Modified: Tue, 09 Dec 2025 02:03:41 GMT  
		Size: 2.8 MB (2785371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eb9ee873592ccbfeee433924aabc25ee108c72d7c806ec17c97b633456ef409`  
		Last Modified: Tue, 09 Dec 2025 02:03:42 GMT  
		Size: 13.6 KB (13586 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:latest` - linux; s390x

```console
$ docker pull rethinkdb@sha256:a5662909b26f2d0165fb63b3612172978215afdaeae52ae1f4509443cfd9aa26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45487677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c8978f1ac9cc9cde7ef72628628fec0155e0d1a7796cae5e0b53b8e90ab0e8`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:01:27 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:01:28 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Tue, 18 Nov 2025 04:01:32 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 18 Nov 2025 04:01:32 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:01:32 GMT
VOLUME [/data]
# Tue, 18 Nov 2025 04:01:32 GMT
WORKDIR /data
# Tue, 18 Nov 2025 04:01:32 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 18 Nov 2025 04:01:32 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:9c38e4ef02fd030fdf68385dfbbfcada530597ca5203cf2638356502ae852f19`  
		Last Modified: Tue, 18 Nov 2025 01:11:11 GMT  
		Size: 26.9 MB (26884392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60efc471bf6acd5e67630925eb1db1aea89f52fd848d2040e71bcfb7fb758c0`  
		Last Modified: Tue, 18 Nov 2025 04:01:50 GMT  
		Size: 9.3 MB (9296831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab432923dd79e4f05c80e4b67a294bb6eb3ea59634c3d6e30040e6d6f59f27e`  
		Last Modified: Tue, 18 Nov 2025 04:01:49 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01d544b4b2ac409cbadb766f36aa053de0f213b5ee9f2612c57eb2ec229ca38`  
		Last Modified: Tue, 18 Nov 2025 04:01:50 GMT  
		Size: 9.3 MB (9303695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fce6638cfc1efdfb4b1ee1f956adaa8faa368ab875ae5f8f33491a701707653e`  
		Last Modified: Tue, 18 Nov 2025 04:01:49 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:latest` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:8b6ffc3e672a0fb42ce24651684c47ad75df3bb754727b38bc59e4591a4fd358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daca7e2d3c6853ff6a1520ac7542a3472b4aa0a00b2bfd87b95ad31d105d81e8`

```dockerfile
```

-	Layers:
	-	`sha256:679dd2be8a4dd02248bc4a2ddadf0e860c1d71be186e539432b25f0fc1ede0c8`  
		Last Modified: Tue, 18 Nov 2025 05:04:30 GMT  
		Size: 2.8 MB (2781238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c342f999628120dac32c9ca5f59b00e340d96b16c43377d919bf2babdd36c1e`  
		Last Modified: Tue, 18 Nov 2025 05:04:30 GMT  
		Size: 13.4 KB (13403 bytes)  
		MIME: application/vnd.in-toto+json
