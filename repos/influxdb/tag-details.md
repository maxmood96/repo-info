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
$ docker pull influxdb@sha256:9bb0359a467ca7b5c184a717ae2c82f04e445afa639aa4d4929fc92900321b77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:48f02098c2e15b7148d5b0452a712bffc11409db9f3ffef5cd047afc6fcbbd86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42924335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd87858dca357f6e0d56e0a56ce27b47c250fffde09e3dff67f271a6ad895f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
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
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c266adf412b1887190bc0baa2363569b9d17f4e6d5ef01303411eeece661fe2`  
		Last Modified: Wed, 08 Oct 2025 23:10:24 GMT  
		Size: 1.2 MB (1224596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2286d3bdb9b240a8e73a50cc45ff08cac484d9bd916b7c2731d29c6781731f1`  
		Last Modified: Wed, 08 Oct 2025 23:10:32 GMT  
		Size: 38.1 MB (38069965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bd812bdffaf5a51fdc5ad2690ccb55dec4a092395243bf366e01cf45511ac7`  
		Last Modified: Wed, 08 Oct 2025 23:10:24 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ccae7d91ef8bb0ea37a95450db36eaa796c974b09f7a0589106acf87072085a`  
		Last Modified: Wed, 08 Oct 2025 23:10:24 GMT  
		Size: 1.0 KB (1004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce755337386479f3084609d415719dae3d4f17e49deeb6a099a77ddeca8e2cb`  
		Last Modified: Wed, 08 Oct 2025 23:10:24 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e2d3d495f76618c744d89e0710cd06db610e65e6019e022899e6a4de4fc2e2`  
		Last Modified: Wed, 08 Oct 2025 23:10:25 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:fa2d956e3f54c6a408c1f5844bf99a56f23140b31f97da560a8f5eb12da7bddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.4 KB (760359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8057230e97272f215cdf8d5d7c57b1a6ab77033334af884fc23310fb7652f99`

```dockerfile
```

-	Layers:
	-	`sha256:310a89661a2fc7900bdde751ff701074d5950205f4b15a793563694b2d2d013f`  
		Last Modified: Thu, 09 Oct 2025 02:20:19 GMT  
		Size: 742.5 KB (742482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2c6fe293831b00cc186f0ab8fd0030085d57e84e8eeb22c232095ac36d6ccd8`  
		Last Modified: Thu, 09 Oct 2025 02:20:19 GMT  
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
$ docker pull influxdb@sha256:7d22b120047d2262986edb6e3fc053cf7bd34118239f4bc4843f4dd9541dacca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:e19598cc857486b7eb06bd5b360851040766115ed76d0c619905728a5fb45244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (46959618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:706cdd4b67ccf9beb18d1345a260789466ed4d29b5324f0dc892f55571615da4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Tue, 30 Sep 2025 13:56:01 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b7c681266c61781b5e9483f43fa6ad59b0acafe3c400aa10ba1e43ec0963a0`  
		Last Modified: Wed, 08 Oct 2025 23:10:23 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b114d197f0b29a6932d8b9d445b0628a19b4157668f6eb76571600ecaf25723`  
		Last Modified: Wed, 08 Oct 2025 23:10:23 GMT  
		Size: 1.2 MB (1224592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3358124fd2820053c690bcf986afef42d2564531fcff8ba0b814614bc23b3bbe`  
		Last Modified: Wed, 08 Oct 2025 23:10:30 GMT  
		Size: 42.1 MB (42105919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63d4466a6a2e285d8482d3dce7c47f8f5a2bbdf6c366916cfb45ea2790337a9`  
		Last Modified: Wed, 08 Oct 2025 23:10:24 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e120ca154a1d12d672fecfc7212adcc4973d001dce2328028c3ab256b7f20b9`  
		Last Modified: Wed, 08 Oct 2025 23:10:23 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a0d8b4e8d0cf5b5a88b2dc5d203d42a530f015d833f41790286c1098b9be04`  
		Last Modified: Wed, 08 Oct 2025 23:10:24 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:34ac15f902b8907e65c3ec4432f28b3de55ac12f03c7b79ed9632454675063bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.6 KB (785632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a0fd5325de66f35f4367c4e1892be82ff21cf5a48e19fabc9888a783ba6cdc`

```dockerfile
```

-	Layers:
	-	`sha256:42b8f7363028d21427e8f398bac58ecff5c02cec3eac379e0dce85371a26fb2a`  
		Last Modified: Thu, 09 Oct 2025 02:20:24 GMT  
		Size: 769.0 KB (768993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95c8c2a7537102693c04e00ab640a007908a8cdec2fa3201d77b6b835d83c362`  
		Last Modified: Thu, 09 Oct 2025 02:20:25 GMT  
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
$ docker pull influxdb@sha256:3786c85254cdf499b874b247ec0b7fdd5ef8af5fbd719df6e5ee06f066500955
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:6c020578fb9c06bd21f4356170c21bd5ef4274dc05fa08e82e63e8d94f4d3c22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23402378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bcd086cb1f86062412478c7ed47e21bae8a3aba6b6d2e9ea20d2fed8e1988b6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Tue, 30 Sep 2025 13:56:01 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af74a58a446b59e39793a690435f78e585a91ea73edb6406a99a3283db12a3a2`  
		Last Modified: Wed, 08 Oct 2025 23:01:06 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be22d087a3e55404f6a8b32177effbd6c3829e421c0b5ef02b11b38be4785b3`  
		Last Modified: Wed, 08 Oct 2025 23:10:28 GMT  
		Size: 1.2 MB (1224606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d72c9781c814dfaa052605afbb9e8d8be20811f6843ddb55b2cc0645fd96a7`  
		Last Modified: Wed, 08 Oct 2025 23:10:30 GMT  
		Size: 18.5 MB (18549871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66e2e10d6786167404e416ab04e6d4485db03583db3118244df06813625bad4`  
		Last Modified: Wed, 08 Oct 2025 23:10:28 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1362d7c20d172d913583e0a7dd8615a994bb4d5c13a7df7265d4dd009dfdbe`  
		Last Modified: Wed, 08 Oct 2025 23:10:28 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:f5c20e593d6fa019a8d711341d1462f293da3418f4c51358c6c7711eca95aa56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.6 KB (691632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff4aaa72e275158f64bdb7a0e14b89336f3793f64bf51dbab7320f83a05f3d8d`

```dockerfile
```

-	Layers:
	-	`sha256:0ad0a9d5310a18e73a4f13e3fe81fc690a2e3fa594fdf23fba47d3e7b5528e9f`  
		Last Modified: Thu, 09 Oct 2025 02:20:30 GMT  
		Size: 676.6 KB (676622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24dde11f34792d696d7baefa980d47a9bb0ec06c1640475e5f37e93aa05a49ae`  
		Last Modified: Thu, 09 Oct 2025 02:20:30 GMT  
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
$ docker pull influxdb@sha256:9bb0359a467ca7b5c184a717ae2c82f04e445afa639aa4d4929fc92900321b77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11.8-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:48f02098c2e15b7148d5b0452a712bffc11409db9f3ffef5cd047afc6fcbbd86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42924335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd87858dca357f6e0d56e0a56ce27b47c250fffde09e3dff67f271a6ad895f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
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
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c266adf412b1887190bc0baa2363569b9d17f4e6d5ef01303411eeece661fe2`  
		Last Modified: Wed, 08 Oct 2025 23:10:24 GMT  
		Size: 1.2 MB (1224596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2286d3bdb9b240a8e73a50cc45ff08cac484d9bd916b7c2731d29c6781731f1`  
		Last Modified: Wed, 08 Oct 2025 23:10:32 GMT  
		Size: 38.1 MB (38069965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bd812bdffaf5a51fdc5ad2690ccb55dec4a092395243bf366e01cf45511ac7`  
		Last Modified: Wed, 08 Oct 2025 23:10:24 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ccae7d91ef8bb0ea37a95450db36eaa796c974b09f7a0589106acf87072085a`  
		Last Modified: Wed, 08 Oct 2025 23:10:24 GMT  
		Size: 1.0 KB (1004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce755337386479f3084609d415719dae3d4f17e49deeb6a099a77ddeca8e2cb`  
		Last Modified: Wed, 08 Oct 2025 23:10:24 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e2d3d495f76618c744d89e0710cd06db610e65e6019e022899e6a4de4fc2e2`  
		Last Modified: Wed, 08 Oct 2025 23:10:25 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:fa2d956e3f54c6a408c1f5844bf99a56f23140b31f97da560a8f5eb12da7bddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.4 KB (760359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8057230e97272f215cdf8d5d7c57b1a6ab77033334af884fc23310fb7652f99`

```dockerfile
```

-	Layers:
	-	`sha256:310a89661a2fc7900bdde751ff701074d5950205f4b15a793563694b2d2d013f`  
		Last Modified: Thu, 09 Oct 2025 02:20:19 GMT  
		Size: 742.5 KB (742482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2c6fe293831b00cc186f0ab8fd0030085d57e84e8eeb22c232095ac36d6ccd8`  
		Last Modified: Thu, 09 Oct 2025 02:20:19 GMT  
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
$ docker pull influxdb@sha256:7d22b120047d2262986edb6e3fc053cf7bd34118239f4bc4843f4dd9541dacca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.9-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:e19598cc857486b7eb06bd5b360851040766115ed76d0c619905728a5fb45244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (46959618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:706cdd4b67ccf9beb18d1345a260789466ed4d29b5324f0dc892f55571615da4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Tue, 30 Sep 2025 13:56:01 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b7c681266c61781b5e9483f43fa6ad59b0acafe3c400aa10ba1e43ec0963a0`  
		Last Modified: Wed, 08 Oct 2025 23:10:23 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b114d197f0b29a6932d8b9d445b0628a19b4157668f6eb76571600ecaf25723`  
		Last Modified: Wed, 08 Oct 2025 23:10:23 GMT  
		Size: 1.2 MB (1224592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3358124fd2820053c690bcf986afef42d2564531fcff8ba0b814614bc23b3bbe`  
		Last Modified: Wed, 08 Oct 2025 23:10:30 GMT  
		Size: 42.1 MB (42105919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63d4466a6a2e285d8482d3dce7c47f8f5a2bbdf6c366916cfb45ea2790337a9`  
		Last Modified: Wed, 08 Oct 2025 23:10:24 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e120ca154a1d12d672fecfc7212adcc4973d001dce2328028c3ab256b7f20b9`  
		Last Modified: Wed, 08 Oct 2025 23:10:23 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a0d8b4e8d0cf5b5a88b2dc5d203d42a530f015d833f41790286c1098b9be04`  
		Last Modified: Wed, 08 Oct 2025 23:10:24 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.9-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:34ac15f902b8907e65c3ec4432f28b3de55ac12f03c7b79ed9632454675063bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.6 KB (785632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a0fd5325de66f35f4367c4e1892be82ff21cf5a48e19fabc9888a783ba6cdc`

```dockerfile
```

-	Layers:
	-	`sha256:42b8f7363028d21427e8f398bac58ecff5c02cec3eac379e0dce85371a26fb2a`  
		Last Modified: Thu, 09 Oct 2025 02:20:24 GMT  
		Size: 769.0 KB (768993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95c8c2a7537102693c04e00ab640a007908a8cdec2fa3201d77b6b835d83c362`  
		Last Modified: Thu, 09 Oct 2025 02:20:25 GMT  
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
$ docker pull influxdb@sha256:3786c85254cdf499b874b247ec0b7fdd5ef8af5fbd719df6e5ee06f066500955
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.9-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:6c020578fb9c06bd21f4356170c21bd5ef4274dc05fa08e82e63e8d94f4d3c22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23402378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bcd086cb1f86062412478c7ed47e21bae8a3aba6b6d2e9ea20d2fed8e1988b6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Tue, 30 Sep 2025 13:56:01 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af74a58a446b59e39793a690435f78e585a91ea73edb6406a99a3283db12a3a2`  
		Last Modified: Wed, 08 Oct 2025 23:01:06 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be22d087a3e55404f6a8b32177effbd6c3829e421c0b5ef02b11b38be4785b3`  
		Last Modified: Wed, 08 Oct 2025 23:10:28 GMT  
		Size: 1.2 MB (1224606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d72c9781c814dfaa052605afbb9e8d8be20811f6843ddb55b2cc0645fd96a7`  
		Last Modified: Wed, 08 Oct 2025 23:10:30 GMT  
		Size: 18.5 MB (18549871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66e2e10d6786167404e416ab04e6d4485db03583db3118244df06813625bad4`  
		Last Modified: Wed, 08 Oct 2025 23:10:28 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1362d7c20d172d913583e0a7dd8615a994bb4d5c13a7df7265d4dd009dfdbe`  
		Last Modified: Wed, 08 Oct 2025 23:10:28 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.9-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:f5c20e593d6fa019a8d711341d1462f293da3418f4c51358c6c7711eca95aa56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.6 KB (691632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff4aaa72e275158f64bdb7a0e14b89336f3793f64bf51dbab7320f83a05f3d8d`

```dockerfile
```

-	Layers:
	-	`sha256:0ad0a9d5310a18e73a4f13e3fe81fc690a2e3fa594fdf23fba47d3e7b5528e9f`  
		Last Modified: Thu, 09 Oct 2025 02:20:30 GMT  
		Size: 676.6 KB (676622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24dde11f34792d696d7baefa980d47a9bb0ec06c1640475e5f37e93aa05a49ae`  
		Last Modified: Thu, 09 Oct 2025 02:20:30 GMT  
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
$ docker pull influxdb@sha256:9be6bb8f77c1401e77aca7a95487763c74ceb9e7c969c7d53d8b195a833e3f97
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.12-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:693d5e087aebfa80ada39aab693673e0006fb092759889dc89a1c22de3d10a0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46122314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4580b750c0220e5f38c52cbcaf2a62c48c9110319d6ec9a2d395a04c9b4ff0cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
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
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833a534ae7d9b744b01293824d76272ab350ec43a3ea6e2461ff7af8abc50a6a`  
		Last Modified: Wed, 08 Oct 2025 23:09:35 GMT  
		Size: 1.2 MB (1225336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c347910584b08baf1a48bdf46c5c50dd24038eb1302b7007f31ce71bc927b592`  
		Last Modified: Wed, 08 Oct 2025 23:09:38 GMT  
		Size: 41.3 MB (41251703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a935c4d2c88a22b2b988a0ccac55421ea76be53d52269f7b632dcf92c515813`  
		Last Modified: Wed, 08 Oct 2025 23:09:35 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a53405a7e90893d67726045e12be0b8d6c77efc4329d83b02742c7dc703c64`  
		Last Modified: Wed, 08 Oct 2025 23:09:35 GMT  
		Size: 993.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559f188f2dcf26e5cc25cbe55a6ec7068097f6735e694bf00a27874305fe66fa`  
		Last Modified: Wed, 08 Oct 2025 23:09:35 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafd7a2e4b50b127938200eed101e836d8f93fbdeeeb0d43f571a379f42a5173`  
		Last Modified: Wed, 08 Oct 2025 23:09:35 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:e81e0d6fcdd78898b7d541628dd5f046c11ade938248deb9bfbab0239e111139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **780.5 KB (780522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:062a1e459573f824fd571b3df5adc062fdf691d6b759359c318fc1e4a6f81b99`

```dockerfile
```

-	Layers:
	-	`sha256:5e2652a38eb252eea390f6eb8de70303b2ba32a60a44d0115cc4d95141919caf`  
		Last Modified: Thu, 09 Oct 2025 02:20:56 GMT  
		Size: 761.9 KB (761859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efdc33ff6b4a8b7da52daf4a11c7f9b03b3ba5c78a7c13b748b4e02199fa9284`  
		Last Modified: Thu, 09 Oct 2025 02:20:57 GMT  
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
$ docker pull influxdb@sha256:ce2ffe52a626e318a7eb9a37591b2dab8918b4b9a2db82d40376d10f49ec655c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:a9119ce752787d7bc02d05b19c71cf1c52c3ec36e7d53ffac794bc9e9e856105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47123983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:778a4ce21945169b3579e3c00ae06210f014bbaa4c94491ed2d6813ee148bdce`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Tue, 30 Sep 2025 13:56:01 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"         "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     tar -xvf "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz"         -C / --strip-components 1 --wildcards             'influxdb-*/usr/bin/influx'             'influxdb-*/usr/bin/influx_inspect'             'influxdb-*/usr/bin/influxd' &&     rm "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"        "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     apk del .build-deps # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a3788b43dae292831ae0448a5ed504046ffa71fe7a9f09db40713951fbf944`  
		Last Modified: Wed, 08 Oct 2025 23:10:06 GMT  
		Size: 1.2 MB (1225329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e0170f82fea093122d3570e0d358e936d1db98ed05a0d6a48d33037501b351`  
		Last Modified: Wed, 08 Oct 2025 23:10:13 GMT  
		Size: 42.3 MB (42254311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b0661d8dbfc3b43d49ec386e18c197ae353dd5d5c77c548207da941ba2ee68`  
		Last Modified: Wed, 08 Oct 2025 23:10:05 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39225506d3b8f10fd5e6623059b8c1e0d7efadec626f71dcf9da78fee4f7e2a`  
		Last Modified: Wed, 08 Oct 2025 23:10:06 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d72d987f87daa2925154010870639046590c11fa247eb8c38fdd2ea9c6094b`  
		Last Modified: Wed, 08 Oct 2025 23:10:06 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:f218c7220d82f4546bb998858096a34a8dfce6b65860ed72b6874ed1b0a3eb4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **791.0 KB (791001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12e3605d003749db319aa7f2e79a5cb86a94e980bcb7a857759a1dc3a916e76d`

```dockerfile
```

-	Layers:
	-	`sha256:6aeb326ff9d4e15849772b799e87c132f6edf8dcdfacc3879b8fb8f19a22fca9`  
		Last Modified: Thu, 09 Oct 2025 02:20:47 GMT  
		Size: 775.8 KB (775810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f65ff52ae85ef9fa76b501b5f6ab0974038c20801b32cc1c20d90c94d731471`  
		Last Modified: Thu, 09 Oct 2025 02:20:48 GMT  
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
$ docker pull influxdb@sha256:811acdf4664b52af3f6d703e48787e2b4606ae470747606bfa84ebf6e3395179
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:eafc8ce951405cbc7907d39b292cbde2a07e4f8bb20e15f5de12110ff310c811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23590971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a57259f8ac7012ee31aebecf1b6497bcb8758c5d887d973b483ddbdbcf723da`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Tue, 30 Sep 2025 13:56:01 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"         "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     tar -xvf "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz"         -C / --strip-components 1 --wildcards             'influxdb-*/usr/bin/influxd-ctl'             'influxdb-*/usr/bin/influxd-meta' &&     rm "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"        "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     apk del .build-deps # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1506a520a1ca51f516d5068e753e243431efab0ef69c7b1634e53985ce44a2`  
		Last Modified: Wed, 08 Oct 2025 23:10:05 GMT  
		Size: 1.2 MB (1225337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8df8f8e418a27917114426b3d245a3728772fe30be9e1b0b609e79b9ccb3b1d`  
		Last Modified: Wed, 08 Oct 2025 23:10:06 GMT  
		Size: 18.7 MB (18722501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96fdeefb85b445c179f78bb53968e8210d7aaa4a30cccb4d6452d9ac4a7b000`  
		Last Modified: Wed, 08 Oct 2025 23:10:04 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5817ad78e6b46e06d7f07b733f09a0eddd15b789d78398b86fe406d8cd2fdf7`  
		Last Modified: Wed, 08 Oct 2025 23:10:04 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:7df6901865ed7a906f1c751eba50de606f5f89648541f49d5c79af65530b1190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **695.3 KB (695336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:523ace161067c6e86bd41d82cc97db7e8a4993f3da53f36d6d5629e38bee6daa`

```dockerfile
```

-	Layers:
	-	`sha256:3d4d976d2a8846a9f10e6d2d34d790872d5e7ed7b1b351117c82f8b927502399`  
		Last Modified: Thu, 09 Oct 2025 02:20:59 GMT  
		Size: 681.8 KB (681759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e71c697656e9ce6a76bcb04d0f78aff32c9bc6715c511aa163637cbd6c96a2ac`  
		Last Modified: Thu, 09 Oct 2025 02:20:59 GMT  
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
$ docker pull influxdb@sha256:9be6bb8f77c1401e77aca7a95487763c74ceb9e7c969c7d53d8b195a833e3f97
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.12.2-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:693d5e087aebfa80ada39aab693673e0006fb092759889dc89a1c22de3d10a0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46122314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4580b750c0220e5f38c52cbcaf2a62c48c9110319d6ec9a2d395a04c9b4ff0cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
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
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833a534ae7d9b744b01293824d76272ab350ec43a3ea6e2461ff7af8abc50a6a`  
		Last Modified: Wed, 08 Oct 2025 23:09:35 GMT  
		Size: 1.2 MB (1225336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c347910584b08baf1a48bdf46c5c50dd24038eb1302b7007f31ce71bc927b592`  
		Last Modified: Wed, 08 Oct 2025 23:09:38 GMT  
		Size: 41.3 MB (41251703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a935c4d2c88a22b2b988a0ccac55421ea76be53d52269f7b632dcf92c515813`  
		Last Modified: Wed, 08 Oct 2025 23:09:35 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a53405a7e90893d67726045e12be0b8d6c77efc4329d83b02742c7dc703c64`  
		Last Modified: Wed, 08 Oct 2025 23:09:35 GMT  
		Size: 993.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559f188f2dcf26e5cc25cbe55a6ec7068097f6735e694bf00a27874305fe66fa`  
		Last Modified: Wed, 08 Oct 2025 23:09:35 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafd7a2e4b50b127938200eed101e836d8f93fbdeeeb0d43f571a379f42a5173`  
		Last Modified: Wed, 08 Oct 2025 23:09:35 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:e81e0d6fcdd78898b7d541628dd5f046c11ade938248deb9bfbab0239e111139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **780.5 KB (780522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:062a1e459573f824fd571b3df5adc062fdf691d6b759359c318fc1e4a6f81b99`

```dockerfile
```

-	Layers:
	-	`sha256:5e2652a38eb252eea390f6eb8de70303b2ba32a60a44d0115cc4d95141919caf`  
		Last Modified: Thu, 09 Oct 2025 02:20:56 GMT  
		Size: 761.9 KB (761859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efdc33ff6b4a8b7da52daf4a11c7f9b03b3ba5c78a7c13b748b4e02199fa9284`  
		Last Modified: Thu, 09 Oct 2025 02:20:57 GMT  
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
$ docker pull influxdb@sha256:ce2ffe52a626e318a7eb9a37591b2dab8918b4b9a2db82d40376d10f49ec655c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12.2-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:a9119ce752787d7bc02d05b19c71cf1c52c3ec36e7d53ffac794bc9e9e856105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47123983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:778a4ce21945169b3579e3c00ae06210f014bbaa4c94491ed2d6813ee148bdce`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Tue, 30 Sep 2025 13:56:01 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"         "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     tar -xvf "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz"         -C / --strip-components 1 --wildcards             'influxdb-*/usr/bin/influx'             'influxdb-*/usr/bin/influx_inspect'             'influxdb-*/usr/bin/influxd' &&     rm "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"        "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     apk del .build-deps # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a3788b43dae292831ae0448a5ed504046ffa71fe7a9f09db40713951fbf944`  
		Last Modified: Wed, 08 Oct 2025 23:10:06 GMT  
		Size: 1.2 MB (1225329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e0170f82fea093122d3570e0d358e936d1db98ed05a0d6a48d33037501b351`  
		Last Modified: Wed, 08 Oct 2025 23:10:13 GMT  
		Size: 42.3 MB (42254311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b0661d8dbfc3b43d49ec386e18c197ae353dd5d5c77c548207da941ba2ee68`  
		Last Modified: Wed, 08 Oct 2025 23:10:05 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39225506d3b8f10fd5e6623059b8c1e0d7efadec626f71dcf9da78fee4f7e2a`  
		Last Modified: Wed, 08 Oct 2025 23:10:06 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d72d987f87daa2925154010870639046590c11fa247eb8c38fdd2ea9c6094b`  
		Last Modified: Wed, 08 Oct 2025 23:10:06 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:f218c7220d82f4546bb998858096a34a8dfce6b65860ed72b6874ed1b0a3eb4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **791.0 KB (791001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12e3605d003749db319aa7f2e79a5cb86a94e980bcb7a857759a1dc3a916e76d`

```dockerfile
```

-	Layers:
	-	`sha256:6aeb326ff9d4e15849772b799e87c132f6edf8dcdfacc3879b8fb8f19a22fca9`  
		Last Modified: Thu, 09 Oct 2025 02:20:47 GMT  
		Size: 775.8 KB (775810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f65ff52ae85ef9fa76b501b5f6ab0974038c20801b32cc1c20d90c94d731471`  
		Last Modified: Thu, 09 Oct 2025 02:20:48 GMT  
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
$ docker pull influxdb@sha256:811acdf4664b52af3f6d703e48787e2b4606ae470747606bfa84ebf6e3395179
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12.2-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:eafc8ce951405cbc7907d39b292cbde2a07e4f8bb20e15f5de12110ff310c811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23590971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a57259f8ac7012ee31aebecf1b6497bcb8758c5d887d973b483ddbdbcf723da`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Tue, 30 Sep 2025 13:56:01 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"         "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     tar -xvf "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz"         -C / --strip-components 1 --wildcards             'influxdb-*/usr/bin/influxd-ctl'             'influxdb-*/usr/bin/influxd-meta' &&     rm "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"        "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     apk del .build-deps # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 30 Sep 2025 13:56:01 GMT
VOLUME [/var/lib/influxdb]
# Tue, 30 Sep 2025 13:56:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 30 Sep 2025 13:56:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 13:56:01 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1506a520a1ca51f516d5068e753e243431efab0ef69c7b1634e53985ce44a2`  
		Last Modified: Wed, 08 Oct 2025 23:10:05 GMT  
		Size: 1.2 MB (1225337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8df8f8e418a27917114426b3d245a3728772fe30be9e1b0b609e79b9ccb3b1d`  
		Last Modified: Wed, 08 Oct 2025 23:10:06 GMT  
		Size: 18.7 MB (18722501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96fdeefb85b445c179f78bb53968e8210d7aaa4a30cccb4d6452d9ac4a7b000`  
		Last Modified: Wed, 08 Oct 2025 23:10:04 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5817ad78e6b46e06d7f07b733f09a0eddd15b789d78398b86fe406d8cd2fdf7`  
		Last Modified: Wed, 08 Oct 2025 23:10:04 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:7df6901865ed7a906f1c751eba50de606f5f89648541f49d5c79af65530b1190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **695.3 KB (695336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:523ace161067c6e86bd41d82cc97db7e8a4993f3da53f36d6d5629e38bee6daa`

```dockerfile
```

-	Layers:
	-	`sha256:3d4d976d2a8846a9f10e6d2d34d790872d5e7ed7b1b351117c82f8b927502399`  
		Last Modified: Thu, 09 Oct 2025 02:20:59 GMT  
		Size: 681.8 KB (681759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e71c697656e9ce6a76bcb04d0f78aff32c9bc6715c511aa163637cbd6c96a2ac`  
		Last Modified: Thu, 09 Oct 2025 02:20:59 GMT  
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
$ docker pull influxdb@sha256:b4dbe25bb8f8be38f9cf5a12cbca453318a1ad3475954e9d37c38f6e5bc5006b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:14226eaac248bf27cf33cb39e93a3ca48e25440df27248181211bc30691e75df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81561836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917cdd480ab4907f6579b8f23e62b3c7ab08bd863de9c46eaad5b7a130b1a916`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
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
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2298af3f5be87a5532b043f27cf04fb5779734556bb16f47af70b80d01bce6f9`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53835a8d0d20cd34e4a7681b4ff49af99d05ec1c6417ae07f5f2ab28eb1d91d7`  
		Last Modified: Wed, 08 Oct 2025 23:11:06 GMT  
		Size: 9.9 MB (9862172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68829d4164c16e8135e6bf03046861f1566a9d374a3e99a820a143903d7291a`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 6.2 MB (6156988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9072b4a07b3f8dca037d515274838693bb0e168a1fc7b3118370baabde5fb4fb`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7b3f5da15b92af08a9ed64ddc91ab3b683642efb4ab6f3b672da89a0e1e868`  
		Last Modified: Wed, 08 Oct 2025 23:11:08 GMT  
		Size: 50.1 MB (50118379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b2ed5e22ac99676c240cb61c758189300e7929cfc6729851c369529ad53d8d`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 11.8 MB (11773778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68db778755a7a92ab67642d92cc7aa0c820cd21e5943b496d3b32e9fd2403de7`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d366f9033d07efa0b056a0d9362d12bf8f19cf51deec87929bb9a095810b8c21`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024a54836f3da745e3ea2b1a54e11d6a3a24d9402e2007b4610da65910613fe2`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:deb2d219dabedf8726ae51cb51e71cbaff4b1141357813c1b7e667a1e586b227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.6 KB (944584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a5ef07f0846c1450fa1eea4dc4e9a79f80492233cf1cf149f6ec9c9810e275a`

```dockerfile
```

-	Layers:
	-	`sha256:afb943795c0ce1f504024d5c58671df0aa1345208fa615fb7245377bb6894323`  
		Last Modified: Thu, 09 Oct 2025 02:21:09 GMT  
		Size: 913.8 KB (913815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e562735d7f12f937fbcb209933eb7986ea94c4b843ec47db133b14f1a8a2bc88`  
		Last Modified: Thu, 09 Oct 2025 02:21:09 GMT  
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
$ docker pull influxdb@sha256:b4dbe25bb8f8be38f9cf5a12cbca453318a1ad3475954e9d37c38f6e5bc5006b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:14226eaac248bf27cf33cb39e93a3ca48e25440df27248181211bc30691e75df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81561836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917cdd480ab4907f6579b8f23e62b3c7ab08bd863de9c46eaad5b7a130b1a916`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
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
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2298af3f5be87a5532b043f27cf04fb5779734556bb16f47af70b80d01bce6f9`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53835a8d0d20cd34e4a7681b4ff49af99d05ec1c6417ae07f5f2ab28eb1d91d7`  
		Last Modified: Wed, 08 Oct 2025 23:11:06 GMT  
		Size: 9.9 MB (9862172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68829d4164c16e8135e6bf03046861f1566a9d374a3e99a820a143903d7291a`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 6.2 MB (6156988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9072b4a07b3f8dca037d515274838693bb0e168a1fc7b3118370baabde5fb4fb`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7b3f5da15b92af08a9ed64ddc91ab3b683642efb4ab6f3b672da89a0e1e868`  
		Last Modified: Wed, 08 Oct 2025 23:11:08 GMT  
		Size: 50.1 MB (50118379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b2ed5e22ac99676c240cb61c758189300e7929cfc6729851c369529ad53d8d`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 11.8 MB (11773778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68db778755a7a92ab67642d92cc7aa0c820cd21e5943b496d3b32e9fd2403de7`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d366f9033d07efa0b056a0d9362d12bf8f19cf51deec87929bb9a095810b8c21`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024a54836f3da745e3ea2b1a54e11d6a3a24d9402e2007b4610da65910613fe2`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:deb2d219dabedf8726ae51cb51e71cbaff4b1141357813c1b7e667a1e586b227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.6 KB (944584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a5ef07f0846c1450fa1eea4dc4e9a79f80492233cf1cf149f6ec9c9810e275a`

```dockerfile
```

-	Layers:
	-	`sha256:afb943795c0ce1f504024d5c58671df0aa1345208fa615fb7245377bb6894323`  
		Last Modified: Thu, 09 Oct 2025 02:21:09 GMT  
		Size: 913.8 KB (913815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e562735d7f12f937fbcb209933eb7986ea94c4b843ec47db133b14f1a8a2bc88`  
		Last Modified: Thu, 09 Oct 2025 02:21:09 GMT  
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
$ docker pull influxdb@sha256:b4dbe25bb8f8be38f9cf5a12cbca453318a1ad3475954e9d37c38f6e5bc5006b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.12-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:14226eaac248bf27cf33cb39e93a3ca48e25440df27248181211bc30691e75df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81561836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917cdd480ab4907f6579b8f23e62b3c7ab08bd863de9c46eaad5b7a130b1a916`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
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
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2298af3f5be87a5532b043f27cf04fb5779734556bb16f47af70b80d01bce6f9`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53835a8d0d20cd34e4a7681b4ff49af99d05ec1c6417ae07f5f2ab28eb1d91d7`  
		Last Modified: Wed, 08 Oct 2025 23:11:06 GMT  
		Size: 9.9 MB (9862172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68829d4164c16e8135e6bf03046861f1566a9d374a3e99a820a143903d7291a`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 6.2 MB (6156988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9072b4a07b3f8dca037d515274838693bb0e168a1fc7b3118370baabde5fb4fb`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7b3f5da15b92af08a9ed64ddc91ab3b683642efb4ab6f3b672da89a0e1e868`  
		Last Modified: Wed, 08 Oct 2025 23:11:08 GMT  
		Size: 50.1 MB (50118379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b2ed5e22ac99676c240cb61c758189300e7929cfc6729851c369529ad53d8d`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 11.8 MB (11773778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68db778755a7a92ab67642d92cc7aa0c820cd21e5943b496d3b32e9fd2403de7`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d366f9033d07efa0b056a0d9362d12bf8f19cf51deec87929bb9a095810b8c21`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024a54836f3da745e3ea2b1a54e11d6a3a24d9402e2007b4610da65910613fe2`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:deb2d219dabedf8726ae51cb51e71cbaff4b1141357813c1b7e667a1e586b227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.6 KB (944584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a5ef07f0846c1450fa1eea4dc4e9a79f80492233cf1cf149f6ec9c9810e275a`

```dockerfile
```

-	Layers:
	-	`sha256:afb943795c0ce1f504024d5c58671df0aa1345208fa615fb7245377bb6894323`  
		Last Modified: Thu, 09 Oct 2025 02:21:09 GMT  
		Size: 913.8 KB (913815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e562735d7f12f937fbcb209933eb7986ea94c4b843ec47db133b14f1a8a2bc88`  
		Last Modified: Thu, 09 Oct 2025 02:21:09 GMT  
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
$ docker pull influxdb@sha256:6fa417245fe0474ed239579885a7dd6b56ba532d33f047dbca7bf66debcc1466
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-core` - linux; amd64

```console
$ docker pull influxdb@sha256:28cb716470df458e81cf299ffe6a8f778452b0e648d19d23ba9162a224ed06cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.2 MB (117162779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e0f4cc8be7a713b2e99e134e93532d7c9a2a14c90c40f26eac726106c36345`
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
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
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
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7221b83a2b2631bb18e13caf819e88b9282d00d4ebda0512003064c95c22789e`  
		Last Modified: Thu, 09 Oct 2025 21:18:03 GMT  
		Size: 6.7 MB (6666057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7291bda70a4dee13a6dcf2c0f3ee7977fb5567c1855ca5c44b151b52db5f702d`  
		Last Modified: Thu, 09 Oct 2025 21:18:02 GMT  
		Size: 3.7 KB (3651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38bd1eeadf862306bfcba82c3d2948fe5ad479283821aad77619a05f01291e5`  
		Last Modified: Thu, 09 Oct 2025 21:18:08 GMT  
		Size: 80.8 MB (80769452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b683580546fa4238292917e9384da86b9734e59a88a0563ebb7bb0a31844947`  
		Last Modified: Thu, 09 Oct 2025 21:18:02 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a51dfa9f5a58f8f0e16f4efa9385e19c2dcd80fc9aa2b171fe3f1772a32b44`  
		Last Modified: Thu, 09 Oct 2025 21:18:02 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:fa9a56a57d64155ae3b5e1ae05a2807dddcaef73b57908755a4d746e09de3e4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79dce04c0f2b47de159c180dd559ad294e01af9f1c58c13d121fac747f1edd79`

```dockerfile
```

-	Layers:
	-	`sha256:ca086edd667f9828796610b5480c42013cac44b288e64cf8e2076e1be4a5b7af`  
		Last Modified: Thu, 09 Oct 2025 23:21:15 GMT  
		Size: 2.3 MB (2311329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1563a75666778e66833345e12e00bc5911ebf61d82dca6e33d7adc7b4ecf9ff7`  
		Last Modified: Thu, 09 Oct 2025 23:21:18 GMT  
		Size: 17.6 KB (17592 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:aa9b048b1afcb83681c078090d3fe272ecf2034605e9860e01742a405c478729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.8 MB (107752299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad53ca51f9da9212e76201f4aa5a5603116b681f9b9a917e0e98f2ec5b61420`
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
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
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
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a635cb84e6f3173e9d283e09541c4a8fc440ee7ec66cd3f85117b98f0deb2088`  
		Last Modified: Thu, 09 Oct 2025 21:20:04 GMT  
		Size: 6.7 MB (6676662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb23ade74b2c238862fe80748ae2747dce594522db437538e7cd7744efb5908`  
		Last Modified: Thu, 09 Oct 2025 21:20:00 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202ab152f61be8187c17a40010f7e47639bfd8e2e818eb5dff2a28ccbbf3af78`  
		Last Modified: Thu, 09 Oct 2025 21:20:07 GMT  
		Size: 72.2 MB (72209799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a975d3a543ffef9d252fd101cefb96e5d39280b6be01eb08af569d800313e855`  
		Last Modified: Thu, 09 Oct 2025 21:20:01 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d80034335117bf35d2582062a5d98faac9f4d043ac0d64299bbe9b9acc27c6`  
		Last Modified: Thu, 09 Oct 2025 21:20:01 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:5657515acee21a1231394a2a248aa29eabf08a4e6c391934ec5b60f5cbb00650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60f0921faef72990a0248a955c6a5e88cbd29628547e5efe1bf90c9779a725a6`

```dockerfile
```

-	Layers:
	-	`sha256:3182ceee96e25b61017b0e1e08a43cd057fefb13f8e0948fba777243fe54b63d`  
		Last Modified: Thu, 09 Oct 2025 23:21:22 GMT  
		Size: 2.3 MB (2312411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c90fdc4abe22c6c0127dcb90c36e2395a820e484d5fa474fa2b436d12427752`  
		Last Modified: Thu, 09 Oct 2025 23:21:23 GMT  
		Size: 17.7 KB (17741 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3-enterprise`

```console
$ docker pull influxdb@sha256:97a9a1dbeb7977c74657c531bd4c7200628850c7bda11f056817f662b382724a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:ecf1d8a9c7f2d3ddf21ee009e3517e07c86b33decc69c5e13fc8acab41b2bb82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.4 MB (123425444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe081e74576acb4129048cf32368129189d5bc2f13555eab5e84ef8fe167bf0`
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
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
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
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2074944060833531a3a0bb7a9eba36af26dcd8ef455569420523f7f4e82501af`  
		Last Modified: Thu, 09 Oct 2025 21:18:04 GMT  
		Size: 6.7 MB (6666093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a6cc3c11f56044f264d711586c010c0b382f47b51357579a06dbf11e8f2424`  
		Last Modified: Thu, 09 Oct 2025 21:18:03 GMT  
		Size: 3.6 KB (3649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac8b4be75dc281ee9c15d7d8c84c4a327c8f2b4103081e20065ec4065062635`  
		Last Modified: Thu, 09 Oct 2025 21:18:13 GMT  
		Size: 87.0 MB (87032081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a43964e82bbb42d09f6fc4e7e7ba30df9885681dd909e3413ea0215c9e36a9`  
		Last Modified: Thu, 09 Oct 2025 21:18:03 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ce1a2f299b58e1b83ae2229e41ea1ff8d13c8a1b51c2c5a143d4c1f3e0426b`  
		Last Modified: Thu, 09 Oct 2025 21:18:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:4751a80bea16cd9b2b6a8156d6a4f0e6d05b5c8b34c6db6c8e706490d0a6a9fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac397886bbb08ec89c7bf329bd2974172718add62d3653157758214d21001ac9`

```dockerfile
```

-	Layers:
	-	`sha256:285e32fe67c49db6854d8972b9cb4c3398476c070d652fcd21ca273b916ce02a`  
		Last Modified: Thu, 09 Oct 2025 23:20:48 GMT  
		Size: 2.3 MB (2311377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72c07346f3df03bd6ec760544f71f756cbfbd0c6e78d622797b01edd6cdb5a9f`  
		Last Modified: Thu, 09 Oct 2025 23:20:53 GMT  
		Size: 17.8 KB (17772 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:71c9049895ba829877fd02607f36f17e7e65fc66541817df7824b6b6d3d8da8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.9 MB (113942507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52fc5558aed56ab00633530f0a8fee045ae01f3f182ae10e815a2040a6930d72`
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
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
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
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d1733bc4fee8d703b3bea732c49e2ed8ea4138e83a5f5ec77e3a477e89b026`  
		Last Modified: Thu, 09 Oct 2025 21:20:03 GMT  
		Size: 6.7 MB (6676656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d6ab116eb4f82815571acd5e86bbea832c686f3f54cd5afd45961577c53c33`  
		Last Modified: Thu, 09 Oct 2025 21:20:02 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6823ff710709163e6810d4878035c022ad82c5ed7c158675d9cf58374e43c3a`  
		Last Modified: Thu, 09 Oct 2025 21:20:07 GMT  
		Size: 78.4 MB (78400011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52fbd72ef10adf7437fdffc985f2db5e1fe9fc313e57ca119f1a02b1ef5db0ac`  
		Last Modified: Thu, 09 Oct 2025 21:20:02 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680c309c6a44c8d72ed91bb939dfeccb918de9b8548831f58ad6b4a21bc3de02`  
		Last Modified: Thu, 09 Oct 2025 21:20:02 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:3a13d5375fb9f99131bb61a6176cec7798d02b0ae15c4b7657c57785d2d70f3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4daf889bfc69f7ded045b6eeb097b7be79978004b2ba3962c216798c377be1f0`

```dockerfile
```

-	Layers:
	-	`sha256:881fed221da0338493923e6e4ac16a25aed6bfefa1e9370933471ccc03bc835b`  
		Last Modified: Thu, 09 Oct 2025 23:21:00 GMT  
		Size: 2.3 MB (2312459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2409fcd817bc75b242eae81d82d53bbe811a25baadb89f704f6b3ab0d1a209df`  
		Last Modified: Thu, 09 Oct 2025 23:21:02 GMT  
		Size: 17.9 KB (17921 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.5-core`

```console
$ docker pull influxdb@sha256:6fa417245fe0474ed239579885a7dd6b56ba532d33f047dbca7bf66debcc1466
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.5-core` - linux; amd64

```console
$ docker pull influxdb@sha256:28cb716470df458e81cf299ffe6a8f778452b0e648d19d23ba9162a224ed06cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.2 MB (117162779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e0f4cc8be7a713b2e99e134e93532d7c9a2a14c90c40f26eac726106c36345`
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
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
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
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7221b83a2b2631bb18e13caf819e88b9282d00d4ebda0512003064c95c22789e`  
		Last Modified: Thu, 09 Oct 2025 21:18:03 GMT  
		Size: 6.7 MB (6666057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7291bda70a4dee13a6dcf2c0f3ee7977fb5567c1855ca5c44b151b52db5f702d`  
		Last Modified: Thu, 09 Oct 2025 21:18:02 GMT  
		Size: 3.7 KB (3651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38bd1eeadf862306bfcba82c3d2948fe5ad479283821aad77619a05f01291e5`  
		Last Modified: Thu, 09 Oct 2025 21:18:08 GMT  
		Size: 80.8 MB (80769452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b683580546fa4238292917e9384da86b9734e59a88a0563ebb7bb0a31844947`  
		Last Modified: Thu, 09 Oct 2025 21:18:02 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a51dfa9f5a58f8f0e16f4efa9385e19c2dcd80fc9aa2b171fe3f1772a32b44`  
		Last Modified: Thu, 09 Oct 2025 21:18:02 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.5-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:fa9a56a57d64155ae3b5e1ae05a2807dddcaef73b57908755a4d746e09de3e4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79dce04c0f2b47de159c180dd559ad294e01af9f1c58c13d121fac747f1edd79`

```dockerfile
```

-	Layers:
	-	`sha256:ca086edd667f9828796610b5480c42013cac44b288e64cf8e2076e1be4a5b7af`  
		Last Modified: Thu, 09 Oct 2025 23:21:15 GMT  
		Size: 2.3 MB (2311329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1563a75666778e66833345e12e00bc5911ebf61d82dca6e33d7adc7b4ecf9ff7`  
		Last Modified: Thu, 09 Oct 2025 23:21:18 GMT  
		Size: 17.6 KB (17592 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.5-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:aa9b048b1afcb83681c078090d3fe272ecf2034605e9860e01742a405c478729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.8 MB (107752299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad53ca51f9da9212e76201f4aa5a5603116b681f9b9a917e0e98f2ec5b61420`
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
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
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
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a635cb84e6f3173e9d283e09541c4a8fc440ee7ec66cd3f85117b98f0deb2088`  
		Last Modified: Thu, 09 Oct 2025 21:20:04 GMT  
		Size: 6.7 MB (6676662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb23ade74b2c238862fe80748ae2747dce594522db437538e7cd7744efb5908`  
		Last Modified: Thu, 09 Oct 2025 21:20:00 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202ab152f61be8187c17a40010f7e47639bfd8e2e818eb5dff2a28ccbbf3af78`  
		Last Modified: Thu, 09 Oct 2025 21:20:07 GMT  
		Size: 72.2 MB (72209799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a975d3a543ffef9d252fd101cefb96e5d39280b6be01eb08af569d800313e855`  
		Last Modified: Thu, 09 Oct 2025 21:20:01 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d80034335117bf35d2582062a5d98faac9f4d043ac0d64299bbe9b9acc27c6`  
		Last Modified: Thu, 09 Oct 2025 21:20:01 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.5-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:5657515acee21a1231394a2a248aa29eabf08a4e6c391934ec5b60f5cbb00650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60f0921faef72990a0248a955c6a5e88cbd29628547e5efe1bf90c9779a725a6`

```dockerfile
```

-	Layers:
	-	`sha256:3182ceee96e25b61017b0e1e08a43cd057fefb13f8e0948fba777243fe54b63d`  
		Last Modified: Thu, 09 Oct 2025 23:21:22 GMT  
		Size: 2.3 MB (2312411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c90fdc4abe22c6c0127dcb90c36e2395a820e484d5fa474fa2b436d12427752`  
		Last Modified: Thu, 09 Oct 2025 23:21:23 GMT  
		Size: 17.7 KB (17741 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.5-enterprise`

```console
$ docker pull influxdb@sha256:97a9a1dbeb7977c74657c531bd4c7200628850c7bda11f056817f662b382724a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.5-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:ecf1d8a9c7f2d3ddf21ee009e3517e07c86b33decc69c5e13fc8acab41b2bb82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.4 MB (123425444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe081e74576acb4129048cf32368129189d5bc2f13555eab5e84ef8fe167bf0`
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
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
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
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2074944060833531a3a0bb7a9eba36af26dcd8ef455569420523f7f4e82501af`  
		Last Modified: Thu, 09 Oct 2025 21:18:04 GMT  
		Size: 6.7 MB (6666093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a6cc3c11f56044f264d711586c010c0b382f47b51357579a06dbf11e8f2424`  
		Last Modified: Thu, 09 Oct 2025 21:18:03 GMT  
		Size: 3.6 KB (3649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac8b4be75dc281ee9c15d7d8c84c4a327c8f2b4103081e20065ec4065062635`  
		Last Modified: Thu, 09 Oct 2025 21:18:13 GMT  
		Size: 87.0 MB (87032081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a43964e82bbb42d09f6fc4e7e7ba30df9885681dd909e3413ea0215c9e36a9`  
		Last Modified: Thu, 09 Oct 2025 21:18:03 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ce1a2f299b58e1b83ae2229e41ea1ff8d13c8a1b51c2c5a143d4c1f3e0426b`  
		Last Modified: Thu, 09 Oct 2025 21:18:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.5-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:4751a80bea16cd9b2b6a8156d6a4f0e6d05b5c8b34c6db6c8e706490d0a6a9fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac397886bbb08ec89c7bf329bd2974172718add62d3653157758214d21001ac9`

```dockerfile
```

-	Layers:
	-	`sha256:285e32fe67c49db6854d8972b9cb4c3398476c070d652fcd21ca273b916ce02a`  
		Last Modified: Thu, 09 Oct 2025 23:20:48 GMT  
		Size: 2.3 MB (2311377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72c07346f3df03bd6ec760544f71f756cbfbd0c6e78d622797b01edd6cdb5a9f`  
		Last Modified: Thu, 09 Oct 2025 23:20:53 GMT  
		Size: 17.8 KB (17772 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.5-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:71c9049895ba829877fd02607f36f17e7e65fc66541817df7824b6b6d3d8da8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.9 MB (113942507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52fc5558aed56ab00633530f0a8fee045ae01f3f182ae10e815a2040a6930d72`
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
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
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
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d1733bc4fee8d703b3bea732c49e2ed8ea4138e83a5f5ec77e3a477e89b026`  
		Last Modified: Thu, 09 Oct 2025 21:20:03 GMT  
		Size: 6.7 MB (6676656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d6ab116eb4f82815571acd5e86bbea832c686f3f54cd5afd45961577c53c33`  
		Last Modified: Thu, 09 Oct 2025 21:20:02 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6823ff710709163e6810d4878035c022ad82c5ed7c158675d9cf58374e43c3a`  
		Last Modified: Thu, 09 Oct 2025 21:20:07 GMT  
		Size: 78.4 MB (78400011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52fbd72ef10adf7437fdffc985f2db5e1fe9fc313e57ca119f1a02b1ef5db0ac`  
		Last Modified: Thu, 09 Oct 2025 21:20:02 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680c309c6a44c8d72ed91bb939dfeccb918de9b8548831f58ad6b4a21bc3de02`  
		Last Modified: Thu, 09 Oct 2025 21:20:02 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.5-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:3a13d5375fb9f99131bb61a6176cec7798d02b0ae15c4b7657c57785d2d70f3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4daf889bfc69f7ded045b6eeb097b7be79978004b2ba3962c216798c377be1f0`

```dockerfile
```

-	Layers:
	-	`sha256:881fed221da0338493923e6e4ac16a25aed6bfefa1e9370933471ccc03bc835b`  
		Last Modified: Thu, 09 Oct 2025 23:21:00 GMT  
		Size: 2.3 MB (2312459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2409fcd817bc75b242eae81d82d53bbe811a25baadb89f704f6b3ab0d1a209df`  
		Last Modified: Thu, 09 Oct 2025 23:21:02 GMT  
		Size: 17.9 KB (17921 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.5.0-core`

```console
$ docker pull influxdb@sha256:6fa417245fe0474ed239579885a7dd6b56ba532d33f047dbca7bf66debcc1466
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.5.0-core` - linux; amd64

```console
$ docker pull influxdb@sha256:28cb716470df458e81cf299ffe6a8f778452b0e648d19d23ba9162a224ed06cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.2 MB (117162779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e0f4cc8be7a713b2e99e134e93532d7c9a2a14c90c40f26eac726106c36345`
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
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
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
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7221b83a2b2631bb18e13caf819e88b9282d00d4ebda0512003064c95c22789e`  
		Last Modified: Thu, 09 Oct 2025 21:18:03 GMT  
		Size: 6.7 MB (6666057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7291bda70a4dee13a6dcf2c0f3ee7977fb5567c1855ca5c44b151b52db5f702d`  
		Last Modified: Thu, 09 Oct 2025 21:18:02 GMT  
		Size: 3.7 KB (3651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38bd1eeadf862306bfcba82c3d2948fe5ad479283821aad77619a05f01291e5`  
		Last Modified: Thu, 09 Oct 2025 21:18:08 GMT  
		Size: 80.8 MB (80769452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b683580546fa4238292917e9384da86b9734e59a88a0563ebb7bb0a31844947`  
		Last Modified: Thu, 09 Oct 2025 21:18:02 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a51dfa9f5a58f8f0e16f4efa9385e19c2dcd80fc9aa2b171fe3f1772a32b44`  
		Last Modified: Thu, 09 Oct 2025 21:18:02 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.5.0-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:fa9a56a57d64155ae3b5e1ae05a2807dddcaef73b57908755a4d746e09de3e4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79dce04c0f2b47de159c180dd559ad294e01af9f1c58c13d121fac747f1edd79`

```dockerfile
```

-	Layers:
	-	`sha256:ca086edd667f9828796610b5480c42013cac44b288e64cf8e2076e1be4a5b7af`  
		Last Modified: Thu, 09 Oct 2025 23:21:15 GMT  
		Size: 2.3 MB (2311329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1563a75666778e66833345e12e00bc5911ebf61d82dca6e33d7adc7b4ecf9ff7`  
		Last Modified: Thu, 09 Oct 2025 23:21:18 GMT  
		Size: 17.6 KB (17592 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.5.0-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:aa9b048b1afcb83681c078090d3fe272ecf2034605e9860e01742a405c478729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.8 MB (107752299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad53ca51f9da9212e76201f4aa5a5603116b681f9b9a917e0e98f2ec5b61420`
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
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
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
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a635cb84e6f3173e9d283e09541c4a8fc440ee7ec66cd3f85117b98f0deb2088`  
		Last Modified: Thu, 09 Oct 2025 21:20:04 GMT  
		Size: 6.7 MB (6676662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb23ade74b2c238862fe80748ae2747dce594522db437538e7cd7744efb5908`  
		Last Modified: Thu, 09 Oct 2025 21:20:00 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202ab152f61be8187c17a40010f7e47639bfd8e2e818eb5dff2a28ccbbf3af78`  
		Last Modified: Thu, 09 Oct 2025 21:20:07 GMT  
		Size: 72.2 MB (72209799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a975d3a543ffef9d252fd101cefb96e5d39280b6be01eb08af569d800313e855`  
		Last Modified: Thu, 09 Oct 2025 21:20:01 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d80034335117bf35d2582062a5d98faac9f4d043ac0d64299bbe9b9acc27c6`  
		Last Modified: Thu, 09 Oct 2025 21:20:01 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.5.0-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:5657515acee21a1231394a2a248aa29eabf08a4e6c391934ec5b60f5cbb00650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60f0921faef72990a0248a955c6a5e88cbd29628547e5efe1bf90c9779a725a6`

```dockerfile
```

-	Layers:
	-	`sha256:3182ceee96e25b61017b0e1e08a43cd057fefb13f8e0948fba777243fe54b63d`  
		Last Modified: Thu, 09 Oct 2025 23:21:22 GMT  
		Size: 2.3 MB (2312411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c90fdc4abe22c6c0127dcb90c36e2395a820e484d5fa474fa2b436d12427752`  
		Last Modified: Thu, 09 Oct 2025 23:21:23 GMT  
		Size: 17.7 KB (17741 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.5.0-enterprise`

```console
$ docker pull influxdb@sha256:97a9a1dbeb7977c74657c531bd4c7200628850c7bda11f056817f662b382724a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.5.0-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:ecf1d8a9c7f2d3ddf21ee009e3517e07c86b33decc69c5e13fc8acab41b2bb82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.4 MB (123425444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe081e74576acb4129048cf32368129189d5bc2f13555eab5e84ef8fe167bf0`
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
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
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
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2074944060833531a3a0bb7a9eba36af26dcd8ef455569420523f7f4e82501af`  
		Last Modified: Thu, 09 Oct 2025 21:18:04 GMT  
		Size: 6.7 MB (6666093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a6cc3c11f56044f264d711586c010c0b382f47b51357579a06dbf11e8f2424`  
		Last Modified: Thu, 09 Oct 2025 21:18:03 GMT  
		Size: 3.6 KB (3649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac8b4be75dc281ee9c15d7d8c84c4a327c8f2b4103081e20065ec4065062635`  
		Last Modified: Thu, 09 Oct 2025 21:18:13 GMT  
		Size: 87.0 MB (87032081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a43964e82bbb42d09f6fc4e7e7ba30df9885681dd909e3413ea0215c9e36a9`  
		Last Modified: Thu, 09 Oct 2025 21:18:03 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ce1a2f299b58e1b83ae2229e41ea1ff8d13c8a1b51c2c5a143d4c1f3e0426b`  
		Last Modified: Thu, 09 Oct 2025 21:18:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.5.0-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:4751a80bea16cd9b2b6a8156d6a4f0e6d05b5c8b34c6db6c8e706490d0a6a9fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac397886bbb08ec89c7bf329bd2974172718add62d3653157758214d21001ac9`

```dockerfile
```

-	Layers:
	-	`sha256:285e32fe67c49db6854d8972b9cb4c3398476c070d652fcd21ca273b916ce02a`  
		Last Modified: Thu, 09 Oct 2025 23:20:48 GMT  
		Size: 2.3 MB (2311377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72c07346f3df03bd6ec760544f71f756cbfbd0c6e78d622797b01edd6cdb5a9f`  
		Last Modified: Thu, 09 Oct 2025 23:20:53 GMT  
		Size: 17.8 KB (17772 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.5.0-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:71c9049895ba829877fd02607f36f17e7e65fc66541817df7824b6b6d3d8da8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.9 MB (113942507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52fc5558aed56ab00633530f0a8fee045ae01f3f182ae10e815a2040a6930d72`
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
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
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
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d1733bc4fee8d703b3bea732c49e2ed8ea4138e83a5f5ec77e3a477e89b026`  
		Last Modified: Thu, 09 Oct 2025 21:20:03 GMT  
		Size: 6.7 MB (6676656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d6ab116eb4f82815571acd5e86bbea832c686f3f54cd5afd45961577c53c33`  
		Last Modified: Thu, 09 Oct 2025 21:20:02 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6823ff710709163e6810d4878035c022ad82c5ed7c158675d9cf58374e43c3a`  
		Last Modified: Thu, 09 Oct 2025 21:20:07 GMT  
		Size: 78.4 MB (78400011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52fbd72ef10adf7437fdffc985f2db5e1fe9fc313e57ca119f1a02b1ef5db0ac`  
		Last Modified: Thu, 09 Oct 2025 21:20:02 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680c309c6a44c8d72ed91bb939dfeccb918de9b8548831f58ad6b4a21bc3de02`  
		Last Modified: Thu, 09 Oct 2025 21:20:02 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.5.0-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:3a13d5375fb9f99131bb61a6176cec7798d02b0ae15c4b7657c57785d2d70f3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4daf889bfc69f7ded045b6eeb097b7be79978004b2ba3962c216798c377be1f0`

```dockerfile
```

-	Layers:
	-	`sha256:881fed221da0338493923e6e4ac16a25aed6bfefa1e9370933471ccc03bc835b`  
		Last Modified: Thu, 09 Oct 2025 23:21:00 GMT  
		Size: 2.3 MB (2312459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2409fcd817bc75b242eae81d82d53bbe811a25baadb89f704f6b3ab0d1a209df`  
		Last Modified: Thu, 09 Oct 2025 23:21:02 GMT  
		Size: 17.9 KB (17921 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:b4dbe25bb8f8be38f9cf5a12cbca453318a1ad3475954e9d37c38f6e5bc5006b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:14226eaac248bf27cf33cb39e93a3ca48e25440df27248181211bc30691e75df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81561836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917cdd480ab4907f6579b8f23e62b3c7ab08bd863de9c46eaad5b7a130b1a916`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 30 Sep 2025 13:56:01 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
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
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2298af3f5be87a5532b043f27cf04fb5779734556bb16f47af70b80d01bce6f9`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53835a8d0d20cd34e4a7681b4ff49af99d05ec1c6417ae07f5f2ab28eb1d91d7`  
		Last Modified: Wed, 08 Oct 2025 23:11:06 GMT  
		Size: 9.9 MB (9862172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68829d4164c16e8135e6bf03046861f1566a9d374a3e99a820a143903d7291a`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 6.2 MB (6156988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9072b4a07b3f8dca037d515274838693bb0e168a1fc7b3118370baabde5fb4fb`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7b3f5da15b92af08a9ed64ddc91ab3b683642efb4ab6f3b672da89a0e1e868`  
		Last Modified: Wed, 08 Oct 2025 23:11:08 GMT  
		Size: 50.1 MB (50118379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b2ed5e22ac99676c240cb61c758189300e7929cfc6729851c369529ad53d8d`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 11.8 MB (11773778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68db778755a7a92ab67642d92cc7aa0c820cd21e5943b496d3b32e9fd2403de7`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d366f9033d07efa0b056a0d9362d12bf8f19cf51deec87929bb9a095810b8c21`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024a54836f3da745e3ea2b1a54e11d6a3a24d9402e2007b4610da65910613fe2`  
		Last Modified: Wed, 08 Oct 2025 23:11:05 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:deb2d219dabedf8726ae51cb51e71cbaff4b1141357813c1b7e667a1e586b227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **944.6 KB (944584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a5ef07f0846c1450fa1eea4dc4e9a79f80492233cf1cf149f6ec9c9810e275a`

```dockerfile
```

-	Layers:
	-	`sha256:afb943795c0ce1f504024d5c58671df0aa1345208fa615fb7245377bb6894323`  
		Last Modified: Thu, 09 Oct 2025 02:21:09 GMT  
		Size: 913.8 KB (913815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e562735d7f12f937fbcb209933eb7986ea94c4b843ec47db133b14f1a8a2bc88`  
		Last Modified: Thu, 09 Oct 2025 02:21:09 GMT  
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
$ docker pull influxdb@sha256:6fa417245fe0474ed239579885a7dd6b56ba532d33f047dbca7bf66debcc1466
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:core` - linux; amd64

```console
$ docker pull influxdb@sha256:28cb716470df458e81cf299ffe6a8f778452b0e648d19d23ba9162a224ed06cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.2 MB (117162779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e0f4cc8be7a713b2e99e134e93532d7c9a2a14c90c40f26eac726106c36345`
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
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
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
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7221b83a2b2631bb18e13caf819e88b9282d00d4ebda0512003064c95c22789e`  
		Last Modified: Thu, 09 Oct 2025 21:18:03 GMT  
		Size: 6.7 MB (6666057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7291bda70a4dee13a6dcf2c0f3ee7977fb5567c1855ca5c44b151b52db5f702d`  
		Last Modified: Thu, 09 Oct 2025 21:18:02 GMT  
		Size: 3.7 KB (3651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38bd1eeadf862306bfcba82c3d2948fe5ad479283821aad77619a05f01291e5`  
		Last Modified: Thu, 09 Oct 2025 21:18:08 GMT  
		Size: 80.8 MB (80769452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b683580546fa4238292917e9384da86b9734e59a88a0563ebb7bb0a31844947`  
		Last Modified: Thu, 09 Oct 2025 21:18:02 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a51dfa9f5a58f8f0e16f4efa9385e19c2dcd80fc9aa2b171fe3f1772a32b44`  
		Last Modified: Thu, 09 Oct 2025 21:18:02 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:fa9a56a57d64155ae3b5e1ae05a2807dddcaef73b57908755a4d746e09de3e4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79dce04c0f2b47de159c180dd559ad294e01af9f1c58c13d121fac747f1edd79`

```dockerfile
```

-	Layers:
	-	`sha256:ca086edd667f9828796610b5480c42013cac44b288e64cf8e2076e1be4a5b7af`  
		Last Modified: Thu, 09 Oct 2025 23:21:15 GMT  
		Size: 2.3 MB (2311329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1563a75666778e66833345e12e00bc5911ebf61d82dca6e33d7adc7b4ecf9ff7`  
		Last Modified: Thu, 09 Oct 2025 23:21:18 GMT  
		Size: 17.6 KB (17592 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:aa9b048b1afcb83681c078090d3fe272ecf2034605e9860e01742a405c478729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.8 MB (107752299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad53ca51f9da9212e76201f4aa5a5603116b681f9b9a917e0e98f2ec5b61420`
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
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
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
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a635cb84e6f3173e9d283e09541c4a8fc440ee7ec66cd3f85117b98f0deb2088`  
		Last Modified: Thu, 09 Oct 2025 21:20:04 GMT  
		Size: 6.7 MB (6676662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb23ade74b2c238862fe80748ae2747dce594522db437538e7cd7744efb5908`  
		Last Modified: Thu, 09 Oct 2025 21:20:00 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202ab152f61be8187c17a40010f7e47639bfd8e2e818eb5dff2a28ccbbf3af78`  
		Last Modified: Thu, 09 Oct 2025 21:20:07 GMT  
		Size: 72.2 MB (72209799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a975d3a543ffef9d252fd101cefb96e5d39280b6be01eb08af569d800313e855`  
		Last Modified: Thu, 09 Oct 2025 21:20:01 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d80034335117bf35d2582062a5d98faac9f4d043ac0d64299bbe9b9acc27c6`  
		Last Modified: Thu, 09 Oct 2025 21:20:01 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:5657515acee21a1231394a2a248aa29eabf08a4e6c391934ec5b60f5cbb00650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60f0921faef72990a0248a955c6a5e88cbd29628547e5efe1bf90c9779a725a6`

```dockerfile
```

-	Layers:
	-	`sha256:3182ceee96e25b61017b0e1e08a43cd057fefb13f8e0948fba777243fe54b63d`  
		Last Modified: Thu, 09 Oct 2025 23:21:22 GMT  
		Size: 2.3 MB (2312411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c90fdc4abe22c6c0127dcb90c36e2395a820e484d5fa474fa2b436d12427752`  
		Last Modified: Thu, 09 Oct 2025 23:21:23 GMT  
		Size: 17.7 KB (17741 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:enterprise`

```console
$ docker pull influxdb@sha256:97a9a1dbeb7977c74657c531bd4c7200628850c7bda11f056817f662b382724a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:ecf1d8a9c7f2d3ddf21ee009e3517e07c86b33decc69c5e13fc8acab41b2bb82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.4 MB (123425444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe081e74576acb4129048cf32368129189d5bc2f13555eab5e84ef8fe167bf0`
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
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
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
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2074944060833531a3a0bb7a9eba36af26dcd8ef455569420523f7f4e82501af`  
		Last Modified: Thu, 09 Oct 2025 21:18:04 GMT  
		Size: 6.7 MB (6666093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a6cc3c11f56044f264d711586c010c0b382f47b51357579a06dbf11e8f2424`  
		Last Modified: Thu, 09 Oct 2025 21:18:03 GMT  
		Size: 3.6 KB (3649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac8b4be75dc281ee9c15d7d8c84c4a327c8f2b4103081e20065ec4065062635`  
		Last Modified: Thu, 09 Oct 2025 21:18:13 GMT  
		Size: 87.0 MB (87032081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a43964e82bbb42d09f6fc4e7e7ba30df9885681dd909e3413ea0215c9e36a9`  
		Last Modified: Thu, 09 Oct 2025 21:18:03 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ce1a2f299b58e1b83ae2229e41ea1ff8d13c8a1b51c2c5a143d4c1f3e0426b`  
		Last Modified: Thu, 09 Oct 2025 21:18:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:4751a80bea16cd9b2b6a8156d6a4f0e6d05b5c8b34c6db6c8e706490d0a6a9fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac397886bbb08ec89c7bf329bd2974172718add62d3653157758214d21001ac9`

```dockerfile
```

-	Layers:
	-	`sha256:285e32fe67c49db6854d8972b9cb4c3398476c070d652fcd21ca273b916ce02a`  
		Last Modified: Thu, 09 Oct 2025 23:20:48 GMT  
		Size: 2.3 MB (2311377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72c07346f3df03bd6ec760544f71f756cbfbd0c6e78d622797b01edd6cdb5a9f`  
		Last Modified: Thu, 09 Oct 2025 23:20:53 GMT  
		Size: 17.8 KB (17772 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:71c9049895ba829877fd02607f36f17e7e65fc66541817df7824b6b6d3d8da8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.9 MB (113942507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52fc5558aed56ab00633530f0a8fee045ae01f3f182ae10e815a2040a6930d72`
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
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
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
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d1733bc4fee8d703b3bea732c49e2ed8ea4138e83a5f5ec77e3a477e89b026`  
		Last Modified: Thu, 09 Oct 2025 21:20:03 GMT  
		Size: 6.7 MB (6676656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d6ab116eb4f82815571acd5e86bbea832c686f3f54cd5afd45961577c53c33`  
		Last Modified: Thu, 09 Oct 2025 21:20:02 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6823ff710709163e6810d4878035c022ad82c5ed7c158675d9cf58374e43c3a`  
		Last Modified: Thu, 09 Oct 2025 21:20:07 GMT  
		Size: 78.4 MB (78400011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52fbd72ef10adf7437fdffc985f2db5e1fe9fc313e57ca119f1a02b1ef5db0ac`  
		Last Modified: Thu, 09 Oct 2025 21:20:02 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680c309c6a44c8d72ed91bb939dfeccb918de9b8548831f58ad6b4a21bc3de02`  
		Last Modified: Thu, 09 Oct 2025 21:20:02 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:3a13d5375fb9f99131bb61a6176cec7798d02b0ae15c4b7657c57785d2d70f3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4daf889bfc69f7ded045b6eeb097b7be79978004b2ba3962c216798c377be1f0`

```dockerfile
```

-	Layers:
	-	`sha256:881fed221da0338493923e6e4ac16a25aed6bfefa1e9370933471ccc03bc835b`  
		Last Modified: Thu, 09 Oct 2025 23:21:00 GMT  
		Size: 2.3 MB (2312459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2409fcd817bc75b242eae81d82d53bbe811a25baadb89f704f6b3ab0d1a209df`  
		Last Modified: Thu, 09 Oct 2025 23:21:02 GMT  
		Size: 17.9 KB (17921 bytes)  
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
