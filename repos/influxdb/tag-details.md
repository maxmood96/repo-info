<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `influxdb`

-	[`influxdb:1.11`](#influxdb111)
-	[`influxdb:1.11-alpine`](#influxdb111-alpine)
-	[`influxdb:1.11-data`](#influxdb111-data)
-	[`influxdb:1.11-data-alpine`](#influxdb111-data-alpine)
-	[`influxdb:1.11-meta`](#influxdb111-meta)
-	[`influxdb:1.11-meta-alpine`](#influxdb111-meta-alpine)
-	[`influxdb:1.11.8`](#influxdb1118)
-	[`influxdb:1.11.8-alpine`](#influxdb1118-alpine)
-	[`influxdb:1.11.9-data`](#influxdb1119-data)
-	[`influxdb:1.11.9-data-alpine`](#influxdb1119-data-alpine)
-	[`influxdb:1.11.9-meta`](#influxdb1119-meta)
-	[`influxdb:1.11.9-meta-alpine`](#influxdb1119-meta-alpine)
-	[`influxdb:1.12`](#influxdb112)
-	[`influxdb:1.12-alpine`](#influxdb112-alpine)
-	[`influxdb:1.12-data`](#influxdb112-data)
-	[`influxdb:1.12-data-alpine`](#influxdb112-data-alpine)
-	[`influxdb:1.12-meta`](#influxdb112-meta)
-	[`influxdb:1.12-meta-alpine`](#influxdb112-meta-alpine)
-	[`influxdb:1.12.2`](#influxdb1122)
-	[`influxdb:1.12.2-alpine`](#influxdb1122-alpine)
-	[`influxdb:1.12.2-data`](#influxdb1122-data)
-	[`influxdb:1.12.2-data-alpine`](#influxdb1122-data-alpine)
-	[`influxdb:1.12.2-meta`](#influxdb1122-meta)
-	[`influxdb:1.12.2-meta-alpine`](#influxdb1122-meta-alpine)
-	[`influxdb:2`](#influxdb2)
-	[`influxdb:2-alpine`](#influxdb2-alpine)
-	[`influxdb:2.7`](#influxdb27)
-	[`influxdb:2.7-alpine`](#influxdb27-alpine)
-	[`influxdb:2.7.12`](#influxdb2712)
-	[`influxdb:2.7.12-alpine`](#influxdb2712-alpine)
-	[`influxdb:3-core`](#influxdb3-core)
-	[`influxdb:3-enterprise`](#influxdb3-enterprise)
-	[`influxdb:3.5-core`](#influxdb35-core)
-	[`influxdb:3.5-enterprise`](#influxdb35-enterprise)
-	[`influxdb:3.5.0-core`](#influxdb350-core)
-	[`influxdb:3.5.0-enterprise`](#influxdb350-enterprise)
-	[`influxdb:alpine`](#influxdbalpine)
-	[`influxdb:core`](#influxdbcore)
-	[`influxdb:enterprise`](#influxdbenterprise)
-	[`influxdb:latest`](#influxdblatest)

## `influxdb:1.11`

```console
$ docker pull influxdb@sha256:e189be58ef4193e2c23c1520fb8f15af773a79f5326048b22869d9992359f265
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11` - linux; amd64

```console
$ docker pull influxdb@sha256:a35ad805a07abf6aee2adfc38dfa5cd54e354325c4d47bd08746001fea1aca8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116164496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20910102a28941dd29261f69ff9bbf751fdf959822fd8012f2d2dfa49d28f02b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ARG INFLUXDB_VERSION=1.11.8
# Thu, 25 Sep 2025 13:45:30 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 25 Sep 2025 13:45:30 GMT
VOLUME [/var/lib/influxdb]
# Thu, 25 Sep 2025 13:45:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
USER influxdb
# Thu, 25 Sep 2025 13:45:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Sep 2025 13:45:30 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c6b11972fd12973831818babf60f1ffc1c4047507943d132dffc612884022858`  
		Last Modified: Mon, 29 Sep 2025 23:34:14 GMT  
		Size: 48.5 MB (48480557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3dba6026a3c551d6b8e98308c073fff4fd569fd2fc61f21384cb996da82c9e`  
		Last Modified: Tue, 30 Sep 2025 01:43:53 GMT  
		Size: 24.0 MB (24025876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ad1d614ed574bb8c4130a5acf431d71235af09548e03d21923a42f24de8ea6`  
		Last Modified: Tue, 30 Sep 2025 03:22:05 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb6d0de831560cb1cbc9a1c537901ee0ecbac5ff949d0b7fd49a4854d77ad5e`  
		Last Modified: Tue, 30 Sep 2025 03:22:09 GMT  
		Size: 43.7 MB (43655154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82b6c1c9c6122795bfaecd0e5d187a5fdadc0377e56f1344198023af690feac`  
		Last Modified: Tue, 30 Sep 2025 03:22:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ee8049b7aed544cdf293399e860e0a9f95df0cb9f354a2113921ca23da3b3b`  
		Last Modified: Tue, 30 Sep 2025 03:22:05 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7d749b91fec17b9ee3bf2522632b7a801c87b69714284f5c74499a87986ec8`  
		Last Modified: Tue, 30 Sep 2025 03:22:05 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11` - unknown; unknown

```console
$ docker pull influxdb@sha256:6cdeddaf00c368604c4d9917c76ddec85c3a10718c0c51cb5f9d25f0ac576b08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d5e6d5001262629821d13537e1f5e8bd853e2c678f0e41851ded7094201e5ec`

```dockerfile
```

-	Layers:
	-	`sha256:e9be2da7e3185ff3a26a9e8b7ac583d1c5f4831a98d0ee796426722ac2b898ad`  
		Last Modified: Wed, 01 Oct 2025 14:20:33 GMT  
		Size: 5.1 MB (5078620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6829c60e679d5e2135d1655b415f65c9d28620810b6d5c53b5cacdd703bc0baa`  
		Last Modified: Wed, 01 Oct 2025 14:20:34 GMT  
		Size: 15.5 KB (15529 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:f6483237c2287e488e2bacfc5b9d4f51538e49c548f69225bfe70df7c0b7bf1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113075203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956864e5ca7c01dfb3d3e328edeb3981c7632bc8b75f4044251e9c743e1ac64b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ARG INFLUXDB_VERSION=1.11.8
# Thu, 25 Sep 2025 13:45:30 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 25 Sep 2025 13:45:30 GMT
VOLUME [/var/lib/influxdb]
# Thu, 25 Sep 2025 13:45:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
USER influxdb
# Thu, 25 Sep 2025 13:45:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Sep 2025 13:45:30 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:f7b43f0d0a8b99591b27457b368e70a582002600d32503fd07798c1bee7cd134`  
		Last Modified: Mon, 29 Sep 2025 23:34:16 GMT  
		Size: 48.4 MB (48358915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b261306f7eb1436ff95e3b9d948f5373b0dcf6ca1223aaa4c2fb303b03e744c`  
		Last Modified: Tue, 30 Sep 2025 00:56:21 GMT  
		Size: 23.6 MB (23594734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df9d7fdc095ca39f77a2706425da7fb9c0692bbb99fb4bf7b1d7a66540f1e8c`  
		Last Modified: Tue, 30 Sep 2025 01:19:34 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613e5866479a8a23f2acbac0d444d840a15e562cc964107c1f4a286ded862371`  
		Last Modified: Wed, 01 Oct 2025 11:35:10 GMT  
		Size: 41.1 MB (41118648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3733b4d6307c335d0fed90b2ec5a554b36da5afc284f9ca41566d158bd2aa2`  
		Last Modified: Tue, 30 Sep 2025 02:00:06 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d409747fdb76d7eaf795e79cdf6c0a0bf2ccb6214b67ac3f618c9d30e21ae5`  
		Last Modified: Tue, 30 Sep 2025 02:00:05 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff90e83c0d713e519bc7de776187577b8b81e6166af5466a1b619e5c06b2c7fc`  
		Last Modified: Tue, 30 Sep 2025 02:00:06 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11` - unknown; unknown

```console
$ docker pull influxdb@sha256:df33ed62a28c49e25c31414cfe611594f10428f732ba1067f3456de39c5b8b31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5093709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59915f576bd73a45a5535c8be7b23fdbdb3caf6a1d3538dbaf0bf9b32bf85924`

```dockerfile
```

-	Layers:
	-	`sha256:c11eaa6ca3c33c4d89bdf494fa46795eeb73340fc6805decb40eaa3edde8bfe6`  
		Last Modified: Wed, 01 Oct 2025 11:34:40 GMT  
		Size: 5.1 MB (5078085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d1e03b6a720ee01afd053a0012f8ee0be1c7ed8067c567fe9eef0f229e92ffb`  
		Last Modified: Wed, 01 Oct 2025 11:34:41 GMT  
		Size: 15.6 KB (15624 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-alpine`

```console
$ docker pull influxdb@sha256:f6e4606fea3bf316d3551c7ec7c9f8926a35d8fc38d108c583515b64366e8b0e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:f8e41e81325ff6810bff30223a8dafad74a5d2cc44d8b6fd43456a9d80897498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42910480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31443016c597ac7547f2e481b163ef6d8c5f1a3c1fd7258b498845812aa91376`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 15 Jul 2025 11:31:35 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:31:35 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache       bash       ca-certificates       tzdata &&     update-ca-certificates # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ARG INFLUXDB_VERSION=1.11.8
# Wed, 24 Sep 2025 16:08:46 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN apk add --no-cache --virtual .build-deps       curl       gnupg       tar &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     case "$(apk --print-arch)" in       x86_64)  ARCH=amd64 ;;       aarch64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_TAR=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_TAR}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_TAR}" &&     tar -xf "${INFLUXDB_TAR}" -C /usr/bin       influx       influx_inspect       influxd &&     rm -rf "${INFLUXDB_TAR}"            "${INFLUXDB_ASC}" &&     apk del .build-deps # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
USER influxdb
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3c45e0960f73f468b1c3cca987dfc03c0b750169af93afeb2130cdbf9d757b`  
		Last Modified: Thu, 25 Sep 2025 01:11:54 GMT  
		Size: 1.2 MB (1217687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd607992f18a72767e3fcf98637d34928ab4d49a0c8bd13e1ebb04ee17112a9`  
		Last Modified: Thu, 25 Sep 2025 01:11:56 GMT  
		Size: 38.1 MB (38069600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01393d06d8e58e859d34fc3266d2a2742dd68e8ae5c868ca968f6eb2e62c4d43`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f17e29fc370a24778a2e406b30332b621275ef1e4fc214fbd64b154cafc8e2`  
		Last Modified: Thu, 25 Sep 2025 01:11:54 GMT  
		Size: 1.0 KB (1003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7ad26c6856d0f25616d37fe4c8e7fbc5d48917c02856dd28cc167168ff70aa`  
		Last Modified: Thu, 25 Sep 2025 01:11:54 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eddc754283c9c6c037f9393a8ec9f81afa62a1452c53a8665421116f58a33e4`  
		Last Modified: Thu, 25 Sep 2025 01:11:54 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:d5c5c28a9535e1be2d1e69605f0d5d7b403366a12b02c6ad3d5e0d073f6f8752
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **757.7 KB (757746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c9f157a0e4f2c4f52075be0d5fc326440f5f906af7b762b3ec0101e7b8d0b45`

```dockerfile
```

-	Layers:
	-	`sha256:f4815b044ecf29fae64279ec17eb007044cc6406ab0200468d7a052f845aa5d2`  
		Last Modified: Thu, 25 Sep 2025 02:20:28 GMT  
		Size: 739.9 KB (739869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8989e87c3df574ae8677346c0d7bcd80dc5b06e9a950186f9cf742ff88ea6c97`  
		Last Modified: Thu, 25 Sep 2025 02:20:29 GMT  
		Size: 17.9 KB (17877 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:76c208171d828df5113ba044462bf2933fadb76114351a273eeb8cd5cdb4fd6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40942247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a57d65ac967a56f76b479c24877794c880ecede170f3fe1259774dff1d98b69`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ADD alpine-minirootfs-3.20.8-aarch64.tar.gz / # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN apk add --no-cache       bash       ca-certificates       tzdata &&     update-ca-certificates # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ARG INFLUXDB_VERSION=1.11.8
# Tue, 30 Sep 2025 13:56:01 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN apk add --no-cache --virtual .build-deps       curl       gnupg       tar &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     case "$(apk --print-arch)" in       x86_64)  ARCH=amd64 ;;       aarch64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_TAR=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_TAR}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_TAR}" &&     tar -xf "${INFLUXDB_TAR}" -C /usr/bin       influx       influx_inspect       influxd &&     rm -rf "${INFLUXDB_TAR}"            "${INFLUXDB_ASC}" &&     apk del .build-deps # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
USER influxdb
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c765ae84869fd59a62821873e5413a3e92e36bdc1ced8fab3520334863720a49`  
		Last Modified: Wed, 08 Oct 2025 12:03:09 GMT  
		Size: 4.1 MB (4089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f28be0243b3bb965b6c9b2e07c70b019eb69070fb075e2cc8660b856e4efba`  
		Last Modified: Wed, 08 Oct 2025 21:55:23 GMT  
		Size: 1.3 MB (1304645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f38f6a643f7a256b8eaf81222d2fb2520d2be7423f755c8fa2624e6324abf87`  
		Last Modified: Wed, 08 Oct 2025 21:55:25 GMT  
		Size: 35.5 MB (35545508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbc3962e590201f79eb734b9201590ddc739436a716accc9e14fb795530a3aa`  
		Last Modified: Wed, 08 Oct 2025 21:55:22 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7483ae23f176c3e011cc9c62d96dc29c2b740b7113fe61fb024b8c9201e25f6`  
		Last Modified: Wed, 08 Oct 2025 21:55:22 GMT  
		Size: 1.0 KB (1003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c3334a00d999c2ee2e76dd34dda278c84adead0715ce0da308c6c627e7c6e61`  
		Last Modified: Wed, 08 Oct 2025 21:55:22 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59987b4485557de9f3528ce3b0b97ae5391e16364283ca810e800de91ba5af0`  
		Last Modified: Wed, 08 Oct 2025 21:55:22 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:bad00ca3dd4f80fb8c42eef78284b891a27277bb112cd9a2028841c0fee80707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.7 KB (759696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e822c342492bed1b5c9e1f180e332588366ece7da2b01ca6523ba5d9cbdeaf43`

```dockerfile
```

-	Layers:
	-	`sha256:2bbf5af7d695b365d53f9e9e0967e03275a14f77264f696ccb72a7b0a5d9de27`  
		Last Modified: Wed, 08 Oct 2025 23:20:22 GMT  
		Size: 741.7 KB (741709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30a79558e16dbe151165e5e7ba57ab7f1e7e4b481fd539ff01a4ba11dc4c7e52`  
		Last Modified: Wed, 08 Oct 2025 23:20:23 GMT  
		Size: 18.0 KB (17987 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-data`

```console
$ docker pull influxdb@sha256:24b7b15ae8b2b962562bde6726f98bc75cc34d592e548215c9b65579bd53f105
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data` - linux; amd64

```console
$ docker pull influxdb@sha256:5ca5c032f174ea27fbe34afff041897a33ec1c2ed6ad8216de4c5b6619d933d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114677323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc24f75e9067b20410652a42ed12fefa4e05375de437f672a3fcba9db04269b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Thu, 25 Sep 2025 13:45:30 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 25 Sep 2025 13:45:30 GMT
VOLUME [/var/lib/influxdb]
# Thu, 25 Sep 2025 13:45:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Sep 2025 13:45:30 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c6b11972fd12973831818babf60f1ffc1c4047507943d132dffc612884022858`  
		Last Modified: Mon, 29 Sep 2025 23:34:14 GMT  
		Size: 48.5 MB (48480557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3dba6026a3c551d6b8e98308c073fff4fd569fd2fc61f21384cb996da82c9e`  
		Last Modified: Tue, 30 Sep 2025 01:43:53 GMT  
		Size: 24.0 MB (24025876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd30c831b74310aab770b935e8747d3880dd2b65288e178d7dc11ecab4e53498`  
		Last Modified: Tue, 30 Sep 2025 03:22:05 GMT  
		Size: 3.5 KB (3452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b887499a179326e3aeb2fc66e513a81df91387b500a695d5de0f6ebc9e3fa8`  
		Last Modified: Tue, 30 Sep 2025 03:22:11 GMT  
		Size: 42.2 MB (42165661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:732ae659759b0bb8a8119d0e0140c17694b6d08291ea44dcd39e21de1beb476c`  
		Last Modified: Tue, 30 Sep 2025 03:22:06 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4edfdbec9a508e771793cae14632a548bf4eb74461141a6234763272a42bfe`  
		Last Modified: Tue, 30 Sep 2025 03:22:06 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f376297d31f57a2c81fcc660c49fe074af49f9da9ac723ea7dc03f605f339f2`  
		Last Modified: Tue, 30 Sep 2025 03:22:06 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:ec3cced862cbb091ec7dd3ccbd9436211fe2a57832fd499a990dcaa830346f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4698470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888220618dab1ed1778ed929c7a9c3232cd9ead9490e4d7976ce3556faa72451`

```dockerfile
```

-	Layers:
	-	`sha256:2846b88d218bffbdcf67c3655cc69de885df62685331301457c1c89dbc4e36f5`  
		Last Modified: Wed, 01 Oct 2025 14:20:35 GMT  
		Size: 4.7 MB (4683763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2600774dc47a5015c7320947c89b212a21b6710781e01c0ed11e1bc3136a8578`  
		Last Modified: Wed, 01 Oct 2025 14:20:36 GMT  
		Size: 14.7 KB (14707 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-data-alpine`

```console
$ docker pull influxdb@sha256:79a152f475ff298df71cd58706e1a14bcb5f19ddceb535325e814d75b04237ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:4f85314f22a90ea3da80e052d0563021b63b9d1878cacc97dbf2ab8086be06cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46946036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75ba4ab381dc10fbb06ef5fdb72d1d565d310e23dfbd2171546275268d699a41`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 15 Jul 2025 11:31:35 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:31:35 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Wed, 24 Sep 2025 16:08:46 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d6a3f1ca39ef7aecc1aa054022ad806b14759ae15643a076798d5854f5aa7b`  
		Last Modified: Thu, 25 Sep 2025 01:11:21 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042b4eb3c817da1b0174464d0eec4641de11cd9839ba4c369eaf3d702a601d9a`  
		Last Modified: Thu, 25 Sep 2025 01:11:21 GMT  
		Size: 1.2 MB (1217669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d0ca7f1894f7b6f6ee9006850a32bb1045898d76566fb121d2703918a4c6b1`  
		Last Modified: Thu, 25 Sep 2025 01:11:25 GMT  
		Size: 42.1 MB (42105839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda602257b6c21bf51a77ca06b7ac2c712c884e50b5f5a82c37fe1faaed4f54a`  
		Last Modified: Thu, 25 Sep 2025 01:11:21 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1fd55f793e7a90d65824e5f00da6c010601bb1a43bf3fea8f6d78136cf5ab8f`  
		Last Modified: Thu, 25 Sep 2025 01:11:21 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691072363c753e746abeb7fd61d2dc22cd76ded649696e174fa10d9fc574544f`  
		Last Modified: Thu, 25 Sep 2025 01:11:21 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:d5eed4ec134e6cc48b3b24056166938ad17605a35632e79a2ced9f022509fab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **783.0 KB (783019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d46a8890f173290743b1a53dfddc7f06dec11c893cddf84f3fb34e3bfc1a20`

```dockerfile
```

-	Layers:
	-	`sha256:c23a1a6278a0172f9fc42704b4acd75183eae245c6b7d9b04f0036cbb8f0a40e`  
		Last Modified: Thu, 25 Sep 2025 02:20:41 GMT  
		Size: 766.4 KB (766380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84bb2c5583be579d7b91f838fdd30e3f446ac4870133773d5de119ef0b9dd0c6`  
		Last Modified: Thu, 25 Sep 2025 02:20:41 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-meta`

```console
$ docker pull influxdb@sha256:e87356a965e9476e8c8092a73de78fe7689c58c27a882f90aecfabcfebf5e5e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:62a25d959c84a3d554cc7e79cd0d475b787aba45e489916637fd2305b536a7eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91106558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6162dba0758768863cc61be06cca5f5d06296ad38509c22561178102db11fca2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Thu, 25 Sep 2025 13:45:30 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
EXPOSE map[8091/tcp:{}]
# Thu, 25 Sep 2025 13:45:30 GMT
VOLUME [/var/lib/influxdb]
# Thu, 25 Sep 2025 13:45:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Sep 2025 13:45:30 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:c6b11972fd12973831818babf60f1ffc1c4047507943d132dffc612884022858`  
		Last Modified: Mon, 29 Sep 2025 23:34:14 GMT  
		Size: 48.5 MB (48480557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3dba6026a3c551d6b8e98308c073fff4fd569fd2fc61f21384cb996da82c9e`  
		Last Modified: Tue, 30 Sep 2025 01:43:53 GMT  
		Size: 24.0 MB (24025876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3f3ced2b16472db28602f2de7751a8988da09484804d1307bd0e0bc19b393f`  
		Last Modified: Tue, 30 Sep 2025 03:22:05 GMT  
		Size: 3.4 KB (3442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b8d321f891aa2a7ba027d462a1a05a0a19eb574aceba5b4606f27461ad520f4`  
		Last Modified: Tue, 30 Sep 2025 03:22:07 GMT  
		Size: 18.6 MB (18596113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad9a5a47f05b342351c53f250edd5ae47a16d85df20e24153cecb8ede4cdf2f`  
		Last Modified: Tue, 30 Sep 2025 03:22:05 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2b40c6a0fb2818cbdf4f2e12dafdc91da8fdcf7f16e350de40c0b93c4f891e`  
		Last Modified: Tue, 30 Sep 2025 03:22:05 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:f1880337bbd5816acef1d65f9d7872fb3b74ad450f9c66163a04ef6e1c7afb6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4603673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe8c06979f99d4ee77953cd33221a5d0a460d906aa6e5b8ed46a468a7d9e686`

```dockerfile
```

-	Layers:
	-	`sha256:5800a6293ffe3ce208a597829e3a6c1d8533f5f0c38ef902cd4cc0b0d1b4b414`  
		Last Modified: Wed, 01 Oct 2025 14:20:39 GMT  
		Size: 4.6 MB (4590606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd3ecd92e383fd2222ebc5e7a811e617415b7f3e9e57bbf0f4e10be7078e0afb`  
		Last Modified: Wed, 01 Oct 2025 14:20:39 GMT  
		Size: 13.1 KB (13067 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-meta-alpine`

```console
$ docker pull influxdb@sha256:9a08d01311da9282ba27751a776b405f2a1b98aab7ac04c9cf8dbf1062ca2920
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:30ff364cec9fd19b571f4271d3c53e7d670ca4993f004565a0c9e6818060766f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23388787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e1e71058086d3a3f9e592065e485fddbabca3996c1feae3ea675ceb9240bf68`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 15 Jul 2025 11:31:35 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:31:35 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Wed, 24 Sep 2025 16:08:46 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8091/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a7d34400c8c5dcbbbf7b7cd40818e869dcd03b967ff1fee7bb14e96e138525`  
		Last Modified: Thu, 25 Sep 2025 01:11:26 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fb82d0e29221bab1f6b5d12453c4c63d74d830fbded9a1b182a41fa0d313df`  
		Last Modified: Thu, 25 Sep 2025 01:11:26 GMT  
		Size: 1.2 MB (1217674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15ae145d2a72a7aea82b29f12d68053e6ed0c44ec880b222c896257fce9dc63`  
		Last Modified: Thu, 25 Sep 2025 01:11:26 GMT  
		Size: 18.5 MB (18549791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d72fee249b98bda2b81595a42e765e9d9e8737d6a4191bd1c1f8ce755138364`  
		Last Modified: Thu, 25 Sep 2025 01:11:26 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1607c10bcc9fd15027c82d9ab4a51faa14afcec3bc8a064fd685e7ff7c9a536`  
		Last Modified: Thu, 25 Sep 2025 01:11:26 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:674f3427ed7d18b3caa08ce7e4538561ac8dfe80cf65d02d2fe144e0e76b87fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **689.0 KB (689019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f078f32af95ac7ce888f8d2e179f0dc3413a5cc32ba3eb74c8e7d2cea2531f3d`

```dockerfile
```

-	Layers:
	-	`sha256:9df14aceb0c253e684682fb8eaa7f1c75b4e13ff0d92e0c2dc4bf91d032c7f06`  
		Last Modified: Thu, 25 Sep 2025 02:20:48 GMT  
		Size: 674.0 KB (674009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93a2735de13f578098fc4b19a35562ce3fbad7656d513fb4017422507d78fd31`  
		Last Modified: Thu, 25 Sep 2025 02:20:49 GMT  
		Size: 15.0 KB (15010 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.8`

```console
$ docker pull influxdb@sha256:e189be58ef4193e2c23c1520fb8f15af773a79f5326048b22869d9992359f265
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11.8` - linux; amd64

```console
$ docker pull influxdb@sha256:a35ad805a07abf6aee2adfc38dfa5cd54e354325c4d47bd08746001fea1aca8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116164496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20910102a28941dd29261f69ff9bbf751fdf959822fd8012f2d2dfa49d28f02b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ARG INFLUXDB_VERSION=1.11.8
# Thu, 25 Sep 2025 13:45:30 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 25 Sep 2025 13:45:30 GMT
VOLUME [/var/lib/influxdb]
# Thu, 25 Sep 2025 13:45:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
USER influxdb
# Thu, 25 Sep 2025 13:45:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Sep 2025 13:45:30 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c6b11972fd12973831818babf60f1ffc1c4047507943d132dffc612884022858`  
		Last Modified: Mon, 29 Sep 2025 23:34:14 GMT  
		Size: 48.5 MB (48480557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3dba6026a3c551d6b8e98308c073fff4fd569fd2fc61f21384cb996da82c9e`  
		Last Modified: Tue, 30 Sep 2025 01:43:53 GMT  
		Size: 24.0 MB (24025876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ad1d614ed574bb8c4130a5acf431d71235af09548e03d21923a42f24de8ea6`  
		Last Modified: Tue, 30 Sep 2025 03:22:05 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb6d0de831560cb1cbc9a1c537901ee0ecbac5ff949d0b7fd49a4854d77ad5e`  
		Last Modified: Tue, 30 Sep 2025 03:22:09 GMT  
		Size: 43.7 MB (43655154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82b6c1c9c6122795bfaecd0e5d187a5fdadc0377e56f1344198023af690feac`  
		Last Modified: Tue, 30 Sep 2025 03:22:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ee8049b7aed544cdf293399e860e0a9f95df0cb9f354a2113921ca23da3b3b`  
		Last Modified: Tue, 30 Sep 2025 03:22:05 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7d749b91fec17b9ee3bf2522632b7a801c87b69714284f5c74499a87986ec8`  
		Last Modified: Tue, 30 Sep 2025 03:22:05 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:6cdeddaf00c368604c4d9917c76ddec85c3a10718c0c51cb5f9d25f0ac576b08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d5e6d5001262629821d13537e1f5e8bd853e2c678f0e41851ded7094201e5ec`

```dockerfile
```

-	Layers:
	-	`sha256:e9be2da7e3185ff3a26a9e8b7ac583d1c5f4831a98d0ee796426722ac2b898ad`  
		Last Modified: Wed, 01 Oct 2025 14:20:33 GMT  
		Size: 5.1 MB (5078620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6829c60e679d5e2135d1655b415f65c9d28620810b6d5c53b5cacdd703bc0baa`  
		Last Modified: Wed, 01 Oct 2025 14:20:34 GMT  
		Size: 15.5 KB (15529 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:f6483237c2287e488e2bacfc5b9d4f51538e49c548f69225bfe70df7c0b7bf1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113075203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956864e5ca7c01dfb3d3e328edeb3981c7632bc8b75f4044251e9c743e1ac64b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ARG INFLUXDB_VERSION=1.11.8
# Thu, 25 Sep 2025 13:45:30 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 25 Sep 2025 13:45:30 GMT
VOLUME [/var/lib/influxdb]
# Thu, 25 Sep 2025 13:45:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
USER influxdb
# Thu, 25 Sep 2025 13:45:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Sep 2025 13:45:30 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:f7b43f0d0a8b99591b27457b368e70a582002600d32503fd07798c1bee7cd134`  
		Last Modified: Mon, 29 Sep 2025 23:34:16 GMT  
		Size: 48.4 MB (48358915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b261306f7eb1436ff95e3b9d948f5373b0dcf6ca1223aaa4c2fb303b03e744c`  
		Last Modified: Tue, 30 Sep 2025 00:56:21 GMT  
		Size: 23.6 MB (23594734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df9d7fdc095ca39f77a2706425da7fb9c0692bbb99fb4bf7b1d7a66540f1e8c`  
		Last Modified: Tue, 30 Sep 2025 01:19:34 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613e5866479a8a23f2acbac0d444d840a15e562cc964107c1f4a286ded862371`  
		Last Modified: Wed, 01 Oct 2025 11:35:10 GMT  
		Size: 41.1 MB (41118648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3733b4d6307c335d0fed90b2ec5a554b36da5afc284f9ca41566d158bd2aa2`  
		Last Modified: Tue, 30 Sep 2025 02:00:06 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d409747fdb76d7eaf795e79cdf6c0a0bf2ccb6214b67ac3f618c9d30e21ae5`  
		Last Modified: Tue, 30 Sep 2025 02:00:05 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff90e83c0d713e519bc7de776187577b8b81e6166af5466a1b619e5c06b2c7fc`  
		Last Modified: Tue, 30 Sep 2025 02:00:06 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:df33ed62a28c49e25c31414cfe611594f10428f732ba1067f3456de39c5b8b31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5093709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59915f576bd73a45a5535c8be7b23fdbdb3caf6a1d3538dbaf0bf9b32bf85924`

```dockerfile
```

-	Layers:
	-	`sha256:c11eaa6ca3c33c4d89bdf494fa46795eeb73340fc6805decb40eaa3edde8bfe6`  
		Last Modified: Wed, 01 Oct 2025 11:34:40 GMT  
		Size: 5.1 MB (5078085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d1e03b6a720ee01afd053a0012f8ee0be1c7ed8067c567fe9eef0f229e92ffb`  
		Last Modified: Wed, 01 Oct 2025 11:34:41 GMT  
		Size: 15.6 KB (15624 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.8-alpine`

```console
$ docker pull influxdb@sha256:f6e4606fea3bf316d3551c7ec7c9f8926a35d8fc38d108c583515b64366e8b0e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11.8-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:f8e41e81325ff6810bff30223a8dafad74a5d2cc44d8b6fd43456a9d80897498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42910480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31443016c597ac7547f2e481b163ef6d8c5f1a3c1fd7258b498845812aa91376`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 15 Jul 2025 11:31:35 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:31:35 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache       bash       ca-certificates       tzdata &&     update-ca-certificates # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ARG INFLUXDB_VERSION=1.11.8
# Wed, 24 Sep 2025 16:08:46 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN apk add --no-cache --virtual .build-deps       curl       gnupg       tar &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     case "$(apk --print-arch)" in       x86_64)  ARCH=amd64 ;;       aarch64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_TAR=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_TAR}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_TAR}" &&     tar -xf "${INFLUXDB_TAR}" -C /usr/bin       influx       influx_inspect       influxd &&     rm -rf "${INFLUXDB_TAR}"            "${INFLUXDB_ASC}" &&     apk del .build-deps # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
USER influxdb
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3c45e0960f73f468b1c3cca987dfc03c0b750169af93afeb2130cdbf9d757b`  
		Last Modified: Thu, 25 Sep 2025 01:11:54 GMT  
		Size: 1.2 MB (1217687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd607992f18a72767e3fcf98637d34928ab4d49a0c8bd13e1ebb04ee17112a9`  
		Last Modified: Thu, 25 Sep 2025 01:11:56 GMT  
		Size: 38.1 MB (38069600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01393d06d8e58e859d34fc3266d2a2742dd68e8ae5c868ca968f6eb2e62c4d43`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f17e29fc370a24778a2e406b30332b621275ef1e4fc214fbd64b154cafc8e2`  
		Last Modified: Thu, 25 Sep 2025 01:11:54 GMT  
		Size: 1.0 KB (1003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7ad26c6856d0f25616d37fe4c8e7fbc5d48917c02856dd28cc167168ff70aa`  
		Last Modified: Thu, 25 Sep 2025 01:11:54 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eddc754283c9c6c037f9393a8ec9f81afa62a1452c53a8665421116f58a33e4`  
		Last Modified: Thu, 25 Sep 2025 01:11:54 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:d5c5c28a9535e1be2d1e69605f0d5d7b403366a12b02c6ad3d5e0d073f6f8752
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **757.7 KB (757746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c9f157a0e4f2c4f52075be0d5fc326440f5f906af7b762b3ec0101e7b8d0b45`

```dockerfile
```

-	Layers:
	-	`sha256:f4815b044ecf29fae64279ec17eb007044cc6406ab0200468d7a052f845aa5d2`  
		Last Modified: Thu, 25 Sep 2025 02:20:28 GMT  
		Size: 739.9 KB (739869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8989e87c3df574ae8677346c0d7bcd80dc5b06e9a950186f9cf742ff88ea6c97`  
		Last Modified: Thu, 25 Sep 2025 02:20:29 GMT  
		Size: 17.9 KB (17877 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11.8-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:76c208171d828df5113ba044462bf2933fadb76114351a273eeb8cd5cdb4fd6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40942247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a57d65ac967a56f76b479c24877794c880ecede170f3fe1259774dff1d98b69`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ADD alpine-minirootfs-3.20.8-aarch64.tar.gz / # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN apk add --no-cache       bash       ca-certificates       tzdata &&     update-ca-certificates # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ARG INFLUXDB_VERSION=1.11.8
# Tue, 30 Sep 2025 13:56:01 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN apk add --no-cache --virtual .build-deps       curl       gnupg       tar &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     case "$(apk --print-arch)" in       x86_64)  ARCH=amd64 ;;       aarch64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_TAR=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_TAR}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_TAR}" &&     tar -xf "${INFLUXDB_TAR}" -C /usr/bin       influx       influx_inspect       influxd &&     rm -rf "${INFLUXDB_TAR}"            "${INFLUXDB_ASC}" &&     apk del .build-deps # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
USER influxdb
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c765ae84869fd59a62821873e5413a3e92e36bdc1ced8fab3520334863720a49`  
		Last Modified: Wed, 08 Oct 2025 12:03:09 GMT  
		Size: 4.1 MB (4089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f28be0243b3bb965b6c9b2e07c70b019eb69070fb075e2cc8660b856e4efba`  
		Last Modified: Wed, 08 Oct 2025 21:55:23 GMT  
		Size: 1.3 MB (1304645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f38f6a643f7a256b8eaf81222d2fb2520d2be7423f755c8fa2624e6324abf87`  
		Last Modified: Wed, 08 Oct 2025 21:55:25 GMT  
		Size: 35.5 MB (35545508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbc3962e590201f79eb734b9201590ddc739436a716accc9e14fb795530a3aa`  
		Last Modified: Wed, 08 Oct 2025 21:55:22 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7483ae23f176c3e011cc9c62d96dc29c2b740b7113fe61fb024b8c9201e25f6`  
		Last Modified: Wed, 08 Oct 2025 21:55:22 GMT  
		Size: 1.0 KB (1003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c3334a00d999c2ee2e76dd34dda278c84adead0715ce0da308c6c627e7c6e61`  
		Last Modified: Wed, 08 Oct 2025 21:55:22 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59987b4485557de9f3528ce3b0b97ae5391e16364283ca810e800de91ba5af0`  
		Last Modified: Wed, 08 Oct 2025 21:55:22 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:bad00ca3dd4f80fb8c42eef78284b891a27277bb112cd9a2028841c0fee80707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.7 KB (759696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e822c342492bed1b5c9e1f180e332588366ece7da2b01ca6523ba5d9cbdeaf43`

```dockerfile
```

-	Layers:
	-	`sha256:2bbf5af7d695b365d53f9e9e0967e03275a14f77264f696ccb72a7b0a5d9de27`  
		Last Modified: Wed, 08 Oct 2025 23:20:22 GMT  
		Size: 741.7 KB (741709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30a79558e16dbe151165e5e7ba57ab7f1e7e4b481fd539ff01a4ba11dc4c7e52`  
		Last Modified: Wed, 08 Oct 2025 23:20:23 GMT  
		Size: 18.0 KB (17987 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.9-data`

```console
$ docker pull influxdb@sha256:24b7b15ae8b2b962562bde6726f98bc75cc34d592e548215c9b65579bd53f105
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.9-data` - linux; amd64

```console
$ docker pull influxdb@sha256:5ca5c032f174ea27fbe34afff041897a33ec1c2ed6ad8216de4c5b6619d933d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114677323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc24f75e9067b20410652a42ed12fefa4e05375de437f672a3fcba9db04269b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Thu, 25 Sep 2025 13:45:30 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 25 Sep 2025 13:45:30 GMT
VOLUME [/var/lib/influxdb]
# Thu, 25 Sep 2025 13:45:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Sep 2025 13:45:30 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c6b11972fd12973831818babf60f1ffc1c4047507943d132dffc612884022858`  
		Last Modified: Mon, 29 Sep 2025 23:34:14 GMT  
		Size: 48.5 MB (48480557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3dba6026a3c551d6b8e98308c073fff4fd569fd2fc61f21384cb996da82c9e`  
		Last Modified: Tue, 30 Sep 2025 01:43:53 GMT  
		Size: 24.0 MB (24025876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd30c831b74310aab770b935e8747d3880dd2b65288e178d7dc11ecab4e53498`  
		Last Modified: Tue, 30 Sep 2025 03:22:05 GMT  
		Size: 3.5 KB (3452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b887499a179326e3aeb2fc66e513a81df91387b500a695d5de0f6ebc9e3fa8`  
		Last Modified: Tue, 30 Sep 2025 03:22:11 GMT  
		Size: 42.2 MB (42165661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:732ae659759b0bb8a8119d0e0140c17694b6d08291ea44dcd39e21de1beb476c`  
		Last Modified: Tue, 30 Sep 2025 03:22:06 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4edfdbec9a508e771793cae14632a548bf4eb74461141a6234763272a42bfe`  
		Last Modified: Tue, 30 Sep 2025 03:22:06 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f376297d31f57a2c81fcc660c49fe074af49f9da9ac723ea7dc03f605f339f2`  
		Last Modified: Tue, 30 Sep 2025 03:22:06 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.9-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:ec3cced862cbb091ec7dd3ccbd9436211fe2a57832fd499a990dcaa830346f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4698470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888220618dab1ed1778ed929c7a9c3232cd9ead9490e4d7976ce3556faa72451`

```dockerfile
```

-	Layers:
	-	`sha256:2846b88d218bffbdcf67c3655cc69de885df62685331301457c1c89dbc4e36f5`  
		Last Modified: Wed, 01 Oct 2025 14:20:35 GMT  
		Size: 4.7 MB (4683763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2600774dc47a5015c7320947c89b212a21b6710781e01c0ed11e1bc3136a8578`  
		Last Modified: Wed, 01 Oct 2025 14:20:36 GMT  
		Size: 14.7 KB (14707 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.9-data-alpine`

```console
$ docker pull influxdb@sha256:79a152f475ff298df71cd58706e1a14bcb5f19ddceb535325e814d75b04237ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.9-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:4f85314f22a90ea3da80e052d0563021b63b9d1878cacc97dbf2ab8086be06cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46946036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75ba4ab381dc10fbb06ef5fdb72d1d565d310e23dfbd2171546275268d699a41`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 15 Jul 2025 11:31:35 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:31:35 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Wed, 24 Sep 2025 16:08:46 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d6a3f1ca39ef7aecc1aa054022ad806b14759ae15643a076798d5854f5aa7b`  
		Last Modified: Thu, 25 Sep 2025 01:11:21 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042b4eb3c817da1b0174464d0eec4641de11cd9839ba4c369eaf3d702a601d9a`  
		Last Modified: Thu, 25 Sep 2025 01:11:21 GMT  
		Size: 1.2 MB (1217669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d0ca7f1894f7b6f6ee9006850a32bb1045898d76566fb121d2703918a4c6b1`  
		Last Modified: Thu, 25 Sep 2025 01:11:25 GMT  
		Size: 42.1 MB (42105839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda602257b6c21bf51a77ca06b7ac2c712c884e50b5f5a82c37fe1faaed4f54a`  
		Last Modified: Thu, 25 Sep 2025 01:11:21 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1fd55f793e7a90d65824e5f00da6c010601bb1a43bf3fea8f6d78136cf5ab8f`  
		Last Modified: Thu, 25 Sep 2025 01:11:21 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691072363c753e746abeb7fd61d2dc22cd76ded649696e174fa10d9fc574544f`  
		Last Modified: Thu, 25 Sep 2025 01:11:21 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.9-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:d5eed4ec134e6cc48b3b24056166938ad17605a35632e79a2ced9f022509fab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **783.0 KB (783019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d46a8890f173290743b1a53dfddc7f06dec11c893cddf84f3fb34e3bfc1a20`

```dockerfile
```

-	Layers:
	-	`sha256:c23a1a6278a0172f9fc42704b4acd75183eae245c6b7d9b04f0036cbb8f0a40e`  
		Last Modified: Thu, 25 Sep 2025 02:20:41 GMT  
		Size: 766.4 KB (766380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84bb2c5583be579d7b91f838fdd30e3f446ac4870133773d5de119ef0b9dd0c6`  
		Last Modified: Thu, 25 Sep 2025 02:20:41 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.9-meta`

```console
$ docker pull influxdb@sha256:e87356a965e9476e8c8092a73de78fe7689c58c27a882f90aecfabcfebf5e5e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.9-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:62a25d959c84a3d554cc7e79cd0d475b787aba45e489916637fd2305b536a7eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91106558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6162dba0758768863cc61be06cca5f5d06296ad38509c22561178102db11fca2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Thu, 25 Sep 2025 13:45:30 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
EXPOSE map[8091/tcp:{}]
# Thu, 25 Sep 2025 13:45:30 GMT
VOLUME [/var/lib/influxdb]
# Thu, 25 Sep 2025 13:45:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Sep 2025 13:45:30 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:c6b11972fd12973831818babf60f1ffc1c4047507943d132dffc612884022858`  
		Last Modified: Mon, 29 Sep 2025 23:34:14 GMT  
		Size: 48.5 MB (48480557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3dba6026a3c551d6b8e98308c073fff4fd569fd2fc61f21384cb996da82c9e`  
		Last Modified: Tue, 30 Sep 2025 01:43:53 GMT  
		Size: 24.0 MB (24025876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3f3ced2b16472db28602f2de7751a8988da09484804d1307bd0e0bc19b393f`  
		Last Modified: Tue, 30 Sep 2025 03:22:05 GMT  
		Size: 3.4 KB (3442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b8d321f891aa2a7ba027d462a1a05a0a19eb574aceba5b4606f27461ad520f4`  
		Last Modified: Tue, 30 Sep 2025 03:22:07 GMT  
		Size: 18.6 MB (18596113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad9a5a47f05b342351c53f250edd5ae47a16d85df20e24153cecb8ede4cdf2f`  
		Last Modified: Tue, 30 Sep 2025 03:22:05 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2b40c6a0fb2818cbdf4f2e12dafdc91da8fdcf7f16e350de40c0b93c4f891e`  
		Last Modified: Tue, 30 Sep 2025 03:22:05 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.9-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:f1880337bbd5816acef1d65f9d7872fb3b74ad450f9c66163a04ef6e1c7afb6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4603673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe8c06979f99d4ee77953cd33221a5d0a460d906aa6e5b8ed46a468a7d9e686`

```dockerfile
```

-	Layers:
	-	`sha256:5800a6293ffe3ce208a597829e3a6c1d8533f5f0c38ef902cd4cc0b0d1b4b414`  
		Last Modified: Wed, 01 Oct 2025 14:20:39 GMT  
		Size: 4.6 MB (4590606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd3ecd92e383fd2222ebc5e7a811e617415b7f3e9e57bbf0f4e10be7078e0afb`  
		Last Modified: Wed, 01 Oct 2025 14:20:39 GMT  
		Size: 13.1 KB (13067 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.9-meta-alpine`

```console
$ docker pull influxdb@sha256:9a08d01311da9282ba27751a776b405f2a1b98aab7ac04c9cf8dbf1062ca2920
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.9-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:30ff364cec9fd19b571f4271d3c53e7d670ca4993f004565a0c9e6818060766f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23388787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e1e71058086d3a3f9e592065e485fddbabca3996c1feae3ea675ceb9240bf68`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 15 Jul 2025 11:31:35 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:31:35 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Wed, 24 Sep 2025 16:08:46 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8091/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a7d34400c8c5dcbbbf7b7cd40818e869dcd03b967ff1fee7bb14e96e138525`  
		Last Modified: Thu, 25 Sep 2025 01:11:26 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fb82d0e29221bab1f6b5d12453c4c63d74d830fbded9a1b182a41fa0d313df`  
		Last Modified: Thu, 25 Sep 2025 01:11:26 GMT  
		Size: 1.2 MB (1217674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15ae145d2a72a7aea82b29f12d68053e6ed0c44ec880b222c896257fce9dc63`  
		Last Modified: Thu, 25 Sep 2025 01:11:26 GMT  
		Size: 18.5 MB (18549791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d72fee249b98bda2b81595a42e765e9d9e8737d6a4191bd1c1f8ce755138364`  
		Last Modified: Thu, 25 Sep 2025 01:11:26 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1607c10bcc9fd15027c82d9ab4a51faa14afcec3bc8a064fd685e7ff7c9a536`  
		Last Modified: Thu, 25 Sep 2025 01:11:26 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.9-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:674f3427ed7d18b3caa08ce7e4538561ac8dfe80cf65d02d2fe144e0e76b87fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **689.0 KB (689019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f078f32af95ac7ce888f8d2e179f0dc3413a5cc32ba3eb74c8e7d2cea2531f3d`

```dockerfile
```

-	Layers:
	-	`sha256:9df14aceb0c253e684682fb8eaa7f1c75b4e13ff0d92e0c2dc4bf91d032c7f06`  
		Last Modified: Thu, 25 Sep 2025 02:20:48 GMT  
		Size: 674.0 KB (674009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93a2735de13f578098fc4b19a35562ce3fbad7656d513fb4017422507d78fd31`  
		Last Modified: Thu, 25 Sep 2025 02:20:49 GMT  
		Size: 15.0 KB (15010 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12`

```console
$ docker pull influxdb@sha256:c828208c58c9d5aab4a00e23d2f6070e90186a73a0abf5d2650862dfdcd4d171
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.12` - linux; amd64

```console
$ docker pull influxdb@sha256:bdd397c6ad92ede8322da33be448bd9b4ee352c3dd68803115df04bf8f709b10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.8 MB (113839670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd37fdd950f357c2aad7a517692b739ecec4cbd8464d54b8a6bd3df108153b86`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ARG INFLUXDB_VERSION=1.12.2
# Thu, 25 Sep 2025 13:45:30 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 25 Sep 2025 13:45:30 GMT
VOLUME [/var/lib/influxdb]
# Thu, 25 Sep 2025 13:45:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
USER influxdb
# Thu, 25 Sep 2025 13:45:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Sep 2025 13:45:30 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c6b11972fd12973831818babf60f1ffc1c4047507943d132dffc612884022858`  
		Last Modified: Mon, 29 Sep 2025 23:34:14 GMT  
		Size: 48.5 MB (48480557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3dba6026a3c551d6b8e98308c073fff4fd569fd2fc61f21384cb996da82c9e`  
		Last Modified: Tue, 30 Sep 2025 01:43:53 GMT  
		Size: 24.0 MB (24025876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c451edfd7b3717e4a7d25dc1c5894af74ea28336a6aacdde78a7786dfede7b5a`  
		Last Modified: Tue, 30 Sep 2025 03:21:21 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32e37c1e94e05c00a3ab50f8ebd1b6d704c5d717a27a19f9dc7cf4f240536dc`  
		Last Modified: Tue, 30 Sep 2025 03:21:23 GMT  
		Size: 41.3 MB (41330326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd078c6a1c04be5a01069f14d5229326a819933eda03268b4f7f0b817c868686`  
		Last Modified: Tue, 30 Sep 2025 03:21:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e7bbab3aa9a75a79de439040d42d6c0bc94ea70c38bf914c4e6cad288b05e1`  
		Last Modified: Tue, 30 Sep 2025 03:21:21 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8ec53a3d09ce60e02d8f43046763a25fcab9fc9112b4441cb3ea40602ba195`  
		Last Modified: Tue, 30 Sep 2025 03:21:21 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:32518129dbd5df860b2f46f88eda83c821348a5af09f0ba52195af4f54e888a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4692311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f824013bc50a35ed1d863f28573beb811dcd055ca36a553cd682386dcbcc0b96`

```dockerfile
```

-	Layers:
	-	`sha256:d8f1bbf3fc6e7328034d6bb8d3a179430180ed1ce94f3a130b8067d101827e82`  
		Last Modified: Tue, 30 Sep 2025 20:20:23 GMT  
		Size: 4.7 MB (4675813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a760a533c37a7d6d0a9923560eb3402039153ed4169f10e98906c5962234d5c`  
		Last Modified: Tue, 30 Sep 2025 20:20:24 GMT  
		Size: 16.5 KB (16498 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.12` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:d203572116b61b0c1f1223cb11a2877c54d36b08ac0a0844874fd41bbbd3fcf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110087321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c0c2b1d74c8e43c0f981162600044c62c9b54a4ca39381f86f80f2704e4c3f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ARG INFLUXDB_VERSION=1.12.2
# Thu, 25 Sep 2025 13:45:30 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 25 Sep 2025 13:45:30 GMT
VOLUME [/var/lib/influxdb]
# Thu, 25 Sep 2025 13:45:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
USER influxdb
# Thu, 25 Sep 2025 13:45:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Sep 2025 13:45:30 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:f7b43f0d0a8b99591b27457b368e70a582002600d32503fd07798c1bee7cd134`  
		Last Modified: Mon, 29 Sep 2025 23:34:16 GMT  
		Size: 48.4 MB (48358915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b261306f7eb1436ff95e3b9d948f5373b0dcf6ca1223aaa4c2fb303b03e744c`  
		Last Modified: Tue, 30 Sep 2025 00:56:21 GMT  
		Size: 23.6 MB (23594734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df9d7fdc095ca39f77a2706425da7fb9c0692bbb99fb4bf7b1d7a66540f1e8c`  
		Last Modified: Tue, 30 Sep 2025 01:19:34 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012f4ff43fa54a01187773f7f7f858b4cb4469c7d421e7d80d2e41cc1c5b199e`  
		Last Modified: Tue, 30 Sep 2025 01:19:36 GMT  
		Size: 38.1 MB (38130762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e28b9bea990d64b3eb382e6b0a0e67f2210b5faa77dc02bc1969d48337c339`  
		Last Modified: Tue, 30 Sep 2025 01:19:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c233a9a2d80f823ab02b7445761bcbbb9e93d4399d1b3c27d4af04f8dbe6858`  
		Last Modified: Tue, 30 Sep 2025 01:19:34 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7aa7f00c7e4f8306b389a35abf8efaeeaf5ccf776d9e3f5292fef98676d225`  
		Last Modified: Tue, 30 Sep 2025 01:19:35 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:028240475a243c2596e1385b0bdb09fc5c32b6e36f91a21bd3b7b4328874466f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4691865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97028a1327bea1c7b5d27b5d90f052000a258471bfb7e2b22fcc9ba60406b233`

```dockerfile
```

-	Layers:
	-	`sha256:2aa033cdc539d6b4b68f51321493657fc9503b69468a4a2a38069e9ca8ff2b4e`  
		Last Modified: Wed, 01 Oct 2025 11:34:49 GMT  
		Size: 4.7 MB (4675271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f0c01f239e505063b55ac0580ec8d3f3b119b7904959f7a100452de9e35e215`  
		Last Modified: Wed, 01 Oct 2025 11:34:50 GMT  
		Size: 16.6 KB (16594 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12-alpine`

```console
$ docker pull influxdb@sha256:786d21195cfae2a4e33a2a9f1e090f3c2f6ec16fbce03ff68665e6846072ffae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.12-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:66d2329a46d68b73f4fe44a8ecc2e1a66c470cc0bf686b41d474b82dc4819099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46109705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b598749460a540b8467edfc5d27c9176d36136f5fbf77bdf7998e8cbaaf242b2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache bash ca-certificates tzdata &&     update-ca-certificates # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ARG INFLUXDB_VERSION=1.12.2
# Wed, 24 Sep 2025 16:08:46 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     case "$(apk --print-arch)" in         x86_64)  ARCH=amd64 ;;         aarch64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar -xvf "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz"         -C / --strip-components 1 --wildcards             'influxdb-*/usr/bin/influx'             'influxdb-*/usr/bin/influx_inspect'             'influxdb-*/usr/bin/influxd' &&     rm "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"        "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     apk del .build-deps # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
USER influxdb
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf29fd72ecc1ce907ef679e6691bffbc6e2441190fac83926e70c94cf8d3c33a`  
		Last Modified: Thu, 25 Sep 2025 01:11:17 GMT  
		Size: 1.2 MB (1217859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7298ddb7262ac5ecf38aa23565daab66ab05f51c43a14cf5094e40b4eba6cf7e`  
		Last Modified: Thu, 25 Sep 2025 01:11:28 GMT  
		Size: 41.3 MB (41251563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc6d2c35dfc301a4fc344c4cc21bf0203d7b27545d02a185d3463c8c24eeb0d1`  
		Last Modified: Thu, 25 Sep 2025 01:11:17 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c194518376314b2bd83490bbd01e606f06f23d11d0650ab68d302fbaa00e1b`  
		Last Modified: Thu, 25 Sep 2025 01:11:17 GMT  
		Size: 997.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc9b3690d762b0518bf4a2221226cc44c7680f52ff820f551e0f5ebd8edf34b5`  
		Last Modified: Thu, 25 Sep 2025 01:11:17 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc091ce4196a6f6ef52a63c0824ad8f0f9661d03cfdaff16c8aa50d57dba59d`  
		Last Modified: Thu, 25 Sep 2025 01:11:17 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:199e04d8292a4a75cb8a67a517df3c22c97564ba5d49254ff4db29914ee1f964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **777.9 KB (777909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:238053bdd74f2651b16896d6bfbae7baf7a3fae84043e53a238d989bd8d682e0`

```dockerfile
```

-	Layers:
	-	`sha256:8bd1cb6b6e76e5c1e3b5cb4aef4fa7fd296fe013ec246031ba29d39d510a2cd1`  
		Last Modified: Thu, 25 Sep 2025 02:21:17 GMT  
		Size: 759.2 KB (759246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b0bc5543f212c999f8c987694aead38c4b1205df87986ae131f6bdb3890d500`  
		Last Modified: Thu, 25 Sep 2025 02:21:18 GMT  
		Size: 18.7 KB (18663 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.12-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:5da40eb9360fc4761f3503754e978c35db477788533b175a879b3a062c910c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 MB (43344488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1669f3cf5d1d56aa7ff084652faf747d2bd3c1d4f6f6971b1438c471cc34e74a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN apk add --no-cache bash ca-certificates tzdata &&     update-ca-certificates # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ARG INFLUXDB_VERSION=1.12.2
# Tue, 30 Sep 2025 13:56:01 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     case "$(apk --print-arch)" in         x86_64)  ARCH=amd64 ;;         aarch64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar -xvf "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz"         -C / --strip-components 1 --wildcards             'influxdb-*/usr/bin/influx'             'influxdb-*/usr/bin/influx_inspect'             'influxdb-*/usr/bin/influxd' &&     rm "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"        "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     apk del .build-deps # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
USER influxdb
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3778cd6b7947fa40773e4d96fb04b28656fd002578dc1ba35152916dba4eab3`  
		Last Modified: Wed, 08 Oct 2025 21:55:04 GMT  
		Size: 1.3 MB (1290589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193f43b6c8619cf1483f881f1bdef6dd939ea58e7d495e8416bfda3d15d098c2`  
		Last Modified: Wed, 08 Oct 2025 21:55:08 GMT  
		Size: 38.1 MB (38058839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2a6f8e76e4d9c33472e64d72f702c7962ba0b5e4d61db1c648411752212f71`  
		Last Modified: Wed, 08 Oct 2025 21:55:04 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31e522d0a6aa09c893a40e88167d5532ce096d84694b5970672f058e64bc5d6`  
		Last Modified: Wed, 08 Oct 2025 21:55:04 GMT  
		Size: 990.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf7f3756e6d6b4556e7f0ff09c0a747d1b2defff34996459ba9c9fe8623c697`  
		Last Modified: Wed, 08 Oct 2025 21:55:04 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70fba9b3a8b84fe1ceeacd36df99e6d838298f829348550376de111eaa260c5`  
		Last Modified: Wed, 08 Oct 2025 21:55:04 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:16b60655d76eb0ee04a4cf31a1dbf45f8b8d2645b730d3ed43ad5ddc9b659b99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **779.9 KB (779859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cc24c010c052da3fc8e1ef47a608b08adad9afd5df78f43ec7f7e4052f6c8a1`

```dockerfile
```

-	Layers:
	-	`sha256:191b261bcac32e145613440ef72800622e01c14fb6dc6411b1728ac3dedcb34d`  
		Last Modified: Wed, 08 Oct 2025 23:20:31 GMT  
		Size: 761.1 KB (761088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21ee247e175c8dccb7cd34515f34b1749a76fd37134eef6a64643a3885004fe1`  
		Last Modified: Wed, 08 Oct 2025 23:20:32 GMT  
		Size: 18.8 KB (18771 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12-data`

```console
$ docker pull influxdb@sha256:109feaf76fd2cf70e54168cdbfc480facf6db2fc2645e5ddc937dbb7b458c668
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12-data` - linux; amd64

```console
$ docker pull influxdb@sha256:9716bc051b66dea44fc374cfc57f52c8acf3610fcf6fbdca8bf6cf3f21a1b5cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114823921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b28646598eba4e321fa7c622855bb279c15069b1f41eedd9a53ba1e3a7b74273`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Thu, 25 Sep 2025 13:45:30 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"         "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     rm -r "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"           "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 25 Sep 2025 13:45:30 GMT
VOLUME [/var/lib/influxdb]
# Thu, 25 Sep 2025 13:45:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Sep 2025 13:45:30 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c6b11972fd12973831818babf60f1ffc1c4047507943d132dffc612884022858`  
		Last Modified: Mon, 29 Sep 2025 23:34:14 GMT  
		Size: 48.5 MB (48480557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3dba6026a3c551d6b8e98308c073fff4fd569fd2fc61f21384cb996da82c9e`  
		Last Modified: Tue, 30 Sep 2025 01:43:53 GMT  
		Size: 24.0 MB (24025876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac417f32d2f278f17ff7df41097a319c4e154b701ed78228089121f291e45d5e`  
		Last Modified: Tue, 30 Sep 2025 03:21:27 GMT  
		Size: 42.3 MB (42315711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e40eda6cd42c2f5cb50cdc62fae61e212793bb08fa17014ff9611a36af8c3a`  
		Last Modified: Tue, 30 Sep 2025 03:21:25 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890bb29ee113b4de96d3fa559469c9410f2c6f7b8719857b0743d9ae72483f7b`  
		Last Modified: Tue, 30 Sep 2025 03:21:25 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711b1c5c136c3d606c726224fde1d7487b101aa460a97d38a3f9645b6e2c1cc7`  
		Last Modified: Tue, 30 Sep 2025 03:21:25 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:e9c9d620f5dead4bf73eec799cdc6a86c6d002490854c1f3ebd2d87e305b4a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4699273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0dd541abb76178358003986ee4954d640dd6495a75c27a71cfe942aa6182c36`

```dockerfile
```

-	Layers:
	-	`sha256:ec949e2ab4d50222cea5718aba4b8c221a862bdfc1a0823a66dba606186cda37`  
		Last Modified: Wed, 01 Oct 2025 14:20:48 GMT  
		Size: 4.7 MB (4685451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c2adcb17f8c71ec0be90af8e7e92813819e4b40efb080124fbe3f8c885d881b`  
		Last Modified: Wed, 01 Oct 2025 14:20:48 GMT  
		Size: 13.8 KB (13822 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12-data-alpine`

```console
$ docker pull influxdb@sha256:230248f4122b55660ea2f78e44d60d589b8cf6cb8ab48f5fa11355b2aa3437a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:c6d9a496ea1ac3bfbb8fe7051352b68e5687cbce7cc4ade9e4dc92906d70d3ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47111314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:349217c040d7cb8d5ba819df95857de62d7b8c65fe537e562f9eedab6cd09781`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"         "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     tar -xvf "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz"         -C / --strip-components 1 --wildcards             'influxdb-*/usr/bin/influx'             'influxdb-*/usr/bin/influx_inspect'             'influxdb-*/usr/bin/influxd' &&     rm "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"        "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     apk del .build-deps # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69f86ebefe9dfff24be9ab53cd975a2631738b7447af6789e1dff1ca3b2c27f`  
		Last Modified: Thu, 25 Sep 2025 01:11:17 GMT  
		Size: 1.2 MB (1217842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d614cbfebd68939215609c41e791fa77b4faf9c0184838f6f2e088d147d90b`  
		Last Modified: Thu, 25 Sep 2025 01:11:20 GMT  
		Size: 42.3 MB (42254130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b27779e2d36c38b820659ca7fc3113c1733a2a5525df9062e31317c6e945791`  
		Last Modified: Thu, 25 Sep 2025 01:11:17 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042f205ee4f2c54dd0fab79d5ff8ab7fc2d8b532b3b6bf65e1214a3ba864e2b6`  
		Last Modified: Thu, 25 Sep 2025 01:11:17 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc48483cf9f08acfa785e7133e964bccc86be159a441243a8c2e7bf35f5c5a3`  
		Last Modified: Thu, 25 Sep 2025 01:11:17 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:cae64fd7f9afd9ae2714d996f632407d49177f7187e1ea8f0f0cfcc147b719ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **788.4 KB (788388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffc8318dc7f4dd8e8855ad80626a177cb044360e5746e29e2d607ff65ac2aa6a`

```dockerfile
```

-	Layers:
	-	`sha256:a071aa26d75f72d4bd7f30c81a59364f35b5553a0d5e391470b451a6d0354062`  
		Last Modified: Thu, 25 Sep 2025 02:21:25 GMT  
		Size: 773.2 KB (773197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4e9386bff0d6db73eee18d185455902b386dab3efc2240f66243aa380eba25a`  
		Last Modified: Thu, 25 Sep 2025 02:21:26 GMT  
		Size: 15.2 KB (15191 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12-meta`

```console
$ docker pull influxdb@sha256:eb66706708762ad8262268c2a8dcb4a7070f60a44b6242ecf9c7432e278c6547
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:cb76c71f6494f29ab920bebbf11667a25ff162ad7b691cb1b4dc8355396468c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91285988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec49e8777115ad9902de7591dae24a9ffc6552019edde2952c1b22604fd1b3c2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Thu, 25 Sep 2025 13:45:30 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"         "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     rm -r "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"           "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
EXPOSE map[8091/tcp:{}]
# Thu, 25 Sep 2025 13:45:30 GMT
VOLUME [/var/lib/influxdb]
# Thu, 25 Sep 2025 13:45:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Sep 2025 13:45:30 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:c6b11972fd12973831818babf60f1ffc1c4047507943d132dffc612884022858`  
		Last Modified: Mon, 29 Sep 2025 23:34:14 GMT  
		Size: 48.5 MB (48480557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3dba6026a3c551d6b8e98308c073fff4fd569fd2fc61f21384cb996da82c9e`  
		Last Modified: Tue, 30 Sep 2025 01:43:53 GMT  
		Size: 24.0 MB (24025876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc8cbe523bf49114d5cd00d6b16afb02991fb3218f450080c37b2799b582ede`  
		Last Modified: Tue, 30 Sep 2025 03:21:30 GMT  
		Size: 18.8 MB (18778988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4263e2db74f5a8e2b7b08cb3a1896e83e555ff19fd35da34fac577a38ca31ea7`  
		Last Modified: Tue, 30 Sep 2025 03:21:25 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ba22fecbbbe66d020e5a2f00ab33cac5b99b8941b4bf998a02793e5b927af0`  
		Last Modified: Tue, 30 Sep 2025 03:21:25 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:2ad4245a9408493849ffb1b7b90826247660bfc05142b29d4f6b54b0d5b42f98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4602950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c0f9aa8c13351777e04528b37139359c7d138326f6e8a109137106bea0dd8c2`

```dockerfile
```

-	Layers:
	-	`sha256:0528ec79b7bd6d396d6c5eaa0030b5ba2a83324a92d9302cfb93802c04f1495c`  
		Last Modified: Wed, 01 Oct 2025 14:20:54 GMT  
		Size: 4.6 MB (4590614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be82511432d5e991944abe2ceb44d5ff6d16f3024543b901494cf4ce90f05362`  
		Last Modified: Wed, 01 Oct 2025 14:20:54 GMT  
		Size: 12.3 KB (12336 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12-meta-alpine`

```console
$ docker pull influxdb@sha256:fb1c6ce882c6f76575bf00e884eb6a1cb48f015f6dced8852e0632304e0f5e18
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:438d52e3d15ecb0301ecc4b86a960ee9bc6fce7f38f9d2e372347c8525563ab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23578256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31b60e5178733d55db673306b947c186ea7867ea6067cff2db7b2e658a86d9c2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"         "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     tar -xvf "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz"         -C / --strip-components 1 --wildcards             'influxdb-*/usr/bin/influxd-ctl'             'influxdb-*/usr/bin/influxd-meta' &&     rm "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"        "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     apk del .build-deps # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8091/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f49da720c3a823002c9dc61fb96fe6cbaef56f95b70e83f1717b0cbfe3625c2`  
		Last Modified: Thu, 25 Sep 2025 01:11:07 GMT  
		Size: 1.2 MB (1217796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b26514951c314740b0ec3a65e5c10800f94cd828599759c28c959a27cce08fc`  
		Last Modified: Thu, 25 Sep 2025 01:11:08 GMT  
		Size: 18.7 MB (18722325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a69a5b526bf15a075a5b6a8f416149db75a74b0e83960585a33600795990c9e`  
		Last Modified: Thu, 25 Sep 2025 01:11:07 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcaf0d00f6e38d9ddf873ead6554c87a4c001319e00556ec54da121d35ad3db6`  
		Last Modified: Thu, 25 Sep 2025 01:11:07 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:66c0c255fb30f22da06e4e5eb91e6feab97a584430550d8c5fa3641c6e9adc0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **692.7 KB (692723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c204ee4a35a8f1aa76d61d64fe38ae6354d2b8fc6deff8188661dddd18a645`

```dockerfile
```

-	Layers:
	-	`sha256:b6e4d83eeb239e60792a85b357d7d2758fca1759d804b3b06c1ca78d6b90f827`  
		Last Modified: Thu, 25 Sep 2025 02:21:34 GMT  
		Size: 679.1 KB (679146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d892543fbfacd30d46f77df1c4f2bad94927a6e55b406e2082cebc6a60b88c7d`  
		Last Modified: Thu, 25 Sep 2025 02:21:35 GMT  
		Size: 13.6 KB (13577 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12.2`

```console
$ docker pull influxdb@sha256:c828208c58c9d5aab4a00e23d2f6070e90186a73a0abf5d2650862dfdcd4d171
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.12.2` - linux; amd64

```console
$ docker pull influxdb@sha256:bdd397c6ad92ede8322da33be448bd9b4ee352c3dd68803115df04bf8f709b10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.8 MB (113839670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd37fdd950f357c2aad7a517692b739ecec4cbd8464d54b8a6bd3df108153b86`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ARG INFLUXDB_VERSION=1.12.2
# Thu, 25 Sep 2025 13:45:30 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 25 Sep 2025 13:45:30 GMT
VOLUME [/var/lib/influxdb]
# Thu, 25 Sep 2025 13:45:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
USER influxdb
# Thu, 25 Sep 2025 13:45:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Sep 2025 13:45:30 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c6b11972fd12973831818babf60f1ffc1c4047507943d132dffc612884022858`  
		Last Modified: Mon, 29 Sep 2025 23:34:14 GMT  
		Size: 48.5 MB (48480557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3dba6026a3c551d6b8e98308c073fff4fd569fd2fc61f21384cb996da82c9e`  
		Last Modified: Tue, 30 Sep 2025 01:43:53 GMT  
		Size: 24.0 MB (24025876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c451edfd7b3717e4a7d25dc1c5894af74ea28336a6aacdde78a7786dfede7b5a`  
		Last Modified: Tue, 30 Sep 2025 03:21:21 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32e37c1e94e05c00a3ab50f8ebd1b6d704c5d717a27a19f9dc7cf4f240536dc`  
		Last Modified: Tue, 30 Sep 2025 03:21:23 GMT  
		Size: 41.3 MB (41330326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd078c6a1c04be5a01069f14d5229326a819933eda03268b4f7f0b817c868686`  
		Last Modified: Tue, 30 Sep 2025 03:21:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e7bbab3aa9a75a79de439040d42d6c0bc94ea70c38bf914c4e6cad288b05e1`  
		Last Modified: Tue, 30 Sep 2025 03:21:21 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8ec53a3d09ce60e02d8f43046763a25fcab9fc9112b4441cb3ea40602ba195`  
		Last Modified: Tue, 30 Sep 2025 03:21:21 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2` - unknown; unknown

```console
$ docker pull influxdb@sha256:32518129dbd5df860b2f46f88eda83c821348a5af09f0ba52195af4f54e888a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4692311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f824013bc50a35ed1d863f28573beb811dcd055ca36a553cd682386dcbcc0b96`

```dockerfile
```

-	Layers:
	-	`sha256:d8f1bbf3fc6e7328034d6bb8d3a179430180ed1ce94f3a130b8067d101827e82`  
		Last Modified: Tue, 30 Sep 2025 20:20:23 GMT  
		Size: 4.7 MB (4675813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a760a533c37a7d6d0a9923560eb3402039153ed4169f10e98906c5962234d5c`  
		Last Modified: Tue, 30 Sep 2025 20:20:24 GMT  
		Size: 16.5 KB (16498 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.12.2` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:d203572116b61b0c1f1223cb11a2877c54d36b08ac0a0844874fd41bbbd3fcf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110087321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c0c2b1d74c8e43c0f981162600044c62c9b54a4ca39381f86f80f2704e4c3f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ARG INFLUXDB_VERSION=1.12.2
# Thu, 25 Sep 2025 13:45:30 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 25 Sep 2025 13:45:30 GMT
VOLUME [/var/lib/influxdb]
# Thu, 25 Sep 2025 13:45:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
USER influxdb
# Thu, 25 Sep 2025 13:45:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Sep 2025 13:45:30 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:f7b43f0d0a8b99591b27457b368e70a582002600d32503fd07798c1bee7cd134`  
		Last Modified: Mon, 29 Sep 2025 23:34:16 GMT  
		Size: 48.4 MB (48358915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b261306f7eb1436ff95e3b9d948f5373b0dcf6ca1223aaa4c2fb303b03e744c`  
		Last Modified: Tue, 30 Sep 2025 00:56:21 GMT  
		Size: 23.6 MB (23594734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df9d7fdc095ca39f77a2706425da7fb9c0692bbb99fb4bf7b1d7a66540f1e8c`  
		Last Modified: Tue, 30 Sep 2025 01:19:34 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012f4ff43fa54a01187773f7f7f858b4cb4469c7d421e7d80d2e41cc1c5b199e`  
		Last Modified: Tue, 30 Sep 2025 01:19:36 GMT  
		Size: 38.1 MB (38130762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e28b9bea990d64b3eb382e6b0a0e67f2210b5faa77dc02bc1969d48337c339`  
		Last Modified: Tue, 30 Sep 2025 01:19:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c233a9a2d80f823ab02b7445761bcbbb9e93d4399d1b3c27d4af04f8dbe6858`  
		Last Modified: Tue, 30 Sep 2025 01:19:34 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7aa7f00c7e4f8306b389a35abf8efaeeaf5ccf776d9e3f5292fef98676d225`  
		Last Modified: Tue, 30 Sep 2025 01:19:35 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2` - unknown; unknown

```console
$ docker pull influxdb@sha256:028240475a243c2596e1385b0bdb09fc5c32b6e36f91a21bd3b7b4328874466f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4691865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97028a1327bea1c7b5d27b5d90f052000a258471bfb7e2b22fcc9ba60406b233`

```dockerfile
```

-	Layers:
	-	`sha256:2aa033cdc539d6b4b68f51321493657fc9503b69468a4a2a38069e9ca8ff2b4e`  
		Last Modified: Wed, 01 Oct 2025 11:34:49 GMT  
		Size: 4.7 MB (4675271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f0c01f239e505063b55ac0580ec8d3f3b119b7904959f7a100452de9e35e215`  
		Last Modified: Wed, 01 Oct 2025 11:34:50 GMT  
		Size: 16.6 KB (16594 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12.2-alpine`

```console
$ docker pull influxdb@sha256:786d21195cfae2a4e33a2a9f1e090f3c2f6ec16fbce03ff68665e6846072ffae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.12.2-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:66d2329a46d68b73f4fe44a8ecc2e1a66c470cc0bf686b41d474b82dc4819099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46109705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b598749460a540b8467edfc5d27c9176d36136f5fbf77bdf7998e8cbaaf242b2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache bash ca-certificates tzdata &&     update-ca-certificates # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ARG INFLUXDB_VERSION=1.12.2
# Wed, 24 Sep 2025 16:08:46 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     case "$(apk --print-arch)" in         x86_64)  ARCH=amd64 ;;         aarch64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar -xvf "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz"         -C / --strip-components 1 --wildcards             'influxdb-*/usr/bin/influx'             'influxdb-*/usr/bin/influx_inspect'             'influxdb-*/usr/bin/influxd' &&     rm "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"        "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     apk del .build-deps # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
USER influxdb
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf29fd72ecc1ce907ef679e6691bffbc6e2441190fac83926e70c94cf8d3c33a`  
		Last Modified: Thu, 25 Sep 2025 01:11:17 GMT  
		Size: 1.2 MB (1217859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7298ddb7262ac5ecf38aa23565daab66ab05f51c43a14cf5094e40b4eba6cf7e`  
		Last Modified: Thu, 25 Sep 2025 01:11:28 GMT  
		Size: 41.3 MB (41251563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc6d2c35dfc301a4fc344c4cc21bf0203d7b27545d02a185d3463c8c24eeb0d1`  
		Last Modified: Thu, 25 Sep 2025 01:11:17 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c194518376314b2bd83490bbd01e606f06f23d11d0650ab68d302fbaa00e1b`  
		Last Modified: Thu, 25 Sep 2025 01:11:17 GMT  
		Size: 997.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc9b3690d762b0518bf4a2221226cc44c7680f52ff820f551e0f5ebd8edf34b5`  
		Last Modified: Thu, 25 Sep 2025 01:11:17 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc091ce4196a6f6ef52a63c0824ad8f0f9661d03cfdaff16c8aa50d57dba59d`  
		Last Modified: Thu, 25 Sep 2025 01:11:17 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:199e04d8292a4a75cb8a67a517df3c22c97564ba5d49254ff4db29914ee1f964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **777.9 KB (777909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:238053bdd74f2651b16896d6bfbae7baf7a3fae84043e53a238d989bd8d682e0`

```dockerfile
```

-	Layers:
	-	`sha256:8bd1cb6b6e76e5c1e3b5cb4aef4fa7fd296fe013ec246031ba29d39d510a2cd1`  
		Last Modified: Thu, 25 Sep 2025 02:21:17 GMT  
		Size: 759.2 KB (759246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b0bc5543f212c999f8c987694aead38c4b1205df87986ae131f6bdb3890d500`  
		Last Modified: Thu, 25 Sep 2025 02:21:18 GMT  
		Size: 18.7 KB (18663 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.12.2-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:5da40eb9360fc4761f3503754e978c35db477788533b175a879b3a062c910c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 MB (43344488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1669f3cf5d1d56aa7ff084652faf747d2bd3c1d4f6f6971b1438c471cc34e74a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN apk add --no-cache bash ca-certificates tzdata &&     update-ca-certificates # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ARG INFLUXDB_VERSION=1.12.2
# Tue, 30 Sep 2025 13:56:01 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     case "$(apk --print-arch)" in         x86_64)  ARCH=amd64 ;;         aarch64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar -xvf "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz"         -C / --strip-components 1 --wildcards             'influxdb-*/usr/bin/influx'             'influxdb-*/usr/bin/influx_inspect'             'influxdb-*/usr/bin/influxd' &&     rm "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"        "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     apk del .build-deps # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
USER influxdb
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3778cd6b7947fa40773e4d96fb04b28656fd002578dc1ba35152916dba4eab3`  
		Last Modified: Wed, 08 Oct 2025 21:55:04 GMT  
		Size: 1.3 MB (1290589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193f43b6c8619cf1483f881f1bdef6dd939ea58e7d495e8416bfda3d15d098c2`  
		Last Modified: Wed, 08 Oct 2025 21:55:08 GMT  
		Size: 38.1 MB (38058839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2a6f8e76e4d9c33472e64d72f702c7962ba0b5e4d61db1c648411752212f71`  
		Last Modified: Wed, 08 Oct 2025 21:55:04 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31e522d0a6aa09c893a40e88167d5532ce096d84694b5970672f058e64bc5d6`  
		Last Modified: Wed, 08 Oct 2025 21:55:04 GMT  
		Size: 990.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf7f3756e6d6b4556e7f0ff09c0a747d1b2defff34996459ba9c9fe8623c697`  
		Last Modified: Wed, 08 Oct 2025 21:55:04 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70fba9b3a8b84fe1ceeacd36df99e6d838298f829348550376de111eaa260c5`  
		Last Modified: Wed, 08 Oct 2025 21:55:04 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:16b60655d76eb0ee04a4cf31a1dbf45f8b8d2645b730d3ed43ad5ddc9b659b99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **779.9 KB (779859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cc24c010c052da3fc8e1ef47a608b08adad9afd5df78f43ec7f7e4052f6c8a1`

```dockerfile
```

-	Layers:
	-	`sha256:191b261bcac32e145613440ef72800622e01c14fb6dc6411b1728ac3dedcb34d`  
		Last Modified: Wed, 08 Oct 2025 23:20:31 GMT  
		Size: 761.1 KB (761088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21ee247e175c8dccb7cd34515f34b1749a76fd37134eef6a64643a3885004fe1`  
		Last Modified: Wed, 08 Oct 2025 23:20:32 GMT  
		Size: 18.8 KB (18771 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12.2-data`

```console
$ docker pull influxdb@sha256:109feaf76fd2cf70e54168cdbfc480facf6db2fc2645e5ddc937dbb7b458c668
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12.2-data` - linux; amd64

```console
$ docker pull influxdb@sha256:9716bc051b66dea44fc374cfc57f52c8acf3610fcf6fbdca8bf6cf3f21a1b5cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114823921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b28646598eba4e321fa7c622855bb279c15069b1f41eedd9a53ba1e3a7b74273`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Thu, 25 Sep 2025 13:45:30 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"         "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     rm -r "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"           "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 25 Sep 2025 13:45:30 GMT
VOLUME [/var/lib/influxdb]
# Thu, 25 Sep 2025 13:45:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Sep 2025 13:45:30 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c6b11972fd12973831818babf60f1ffc1c4047507943d132dffc612884022858`  
		Last Modified: Mon, 29 Sep 2025 23:34:14 GMT  
		Size: 48.5 MB (48480557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3dba6026a3c551d6b8e98308c073fff4fd569fd2fc61f21384cb996da82c9e`  
		Last Modified: Tue, 30 Sep 2025 01:43:53 GMT  
		Size: 24.0 MB (24025876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac417f32d2f278f17ff7df41097a319c4e154b701ed78228089121f291e45d5e`  
		Last Modified: Tue, 30 Sep 2025 03:21:27 GMT  
		Size: 42.3 MB (42315711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e40eda6cd42c2f5cb50cdc62fae61e212793bb08fa17014ff9611a36af8c3a`  
		Last Modified: Tue, 30 Sep 2025 03:21:25 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890bb29ee113b4de96d3fa559469c9410f2c6f7b8719857b0743d9ae72483f7b`  
		Last Modified: Tue, 30 Sep 2025 03:21:25 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711b1c5c136c3d606c726224fde1d7487b101aa460a97d38a3f9645b6e2c1cc7`  
		Last Modified: Tue, 30 Sep 2025 03:21:25 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:e9c9d620f5dead4bf73eec799cdc6a86c6d002490854c1f3ebd2d87e305b4a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4699273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0dd541abb76178358003986ee4954d640dd6495a75c27a71cfe942aa6182c36`

```dockerfile
```

-	Layers:
	-	`sha256:ec949e2ab4d50222cea5718aba4b8c221a862bdfc1a0823a66dba606186cda37`  
		Last Modified: Wed, 01 Oct 2025 14:20:48 GMT  
		Size: 4.7 MB (4685451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c2adcb17f8c71ec0be90af8e7e92813819e4b40efb080124fbe3f8c885d881b`  
		Last Modified: Wed, 01 Oct 2025 14:20:48 GMT  
		Size: 13.8 KB (13822 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12.2-data-alpine`

```console
$ docker pull influxdb@sha256:230248f4122b55660ea2f78e44d60d589b8cf6cb8ab48f5fa11355b2aa3437a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12.2-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:c6d9a496ea1ac3bfbb8fe7051352b68e5687cbce7cc4ade9e4dc92906d70d3ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47111314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:349217c040d7cb8d5ba819df95857de62d7b8c65fe537e562f9eedab6cd09781`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"         "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     tar -xvf "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz"         -C / --strip-components 1 --wildcards             'influxdb-*/usr/bin/influx'             'influxdb-*/usr/bin/influx_inspect'             'influxdb-*/usr/bin/influxd' &&     rm "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"        "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     apk del .build-deps # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69f86ebefe9dfff24be9ab53cd975a2631738b7447af6789e1dff1ca3b2c27f`  
		Last Modified: Thu, 25 Sep 2025 01:11:17 GMT  
		Size: 1.2 MB (1217842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d614cbfebd68939215609c41e791fa77b4faf9c0184838f6f2e088d147d90b`  
		Last Modified: Thu, 25 Sep 2025 01:11:20 GMT  
		Size: 42.3 MB (42254130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b27779e2d36c38b820659ca7fc3113c1733a2a5525df9062e31317c6e945791`  
		Last Modified: Thu, 25 Sep 2025 01:11:17 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042f205ee4f2c54dd0fab79d5ff8ab7fc2d8b532b3b6bf65e1214a3ba864e2b6`  
		Last Modified: Thu, 25 Sep 2025 01:11:17 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc48483cf9f08acfa785e7133e964bccc86be159a441243a8c2e7bf35f5c5a3`  
		Last Modified: Thu, 25 Sep 2025 01:11:17 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:cae64fd7f9afd9ae2714d996f632407d49177f7187e1ea8f0f0cfcc147b719ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **788.4 KB (788388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffc8318dc7f4dd8e8855ad80626a177cb044360e5746e29e2d607ff65ac2aa6a`

```dockerfile
```

-	Layers:
	-	`sha256:a071aa26d75f72d4bd7f30c81a59364f35b5553a0d5e391470b451a6d0354062`  
		Last Modified: Thu, 25 Sep 2025 02:21:25 GMT  
		Size: 773.2 KB (773197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4e9386bff0d6db73eee18d185455902b386dab3efc2240f66243aa380eba25a`  
		Last Modified: Thu, 25 Sep 2025 02:21:26 GMT  
		Size: 15.2 KB (15191 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12.2-meta`

```console
$ docker pull influxdb@sha256:eb66706708762ad8262268c2a8dcb4a7070f60a44b6242ecf9c7432e278c6547
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12.2-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:cb76c71f6494f29ab920bebbf11667a25ff162ad7b691cb1b4dc8355396468c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91285988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec49e8777115ad9902de7591dae24a9ffc6552019edde2952c1b22604fd1b3c2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Thu, 25 Sep 2025 13:45:30 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"         "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     rm -r "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"           "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
EXPOSE map[8091/tcp:{}]
# Thu, 25 Sep 2025 13:45:30 GMT
VOLUME [/var/lib/influxdb]
# Thu, 25 Sep 2025 13:45:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Sep 2025 13:45:30 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:c6b11972fd12973831818babf60f1ffc1c4047507943d132dffc612884022858`  
		Last Modified: Mon, 29 Sep 2025 23:34:14 GMT  
		Size: 48.5 MB (48480557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3dba6026a3c551d6b8e98308c073fff4fd569fd2fc61f21384cb996da82c9e`  
		Last Modified: Tue, 30 Sep 2025 01:43:53 GMT  
		Size: 24.0 MB (24025876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc8cbe523bf49114d5cd00d6b16afb02991fb3218f450080c37b2799b582ede`  
		Last Modified: Tue, 30 Sep 2025 03:21:30 GMT  
		Size: 18.8 MB (18778988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4263e2db74f5a8e2b7b08cb3a1896e83e555ff19fd35da34fac577a38ca31ea7`  
		Last Modified: Tue, 30 Sep 2025 03:21:25 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ba22fecbbbe66d020e5a2f00ab33cac5b99b8941b4bf998a02793e5b927af0`  
		Last Modified: Tue, 30 Sep 2025 03:21:25 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:2ad4245a9408493849ffb1b7b90826247660bfc05142b29d4f6b54b0d5b42f98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4602950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c0f9aa8c13351777e04528b37139359c7d138326f6e8a109137106bea0dd8c2`

```dockerfile
```

-	Layers:
	-	`sha256:0528ec79b7bd6d396d6c5eaa0030b5ba2a83324a92d9302cfb93802c04f1495c`  
		Last Modified: Wed, 01 Oct 2025 14:20:54 GMT  
		Size: 4.6 MB (4590614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be82511432d5e991944abe2ceb44d5ff6d16f3024543b901494cf4ce90f05362`  
		Last Modified: Wed, 01 Oct 2025 14:20:54 GMT  
		Size: 12.3 KB (12336 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12.2-meta-alpine`

```console
$ docker pull influxdb@sha256:fb1c6ce882c6f76575bf00e884eb6a1cb48f015f6dced8852e0632304e0f5e18
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12.2-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:438d52e3d15ecb0301ecc4b86a960ee9bc6fce7f38f9d2e372347c8525563ab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23578256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31b60e5178733d55db673306b947c186ea7867ea6067cff2db7b2e658a86d9c2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"         "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     tar -xvf "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz"         -C / --strip-components 1 --wildcards             'influxdb-*/usr/bin/influxd-ctl'             'influxdb-*/usr/bin/influxd-meta' &&     rm "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"        "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     apk del .build-deps # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8091/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f49da720c3a823002c9dc61fb96fe6cbaef56f95b70e83f1717b0cbfe3625c2`  
		Last Modified: Thu, 25 Sep 2025 01:11:07 GMT  
		Size: 1.2 MB (1217796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b26514951c314740b0ec3a65e5c10800f94cd828599759c28c959a27cce08fc`  
		Last Modified: Thu, 25 Sep 2025 01:11:08 GMT  
		Size: 18.7 MB (18722325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a69a5b526bf15a075a5b6a8f416149db75a74b0e83960585a33600795990c9e`  
		Last Modified: Thu, 25 Sep 2025 01:11:07 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcaf0d00f6e38d9ddf873ead6554c87a4c001319e00556ec54da121d35ad3db6`  
		Last Modified: Thu, 25 Sep 2025 01:11:07 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:66c0c255fb30f22da06e4e5eb91e6feab97a584430550d8c5fa3641c6e9adc0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **692.7 KB (692723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c204ee4a35a8f1aa76d61d64fe38ae6354d2b8fc6deff8188661dddd18a645`

```dockerfile
```

-	Layers:
	-	`sha256:b6e4d83eeb239e60792a85b357d7d2758fca1759d804b3b06c1ca78d6b90f827`  
		Last Modified: Thu, 25 Sep 2025 02:21:34 GMT  
		Size: 679.1 KB (679146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d892543fbfacd30d46f77df1c4f2bad94927a6e55b406e2082cebc6a60b88c7d`  
		Last Modified: Thu, 25 Sep 2025 02:21:35 GMT  
		Size: 13.6 KB (13577 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2`

```console
$ docker pull influxdb@sha256:674911452ada77ca762662d50dd0594c8823312f59b376500623a4f82c44f9be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2` - linux; amd64

```console
$ docker pull influxdb@sha256:0121b1ef000ad9ee6fd18236fbda5b578e2d2b53ebf88b2852a5df1a2e6b88d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157221895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c729c6b61bf04bccae282b4a88b0af07233b54566c44357100bb3f1f93d5bb09`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 25 Sep 2025 13:45:30 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Thu, 25 Sep 2025 13:45:30 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENV GOSU_VER=1.16
# Thu, 25 Sep 2025 13:45:30 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUXDB_VERSION=2.7.12
# Thu, 25 Sep 2025 13:45:30 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Thu, 25 Sep 2025 13:45:30 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 25 Sep 2025 13:45:30 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Sep 2025 13:45:30 GMT
CMD ["influxd"]
# Thu, 25 Sep 2025 13:45:30 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 25 Sep 2025 13:45:30 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811aaf99bbf19a9910d62277e035aceff4198c7f376b20d593edff533f641d1d`  
		Last Modified: Tue, 30 Sep 2025 00:13:36 GMT  
		Size: 9.8 MB (9796261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343156d2f44315d2944d689a3b6ba5fb12db96d0735c74f9f5061dadaa5ee050`  
		Last Modified: Tue, 30 Sep 2025 00:13:36 GMT  
		Size: 6.2 MB (6156974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45de5a0fe55cef8d3934d43433657930fba76ec5ddc4d981cdb77a35dabec0f0`  
		Last Modified: Tue, 30 Sep 2025 01:05:33 GMT  
		Size: 3.2 KB (3224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17580cec1ecab1149b131bab26b9ef493f6544152e36e43a4a8fda262ad2f742`  
		Last Modified: Tue, 30 Sep 2025 01:05:33 GMT  
		Size: 1.0 MB (1012036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33043d02209c6f842255867f3e7a3cad421ba64cbeb2927ddda8ceb54856a854`  
		Last Modified: Wed, 01 Oct 2025 14:21:09 GMT  
		Size: 100.2 MB (100244546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed0f8fa108abae31ed054ba64b943b34c7f988766fc3cabc0fce10f5829c87f`  
		Last Modified: Wed, 01 Oct 2025 14:21:07 GMT  
		Size: 11.8 MB (11773790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6a602b2831120358c8dc7d1f25aeef36e9c54553e633ad61ab3fb092c94ab2`  
		Last Modified: Tue, 30 Sep 2025 01:05:32 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e85a2aece113cd4582f9805ef8101ef31daf5e4fa684167883c30011b7c0606`  
		Last Modified: Tue, 30 Sep 2025 01:05:33 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf6f0e586b1a73cc1ab4ccebc8f1a38ca717d394b624b137718be85c1bbeeeb`  
		Last Modified: Tue, 30 Sep 2025 01:05:32 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:185b77ece5df1f271f383b88de53edf5a6de19f2ffe13d95248ad30a48bc316d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3015606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd30accab1f61a0131fa41611377459c8480e8dd58fe1768c27ca200763ac693`

```dockerfile
```

-	Layers:
	-	`sha256:92d23af2aaf90e882cd2ebd504b46e52e629c0f42394d304d6939d7b8560f61f`  
		Last Modified: Wed, 01 Oct 2025 14:21:04 GMT  
		Size: 3.0 MB (2982068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e33518cd60ed9dd866b1f385742a274e53eecdf30023662122b59428aedd35a`  
		Last Modified: Wed, 01 Oct 2025 14:21:05 GMT  
		Size: 33.5 KB (33538 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:8082b154781eaebf6a996ea7d6b8e168f75791852a0ada8a91170a1c2d47b6d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151606772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1af681f1c20860f9abf95e03acb5611917958551f8ba30ec43ec3f23b6058c42`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 25 Sep 2025 13:45:30 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Thu, 25 Sep 2025 13:45:30 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENV GOSU_VER=1.16
# Thu, 25 Sep 2025 13:45:30 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUXDB_VERSION=2.7.12
# Thu, 25 Sep 2025 13:45:30 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Thu, 25 Sep 2025 13:45:30 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 25 Sep 2025 13:45:30 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Sep 2025 13:45:30 GMT
CMD ["influxd"]
# Thu, 25 Sep 2025 13:45:30 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 25 Sep 2025 13:45:30 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082090d89175918857dcc8282e145311f059b5b017dc01f9a6121a6b278a9487`  
		Last Modified: Tue, 30 Sep 2025 00:17:38 GMT  
		Size: 9.6 MB (9626389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cebe74b7eaf8b3bc1b970e333e60268a909d8d3552e00442ad46718221c4c732`  
		Last Modified: Tue, 30 Sep 2025 00:17:40 GMT  
		Size: 5.8 MB (5790423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6360dbdbebcd1552db8e529acc86ead1dd06ff0fc6d02b4edfd492fb84f4f4`  
		Last Modified: Tue, 30 Sep 2025 00:17:39 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5cfca2c3199900213baadd0d387cbd6a978c4b499f7a754544c87f215d91eb3`  
		Last Modified: Tue, 30 Sep 2025 00:17:40 GMT  
		Size: 938.9 KB (938877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9236bff4709329221210f80370f34d8143cba158e827d1b7d5befc8bbe5ab87e`  
		Last Modified: Tue, 30 Sep 2025 00:17:51 GMT  
		Size: 96.0 MB (96038992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ded161eaa69ae91d1d7bf0c155e1d1facb0eaf2ef3c6cfb520c40024f5b8d36`  
		Last Modified: Tue, 30 Sep 2025 00:17:43 GMT  
		Size: 11.1 MB (11099994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd77ea3562d6f2442138d60ad311221076c2d671d1166ce9dbe1eb17e371ce97`  
		Last Modified: Tue, 30 Sep 2025 00:17:41 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2de2120c066eb9a1231dd3d23cbcacb1f194daf4995009e45c695157b6e026`  
		Last Modified: Tue, 30 Sep 2025 00:17:42 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9972a62410f906ab8092ded9c34d97da94f43fc95a74e0a9b46a2147c441b81`  
		Last Modified: Tue, 30 Sep 2025 00:17:35 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:93465f8e0525b500bcf956c05920220caa5ba91b14b2ec23e6c8b00482747995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3015017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfcabdba78ebb2d6a410efdb1679524330e6bda30e8238df63bc5a929b35bdac`

```dockerfile
```

-	Layers:
	-	`sha256:c62b73da34672ba9622e16b068686545412cc06cec03c481b03e578626525369`  
		Last Modified: Wed, 01 Oct 2025 11:35:02 GMT  
		Size: 3.0 MB (2981296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bece50323750999f98c31f931dd719c0349234cc48534b78d16dbb5110054b39`  
		Last Modified: Wed, 01 Oct 2025 11:35:03 GMT  
		Size: 33.7 KB (33721 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2-alpine`

```console
$ docker pull influxdb@sha256:8fe50632b89ac1d44ae4875172d7017113635a537548037f7b66d62e603cc527
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:cff6f2ab47c82bede8226eaa115bb26a3c6b687ca6d1600c4daf951debdab495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.5 MB (81514718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e97594fdb74be0f41ef523f1d997467fd03327d8d08cfda4c4ac4e33bf5a76b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 24 Sep 2025 16:08:46 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0a8ae42cc4bbee908d14c07fc4ec8c8407af6310249f9dfeae0f8509bdc7af`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c7bfad06ee97b9a79123f8649a25c2c85621f43c09f683fc22058f5a07f5d6`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 9.8 MB (9819983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a34cab64443b962a114bd2a6beffb95756ba52160469829a5d45a76fcba800`  
		Last Modified: Thu, 25 Sep 2025 01:11:54 GMT  
		Size: 6.2 MB (6156990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a8939940eb42b2ce365e0ace1c34d67dbdaf70d81621f34c5fca12f3bfd8f7`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda56c435bfb0f3172c6ba8994e754a3757983ee0517a7f6b2584a903a27e12e`  
		Last Modified: Thu, 25 Sep 2025 01:11:57 GMT  
		Size: 50.1 MB (50118442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5092574230696c38c9b6d5e80c3b0052a6775a347fc390fb3ddfbed0312b110b`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 11.8 MB (11773781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6964e799275484d75822451544c8b8aeb0525a898edf53d62dc5b2bea9ec4f23`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07acd36aa62e4aa31c3926c29dbc6d78b9952999a9f6d5a20d03ad2ac4ce55cd`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2256c74f4ebf0907ad02de26150d5f5f37dbd8fca3e5b1db457560709bcdc17`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:4cecdea6552df534fc6ff5b0baf01df080318ad872171cb76d8d681529a60c69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **941.4 KB (941372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e5b13134ce9c59f59464dd153938abe2b1fb108f183574cf50f20c34593ab1`

```dockerfile
```

-	Layers:
	-	`sha256:24d2b9eb10c23f5c732a7e37c15a0f780289592f3ff141a1cf3aed71130b5200`  
		Last Modified: Thu, 25 Sep 2025 02:22:05 GMT  
		Size: 910.6 KB (910603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecc19b40f79ef646496790610a3aa4aeb69ed7919b9a4f647f14c2cd431b643e`  
		Last Modified: Thu, 25 Sep 2025 02:22:06 GMT  
		Size: 30.8 KB (30769 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:c0b4bb9622f30c203d6164e4608265058ec2133de5fecec638a96afe1fc77b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78730374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3df955cee3af183aedd38baa540b6cf616ee4e64c4c7704593b9840e7e51c5b8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 30 Sep 2025 13:56:01 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxd"]
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 30 Sep 2025 13:56:01 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e9f8ae4bf7158674e53e799e39195db08dc922549798b1c92b5db881e75950`  
		Last Modified: Wed, 08 Oct 2025 21:55:31 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db47b23aa319f26ace574a307a140d466205a9c8792ea299825977016c72027`  
		Last Modified: Wed, 08 Oct 2025 21:55:32 GMT  
		Size: 9.8 MB (9822482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e75ad98f92c131cb2c24f50a1f955f559cb081760bb3ebaba411aff5652c0b1`  
		Last Modified: Wed, 08 Oct 2025 21:55:35 GMT  
		Size: 5.8 MB (5790429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0846ab0df2a8dd47b00f9e08910902bc9137be17fc01ecb2ab92865324a0a692`  
		Last Modified: Wed, 08 Oct 2025 21:55:31 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee341d51fc6d484c991e3e387ad2bab42cc99f8c5f0c144f3548538763046b7`  
		Last Modified: Wed, 08 Oct 2025 21:55:33 GMT  
		Size: 48.0 MB (48017161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5467babbc25c511c880690592c05bf5c8bf7eb3718a0ffcbb6bb66881d449be0`  
		Last Modified: Wed, 08 Oct 2025 21:55:31 GMT  
		Size: 11.1 MB (11099994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73275e145aac044b3ee173c0907851a448d495a9d0f964f1d943e707c8a79108`  
		Last Modified: Wed, 08 Oct 2025 21:55:31 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501e2a94b5ef2caef075bbdb0a7105d248f3f7d5e3a45540947b4843f21e8702`  
		Last Modified: Wed, 08 Oct 2025 21:55:31 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0bc70a0456678acb89ee83669fb653b9be40154e9167dec954aa525d35f87c`  
		Last Modified: Wed, 08 Oct 2025 21:55:31 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:c0855268e95dc31f5a9cac070c75e0c671fb7a46b90288fefc74be913b3869f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.0 KB (944029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f493a124da258c44e6401fe8b1e7f376cd7e326f841643ef5833690bb86f4d0`

```dockerfile
```

-	Layers:
	-	`sha256:0cf6c5db23c7a94944a2efa242d33b1a09e07eed2c284228b76d51eb51068db0`  
		Last Modified: Wed, 08 Oct 2025 23:20:42 GMT  
		Size: 913.1 KB (913066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:868968715be1dde5591f2d64233e6a60defbc05776d1a13313f5f018438e6317`  
		Last Modified: Wed, 08 Oct 2025 23:20:44 GMT  
		Size: 31.0 KB (30963 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7`

```console
$ docker pull influxdb@sha256:674911452ada77ca762662d50dd0594c8823312f59b376500623a4f82c44f9be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7` - linux; amd64

```console
$ docker pull influxdb@sha256:0121b1ef000ad9ee6fd18236fbda5b578e2d2b53ebf88b2852a5df1a2e6b88d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157221895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c729c6b61bf04bccae282b4a88b0af07233b54566c44357100bb3f1f93d5bb09`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 25 Sep 2025 13:45:30 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Thu, 25 Sep 2025 13:45:30 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENV GOSU_VER=1.16
# Thu, 25 Sep 2025 13:45:30 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUXDB_VERSION=2.7.12
# Thu, 25 Sep 2025 13:45:30 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Thu, 25 Sep 2025 13:45:30 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 25 Sep 2025 13:45:30 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Sep 2025 13:45:30 GMT
CMD ["influxd"]
# Thu, 25 Sep 2025 13:45:30 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 25 Sep 2025 13:45:30 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811aaf99bbf19a9910d62277e035aceff4198c7f376b20d593edff533f641d1d`  
		Last Modified: Tue, 30 Sep 2025 00:13:36 GMT  
		Size: 9.8 MB (9796261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343156d2f44315d2944d689a3b6ba5fb12db96d0735c74f9f5061dadaa5ee050`  
		Last Modified: Tue, 30 Sep 2025 00:13:36 GMT  
		Size: 6.2 MB (6156974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45de5a0fe55cef8d3934d43433657930fba76ec5ddc4d981cdb77a35dabec0f0`  
		Last Modified: Tue, 30 Sep 2025 01:05:33 GMT  
		Size: 3.2 KB (3224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17580cec1ecab1149b131bab26b9ef493f6544152e36e43a4a8fda262ad2f742`  
		Last Modified: Tue, 30 Sep 2025 01:05:33 GMT  
		Size: 1.0 MB (1012036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33043d02209c6f842255867f3e7a3cad421ba64cbeb2927ddda8ceb54856a854`  
		Last Modified: Wed, 01 Oct 2025 14:21:09 GMT  
		Size: 100.2 MB (100244546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed0f8fa108abae31ed054ba64b943b34c7f988766fc3cabc0fce10f5829c87f`  
		Last Modified: Wed, 01 Oct 2025 14:21:07 GMT  
		Size: 11.8 MB (11773790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6a602b2831120358c8dc7d1f25aeef36e9c54553e633ad61ab3fb092c94ab2`  
		Last Modified: Tue, 30 Sep 2025 01:05:32 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e85a2aece113cd4582f9805ef8101ef31daf5e4fa684167883c30011b7c0606`  
		Last Modified: Tue, 30 Sep 2025 01:05:33 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf6f0e586b1a73cc1ab4ccebc8f1a38ca717d394b624b137718be85c1bbeeeb`  
		Last Modified: Tue, 30 Sep 2025 01:05:32 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:185b77ece5df1f271f383b88de53edf5a6de19f2ffe13d95248ad30a48bc316d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3015606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd30accab1f61a0131fa41611377459c8480e8dd58fe1768c27ca200763ac693`

```dockerfile
```

-	Layers:
	-	`sha256:92d23af2aaf90e882cd2ebd504b46e52e629c0f42394d304d6939d7b8560f61f`  
		Last Modified: Wed, 01 Oct 2025 14:21:04 GMT  
		Size: 3.0 MB (2982068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e33518cd60ed9dd866b1f385742a274e53eecdf30023662122b59428aedd35a`  
		Last Modified: Wed, 01 Oct 2025 14:21:05 GMT  
		Size: 33.5 KB (33538 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:8082b154781eaebf6a996ea7d6b8e168f75791852a0ada8a91170a1c2d47b6d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151606772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1af681f1c20860f9abf95e03acb5611917958551f8ba30ec43ec3f23b6058c42`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 25 Sep 2025 13:45:30 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Thu, 25 Sep 2025 13:45:30 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENV GOSU_VER=1.16
# Thu, 25 Sep 2025 13:45:30 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUXDB_VERSION=2.7.12
# Thu, 25 Sep 2025 13:45:30 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Thu, 25 Sep 2025 13:45:30 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 25 Sep 2025 13:45:30 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Sep 2025 13:45:30 GMT
CMD ["influxd"]
# Thu, 25 Sep 2025 13:45:30 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 25 Sep 2025 13:45:30 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082090d89175918857dcc8282e145311f059b5b017dc01f9a6121a6b278a9487`  
		Last Modified: Tue, 30 Sep 2025 00:17:38 GMT  
		Size: 9.6 MB (9626389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cebe74b7eaf8b3bc1b970e333e60268a909d8d3552e00442ad46718221c4c732`  
		Last Modified: Tue, 30 Sep 2025 00:17:40 GMT  
		Size: 5.8 MB (5790423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6360dbdbebcd1552db8e529acc86ead1dd06ff0fc6d02b4edfd492fb84f4f4`  
		Last Modified: Tue, 30 Sep 2025 00:17:39 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5cfca2c3199900213baadd0d387cbd6a978c4b499f7a754544c87f215d91eb3`  
		Last Modified: Tue, 30 Sep 2025 00:17:40 GMT  
		Size: 938.9 KB (938877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9236bff4709329221210f80370f34d8143cba158e827d1b7d5befc8bbe5ab87e`  
		Last Modified: Tue, 30 Sep 2025 00:17:51 GMT  
		Size: 96.0 MB (96038992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ded161eaa69ae91d1d7bf0c155e1d1facb0eaf2ef3c6cfb520c40024f5b8d36`  
		Last Modified: Tue, 30 Sep 2025 00:17:43 GMT  
		Size: 11.1 MB (11099994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd77ea3562d6f2442138d60ad311221076c2d671d1166ce9dbe1eb17e371ce97`  
		Last Modified: Tue, 30 Sep 2025 00:17:41 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2de2120c066eb9a1231dd3d23cbcacb1f194daf4995009e45c695157b6e026`  
		Last Modified: Tue, 30 Sep 2025 00:17:42 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9972a62410f906ab8092ded9c34d97da94f43fc95a74e0a9b46a2147c441b81`  
		Last Modified: Tue, 30 Sep 2025 00:17:35 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:93465f8e0525b500bcf956c05920220caa5ba91b14b2ec23e6c8b00482747995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3015017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfcabdba78ebb2d6a410efdb1679524330e6bda30e8238df63bc5a929b35bdac`

```dockerfile
```

-	Layers:
	-	`sha256:c62b73da34672ba9622e16b068686545412cc06cec03c481b03e578626525369`  
		Last Modified: Wed, 01 Oct 2025 11:35:02 GMT  
		Size: 3.0 MB (2981296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bece50323750999f98c31f931dd719c0349234cc48534b78d16dbb5110054b39`  
		Last Modified: Wed, 01 Oct 2025 11:35:03 GMT  
		Size: 33.7 KB (33721 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7-alpine`

```console
$ docker pull influxdb@sha256:8fe50632b89ac1d44ae4875172d7017113635a537548037f7b66d62e603cc527
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:cff6f2ab47c82bede8226eaa115bb26a3c6b687ca6d1600c4daf951debdab495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.5 MB (81514718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e97594fdb74be0f41ef523f1d997467fd03327d8d08cfda4c4ac4e33bf5a76b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 24 Sep 2025 16:08:46 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0a8ae42cc4bbee908d14c07fc4ec8c8407af6310249f9dfeae0f8509bdc7af`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c7bfad06ee97b9a79123f8649a25c2c85621f43c09f683fc22058f5a07f5d6`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 9.8 MB (9819983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a34cab64443b962a114bd2a6beffb95756ba52160469829a5d45a76fcba800`  
		Last Modified: Thu, 25 Sep 2025 01:11:54 GMT  
		Size: 6.2 MB (6156990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a8939940eb42b2ce365e0ace1c34d67dbdaf70d81621f34c5fca12f3bfd8f7`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda56c435bfb0f3172c6ba8994e754a3757983ee0517a7f6b2584a903a27e12e`  
		Last Modified: Thu, 25 Sep 2025 01:11:57 GMT  
		Size: 50.1 MB (50118442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5092574230696c38c9b6d5e80c3b0052a6775a347fc390fb3ddfbed0312b110b`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 11.8 MB (11773781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6964e799275484d75822451544c8b8aeb0525a898edf53d62dc5b2bea9ec4f23`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07acd36aa62e4aa31c3926c29dbc6d78b9952999a9f6d5a20d03ad2ac4ce55cd`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2256c74f4ebf0907ad02de26150d5f5f37dbd8fca3e5b1db457560709bcdc17`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:4cecdea6552df534fc6ff5b0baf01df080318ad872171cb76d8d681529a60c69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **941.4 KB (941372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e5b13134ce9c59f59464dd153938abe2b1fb108f183574cf50f20c34593ab1`

```dockerfile
```

-	Layers:
	-	`sha256:24d2b9eb10c23f5c732a7e37c15a0f780289592f3ff141a1cf3aed71130b5200`  
		Last Modified: Thu, 25 Sep 2025 02:22:05 GMT  
		Size: 910.6 KB (910603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecc19b40f79ef646496790610a3aa4aeb69ed7919b9a4f647f14c2cd431b643e`  
		Last Modified: Thu, 25 Sep 2025 02:22:06 GMT  
		Size: 30.8 KB (30769 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:c0b4bb9622f30c203d6164e4608265058ec2133de5fecec638a96afe1fc77b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78730374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3df955cee3af183aedd38baa540b6cf616ee4e64c4c7704593b9840e7e51c5b8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 30 Sep 2025 13:56:01 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxd"]
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 30 Sep 2025 13:56:01 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e9f8ae4bf7158674e53e799e39195db08dc922549798b1c92b5db881e75950`  
		Last Modified: Wed, 08 Oct 2025 21:55:31 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db47b23aa319f26ace574a307a140d466205a9c8792ea299825977016c72027`  
		Last Modified: Wed, 08 Oct 2025 21:55:32 GMT  
		Size: 9.8 MB (9822482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e75ad98f92c131cb2c24f50a1f955f559cb081760bb3ebaba411aff5652c0b1`  
		Last Modified: Wed, 08 Oct 2025 21:55:35 GMT  
		Size: 5.8 MB (5790429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0846ab0df2a8dd47b00f9e08910902bc9137be17fc01ecb2ab92865324a0a692`  
		Last Modified: Wed, 08 Oct 2025 21:55:31 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee341d51fc6d484c991e3e387ad2bab42cc99f8c5f0c144f3548538763046b7`  
		Last Modified: Wed, 08 Oct 2025 21:55:33 GMT  
		Size: 48.0 MB (48017161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5467babbc25c511c880690592c05bf5c8bf7eb3718a0ffcbb6bb66881d449be0`  
		Last Modified: Wed, 08 Oct 2025 21:55:31 GMT  
		Size: 11.1 MB (11099994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73275e145aac044b3ee173c0907851a448d495a9d0f964f1d943e707c8a79108`  
		Last Modified: Wed, 08 Oct 2025 21:55:31 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501e2a94b5ef2caef075bbdb0a7105d248f3f7d5e3a45540947b4843f21e8702`  
		Last Modified: Wed, 08 Oct 2025 21:55:31 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0bc70a0456678acb89ee83669fb653b9be40154e9167dec954aa525d35f87c`  
		Last Modified: Wed, 08 Oct 2025 21:55:31 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:c0855268e95dc31f5a9cac070c75e0c671fb7a46b90288fefc74be913b3869f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.0 KB (944029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f493a124da258c44e6401fe8b1e7f376cd7e326f841643ef5833690bb86f4d0`

```dockerfile
```

-	Layers:
	-	`sha256:0cf6c5db23c7a94944a2efa242d33b1a09e07eed2c284228b76d51eb51068db0`  
		Last Modified: Wed, 08 Oct 2025 23:20:42 GMT  
		Size: 913.1 KB (913066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:868968715be1dde5591f2d64233e6a60defbc05776d1a13313f5f018438e6317`  
		Last Modified: Wed, 08 Oct 2025 23:20:44 GMT  
		Size: 31.0 KB (30963 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7.12`

```console
$ docker pull influxdb@sha256:674911452ada77ca762662d50dd0594c8823312f59b376500623a4f82c44f9be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.12` - linux; amd64

```console
$ docker pull influxdb@sha256:0121b1ef000ad9ee6fd18236fbda5b578e2d2b53ebf88b2852a5df1a2e6b88d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157221895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c729c6b61bf04bccae282b4a88b0af07233b54566c44357100bb3f1f93d5bb09`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 25 Sep 2025 13:45:30 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Thu, 25 Sep 2025 13:45:30 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENV GOSU_VER=1.16
# Thu, 25 Sep 2025 13:45:30 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUXDB_VERSION=2.7.12
# Thu, 25 Sep 2025 13:45:30 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Thu, 25 Sep 2025 13:45:30 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 25 Sep 2025 13:45:30 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Sep 2025 13:45:30 GMT
CMD ["influxd"]
# Thu, 25 Sep 2025 13:45:30 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 25 Sep 2025 13:45:30 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811aaf99bbf19a9910d62277e035aceff4198c7f376b20d593edff533f641d1d`  
		Last Modified: Tue, 30 Sep 2025 00:13:36 GMT  
		Size: 9.8 MB (9796261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343156d2f44315d2944d689a3b6ba5fb12db96d0735c74f9f5061dadaa5ee050`  
		Last Modified: Tue, 30 Sep 2025 00:13:36 GMT  
		Size: 6.2 MB (6156974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45de5a0fe55cef8d3934d43433657930fba76ec5ddc4d981cdb77a35dabec0f0`  
		Last Modified: Tue, 30 Sep 2025 01:05:33 GMT  
		Size: 3.2 KB (3224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17580cec1ecab1149b131bab26b9ef493f6544152e36e43a4a8fda262ad2f742`  
		Last Modified: Tue, 30 Sep 2025 01:05:33 GMT  
		Size: 1.0 MB (1012036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33043d02209c6f842255867f3e7a3cad421ba64cbeb2927ddda8ceb54856a854`  
		Last Modified: Wed, 01 Oct 2025 14:21:09 GMT  
		Size: 100.2 MB (100244546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed0f8fa108abae31ed054ba64b943b34c7f988766fc3cabc0fce10f5829c87f`  
		Last Modified: Wed, 01 Oct 2025 14:21:07 GMT  
		Size: 11.8 MB (11773790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6a602b2831120358c8dc7d1f25aeef36e9c54553e633ad61ab3fb092c94ab2`  
		Last Modified: Tue, 30 Sep 2025 01:05:32 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e85a2aece113cd4582f9805ef8101ef31daf5e4fa684167883c30011b7c0606`  
		Last Modified: Tue, 30 Sep 2025 01:05:33 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf6f0e586b1a73cc1ab4ccebc8f1a38ca717d394b624b137718be85c1bbeeeb`  
		Last Modified: Tue, 30 Sep 2025 01:05:32 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:185b77ece5df1f271f383b88de53edf5a6de19f2ffe13d95248ad30a48bc316d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3015606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd30accab1f61a0131fa41611377459c8480e8dd58fe1768c27ca200763ac693`

```dockerfile
```

-	Layers:
	-	`sha256:92d23af2aaf90e882cd2ebd504b46e52e629c0f42394d304d6939d7b8560f61f`  
		Last Modified: Wed, 01 Oct 2025 14:21:04 GMT  
		Size: 3.0 MB (2982068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e33518cd60ed9dd866b1f385742a274e53eecdf30023662122b59428aedd35a`  
		Last Modified: Wed, 01 Oct 2025 14:21:05 GMT  
		Size: 33.5 KB (33538 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7.12` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:8082b154781eaebf6a996ea7d6b8e168f75791852a0ada8a91170a1c2d47b6d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151606772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1af681f1c20860f9abf95e03acb5611917958551f8ba30ec43ec3f23b6058c42`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 25 Sep 2025 13:45:30 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Thu, 25 Sep 2025 13:45:30 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENV GOSU_VER=1.16
# Thu, 25 Sep 2025 13:45:30 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUXDB_VERSION=2.7.12
# Thu, 25 Sep 2025 13:45:30 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Thu, 25 Sep 2025 13:45:30 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 25 Sep 2025 13:45:30 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Sep 2025 13:45:30 GMT
CMD ["influxd"]
# Thu, 25 Sep 2025 13:45:30 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 25 Sep 2025 13:45:30 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082090d89175918857dcc8282e145311f059b5b017dc01f9a6121a6b278a9487`  
		Last Modified: Tue, 30 Sep 2025 00:17:38 GMT  
		Size: 9.6 MB (9626389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cebe74b7eaf8b3bc1b970e333e60268a909d8d3552e00442ad46718221c4c732`  
		Last Modified: Tue, 30 Sep 2025 00:17:40 GMT  
		Size: 5.8 MB (5790423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6360dbdbebcd1552db8e529acc86ead1dd06ff0fc6d02b4edfd492fb84f4f4`  
		Last Modified: Tue, 30 Sep 2025 00:17:39 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5cfca2c3199900213baadd0d387cbd6a978c4b499f7a754544c87f215d91eb3`  
		Last Modified: Tue, 30 Sep 2025 00:17:40 GMT  
		Size: 938.9 KB (938877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9236bff4709329221210f80370f34d8143cba158e827d1b7d5befc8bbe5ab87e`  
		Last Modified: Tue, 30 Sep 2025 00:17:51 GMT  
		Size: 96.0 MB (96038992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ded161eaa69ae91d1d7bf0c155e1d1facb0eaf2ef3c6cfb520c40024f5b8d36`  
		Last Modified: Tue, 30 Sep 2025 00:17:43 GMT  
		Size: 11.1 MB (11099994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd77ea3562d6f2442138d60ad311221076c2d671d1166ce9dbe1eb17e371ce97`  
		Last Modified: Tue, 30 Sep 2025 00:17:41 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2de2120c066eb9a1231dd3d23cbcacb1f194daf4995009e45c695157b6e026`  
		Last Modified: Tue, 30 Sep 2025 00:17:42 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9972a62410f906ab8092ded9c34d97da94f43fc95a74e0a9b46a2147c441b81`  
		Last Modified: Tue, 30 Sep 2025 00:17:35 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:93465f8e0525b500bcf956c05920220caa5ba91b14b2ec23e6c8b00482747995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3015017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfcabdba78ebb2d6a410efdb1679524330e6bda30e8238df63bc5a929b35bdac`

```dockerfile
```

-	Layers:
	-	`sha256:c62b73da34672ba9622e16b068686545412cc06cec03c481b03e578626525369`  
		Last Modified: Wed, 01 Oct 2025 11:35:02 GMT  
		Size: 3.0 MB (2981296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bece50323750999f98c31f931dd719c0349234cc48534b78d16dbb5110054b39`  
		Last Modified: Wed, 01 Oct 2025 11:35:03 GMT  
		Size: 33.7 KB (33721 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7.12-alpine`

```console
$ docker pull influxdb@sha256:8fe50632b89ac1d44ae4875172d7017113635a537548037f7b66d62e603cc527
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.12-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:cff6f2ab47c82bede8226eaa115bb26a3c6b687ca6d1600c4daf951debdab495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.5 MB (81514718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e97594fdb74be0f41ef523f1d997467fd03327d8d08cfda4c4ac4e33bf5a76b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 24 Sep 2025 16:08:46 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0a8ae42cc4bbee908d14c07fc4ec8c8407af6310249f9dfeae0f8509bdc7af`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c7bfad06ee97b9a79123f8649a25c2c85621f43c09f683fc22058f5a07f5d6`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 9.8 MB (9819983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a34cab64443b962a114bd2a6beffb95756ba52160469829a5d45a76fcba800`  
		Last Modified: Thu, 25 Sep 2025 01:11:54 GMT  
		Size: 6.2 MB (6156990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a8939940eb42b2ce365e0ace1c34d67dbdaf70d81621f34c5fca12f3bfd8f7`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda56c435bfb0f3172c6ba8994e754a3757983ee0517a7f6b2584a903a27e12e`  
		Last Modified: Thu, 25 Sep 2025 01:11:57 GMT  
		Size: 50.1 MB (50118442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5092574230696c38c9b6d5e80c3b0052a6775a347fc390fb3ddfbed0312b110b`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 11.8 MB (11773781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6964e799275484d75822451544c8b8aeb0525a898edf53d62dc5b2bea9ec4f23`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07acd36aa62e4aa31c3926c29dbc6d78b9952999a9f6d5a20d03ad2ac4ce55cd`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2256c74f4ebf0907ad02de26150d5f5f37dbd8fca3e5b1db457560709bcdc17`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:4cecdea6552df534fc6ff5b0baf01df080318ad872171cb76d8d681529a60c69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **941.4 KB (941372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e5b13134ce9c59f59464dd153938abe2b1fb108f183574cf50f20c34593ab1`

```dockerfile
```

-	Layers:
	-	`sha256:24d2b9eb10c23f5c732a7e37c15a0f780289592f3ff141a1cf3aed71130b5200`  
		Last Modified: Thu, 25 Sep 2025 02:22:05 GMT  
		Size: 910.6 KB (910603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecc19b40f79ef646496790610a3aa4aeb69ed7919b9a4f647f14c2cd431b643e`  
		Last Modified: Thu, 25 Sep 2025 02:22:06 GMT  
		Size: 30.8 KB (30769 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7.12-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:c0b4bb9622f30c203d6164e4608265058ec2133de5fecec638a96afe1fc77b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78730374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3df955cee3af183aedd38baa540b6cf616ee4e64c4c7704593b9840e7e51c5b8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 30 Sep 2025 13:56:01 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxd"]
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 30 Sep 2025 13:56:01 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e9f8ae4bf7158674e53e799e39195db08dc922549798b1c92b5db881e75950`  
		Last Modified: Wed, 08 Oct 2025 21:55:31 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db47b23aa319f26ace574a307a140d466205a9c8792ea299825977016c72027`  
		Last Modified: Wed, 08 Oct 2025 21:55:32 GMT  
		Size: 9.8 MB (9822482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e75ad98f92c131cb2c24f50a1f955f559cb081760bb3ebaba411aff5652c0b1`  
		Last Modified: Wed, 08 Oct 2025 21:55:35 GMT  
		Size: 5.8 MB (5790429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0846ab0df2a8dd47b00f9e08910902bc9137be17fc01ecb2ab92865324a0a692`  
		Last Modified: Wed, 08 Oct 2025 21:55:31 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee341d51fc6d484c991e3e387ad2bab42cc99f8c5f0c144f3548538763046b7`  
		Last Modified: Wed, 08 Oct 2025 21:55:33 GMT  
		Size: 48.0 MB (48017161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5467babbc25c511c880690592c05bf5c8bf7eb3718a0ffcbb6bb66881d449be0`  
		Last Modified: Wed, 08 Oct 2025 21:55:31 GMT  
		Size: 11.1 MB (11099994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73275e145aac044b3ee173c0907851a448d495a9d0f964f1d943e707c8a79108`  
		Last Modified: Wed, 08 Oct 2025 21:55:31 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501e2a94b5ef2caef075bbdb0a7105d248f3f7d5e3a45540947b4843f21e8702`  
		Last Modified: Wed, 08 Oct 2025 21:55:31 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0bc70a0456678acb89ee83669fb653b9be40154e9167dec954aa525d35f87c`  
		Last Modified: Wed, 08 Oct 2025 21:55:31 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:c0855268e95dc31f5a9cac070c75e0c671fb7a46b90288fefc74be913b3869f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.0 KB (944029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f493a124da258c44e6401fe8b1e7f376cd7e326f841643ef5833690bb86f4d0`

```dockerfile
```

-	Layers:
	-	`sha256:0cf6c5db23c7a94944a2efa242d33b1a09e07eed2c284228b76d51eb51068db0`  
		Last Modified: Wed, 08 Oct 2025 23:20:42 GMT  
		Size: 913.1 KB (913066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:868968715be1dde5591f2d64233e6a60defbc05776d1a13313f5f018438e6317`  
		Last Modified: Wed, 08 Oct 2025 23:20:44 GMT  
		Size: 31.0 KB (30963 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3-core`

```console
$ docker pull influxdb@sha256:c2e66713994eb677dc8919c03183f8e72f0f2a5391f0385effb952ea4a5ee22c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-core` - linux; amd64

```console
$ docker pull influxdb@sha256:eed842ba953511c47fab71f2f9acaebf5be160d9925f9c86c138a6340bf1aa15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.6 MB (119567120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62ccbe635f0d9dba7479a2bf41f780d26f88686d59e5c9b26d1480460dfdb990`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ARG RELEASE
# Tue, 30 Sep 2025 13:56:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 13:56:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 13:56:01 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 13:56:01 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_VERSION=3.5.0
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
USER influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
ENV LOG_FILTER=info
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9176568c1617553edf67558c49e491d10a685caec2cabcde7badf3c31d36daf6`  
		Last Modified: Thu, 02 Oct 2025 05:08:57 GMT  
		Size: 9.1 MB (9070525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83dbc700e1f3c81457ac3fd53621f80aae3098733b2a6aa5ca495f817c216386`  
		Last Modified: Thu, 02 Oct 2025 05:08:57 GMT  
		Size: 3.7 KB (3651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a146783ab4238c6bcc86604065f3f72944c28b1692dea942fe4c74ec09cc68`  
		Last Modified: Thu, 02 Oct 2025 05:09:03 GMT  
		Size: 80.8 MB (80769459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c766f23747251da3c0ea145b697002e87f5d4dc9cc993b4acccded81cf96fb44`  
		Last Modified: Thu, 02 Oct 2025 05:08:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3078624a7100c87f1417e3a048571597be362dfc1e773ed287a8e0c8ccadc7`  
		Last Modified: Thu, 02 Oct 2025 05:08:56 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:bffdbe3c860936a003619729c6c6f15612f799293cda1b1f2814b0ea3edc220d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb47254a139f6e055600c78f729bb05e1cceeee8e89f63283c2bcd748a01a89`

```dockerfile
```

-	Layers:
	-	`sha256:6cd25241a212dc29b1d4b3bbca5d61a2f76af8fcdac65c7f9014c4a4f74b0a30`  
		Last Modified: Thu, 02 Oct 2025 08:20:29 GMT  
		Size: 2.3 MB (2311329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fabaf8ee19a8cf05b57e15eb77bb63a1c33619d3757294f5292aae118c3d899b`  
		Last Modified: Thu, 02 Oct 2025 08:20:30 GMT  
		Size: 17.6 KB (17592 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:f9a54d370efe6188b3e67bf87cc0ac4d71d9b54c8c7cacfa4b59f159314882ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (109968056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:006f1b55020c1065527d7627191c40214bf4e3c0c59d81667c3e8829376032aa`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ARG RELEASE
# Tue, 30 Sep 2025 13:56:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 13:56:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 13:56:01 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 13:56:01 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_VERSION=3.5.0
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
USER influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
ENV LOG_FILTER=info
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea3ce81d5c74d341a7b4d499f3300b3334181f3386be4d1a6ba7cc207f45395`  
		Last Modified: Thu, 02 Oct 2025 01:24:11 GMT  
		Size: 8.9 MB (8892539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e44e0ae2ff6215e6e8cd4c9c7c5d8395bded92266d2c617f26ff1881c424a3`  
		Last Modified: Thu, 02 Oct 2025 01:24:10 GMT  
		Size: 3.6 KB (3650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d67e730987d463c92b1d2df3dc077d09f61a3bc45fdb4b83e9a234c1f87015`  
		Last Modified: Thu, 02 Oct 2025 01:24:14 GMT  
		Size: 72.2 MB (72209818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa64fb052d027a6f2398fa436bd4c2af5b56e51b049e650f7682b0ddd2e4656`  
		Last Modified: Thu, 02 Oct 2025 01:24:10 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7797be8e2b564103a447e3b3d7d2c10a07b217a23f6c3f8f29a42c3ba1268f6b`  
		Last Modified: Thu, 02 Oct 2025 01:24:10 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:e6b90b6b3a85331f799afc01e5830d79472820bb1291d77a2fa06f227dd9cf6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13457de59bb0f322aef87f61b447049e5fc803dc8e541379fdd054bdd856bb25`

```dockerfile
```

-	Layers:
	-	`sha256:211894dff82c0b4bbf37a9017289b35947306e54d520618a3b9adcd5ad38cb1f`  
		Last Modified: Thu, 02 Oct 2025 05:20:35 GMT  
		Size: 2.3 MB (2312411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf852b6e2f2031b020c2ab1a8acd36c2b5c3036bfe587df3047f08ab63b50570`  
		Last Modified: Thu, 02 Oct 2025 05:20:37 GMT  
		Size: 17.7 KB (17741 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3-enterprise`

```console
$ docker pull influxdb@sha256:c75021ba18b0a86551b10593331b5606c16f778f3ae495b6f2212a4105ea3ff7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:6c51e7d7440be393d65bacf11e1475b5d18ea68f19640aa48c8485bd1aa3d94c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125829821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5624966dcf7c1d8813234fa587718f0a18345e13574a7319f6450500061ec8e5`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ARG RELEASE
# Tue, 30 Sep 2025 13:56:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 13:56:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 13:56:01 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 13:56:01 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_VERSION=3.5.0
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
USER influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
ENV LOG_FILTER=info
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58135b4742ad7ab7fde2d84ac35ffb70c4460efcece64c99429ab49fbfde1848`  
		Last Modified: Thu, 02 Oct 2025 05:09:01 GMT  
		Size: 9.1 MB (9070624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b822677ce7149474eb17d8b2bb719ab134b57dc258ac28e7306639e322d269f4`  
		Last Modified: Thu, 02 Oct 2025 05:08:58 GMT  
		Size: 3.7 KB (3653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6993110cfe96002dbe82f2970c92edeec13e4f3227d6d821c6ac05161b123eff`  
		Last Modified: Thu, 02 Oct 2025 05:09:07 GMT  
		Size: 87.0 MB (87032058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70c1dfab21ede393803c044cc98a552bae418dfe27a39434ccb11ac7c793420`  
		Last Modified: Thu, 02 Oct 2025 05:08:59 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852f3b98ef80c7ea583046ae0d2dff3a56afba76a621d57bc49c3ec7a2d18c18`  
		Last Modified: Thu, 02 Oct 2025 05:08:58 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:2fd31cf487e3fa050feccb33daeafe7214c7e7c9da14f4a339bdc089cd947aae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93dd7daeaf1bf16b43f23383d596816c3baa6adda8529774e61109568bf2a61f`

```dockerfile
```

-	Layers:
	-	`sha256:9a5906f2fb7d99e5a8b020d96e38421ddd6d1a0a8a9e93031bddc3bec9360d31`  
		Last Modified: Thu, 02 Oct 2025 08:20:34 GMT  
		Size: 2.3 MB (2311377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cbc20234791326927d74160ca6f5990c4e0e7834323da0032987cbadb671078`  
		Last Modified: Thu, 02 Oct 2025 08:20:35 GMT  
		Size: 17.8 KB (17772 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:4b65e4afa4793137b88565448d1c4b421a78dd4d9b88f052b4560f0de22ce84e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116158253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:090eb66a46758bb21e05ee0d374d333985b93c0d41ab42ebadb954f79283e7c5`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ARG RELEASE
# Tue, 30 Sep 2025 13:56:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 13:56:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 13:56:01 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 13:56:01 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_VERSION=3.5.0
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
USER influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
ENV LOG_FILTER=info
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeae1910013bf0e361618c72b829e50d3bbdaacb3ef7f87236a7b6704f1a5d39`  
		Last Modified: Thu, 02 Oct 2025 01:24:13 GMT  
		Size: 8.9 MB (8892549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d81e6ff420e726466d2e0e6c3f592d6f07918ddbdbec4c3a2cb6bd912cab10`  
		Last Modified: Thu, 02 Oct 2025 01:24:13 GMT  
		Size: 3.7 KB (3653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dcdaf2322d4771576222f45e766fe939f261778899a002599e6de2449ba6929`  
		Last Modified: Thu, 02 Oct 2025 01:24:21 GMT  
		Size: 78.4 MB (78400002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff341ebda249e4011610f56e3403de7087b365c184af05a201d8ed7ca79668f5`  
		Last Modified: Thu, 02 Oct 2025 01:24:13 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e955fdcba3a0d5795d6109eb17c028c1c3380f4e578b7ede2a271364d14638`  
		Last Modified: Thu, 02 Oct 2025 01:24:13 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:b4f68f62fb9ee3f9c0aeb74d6a20afb0b056ead3a0f2685bacbd9e172d4887ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:838b58787ab46cb6649eb50a038f2a0aea9fe89998d8f69a040e720f7c231bdd`

```dockerfile
```

-	Layers:
	-	`sha256:bf5b4a9c0694efeb04c36c74cfca0ef3ab0354cf22b8b25791734a26d57ba905`  
		Last Modified: Thu, 02 Oct 2025 05:20:38 GMT  
		Size: 2.3 MB (2312459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a01911d86f39a79e1ad18970ad82c646ab57e02b41ea0191902d18e773758793`  
		Last Modified: Thu, 02 Oct 2025 05:20:41 GMT  
		Size: 17.9 KB (17920 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.5-core`

```console
$ docker pull influxdb@sha256:c2e66713994eb677dc8919c03183f8e72f0f2a5391f0385effb952ea4a5ee22c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.5-core` - linux; amd64

```console
$ docker pull influxdb@sha256:eed842ba953511c47fab71f2f9acaebf5be160d9925f9c86c138a6340bf1aa15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.6 MB (119567120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62ccbe635f0d9dba7479a2bf41f780d26f88686d59e5c9b26d1480460dfdb990`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ARG RELEASE
# Tue, 30 Sep 2025 13:56:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 13:56:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 13:56:01 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 13:56:01 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_VERSION=3.5.0
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
USER influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
ENV LOG_FILTER=info
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9176568c1617553edf67558c49e491d10a685caec2cabcde7badf3c31d36daf6`  
		Last Modified: Thu, 02 Oct 2025 05:08:57 GMT  
		Size: 9.1 MB (9070525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83dbc700e1f3c81457ac3fd53621f80aae3098733b2a6aa5ca495f817c216386`  
		Last Modified: Thu, 02 Oct 2025 05:08:57 GMT  
		Size: 3.7 KB (3651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a146783ab4238c6bcc86604065f3f72944c28b1692dea942fe4c74ec09cc68`  
		Last Modified: Thu, 02 Oct 2025 05:09:03 GMT  
		Size: 80.8 MB (80769459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c766f23747251da3c0ea145b697002e87f5d4dc9cc993b4acccded81cf96fb44`  
		Last Modified: Thu, 02 Oct 2025 05:08:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3078624a7100c87f1417e3a048571597be362dfc1e773ed287a8e0c8ccadc7`  
		Last Modified: Thu, 02 Oct 2025 05:08:56 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.5-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:bffdbe3c860936a003619729c6c6f15612f799293cda1b1f2814b0ea3edc220d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb47254a139f6e055600c78f729bb05e1cceeee8e89f63283c2bcd748a01a89`

```dockerfile
```

-	Layers:
	-	`sha256:6cd25241a212dc29b1d4b3bbca5d61a2f76af8fcdac65c7f9014c4a4f74b0a30`  
		Last Modified: Thu, 02 Oct 2025 08:20:29 GMT  
		Size: 2.3 MB (2311329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fabaf8ee19a8cf05b57e15eb77bb63a1c33619d3757294f5292aae118c3d899b`  
		Last Modified: Thu, 02 Oct 2025 08:20:30 GMT  
		Size: 17.6 KB (17592 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.5-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:f9a54d370efe6188b3e67bf87cc0ac4d71d9b54c8c7cacfa4b59f159314882ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (109968056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:006f1b55020c1065527d7627191c40214bf4e3c0c59d81667c3e8829376032aa`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ARG RELEASE
# Tue, 30 Sep 2025 13:56:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 13:56:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 13:56:01 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 13:56:01 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_VERSION=3.5.0
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
USER influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
ENV LOG_FILTER=info
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea3ce81d5c74d341a7b4d499f3300b3334181f3386be4d1a6ba7cc207f45395`  
		Last Modified: Thu, 02 Oct 2025 01:24:11 GMT  
		Size: 8.9 MB (8892539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e44e0ae2ff6215e6e8cd4c9c7c5d8395bded92266d2c617f26ff1881c424a3`  
		Last Modified: Thu, 02 Oct 2025 01:24:10 GMT  
		Size: 3.6 KB (3650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d67e730987d463c92b1d2df3dc077d09f61a3bc45fdb4b83e9a234c1f87015`  
		Last Modified: Thu, 02 Oct 2025 01:24:14 GMT  
		Size: 72.2 MB (72209818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa64fb052d027a6f2398fa436bd4c2af5b56e51b049e650f7682b0ddd2e4656`  
		Last Modified: Thu, 02 Oct 2025 01:24:10 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7797be8e2b564103a447e3b3d7d2c10a07b217a23f6c3f8f29a42c3ba1268f6b`  
		Last Modified: Thu, 02 Oct 2025 01:24:10 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.5-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:e6b90b6b3a85331f799afc01e5830d79472820bb1291d77a2fa06f227dd9cf6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13457de59bb0f322aef87f61b447049e5fc803dc8e541379fdd054bdd856bb25`

```dockerfile
```

-	Layers:
	-	`sha256:211894dff82c0b4bbf37a9017289b35947306e54d520618a3b9adcd5ad38cb1f`  
		Last Modified: Thu, 02 Oct 2025 05:20:35 GMT  
		Size: 2.3 MB (2312411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf852b6e2f2031b020c2ab1a8acd36c2b5c3036bfe587df3047f08ab63b50570`  
		Last Modified: Thu, 02 Oct 2025 05:20:37 GMT  
		Size: 17.7 KB (17741 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.5-enterprise`

```console
$ docker pull influxdb@sha256:c75021ba18b0a86551b10593331b5606c16f778f3ae495b6f2212a4105ea3ff7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.5-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:6c51e7d7440be393d65bacf11e1475b5d18ea68f19640aa48c8485bd1aa3d94c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125829821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5624966dcf7c1d8813234fa587718f0a18345e13574a7319f6450500061ec8e5`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ARG RELEASE
# Tue, 30 Sep 2025 13:56:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 13:56:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 13:56:01 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 13:56:01 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_VERSION=3.5.0
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
USER influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
ENV LOG_FILTER=info
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58135b4742ad7ab7fde2d84ac35ffb70c4460efcece64c99429ab49fbfde1848`  
		Last Modified: Thu, 02 Oct 2025 05:09:01 GMT  
		Size: 9.1 MB (9070624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b822677ce7149474eb17d8b2bb719ab134b57dc258ac28e7306639e322d269f4`  
		Last Modified: Thu, 02 Oct 2025 05:08:58 GMT  
		Size: 3.7 KB (3653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6993110cfe96002dbe82f2970c92edeec13e4f3227d6d821c6ac05161b123eff`  
		Last Modified: Thu, 02 Oct 2025 05:09:07 GMT  
		Size: 87.0 MB (87032058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70c1dfab21ede393803c044cc98a552bae418dfe27a39434ccb11ac7c793420`  
		Last Modified: Thu, 02 Oct 2025 05:08:59 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852f3b98ef80c7ea583046ae0d2dff3a56afba76a621d57bc49c3ec7a2d18c18`  
		Last Modified: Thu, 02 Oct 2025 05:08:58 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.5-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:2fd31cf487e3fa050feccb33daeafe7214c7e7c9da14f4a339bdc089cd947aae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93dd7daeaf1bf16b43f23383d596816c3baa6adda8529774e61109568bf2a61f`

```dockerfile
```

-	Layers:
	-	`sha256:9a5906f2fb7d99e5a8b020d96e38421ddd6d1a0a8a9e93031bddc3bec9360d31`  
		Last Modified: Thu, 02 Oct 2025 08:20:34 GMT  
		Size: 2.3 MB (2311377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cbc20234791326927d74160ca6f5990c4e0e7834323da0032987cbadb671078`  
		Last Modified: Thu, 02 Oct 2025 08:20:35 GMT  
		Size: 17.8 KB (17772 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.5-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:4b65e4afa4793137b88565448d1c4b421a78dd4d9b88f052b4560f0de22ce84e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116158253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:090eb66a46758bb21e05ee0d374d333985b93c0d41ab42ebadb954f79283e7c5`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ARG RELEASE
# Tue, 30 Sep 2025 13:56:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 13:56:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 13:56:01 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 13:56:01 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_VERSION=3.5.0
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
USER influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
ENV LOG_FILTER=info
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeae1910013bf0e361618c72b829e50d3bbdaacb3ef7f87236a7b6704f1a5d39`  
		Last Modified: Thu, 02 Oct 2025 01:24:13 GMT  
		Size: 8.9 MB (8892549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d81e6ff420e726466d2e0e6c3f592d6f07918ddbdbec4c3a2cb6bd912cab10`  
		Last Modified: Thu, 02 Oct 2025 01:24:13 GMT  
		Size: 3.7 KB (3653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dcdaf2322d4771576222f45e766fe939f261778899a002599e6de2449ba6929`  
		Last Modified: Thu, 02 Oct 2025 01:24:21 GMT  
		Size: 78.4 MB (78400002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff341ebda249e4011610f56e3403de7087b365c184af05a201d8ed7ca79668f5`  
		Last Modified: Thu, 02 Oct 2025 01:24:13 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e955fdcba3a0d5795d6109eb17c028c1c3380f4e578b7ede2a271364d14638`  
		Last Modified: Thu, 02 Oct 2025 01:24:13 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.5-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:b4f68f62fb9ee3f9c0aeb74d6a20afb0b056ead3a0f2685bacbd9e172d4887ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:838b58787ab46cb6649eb50a038f2a0aea9fe89998d8f69a040e720f7c231bdd`

```dockerfile
```

-	Layers:
	-	`sha256:bf5b4a9c0694efeb04c36c74cfca0ef3ab0354cf22b8b25791734a26d57ba905`  
		Last Modified: Thu, 02 Oct 2025 05:20:38 GMT  
		Size: 2.3 MB (2312459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a01911d86f39a79e1ad18970ad82c646ab57e02b41ea0191902d18e773758793`  
		Last Modified: Thu, 02 Oct 2025 05:20:41 GMT  
		Size: 17.9 KB (17920 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.5.0-core`

```console
$ docker pull influxdb@sha256:c2e66713994eb677dc8919c03183f8e72f0f2a5391f0385effb952ea4a5ee22c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.5.0-core` - linux; amd64

```console
$ docker pull influxdb@sha256:eed842ba953511c47fab71f2f9acaebf5be160d9925f9c86c138a6340bf1aa15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.6 MB (119567120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62ccbe635f0d9dba7479a2bf41f780d26f88686d59e5c9b26d1480460dfdb990`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ARG RELEASE
# Tue, 30 Sep 2025 13:56:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 13:56:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 13:56:01 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 13:56:01 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_VERSION=3.5.0
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
USER influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
ENV LOG_FILTER=info
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9176568c1617553edf67558c49e491d10a685caec2cabcde7badf3c31d36daf6`  
		Last Modified: Thu, 02 Oct 2025 05:08:57 GMT  
		Size: 9.1 MB (9070525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83dbc700e1f3c81457ac3fd53621f80aae3098733b2a6aa5ca495f817c216386`  
		Last Modified: Thu, 02 Oct 2025 05:08:57 GMT  
		Size: 3.7 KB (3651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a146783ab4238c6bcc86604065f3f72944c28b1692dea942fe4c74ec09cc68`  
		Last Modified: Thu, 02 Oct 2025 05:09:03 GMT  
		Size: 80.8 MB (80769459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c766f23747251da3c0ea145b697002e87f5d4dc9cc993b4acccded81cf96fb44`  
		Last Modified: Thu, 02 Oct 2025 05:08:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3078624a7100c87f1417e3a048571597be362dfc1e773ed287a8e0c8ccadc7`  
		Last Modified: Thu, 02 Oct 2025 05:08:56 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.5.0-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:bffdbe3c860936a003619729c6c6f15612f799293cda1b1f2814b0ea3edc220d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb47254a139f6e055600c78f729bb05e1cceeee8e89f63283c2bcd748a01a89`

```dockerfile
```

-	Layers:
	-	`sha256:6cd25241a212dc29b1d4b3bbca5d61a2f76af8fcdac65c7f9014c4a4f74b0a30`  
		Last Modified: Thu, 02 Oct 2025 08:20:29 GMT  
		Size: 2.3 MB (2311329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fabaf8ee19a8cf05b57e15eb77bb63a1c33619d3757294f5292aae118c3d899b`  
		Last Modified: Thu, 02 Oct 2025 08:20:30 GMT  
		Size: 17.6 KB (17592 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.5.0-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:f9a54d370efe6188b3e67bf87cc0ac4d71d9b54c8c7cacfa4b59f159314882ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (109968056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:006f1b55020c1065527d7627191c40214bf4e3c0c59d81667c3e8829376032aa`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ARG RELEASE
# Tue, 30 Sep 2025 13:56:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 13:56:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 13:56:01 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 13:56:01 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_VERSION=3.5.0
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
USER influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
ENV LOG_FILTER=info
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea3ce81d5c74d341a7b4d499f3300b3334181f3386be4d1a6ba7cc207f45395`  
		Last Modified: Thu, 02 Oct 2025 01:24:11 GMT  
		Size: 8.9 MB (8892539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e44e0ae2ff6215e6e8cd4c9c7c5d8395bded92266d2c617f26ff1881c424a3`  
		Last Modified: Thu, 02 Oct 2025 01:24:10 GMT  
		Size: 3.6 KB (3650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d67e730987d463c92b1d2df3dc077d09f61a3bc45fdb4b83e9a234c1f87015`  
		Last Modified: Thu, 02 Oct 2025 01:24:14 GMT  
		Size: 72.2 MB (72209818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa64fb052d027a6f2398fa436bd4c2af5b56e51b049e650f7682b0ddd2e4656`  
		Last Modified: Thu, 02 Oct 2025 01:24:10 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7797be8e2b564103a447e3b3d7d2c10a07b217a23f6c3f8f29a42c3ba1268f6b`  
		Last Modified: Thu, 02 Oct 2025 01:24:10 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.5.0-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:e6b90b6b3a85331f799afc01e5830d79472820bb1291d77a2fa06f227dd9cf6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13457de59bb0f322aef87f61b447049e5fc803dc8e541379fdd054bdd856bb25`

```dockerfile
```

-	Layers:
	-	`sha256:211894dff82c0b4bbf37a9017289b35947306e54d520618a3b9adcd5ad38cb1f`  
		Last Modified: Thu, 02 Oct 2025 05:20:35 GMT  
		Size: 2.3 MB (2312411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf852b6e2f2031b020c2ab1a8acd36c2b5c3036bfe587df3047f08ab63b50570`  
		Last Modified: Thu, 02 Oct 2025 05:20:37 GMT  
		Size: 17.7 KB (17741 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.5.0-enterprise`

```console
$ docker pull influxdb@sha256:c75021ba18b0a86551b10593331b5606c16f778f3ae495b6f2212a4105ea3ff7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.5.0-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:6c51e7d7440be393d65bacf11e1475b5d18ea68f19640aa48c8485bd1aa3d94c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125829821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5624966dcf7c1d8813234fa587718f0a18345e13574a7319f6450500061ec8e5`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ARG RELEASE
# Tue, 30 Sep 2025 13:56:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 13:56:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 13:56:01 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 13:56:01 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_VERSION=3.5.0
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
USER influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
ENV LOG_FILTER=info
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58135b4742ad7ab7fde2d84ac35ffb70c4460efcece64c99429ab49fbfde1848`  
		Last Modified: Thu, 02 Oct 2025 05:09:01 GMT  
		Size: 9.1 MB (9070624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b822677ce7149474eb17d8b2bb719ab134b57dc258ac28e7306639e322d269f4`  
		Last Modified: Thu, 02 Oct 2025 05:08:58 GMT  
		Size: 3.7 KB (3653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6993110cfe96002dbe82f2970c92edeec13e4f3227d6d821c6ac05161b123eff`  
		Last Modified: Thu, 02 Oct 2025 05:09:07 GMT  
		Size: 87.0 MB (87032058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70c1dfab21ede393803c044cc98a552bae418dfe27a39434ccb11ac7c793420`  
		Last Modified: Thu, 02 Oct 2025 05:08:59 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852f3b98ef80c7ea583046ae0d2dff3a56afba76a621d57bc49c3ec7a2d18c18`  
		Last Modified: Thu, 02 Oct 2025 05:08:58 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.5.0-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:2fd31cf487e3fa050feccb33daeafe7214c7e7c9da14f4a339bdc089cd947aae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93dd7daeaf1bf16b43f23383d596816c3baa6adda8529774e61109568bf2a61f`

```dockerfile
```

-	Layers:
	-	`sha256:9a5906f2fb7d99e5a8b020d96e38421ddd6d1a0a8a9e93031bddc3bec9360d31`  
		Last Modified: Thu, 02 Oct 2025 08:20:34 GMT  
		Size: 2.3 MB (2311377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cbc20234791326927d74160ca6f5990c4e0e7834323da0032987cbadb671078`  
		Last Modified: Thu, 02 Oct 2025 08:20:35 GMT  
		Size: 17.8 KB (17772 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.5.0-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:4b65e4afa4793137b88565448d1c4b421a78dd4d9b88f052b4560f0de22ce84e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116158253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:090eb66a46758bb21e05ee0d374d333985b93c0d41ab42ebadb954f79283e7c5`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ARG RELEASE
# Tue, 30 Sep 2025 13:56:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 13:56:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 13:56:01 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 13:56:01 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_VERSION=3.5.0
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
USER influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
ENV LOG_FILTER=info
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeae1910013bf0e361618c72b829e50d3bbdaacb3ef7f87236a7b6704f1a5d39`  
		Last Modified: Thu, 02 Oct 2025 01:24:13 GMT  
		Size: 8.9 MB (8892549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d81e6ff420e726466d2e0e6c3f592d6f07918ddbdbec4c3a2cb6bd912cab10`  
		Last Modified: Thu, 02 Oct 2025 01:24:13 GMT  
		Size: 3.7 KB (3653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dcdaf2322d4771576222f45e766fe939f261778899a002599e6de2449ba6929`  
		Last Modified: Thu, 02 Oct 2025 01:24:21 GMT  
		Size: 78.4 MB (78400002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff341ebda249e4011610f56e3403de7087b365c184af05a201d8ed7ca79668f5`  
		Last Modified: Thu, 02 Oct 2025 01:24:13 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e955fdcba3a0d5795d6109eb17c028c1c3380f4e578b7ede2a271364d14638`  
		Last Modified: Thu, 02 Oct 2025 01:24:13 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.5.0-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:b4f68f62fb9ee3f9c0aeb74d6a20afb0b056ead3a0f2685bacbd9e172d4887ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:838b58787ab46cb6649eb50a038f2a0aea9fe89998d8f69a040e720f7c231bdd`

```dockerfile
```

-	Layers:
	-	`sha256:bf5b4a9c0694efeb04c36c74cfca0ef3ab0354cf22b8b25791734a26d57ba905`  
		Last Modified: Thu, 02 Oct 2025 05:20:38 GMT  
		Size: 2.3 MB (2312459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a01911d86f39a79e1ad18970ad82c646ab57e02b41ea0191902d18e773758793`  
		Last Modified: Thu, 02 Oct 2025 05:20:41 GMT  
		Size: 17.9 KB (17920 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:8fe50632b89ac1d44ae4875172d7017113635a537548037f7b66d62e603cc527
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:cff6f2ab47c82bede8226eaa115bb26a3c6b687ca6d1600c4daf951debdab495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.5 MB (81514718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e97594fdb74be0f41ef523f1d997467fd03327d8d08cfda4c4ac4e33bf5a76b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 24 Sep 2025 16:08:46 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 24 Sep 2025 16:08:46 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 24 Sep 2025 16:08:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Sep 2025 16:08:46 GMT
CMD ["influxd"]
# Wed, 24 Sep 2025 16:08:46 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 24 Sep 2025 16:08:46 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 24 Sep 2025 16:08:46 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0a8ae42cc4bbee908d14c07fc4ec8c8407af6310249f9dfeae0f8509bdc7af`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c7bfad06ee97b9a79123f8649a25c2c85621f43c09f683fc22058f5a07f5d6`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 9.8 MB (9819983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a34cab64443b962a114bd2a6beffb95756ba52160469829a5d45a76fcba800`  
		Last Modified: Thu, 25 Sep 2025 01:11:54 GMT  
		Size: 6.2 MB (6156990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a8939940eb42b2ce365e0ace1c34d67dbdaf70d81621f34c5fca12f3bfd8f7`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda56c435bfb0f3172c6ba8994e754a3757983ee0517a7f6b2584a903a27e12e`  
		Last Modified: Thu, 25 Sep 2025 01:11:57 GMT  
		Size: 50.1 MB (50118442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5092574230696c38c9b6d5e80c3b0052a6775a347fc390fb3ddfbed0312b110b`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 11.8 MB (11773781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6964e799275484d75822451544c8b8aeb0525a898edf53d62dc5b2bea9ec4f23`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07acd36aa62e4aa31c3926c29dbc6d78b9952999a9f6d5a20d03ad2ac4ce55cd`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2256c74f4ebf0907ad02de26150d5f5f37dbd8fca3e5b1db457560709bcdc17`  
		Last Modified: Thu, 25 Sep 2025 01:11:53 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:4cecdea6552df534fc6ff5b0baf01df080318ad872171cb76d8d681529a60c69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **941.4 KB (941372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e5b13134ce9c59f59464dd153938abe2b1fb108f183574cf50f20c34593ab1`

```dockerfile
```

-	Layers:
	-	`sha256:24d2b9eb10c23f5c732a7e37c15a0f780289592f3ff141a1cf3aed71130b5200`  
		Last Modified: Thu, 25 Sep 2025 02:22:05 GMT  
		Size: 910.6 KB (910603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecc19b40f79ef646496790610a3aa4aeb69ed7919b9a4f647f14c2cd431b643e`  
		Last Modified: Thu, 25 Sep 2025 02:22:06 GMT  
		Size: 30.8 KB (30769 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:c0b4bb9622f30c203d6164e4608265058ec2133de5fecec638a96afe1fc77b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78730374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3df955cee3af183aedd38baa540b6cf616ee4e64c4c7704593b9840e7e51c5b8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 30 Sep 2025 13:56:01 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxd"]
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 30 Sep 2025 13:56:01 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e9f8ae4bf7158674e53e799e39195db08dc922549798b1c92b5db881e75950`  
		Last Modified: Wed, 08 Oct 2025 21:55:31 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db47b23aa319f26ace574a307a140d466205a9c8792ea299825977016c72027`  
		Last Modified: Wed, 08 Oct 2025 21:55:32 GMT  
		Size: 9.8 MB (9822482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e75ad98f92c131cb2c24f50a1f955f559cb081760bb3ebaba411aff5652c0b1`  
		Last Modified: Wed, 08 Oct 2025 21:55:35 GMT  
		Size: 5.8 MB (5790429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0846ab0df2a8dd47b00f9e08910902bc9137be17fc01ecb2ab92865324a0a692`  
		Last Modified: Wed, 08 Oct 2025 21:55:31 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee341d51fc6d484c991e3e387ad2bab42cc99f8c5f0c144f3548538763046b7`  
		Last Modified: Wed, 08 Oct 2025 21:55:33 GMT  
		Size: 48.0 MB (48017161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5467babbc25c511c880690592c05bf5c8bf7eb3718a0ffcbb6bb66881d449be0`  
		Last Modified: Wed, 08 Oct 2025 21:55:31 GMT  
		Size: 11.1 MB (11099994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73275e145aac044b3ee173c0907851a448d495a9d0f964f1d943e707c8a79108`  
		Last Modified: Wed, 08 Oct 2025 21:55:31 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501e2a94b5ef2caef075bbdb0a7105d248f3f7d5e3a45540947b4843f21e8702`  
		Last Modified: Wed, 08 Oct 2025 21:55:31 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0bc70a0456678acb89ee83669fb653b9be40154e9167dec954aa525d35f87c`  
		Last Modified: Wed, 08 Oct 2025 21:55:31 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:c0855268e95dc31f5a9cac070c75e0c671fb7a46b90288fefc74be913b3869f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.0 KB (944029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f493a124da258c44e6401fe8b1e7f376cd7e326f841643ef5833690bb86f4d0`

```dockerfile
```

-	Layers:
	-	`sha256:0cf6c5db23c7a94944a2efa242d33b1a09e07eed2c284228b76d51eb51068db0`  
		Last Modified: Wed, 08 Oct 2025 23:20:42 GMT  
		Size: 913.1 KB (913066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:868968715be1dde5591f2d64233e6a60defbc05776d1a13313f5f018438e6317`  
		Last Modified: Wed, 08 Oct 2025 23:20:44 GMT  
		Size: 31.0 KB (30963 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:core`

```console
$ docker pull influxdb@sha256:c2e66713994eb677dc8919c03183f8e72f0f2a5391f0385effb952ea4a5ee22c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:core` - linux; amd64

```console
$ docker pull influxdb@sha256:eed842ba953511c47fab71f2f9acaebf5be160d9925f9c86c138a6340bf1aa15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.6 MB (119567120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62ccbe635f0d9dba7479a2bf41f780d26f88686d59e5c9b26d1480460dfdb990`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ARG RELEASE
# Tue, 30 Sep 2025 13:56:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 13:56:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 13:56:01 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 13:56:01 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_VERSION=3.5.0
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
USER influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
ENV LOG_FILTER=info
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9176568c1617553edf67558c49e491d10a685caec2cabcde7badf3c31d36daf6`  
		Last Modified: Thu, 02 Oct 2025 05:08:57 GMT  
		Size: 9.1 MB (9070525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83dbc700e1f3c81457ac3fd53621f80aae3098733b2a6aa5ca495f817c216386`  
		Last Modified: Thu, 02 Oct 2025 05:08:57 GMT  
		Size: 3.7 KB (3651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a146783ab4238c6bcc86604065f3f72944c28b1692dea942fe4c74ec09cc68`  
		Last Modified: Thu, 02 Oct 2025 05:09:03 GMT  
		Size: 80.8 MB (80769459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c766f23747251da3c0ea145b697002e87f5d4dc9cc993b4acccded81cf96fb44`  
		Last Modified: Thu, 02 Oct 2025 05:08:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3078624a7100c87f1417e3a048571597be362dfc1e773ed287a8e0c8ccadc7`  
		Last Modified: Thu, 02 Oct 2025 05:08:56 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:bffdbe3c860936a003619729c6c6f15612f799293cda1b1f2814b0ea3edc220d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb47254a139f6e055600c78f729bb05e1cceeee8e89f63283c2bcd748a01a89`

```dockerfile
```

-	Layers:
	-	`sha256:6cd25241a212dc29b1d4b3bbca5d61a2f76af8fcdac65c7f9014c4a4f74b0a30`  
		Last Modified: Thu, 02 Oct 2025 08:20:29 GMT  
		Size: 2.3 MB (2311329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fabaf8ee19a8cf05b57e15eb77bb63a1c33619d3757294f5292aae118c3d899b`  
		Last Modified: Thu, 02 Oct 2025 08:20:30 GMT  
		Size: 17.6 KB (17592 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:f9a54d370efe6188b3e67bf87cc0ac4d71d9b54c8c7cacfa4b59f159314882ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (109968056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:006f1b55020c1065527d7627191c40214bf4e3c0c59d81667c3e8829376032aa`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ARG RELEASE
# Tue, 30 Sep 2025 13:56:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 13:56:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 13:56:01 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 13:56:01 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_VERSION=3.5.0
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
USER influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
ENV LOG_FILTER=info
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea3ce81d5c74d341a7b4d499f3300b3334181f3386be4d1a6ba7cc207f45395`  
		Last Modified: Thu, 02 Oct 2025 01:24:11 GMT  
		Size: 8.9 MB (8892539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e44e0ae2ff6215e6e8cd4c9c7c5d8395bded92266d2c617f26ff1881c424a3`  
		Last Modified: Thu, 02 Oct 2025 01:24:10 GMT  
		Size: 3.6 KB (3650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d67e730987d463c92b1d2df3dc077d09f61a3bc45fdb4b83e9a234c1f87015`  
		Last Modified: Thu, 02 Oct 2025 01:24:14 GMT  
		Size: 72.2 MB (72209818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa64fb052d027a6f2398fa436bd4c2af5b56e51b049e650f7682b0ddd2e4656`  
		Last Modified: Thu, 02 Oct 2025 01:24:10 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7797be8e2b564103a447e3b3d7d2c10a07b217a23f6c3f8f29a42c3ba1268f6b`  
		Last Modified: Thu, 02 Oct 2025 01:24:10 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:e6b90b6b3a85331f799afc01e5830d79472820bb1291d77a2fa06f227dd9cf6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13457de59bb0f322aef87f61b447049e5fc803dc8e541379fdd054bdd856bb25`

```dockerfile
```

-	Layers:
	-	`sha256:211894dff82c0b4bbf37a9017289b35947306e54d520618a3b9adcd5ad38cb1f`  
		Last Modified: Thu, 02 Oct 2025 05:20:35 GMT  
		Size: 2.3 MB (2312411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf852b6e2f2031b020c2ab1a8acd36c2b5c3036bfe587df3047f08ab63b50570`  
		Last Modified: Thu, 02 Oct 2025 05:20:37 GMT  
		Size: 17.7 KB (17741 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:enterprise`

```console
$ docker pull influxdb@sha256:c75021ba18b0a86551b10593331b5606c16f778f3ae495b6f2212a4105ea3ff7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:6c51e7d7440be393d65bacf11e1475b5d18ea68f19640aa48c8485bd1aa3d94c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125829821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5624966dcf7c1d8813234fa587718f0a18345e13574a7319f6450500061ec8e5`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ARG RELEASE
# Tue, 30 Sep 2025 13:56:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 13:56:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 13:56:01 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 13:56:01 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_VERSION=3.5.0
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
USER influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
ENV LOG_FILTER=info
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58135b4742ad7ab7fde2d84ac35ffb70c4460efcece64c99429ab49fbfde1848`  
		Last Modified: Thu, 02 Oct 2025 05:09:01 GMT  
		Size: 9.1 MB (9070624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b822677ce7149474eb17d8b2bb719ab134b57dc258ac28e7306639e322d269f4`  
		Last Modified: Thu, 02 Oct 2025 05:08:58 GMT  
		Size: 3.7 KB (3653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6993110cfe96002dbe82f2970c92edeec13e4f3227d6d821c6ac05161b123eff`  
		Last Modified: Thu, 02 Oct 2025 05:09:07 GMT  
		Size: 87.0 MB (87032058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70c1dfab21ede393803c044cc98a552bae418dfe27a39434ccb11ac7c793420`  
		Last Modified: Thu, 02 Oct 2025 05:08:59 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852f3b98ef80c7ea583046ae0d2dff3a56afba76a621d57bc49c3ec7a2d18c18`  
		Last Modified: Thu, 02 Oct 2025 05:08:58 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:2fd31cf487e3fa050feccb33daeafe7214c7e7c9da14f4a339bdc089cd947aae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93dd7daeaf1bf16b43f23383d596816c3baa6adda8529774e61109568bf2a61f`

```dockerfile
```

-	Layers:
	-	`sha256:9a5906f2fb7d99e5a8b020d96e38421ddd6d1a0a8a9e93031bddc3bec9360d31`  
		Last Modified: Thu, 02 Oct 2025 08:20:34 GMT  
		Size: 2.3 MB (2311377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cbc20234791326927d74160ca6f5990c4e0e7834323da0032987cbadb671078`  
		Last Modified: Thu, 02 Oct 2025 08:20:35 GMT  
		Size: 17.8 KB (17772 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:4b65e4afa4793137b88565448d1c4b421a78dd4d9b88f052b4560f0de22ce84e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116158253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:090eb66a46758bb21e05ee0d374d333985b93c0d41ab42ebadb954f79283e7c5`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ARG RELEASE
# Tue, 30 Sep 2025 13:56:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 13:56:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 13:56:01 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 13:56:01 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_VERSION=3.5.0
# Tue, 30 Sep 2025 13:56:01 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
USER influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 30 Sep 2025 13:56:01 GMT
ENV LOG_FILTER=info
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeae1910013bf0e361618c72b829e50d3bbdaacb3ef7f87236a7b6704f1a5d39`  
		Last Modified: Thu, 02 Oct 2025 01:24:13 GMT  
		Size: 8.9 MB (8892549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d81e6ff420e726466d2e0e6c3f592d6f07918ddbdbec4c3a2cb6bd912cab10`  
		Last Modified: Thu, 02 Oct 2025 01:24:13 GMT  
		Size: 3.7 KB (3653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dcdaf2322d4771576222f45e766fe939f261778899a002599e6de2449ba6929`  
		Last Modified: Thu, 02 Oct 2025 01:24:21 GMT  
		Size: 78.4 MB (78400002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff341ebda249e4011610f56e3403de7087b365c184af05a201d8ed7ca79668f5`  
		Last Modified: Thu, 02 Oct 2025 01:24:13 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e955fdcba3a0d5795d6109eb17c028c1c3380f4e578b7ede2a271364d14638`  
		Last Modified: Thu, 02 Oct 2025 01:24:13 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:b4f68f62fb9ee3f9c0aeb74d6a20afb0b056ead3a0f2685bacbd9e172d4887ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:838b58787ab46cb6649eb50a038f2a0aea9fe89998d8f69a040e720f7c231bdd`

```dockerfile
```

-	Layers:
	-	`sha256:bf5b4a9c0694efeb04c36c74cfca0ef3ab0354cf22b8b25791734a26d57ba905`  
		Last Modified: Thu, 02 Oct 2025 05:20:38 GMT  
		Size: 2.3 MB (2312459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a01911d86f39a79e1ad18970ad82c646ab57e02b41ea0191902d18e773758793`  
		Last Modified: Thu, 02 Oct 2025 05:20:41 GMT  
		Size: 17.9 KB (17920 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:latest`

```console
$ docker pull influxdb@sha256:674911452ada77ca762662d50dd0594c8823312f59b376500623a4f82c44f9be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:0121b1ef000ad9ee6fd18236fbda5b578e2d2b53ebf88b2852a5df1a2e6b88d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157221895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c729c6b61bf04bccae282b4a88b0af07233b54566c44357100bb3f1f93d5bb09`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 25 Sep 2025 13:45:30 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Thu, 25 Sep 2025 13:45:30 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENV GOSU_VER=1.16
# Thu, 25 Sep 2025 13:45:30 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUXDB_VERSION=2.7.12
# Thu, 25 Sep 2025 13:45:30 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Thu, 25 Sep 2025 13:45:30 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 25 Sep 2025 13:45:30 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Sep 2025 13:45:30 GMT
CMD ["influxd"]
# Thu, 25 Sep 2025 13:45:30 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 25 Sep 2025 13:45:30 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811aaf99bbf19a9910d62277e035aceff4198c7f376b20d593edff533f641d1d`  
		Last Modified: Tue, 30 Sep 2025 00:13:36 GMT  
		Size: 9.8 MB (9796261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343156d2f44315d2944d689a3b6ba5fb12db96d0735c74f9f5061dadaa5ee050`  
		Last Modified: Tue, 30 Sep 2025 00:13:36 GMT  
		Size: 6.2 MB (6156974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45de5a0fe55cef8d3934d43433657930fba76ec5ddc4d981cdb77a35dabec0f0`  
		Last Modified: Tue, 30 Sep 2025 01:05:33 GMT  
		Size: 3.2 KB (3224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17580cec1ecab1149b131bab26b9ef493f6544152e36e43a4a8fda262ad2f742`  
		Last Modified: Tue, 30 Sep 2025 01:05:33 GMT  
		Size: 1.0 MB (1012036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33043d02209c6f842255867f3e7a3cad421ba64cbeb2927ddda8ceb54856a854`  
		Last Modified: Wed, 01 Oct 2025 14:21:09 GMT  
		Size: 100.2 MB (100244546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed0f8fa108abae31ed054ba64b943b34c7f988766fc3cabc0fce10f5829c87f`  
		Last Modified: Wed, 01 Oct 2025 14:21:07 GMT  
		Size: 11.8 MB (11773790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6a602b2831120358c8dc7d1f25aeef36e9c54553e633ad61ab3fb092c94ab2`  
		Last Modified: Tue, 30 Sep 2025 01:05:32 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e85a2aece113cd4582f9805ef8101ef31daf5e4fa684167883c30011b7c0606`  
		Last Modified: Tue, 30 Sep 2025 01:05:33 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf6f0e586b1a73cc1ab4ccebc8f1a38ca717d394b624b137718be85c1bbeeeb`  
		Last Modified: Tue, 30 Sep 2025 01:05:32 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:185b77ece5df1f271f383b88de53edf5a6de19f2ffe13d95248ad30a48bc316d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3015606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd30accab1f61a0131fa41611377459c8480e8dd58fe1768c27ca200763ac693`

```dockerfile
```

-	Layers:
	-	`sha256:92d23af2aaf90e882cd2ebd504b46e52e629c0f42394d304d6939d7b8560f61f`  
		Last Modified: Wed, 01 Oct 2025 14:21:04 GMT  
		Size: 3.0 MB (2982068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e33518cd60ed9dd866b1f385742a274e53eecdf30023662122b59428aedd35a`  
		Last Modified: Wed, 01 Oct 2025 14:21:05 GMT  
		Size: 33.5 KB (33538 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:8082b154781eaebf6a996ea7d6b8e168f75791852a0ada8a91170a1c2d47b6d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151606772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1af681f1c20860f9abf95e03acb5611917958551f8ba30ec43ec3f23b6058c42`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 25 Sep 2025 13:45:30 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Thu, 25 Sep 2025 13:45:30 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENV GOSU_VER=1.16
# Thu, 25 Sep 2025 13:45:30 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUXDB_VERSION=2.7.12
# Thu, 25 Sep 2025 13:45:30 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Thu, 25 Sep 2025 13:45:30 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 25 Sep 2025 13:45:30 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 13:45:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 25 Sep 2025 13:45:30 GMT
CMD ["influxd"]
# Thu, 25 Sep 2025 13:45:30 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 25 Sep 2025 13:45:30 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 25 Sep 2025 13:45:30 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082090d89175918857dcc8282e145311f059b5b017dc01f9a6121a6b278a9487`  
		Last Modified: Tue, 30 Sep 2025 00:17:38 GMT  
		Size: 9.6 MB (9626389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cebe74b7eaf8b3bc1b970e333e60268a909d8d3552e00442ad46718221c4c732`  
		Last Modified: Tue, 30 Sep 2025 00:17:40 GMT  
		Size: 5.8 MB (5790423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6360dbdbebcd1552db8e529acc86ead1dd06ff0fc6d02b4edfd492fb84f4f4`  
		Last Modified: Tue, 30 Sep 2025 00:17:39 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5cfca2c3199900213baadd0d387cbd6a978c4b499f7a754544c87f215d91eb3`  
		Last Modified: Tue, 30 Sep 2025 00:17:40 GMT  
		Size: 938.9 KB (938877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9236bff4709329221210f80370f34d8143cba158e827d1b7d5befc8bbe5ab87e`  
		Last Modified: Tue, 30 Sep 2025 00:17:51 GMT  
		Size: 96.0 MB (96038992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ded161eaa69ae91d1d7bf0c155e1d1facb0eaf2ef3c6cfb520c40024f5b8d36`  
		Last Modified: Tue, 30 Sep 2025 00:17:43 GMT  
		Size: 11.1 MB (11099994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd77ea3562d6f2442138d60ad311221076c2d671d1166ce9dbe1eb17e371ce97`  
		Last Modified: Tue, 30 Sep 2025 00:17:41 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2de2120c066eb9a1231dd3d23cbcacb1f194daf4995009e45c695157b6e026`  
		Last Modified: Tue, 30 Sep 2025 00:17:42 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9972a62410f906ab8092ded9c34d97da94f43fc95a74e0a9b46a2147c441b81`  
		Last Modified: Tue, 30 Sep 2025 00:17:35 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:93465f8e0525b500bcf956c05920220caa5ba91b14b2ec23e6c8b00482747995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3015017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfcabdba78ebb2d6a410efdb1679524330e6bda30e8238df63bc5a929b35bdac`

```dockerfile
```

-	Layers:
	-	`sha256:c62b73da34672ba9622e16b068686545412cc06cec03c481b03e578626525369`  
		Last Modified: Wed, 01 Oct 2025 11:35:02 GMT  
		Size: 3.0 MB (2981296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bece50323750999f98c31f931dd719c0349234cc48534b78d16dbb5110054b39`  
		Last Modified: Wed, 01 Oct 2025 11:35:03 GMT  
		Size: 33.7 KB (33721 bytes)  
		MIME: application/vnd.in-toto+json
