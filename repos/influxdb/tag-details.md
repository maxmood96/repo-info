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
-	[`influxdb:1.12.4`](#influxdb1124)
-	[`influxdb:1.12.4-alpine`](#influxdb1124-alpine)
-	[`influxdb:1.12.4-data`](#influxdb1124-data)
-	[`influxdb:1.12.4-data-alpine`](#influxdb1124-data-alpine)
-	[`influxdb:1.12.4-meta`](#influxdb1124-meta)
-	[`influxdb:1.12.4-meta-alpine`](#influxdb1124-meta-alpine)
-	[`influxdb:2`](#influxdb2)
-	[`influxdb:2-alpine`](#influxdb2-alpine)
-	[`influxdb:2.8`](#influxdb28)
-	[`influxdb:2.8-alpine`](#influxdb28-alpine)
-	[`influxdb:2.8.0`](#influxdb280)
-	[`influxdb:2.8.0-alpine`](#influxdb280-alpine)
-	[`influxdb:2.9`](#influxdb29)
-	[`influxdb:2.9-alpine`](#influxdb29-alpine)
-	[`influxdb:2.9.1`](#influxdb291)
-	[`influxdb:2.9.1-alpine`](#influxdb291-alpine)
-	[`influxdb:3-core`](#influxdb3-core)
-	[`influxdb:3-enterprise`](#influxdb3-enterprise)
-	[`influxdb:3.9-core`](#influxdb39-core)
-	[`influxdb:3.9-enterprise`](#influxdb39-enterprise)
-	[`influxdb:3.9.2-core`](#influxdb392-core)
-	[`influxdb:3.9.2-enterprise`](#influxdb392-enterprise)
-	[`influxdb:alpine`](#influxdbalpine)
-	[`influxdb:core`](#influxdbcore)
-	[`influxdb:data`](#influxdbdata)
-	[`influxdb:data-alpine`](#influxdbdata-alpine)
-	[`influxdb:enterprise`](#influxdbenterprise)
-	[`influxdb:latest`](#influxdblatest)
-	[`influxdb:meta`](#influxdbmeta)
-	[`influxdb:meta-alpine`](#influxdbmeta-alpine)

## `influxdb:1.11`

```console
$ docker pull influxdb@sha256:70f8a10e5726d211ab9362bd4a669df9d5e8e3549d22528df3e0e8a1cfa5cbea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11` - linux; amd64

```console
$ docker pull influxdb@sha256:1c15b66266dd49f111fa7f6340628d24c13bb014dfb304b4092e7547a1ed39df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116189812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e6eb06132753abaae1609af5ddd266d258a0f9a62296f07b0fe1371f6dd1aed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:30:54 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Fri, 08 May 2026 20:31:02 GMT
ARG INFLUXDB_VERSION=1.11.8
# Fri, 08 May 2026 20:31:02 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:31:02 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 08 May 2026 20:31:02 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 08 May 2026 20:31:02 GMT
VOLUME [/var/lib/influxdb]
# Fri, 08 May 2026 20:31:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 20:31:02 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 08 May 2026 20:31:02 GMT
USER influxdb
# Fri, 08 May 2026 20:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 20:31:02 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d055cea50c88c57fc27fcd44845ebabfe5b830ea8a0a621b89d38a2b650b7ff3`  
		Last Modified: Fri, 08 May 2026 19:40:29 GMT  
		Size: 24.0 MB (24042180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d1a479d575ada2bb52270e86d838a14e87194f9d0de78fbd42a48b72350831`  
		Last Modified: Fri, 08 May 2026 20:31:14 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f254fee05f3ff0e1c3e9cf4ebb8af9361f14aefebdce87061d682e7701ba382`  
		Last Modified: Fri, 08 May 2026 20:31:15 GMT  
		Size: 43.7 MB (43656039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd4330ebe90c14d751dbdbae8be3299d623176cf1d0ee8e1378081d46c21744`  
		Last Modified: Fri, 08 May 2026 20:31:15 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1e612b9a8e7f312257ab33f0ff665ea04aef07bc6d5cb740ecf12c0f6ba14c`  
		Last Modified: Fri, 08 May 2026 20:31:14 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b5a225ddc6899e9c75779bded72b20a109513816ebeb753ba45b3df1a3cd4a`  
		Last Modified: Fri, 08 May 2026 20:31:15 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11` - unknown; unknown

```console
$ docker pull influxdb@sha256:befbb21962e97b1420386cd3914df97b4209b174ba47f1b1625cf35b781c602c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5960716ed54a9d07a0937b20fe1210c796c731a4edb4ca0a25cac9b69a452eca`

```dockerfile
```

-	Layers:
	-	`sha256:2738c91679e6c3965faf5215f30ed2bbb14179de82c513f542f5a2d2ab434c47`  
		Last Modified: Fri, 08 May 2026 20:31:14 GMT  
		Size: 5.1 MB (5079263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22dd15852d99815234eef981d2fe38857134502695a4d0926e75f6314c511685`  
		Last Modified: Fri, 08 May 2026 20:31:14 GMT  
		Size: 15.5 KB (15486 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:3a3c90d680d1e79747a739495e8ed5be8d0e0e52f9d6d3cadc7fc7dcd9b51fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113108041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e48b5a6a523f5ba6ab40622487c455aa8b30079a1c690e9015dc610e5161d5b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:42:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:36:20 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Fri, 08 May 2026 20:36:28 GMT
ARG INFLUXDB_VERSION=1.11.8
# Fri, 08 May 2026 20:36:28 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:36:28 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 08 May 2026 20:36:28 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 08 May 2026 20:36:28 GMT
VOLUME [/var/lib/influxdb]
# Fri, 08 May 2026 20:36:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 20:36:28 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 08 May 2026 20:36:28 GMT
USER influxdb
# Fri, 08 May 2026 20:36:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 20:36:28 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f56578c9577bd69a05b2319baacd770a986ae61a8568047ddd91db1a1893b4`  
		Last Modified: Fri, 08 May 2026 19:42:30 GMT  
		Size: 23.6 MB (23609357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a5991a527ece9c7cb2d1297712c682f0c2c69bb8bfd91048b4785a80b26e00`  
		Last Modified: Fri, 08 May 2026 20:36:43 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33601031aa7e444585bd97ca31abe468fe1f27fc4a5719fa1f7249326522cc8`  
		Last Modified: Fri, 08 May 2026 20:36:44 GMT  
		Size: 41.1 MB (41122626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49366e22e603f889434100c2186fbd1946e3e22ad4f4a56cdcf676f55872a61c`  
		Last Modified: Fri, 08 May 2026 20:36:43 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec735f59f253ce164a95008a327d7a092986d14907cfef628f0b15a2a922b99`  
		Last Modified: Fri, 08 May 2026 20:36:43 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881a56b2b0412eb8f9ba17b284624545402450756ece8b978090238ba1559591`  
		Last Modified: Fri, 08 May 2026 20:36:44 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11` - unknown; unknown

```console
$ docker pull influxdb@sha256:48f2fbc06a606d005fb042e358ac4cb36e4b0edcc563cd742b3415316bbd106d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bb16709b3ba5dee9e9914aa6ff20d86db646e8844d6edc042e0639d32068257`

```dockerfile
```

-	Layers:
	-	`sha256:25d67e113ed75173e370d8904c77f9846d2d57927e0a7c4dfea1d183535abb42`  
		Last Modified: Fri, 08 May 2026 20:36:44 GMT  
		Size: 5.1 MB (5078728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f372fc26c75495e918f5d6416d8958d6d8c0d2e9b05f128a467f080a4d7fbd1`  
		Last Modified: Fri, 08 May 2026 20:36:43 GMT  
		Size: 15.6 KB (15580 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-alpine`

```console
$ docker pull influxdb@sha256:419e4ffe93ef96b43fc0e5b39526aa3e0ac2226250c23614450841df7688e9e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:4c76eeaa092506d77c8d780d89ac63adc4b304b19f52ff248c88fba14fac9430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42932017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb739a4b0a795f06b6051ebd9d208b590f75888449c7c93d6c537070281dab8f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:26 GMT
ADD alpine-minirootfs-3.20.10-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:26 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:29:34 GMT
RUN apk add --no-cache       bash       ca-certificates       tzdata &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:29:37 GMT
ARG INFLUXDB_VERSION=1.11.8
# Fri, 17 Apr 2026 00:29:37 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN apk add --no-cache --virtual .build-deps       curl       gnupg       tar &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     case "$(apk --print-arch)" in       x86_64)  ARCH=amd64 ;;       aarch64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_TAR=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_TAR}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_TAR}" &&     tar -xf "${INFLUXDB_TAR}" -C /usr/bin       influx       influx_inspect       influxd &&     rm -rf "${INFLUXDB_TAR}"            "${INFLUXDB_ASC}" &&     apk del .build-deps # buildkit
# Fri, 17 Apr 2026 00:29:37 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 17 Apr 2026 00:29:37 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Fri, 17 Apr 2026 00:29:37 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 17 Apr 2026 00:29:37 GMT
VOLUME [/var/lib/influxdb]
# Fri, 17 Apr 2026 00:29:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:29:37 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 17 Apr 2026 00:29:37 GMT
USER influxdb
# Fri, 17 Apr 2026 00:29:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:29:37 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:25f1d6b1951ac8eb3740558fe94cb83d377bdadf95fd9f98b50d2e1b96130471`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.6 MB (3630321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a964c1456688d9e91d17ff249cf8f46b8d248c8ceae20e5ad1e3f631d145106`  
		Last Modified: Fri, 17 Apr 2026 00:29:45 GMT  
		Size: 1.2 MB (1223408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c0b29a6bcc1ddc5f611a1bd4baa046a1fe95c83846e12ccf61275c10a6b50f`  
		Last Modified: Fri, 17 Apr 2026 00:29:47 GMT  
		Size: 38.1 MB (38075567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4484e44f987b74505d93a34532a729c17bac3580abf6689a7b3c011e81e8b5d8`  
		Last Modified: Fri, 17 Apr 2026 00:29:45 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d653f6cd37fe403cbf746db11e4348daf8f5effca8287be5f6edcb6613cb43`  
		Last Modified: Fri, 17 Apr 2026 00:29:45 GMT  
		Size: 1.0 KB (1004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8922b85e83f437e5c0843835d5327a5b394012abcd27cad21dcd98477f2bc42`  
		Last Modified: Fri, 17 Apr 2026 00:29:46 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe88da3c5720a7c41515701414e448e861959fb96f5255700f445ff0d67e81f`  
		Last Modified: Fri, 17 Apr 2026 00:29:47 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:8fbf800cdadfea0b8992cc229b3447e8575b68781c771da3d910b69308e1541f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.6 KB (759628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eea0d8e05628e39054f3a2aba04625b5ee155b8edb1d8b20f2ee1b7f63d74fb`

```dockerfile
```

-	Layers:
	-	`sha256:c668b58232d931805408605abc897b2daf3d2f4b74df70fd24e385d0459b686a`  
		Last Modified: Fri, 17 Apr 2026 00:29:45 GMT  
		Size: 741.8 KB (741795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:077a5ff896fde8f6fd8491992a454a0b7a3fd7e4d044cbf27374ef042d1d92dd`  
		Last Modified: Fri, 17 Apr 2026 00:29:45 GMT  
		Size: 17.8 KB (17833 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:513a0d643ec8b6175a5e24c1b838036c2aa7630185cb5917160bfb09a99eab1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40945964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf44fa8e934f487731190cd92d27f224f93725d2d3a0155b2d620100d17b02f8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:24 GMT
ADD alpine-minirootfs-3.20.10-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:24 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:30:27 GMT
RUN apk add --no-cache       bash       ca-certificates       tzdata &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:30:34 GMT
ARG INFLUXDB_VERSION=1.11.8
# Fri, 17 Apr 2026 00:30:34 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN apk add --no-cache --virtual .build-deps       curl       gnupg       tar &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     case "$(apk --print-arch)" in       x86_64)  ARCH=amd64 ;;       aarch64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_TAR=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_TAR}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_TAR}" &&     tar -xf "${INFLUXDB_TAR}" -C /usr/bin       influx       influx_inspect       influxd &&     rm -rf "${INFLUXDB_TAR}"            "${INFLUXDB_ASC}" &&     apk del .build-deps # buildkit
# Fri, 17 Apr 2026 00:30:34 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 17 Apr 2026 00:30:34 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Fri, 17 Apr 2026 00:30:34 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 17 Apr 2026 00:30:34 GMT
VOLUME [/var/lib/influxdb]
# Fri, 17 Apr 2026 00:30:34 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:30:34 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 17 Apr 2026 00:30:34 GMT
USER influxdb
# Fri, 17 Apr 2026 00:30:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:30:34 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:3f26bc2dec0b515f1c2818f6e13a8f1da1f88179a008445d4e587233386bff78`  
		Last Modified: Thu, 16 Apr 2026 23:53:29 GMT  
		Size: 4.1 MB (4092319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7528f7b477c1f45c788486e4f22d1e625803f9ad343cffad3d7ca4a72ee96885`  
		Last Modified: Fri, 17 Apr 2026 00:30:43 GMT  
		Size: 1.3 MB (1302825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b49b142f1a9c000355769f9367b4aeb76840aa3d4fd22b870f87402ef47f39`  
		Last Modified: Fri, 17 Apr 2026 00:30:44 GMT  
		Size: 35.5 MB (35548102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a29c57e0ca961519e3894dc9b23a85d622fe9ec614292aa0b6147061e0692f5`  
		Last Modified: Fri, 17 Apr 2026 00:30:43 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f1e6f83a12b230e59ce7b7002316f0cc9d99d7d3e3e5443ce0932e65c7ce65`  
		Last Modified: Fri, 17 Apr 2026 00:30:43 GMT  
		Size: 1.0 KB (1003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28cb7fdd045195b6350a98581e48dbba2142ff84106883f3625723d0c2af647f`  
		Last Modified: Fri, 17 Apr 2026 00:30:44 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94841f38abd8c13738008d8c0461ed0510ac114425c1d3f01212dddfadd6bea6`  
		Last Modified: Fri, 17 Apr 2026 00:30:44 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:08933b450391d4178e8e4e4740e31ade6d78698256b6194ace47a35122b4a87f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.0 KB (758966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb9cae961ebdb6f250bbfde78239036b016cf8d85a2c961b92c8c3dd34aaa5d6`

```dockerfile
```

-	Layers:
	-	`sha256:53d2dca8b1153e03244dea4c5a91a26dc89204541192fc1c83b5564269eaa6b6`  
		Last Modified: Fri, 17 Apr 2026 00:30:43 GMT  
		Size: 741.0 KB (741022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f13321e25efbd6bc8e4ee9f35d75f203183eafe497bb18058147b17a5584383`  
		Last Modified: Fri, 17 Apr 2026 00:30:43 GMT  
		Size: 17.9 KB (17944 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-data`

```console
$ docker pull influxdb@sha256:b786934812919d09cab7d154f60be771897539ef551c77edab3840c9c21d48e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data` - linux; amd64

```console
$ docker pull influxdb@sha256:24afc9b640c7ef74740c1e0918cbb9f74338c5d7029656ff4d75e3620877bfeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114703426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:283105d588e67f22f430113426547aecc73725dfb3e33feb43b05037a7bd9019`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:31:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 08 May 2026 20:31:14 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Fri, 08 May 2026 20:31:14 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Fri, 08 May 2026 20:31:14 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 08 May 2026 20:31:14 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 08 May 2026 20:31:14 GMT
VOLUME [/var/lib/influxdb]
# Fri, 08 May 2026 20:31:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 20:31:14 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 08 May 2026 20:31:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 20:31:14 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d055cea50c88c57fc27fcd44845ebabfe5b830ea8a0a621b89d38a2b650b7ff3`  
		Last Modified: Fri, 08 May 2026 19:40:29 GMT  
		Size: 24.0 MB (24042180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242e0e95e73ea58a3c02c9b70b6e59a453571929720a16f5ac236f2c21e1b6a7`  
		Last Modified: Fri, 08 May 2026 20:31:26 GMT  
		Size: 5.1 KB (5056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3516fd77fd8a8dbd6444cd1a5013ac471160e5fbcb34b6d9f01be495a8072740`  
		Last Modified: Fri, 08 May 2026 20:31:28 GMT  
		Size: 42.2 MB (42165740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccc675e260ad6db3305ea9b730e5280069a9f16f1cf20dd342d8275569a027d`  
		Last Modified: Fri, 08 May 2026 20:31:26 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21be18d7f9a1c7a08a3e07f0993b3ea97a0d9193c4ac1b84534e9d5dfc143f9f`  
		Last Modified: Fri, 08 May 2026 20:31:26 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3c0cfceb712532323652c1c1b7e28fa91ec36826fcb3bbff47fdcb20d06d6a`  
		Last Modified: Fri, 08 May 2026 20:31:28 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:ebc8ceed9be5a00fc758a033fe53a59bbfecee3e162dce6206586f202460bbe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4699071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095a3869b3e0fa239ae77fd0cae50b0a6c692c1de4c98abc538dfc9163b09687`

```dockerfile
```

-	Layers:
	-	`sha256:9062516ed121d018d8e87175cfe7bb058a04f605c6139fab0cec84e9c008d3f9`  
		Last Modified: Fri, 08 May 2026 20:31:27 GMT  
		Size: 4.7 MB (4684406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bc34dbc5f340362b9f0be81242eca95ba37ba516c306b0a9e00989fd77c29cd`  
		Last Modified: Fri, 08 May 2026 20:31:26 GMT  
		Size: 14.7 KB (14665 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-data-alpine`

```console
$ docker pull influxdb@sha256:2c730e49a113a126b1281048b9c98c5373f3b3ed9c57a99bdca5af87c064c3bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:0671e00fc1703a2335d7d8ccec6d5c3fc877a7b655e445dbb4d9b7eff7de5466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (46961715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a2c871250391b6e26e632188146322a8300af32771a450554299b21f6a95ce5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:26 GMT
ADD alpine-minirootfs-3.20.10-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:26 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:23:28 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 00:29:35 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:29:40 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Fri, 17 Apr 2026 00:29:40 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 17 Apr 2026 00:29:40 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 17 Apr 2026 00:29:40 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 17 Apr 2026 00:29:40 GMT
VOLUME [/var/lib/influxdb]
# Fri, 17 Apr 2026 00:29:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:29:40 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 17 Apr 2026 00:29:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:29:40 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:25f1d6b1951ac8eb3740558fe94cb83d377bdadf95fd9f98b50d2e1b96130471`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.6 MB (3630321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16e69077797f1a90c5b8946765d6547bd0bbe62c5edf87016fc687d8691b62a`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af57cce8ae005f5a40607aad79b1ddb8723ac2ed76151ffcc1a72c328acacc7d`  
		Last Modified: Fri, 17 Apr 2026 00:29:51 GMT  
		Size: 1.2 MB (1223405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d046eafdb2a4db7f864b62f3ab9ed93e3cd1553bda6057bc02efb3f740c1306d`  
		Last Modified: Fri, 17 Apr 2026 00:29:52 GMT  
		Size: 42.1 MB (42105941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d9ccf75a23a13dff950bb929cd6a60c7208cf7a1699d7c546576a049220dd0`  
		Last Modified: Fri, 17 Apr 2026 00:29:51 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d083a439c971ab903b7be1cd6b575d9ee65e56179ae9825601147ea925a137b`  
		Last Modified: Fri, 17 Apr 2026 00:29:51 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a380e4d1db8548c3b44fce44aa833ff6cdc0b8ca30c39f0d3128651c073c66d`  
		Last Modified: Fri, 17 Apr 2026 00:29:52 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:165efda98c84959e51ced992a98d0cbacdefc15c74a015c0e6dc3b0e0e310660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **784.9 KB (784902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67062268e78fc070e07f5bad9381325bde8f0cabae65bf623ee76e4492cd1b7e`

```dockerfile
```

-	Layers:
	-	`sha256:3ee75c0665dafeeb249371bbbf9d57fcea7ba80183e5d44744949922acfbd7d5`  
		Last Modified: Fri, 17 Apr 2026 00:29:51 GMT  
		Size: 768.3 KB (768306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b01deace176bb6b1fb0eb0ed1ecd4c734ce2a20e172d872b40a93997108554a2`  
		Last Modified: Fri, 17 Apr 2026 00:29:51 GMT  
		Size: 16.6 KB (16596 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-meta`

```console
$ docker pull influxdb@sha256:3c5b2e0bd5581e3d8cbb67e1c5172d38a1e0b42df58445d0605820ab3665a1ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:ea1593b619759437437bc5be1d9a35ddaed80c62d29c89f55d21c059cc4ef8b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91132630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e419949d2b367440de707c7b722cdbe914853b53cf924d90156f735335801ad8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:31:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 08 May 2026 20:31:10 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Fri, 08 May 2026 20:31:10 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Fri, 08 May 2026 20:31:10 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Fri, 08 May 2026 20:31:10 GMT
EXPOSE map[8091/tcp:{}]
# Fri, 08 May 2026 20:31:10 GMT
VOLUME [/var/lib/influxdb]
# Fri, 08 May 2026 20:31:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 20:31:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 20:31:10 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d055cea50c88c57fc27fcd44845ebabfe5b830ea8a0a621b89d38a2b650b7ff3`  
		Last Modified: Fri, 08 May 2026 19:40:29 GMT  
		Size: 24.0 MB (24042180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78bfb5e8d1f9fc3a8975eab40ee71dc7620fc203bc375dbb0b9534aaf417d706`  
		Last Modified: Fri, 08 May 2026 20:31:19 GMT  
		Size: 5.1 KB (5056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b896672d5b689b4a7343388d5f3a4e1a9cef918fc14ef0a990e66803b809e4f`  
		Last Modified: Fri, 08 May 2026 20:31:20 GMT  
		Size: 18.6 MB (18596153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ba7b2860167f73d9d2bdd430d7fc23e349b04da41894f4b0418fa9085b5460`  
		Last Modified: Fri, 08 May 2026 20:31:19 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b4e45f64d1c0baacdce9da58e0d4f6d02f11d4fab80d842ce692c8de20b635`  
		Last Modified: Fri, 08 May 2026 20:31:19 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:43ff505dc544042e4176c136e9385cccc3350eb8beb287d190c53fa191a08ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4604273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4af004f40cae2f2f1f1a3c3d4042881fddb3cbc235cb19973538e203843e220`

```dockerfile
```

-	Layers:
	-	`sha256:d25a540e1080daefdd6b2b80c5c601e76308413dec5d677a40ff5ae13e494430`  
		Last Modified: Fri, 08 May 2026 20:31:19 GMT  
		Size: 4.6 MB (4591249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cfa85d48bc765a776682977fd3d546cd44783a7e6f6d0912e07869847b41290`  
		Last Modified: Fri, 08 May 2026 20:31:19 GMT  
		Size: 13.0 KB (13024 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-meta-alpine`

```console
$ docker pull influxdb@sha256:daddca33674d6c64b22a7b6c8c2de2eacaf080740cd6af5fd19a3e72bb137c5c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:862b7bf142bd9364711341e8f1f3d2520a18116170d0ffae6efd549f8c97f283
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23404458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ea1bdcd315b61c5f93e52bf43f255d6783fb267040bfce52c7db27d36b06c5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:26 GMT
ADD alpine-minirootfs-3.20.10-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:26 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:23:28 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 00:29:48 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:29:51 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Fri, 17 Apr 2026 00:29:51 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 17 Apr 2026 00:29:51 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Fri, 17 Apr 2026 00:29:51 GMT
EXPOSE map[8091/tcp:{}]
# Fri, 17 Apr 2026 00:29:51 GMT
VOLUME [/var/lib/influxdb]
# Fri, 17 Apr 2026 00:29:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:29:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:29:51 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:25f1d6b1951ac8eb3740558fe94cb83d377bdadf95fd9f98b50d2e1b96130471`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.6 MB (3630321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16e69077797f1a90c5b8946765d6547bd0bbe62c5edf87016fc687d8691b62a`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9955919308d229699ac49bbc72bab580fd288f1af2f3b6cc66a957c6d3d24885`  
		Last Modified: Fri, 17 Apr 2026 00:29:58 GMT  
		Size: 1.2 MB (1223402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7a220e4724731871c74b6b012d6715930a5bb3565f1efdffd443db33f3376b`  
		Last Modified: Fri, 17 Apr 2026 00:29:58 GMT  
		Size: 18.5 MB (18549892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d5be0b517eeb7c96c4a09e24f86e5a307ad93bd508d312c16c7e06c47898e4a`  
		Last Modified: Fri, 17 Apr 2026 00:29:58 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:505381ed372988e41482fe95507ecec0af5458d244367e5eb52e8434076157cb`  
		Last Modified: Fri, 17 Apr 2026 00:29:58 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:db9d12f0b4dc24b7138485d50373557147062d696e39c6f45f4bc5af0bac03ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **690.9 KB (690902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88402e2c7be6cf4b869598e08df66f57a37e996b8401a0fb858d27613087a3dc`

```dockerfile
```

-	Layers:
	-	`sha256:f111903fd5464752b27291f2048e29a6a47be84533209ad5256fe7bec19799e9`  
		Last Modified: Fri, 17 Apr 2026 00:29:58 GMT  
		Size: 675.9 KB (675935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28f1a7f75df23b853dcd0246a4244377266683be022a9f0d9df941570b16edc0`  
		Last Modified: Fri, 17 Apr 2026 00:29:58 GMT  
		Size: 15.0 KB (14967 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.8`

```console
$ docker pull influxdb@sha256:70f8a10e5726d211ab9362bd4a669df9d5e8e3549d22528df3e0e8a1cfa5cbea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11.8` - linux; amd64

```console
$ docker pull influxdb@sha256:1c15b66266dd49f111fa7f6340628d24c13bb014dfb304b4092e7547a1ed39df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116189812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e6eb06132753abaae1609af5ddd266d258a0f9a62296f07b0fe1371f6dd1aed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:30:54 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Fri, 08 May 2026 20:31:02 GMT
ARG INFLUXDB_VERSION=1.11.8
# Fri, 08 May 2026 20:31:02 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:31:02 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 08 May 2026 20:31:02 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 08 May 2026 20:31:02 GMT
VOLUME [/var/lib/influxdb]
# Fri, 08 May 2026 20:31:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 20:31:02 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 08 May 2026 20:31:02 GMT
USER influxdb
# Fri, 08 May 2026 20:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 20:31:02 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d055cea50c88c57fc27fcd44845ebabfe5b830ea8a0a621b89d38a2b650b7ff3`  
		Last Modified: Fri, 08 May 2026 19:40:29 GMT  
		Size: 24.0 MB (24042180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d1a479d575ada2bb52270e86d838a14e87194f9d0de78fbd42a48b72350831`  
		Last Modified: Fri, 08 May 2026 20:31:14 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f254fee05f3ff0e1c3e9cf4ebb8af9361f14aefebdce87061d682e7701ba382`  
		Last Modified: Fri, 08 May 2026 20:31:15 GMT  
		Size: 43.7 MB (43656039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd4330ebe90c14d751dbdbae8be3299d623176cf1d0ee8e1378081d46c21744`  
		Last Modified: Fri, 08 May 2026 20:31:15 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1e612b9a8e7f312257ab33f0ff665ea04aef07bc6d5cb740ecf12c0f6ba14c`  
		Last Modified: Fri, 08 May 2026 20:31:14 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b5a225ddc6899e9c75779bded72b20a109513816ebeb753ba45b3df1a3cd4a`  
		Last Modified: Fri, 08 May 2026 20:31:15 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:befbb21962e97b1420386cd3914df97b4209b174ba47f1b1625cf35b781c602c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5960716ed54a9d07a0937b20fe1210c796c731a4edb4ca0a25cac9b69a452eca`

```dockerfile
```

-	Layers:
	-	`sha256:2738c91679e6c3965faf5215f30ed2bbb14179de82c513f542f5a2d2ab434c47`  
		Last Modified: Fri, 08 May 2026 20:31:14 GMT  
		Size: 5.1 MB (5079263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22dd15852d99815234eef981d2fe38857134502695a4d0926e75f6314c511685`  
		Last Modified: Fri, 08 May 2026 20:31:14 GMT  
		Size: 15.5 KB (15486 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:3a3c90d680d1e79747a739495e8ed5be8d0e0e52f9d6d3cadc7fc7dcd9b51fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113108041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e48b5a6a523f5ba6ab40622487c455aa8b30079a1c690e9015dc610e5161d5b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:42:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:36:20 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Fri, 08 May 2026 20:36:28 GMT
ARG INFLUXDB_VERSION=1.11.8
# Fri, 08 May 2026 20:36:28 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:36:28 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 08 May 2026 20:36:28 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 08 May 2026 20:36:28 GMT
VOLUME [/var/lib/influxdb]
# Fri, 08 May 2026 20:36:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 20:36:28 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 08 May 2026 20:36:28 GMT
USER influxdb
# Fri, 08 May 2026 20:36:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 20:36:28 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f56578c9577bd69a05b2319baacd770a986ae61a8568047ddd91db1a1893b4`  
		Last Modified: Fri, 08 May 2026 19:42:30 GMT  
		Size: 23.6 MB (23609357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a5991a527ece9c7cb2d1297712c682f0c2c69bb8bfd91048b4785a80b26e00`  
		Last Modified: Fri, 08 May 2026 20:36:43 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33601031aa7e444585bd97ca31abe468fe1f27fc4a5719fa1f7249326522cc8`  
		Last Modified: Fri, 08 May 2026 20:36:44 GMT  
		Size: 41.1 MB (41122626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49366e22e603f889434100c2186fbd1946e3e22ad4f4a56cdcf676f55872a61c`  
		Last Modified: Fri, 08 May 2026 20:36:43 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec735f59f253ce164a95008a327d7a092986d14907cfef628f0b15a2a922b99`  
		Last Modified: Fri, 08 May 2026 20:36:43 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881a56b2b0412eb8f9ba17b284624545402450756ece8b978090238ba1559591`  
		Last Modified: Fri, 08 May 2026 20:36:44 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:48f2fbc06a606d005fb042e358ac4cb36e4b0edcc563cd742b3415316bbd106d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bb16709b3ba5dee9e9914aa6ff20d86db646e8844d6edc042e0639d32068257`

```dockerfile
```

-	Layers:
	-	`sha256:25d67e113ed75173e370d8904c77f9846d2d57927e0a7c4dfea1d183535abb42`  
		Last Modified: Fri, 08 May 2026 20:36:44 GMT  
		Size: 5.1 MB (5078728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f372fc26c75495e918f5d6416d8958d6d8c0d2e9b05f128a467f080a4d7fbd1`  
		Last Modified: Fri, 08 May 2026 20:36:43 GMT  
		Size: 15.6 KB (15580 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.8-alpine`

```console
$ docker pull influxdb@sha256:419e4ffe93ef96b43fc0e5b39526aa3e0ac2226250c23614450841df7688e9e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11.8-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:4c76eeaa092506d77c8d780d89ac63adc4b304b19f52ff248c88fba14fac9430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42932017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb739a4b0a795f06b6051ebd9d208b590f75888449c7c93d6c537070281dab8f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:26 GMT
ADD alpine-minirootfs-3.20.10-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:26 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:29:34 GMT
RUN apk add --no-cache       bash       ca-certificates       tzdata &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:29:37 GMT
ARG INFLUXDB_VERSION=1.11.8
# Fri, 17 Apr 2026 00:29:37 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN apk add --no-cache --virtual .build-deps       curl       gnupg       tar &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     case "$(apk --print-arch)" in       x86_64)  ARCH=amd64 ;;       aarch64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_TAR=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_TAR}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_TAR}" &&     tar -xf "${INFLUXDB_TAR}" -C /usr/bin       influx       influx_inspect       influxd &&     rm -rf "${INFLUXDB_TAR}"            "${INFLUXDB_ASC}" &&     apk del .build-deps # buildkit
# Fri, 17 Apr 2026 00:29:37 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 17 Apr 2026 00:29:37 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Fri, 17 Apr 2026 00:29:37 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 17 Apr 2026 00:29:37 GMT
VOLUME [/var/lib/influxdb]
# Fri, 17 Apr 2026 00:29:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:29:37 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 17 Apr 2026 00:29:37 GMT
USER influxdb
# Fri, 17 Apr 2026 00:29:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:29:37 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:25f1d6b1951ac8eb3740558fe94cb83d377bdadf95fd9f98b50d2e1b96130471`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.6 MB (3630321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a964c1456688d9e91d17ff249cf8f46b8d248c8ceae20e5ad1e3f631d145106`  
		Last Modified: Fri, 17 Apr 2026 00:29:45 GMT  
		Size: 1.2 MB (1223408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c0b29a6bcc1ddc5f611a1bd4baa046a1fe95c83846e12ccf61275c10a6b50f`  
		Last Modified: Fri, 17 Apr 2026 00:29:47 GMT  
		Size: 38.1 MB (38075567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4484e44f987b74505d93a34532a729c17bac3580abf6689a7b3c011e81e8b5d8`  
		Last Modified: Fri, 17 Apr 2026 00:29:45 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d653f6cd37fe403cbf746db11e4348daf8f5effca8287be5f6edcb6613cb43`  
		Last Modified: Fri, 17 Apr 2026 00:29:45 GMT  
		Size: 1.0 KB (1004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8922b85e83f437e5c0843835d5327a5b394012abcd27cad21dcd98477f2bc42`  
		Last Modified: Fri, 17 Apr 2026 00:29:46 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe88da3c5720a7c41515701414e448e861959fb96f5255700f445ff0d67e81f`  
		Last Modified: Fri, 17 Apr 2026 00:29:47 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:8fbf800cdadfea0b8992cc229b3447e8575b68781c771da3d910b69308e1541f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.6 KB (759628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eea0d8e05628e39054f3a2aba04625b5ee155b8edb1d8b20f2ee1b7f63d74fb`

```dockerfile
```

-	Layers:
	-	`sha256:c668b58232d931805408605abc897b2daf3d2f4b74df70fd24e385d0459b686a`  
		Last Modified: Fri, 17 Apr 2026 00:29:45 GMT  
		Size: 741.8 KB (741795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:077a5ff896fde8f6fd8491992a454a0b7a3fd7e4d044cbf27374ef042d1d92dd`  
		Last Modified: Fri, 17 Apr 2026 00:29:45 GMT  
		Size: 17.8 KB (17833 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11.8-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:513a0d643ec8b6175a5e24c1b838036c2aa7630185cb5917160bfb09a99eab1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40945964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf44fa8e934f487731190cd92d27f224f93725d2d3a0155b2d620100d17b02f8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:24 GMT
ADD alpine-minirootfs-3.20.10-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:24 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:30:27 GMT
RUN apk add --no-cache       bash       ca-certificates       tzdata &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:30:34 GMT
ARG INFLUXDB_VERSION=1.11.8
# Fri, 17 Apr 2026 00:30:34 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN apk add --no-cache --virtual .build-deps       curl       gnupg       tar &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     case "$(apk --print-arch)" in       x86_64)  ARCH=amd64 ;;       aarch64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_TAR=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_TAR}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_TAR}" &&     tar -xf "${INFLUXDB_TAR}" -C /usr/bin       influx       influx_inspect       influxd &&     rm -rf "${INFLUXDB_TAR}"            "${INFLUXDB_ASC}" &&     apk del .build-deps # buildkit
# Fri, 17 Apr 2026 00:30:34 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 17 Apr 2026 00:30:34 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Fri, 17 Apr 2026 00:30:34 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 17 Apr 2026 00:30:34 GMT
VOLUME [/var/lib/influxdb]
# Fri, 17 Apr 2026 00:30:34 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:30:34 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 17 Apr 2026 00:30:34 GMT
USER influxdb
# Fri, 17 Apr 2026 00:30:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:30:34 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:3f26bc2dec0b515f1c2818f6e13a8f1da1f88179a008445d4e587233386bff78`  
		Last Modified: Thu, 16 Apr 2026 23:53:29 GMT  
		Size: 4.1 MB (4092319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7528f7b477c1f45c788486e4f22d1e625803f9ad343cffad3d7ca4a72ee96885`  
		Last Modified: Fri, 17 Apr 2026 00:30:43 GMT  
		Size: 1.3 MB (1302825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b49b142f1a9c000355769f9367b4aeb76840aa3d4fd22b870f87402ef47f39`  
		Last Modified: Fri, 17 Apr 2026 00:30:44 GMT  
		Size: 35.5 MB (35548102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a29c57e0ca961519e3894dc9b23a85d622fe9ec614292aa0b6147061e0692f5`  
		Last Modified: Fri, 17 Apr 2026 00:30:43 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f1e6f83a12b230e59ce7b7002316f0cc9d99d7d3e3e5443ce0932e65c7ce65`  
		Last Modified: Fri, 17 Apr 2026 00:30:43 GMT  
		Size: 1.0 KB (1003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28cb7fdd045195b6350a98581e48dbba2142ff84106883f3625723d0c2af647f`  
		Last Modified: Fri, 17 Apr 2026 00:30:44 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94841f38abd8c13738008d8c0461ed0510ac114425c1d3f01212dddfadd6bea6`  
		Last Modified: Fri, 17 Apr 2026 00:30:44 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:08933b450391d4178e8e4e4740e31ade6d78698256b6194ace47a35122b4a87f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.0 KB (758966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb9cae961ebdb6f250bbfde78239036b016cf8d85a2c961b92c8c3dd34aaa5d6`

```dockerfile
```

-	Layers:
	-	`sha256:53d2dca8b1153e03244dea4c5a91a26dc89204541192fc1c83b5564269eaa6b6`  
		Last Modified: Fri, 17 Apr 2026 00:30:43 GMT  
		Size: 741.0 KB (741022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f13321e25efbd6bc8e4ee9f35d75f203183eafe497bb18058147b17a5584383`  
		Last Modified: Fri, 17 Apr 2026 00:30:43 GMT  
		Size: 17.9 KB (17944 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.9-data`

```console
$ docker pull influxdb@sha256:b786934812919d09cab7d154f60be771897539ef551c77edab3840c9c21d48e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.9-data` - linux; amd64

```console
$ docker pull influxdb@sha256:24afc9b640c7ef74740c1e0918cbb9f74338c5d7029656ff4d75e3620877bfeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114703426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:283105d588e67f22f430113426547aecc73725dfb3e33feb43b05037a7bd9019`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:31:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 08 May 2026 20:31:14 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Fri, 08 May 2026 20:31:14 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Fri, 08 May 2026 20:31:14 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 08 May 2026 20:31:14 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 08 May 2026 20:31:14 GMT
VOLUME [/var/lib/influxdb]
# Fri, 08 May 2026 20:31:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 20:31:14 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 08 May 2026 20:31:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 20:31:14 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d055cea50c88c57fc27fcd44845ebabfe5b830ea8a0a621b89d38a2b650b7ff3`  
		Last Modified: Fri, 08 May 2026 19:40:29 GMT  
		Size: 24.0 MB (24042180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242e0e95e73ea58a3c02c9b70b6e59a453571929720a16f5ac236f2c21e1b6a7`  
		Last Modified: Fri, 08 May 2026 20:31:26 GMT  
		Size: 5.1 KB (5056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3516fd77fd8a8dbd6444cd1a5013ac471160e5fbcb34b6d9f01be495a8072740`  
		Last Modified: Fri, 08 May 2026 20:31:28 GMT  
		Size: 42.2 MB (42165740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccc675e260ad6db3305ea9b730e5280069a9f16f1cf20dd342d8275569a027d`  
		Last Modified: Fri, 08 May 2026 20:31:26 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21be18d7f9a1c7a08a3e07f0993b3ea97a0d9193c4ac1b84534e9d5dfc143f9f`  
		Last Modified: Fri, 08 May 2026 20:31:26 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3c0cfceb712532323652c1c1b7e28fa91ec36826fcb3bbff47fdcb20d06d6a`  
		Last Modified: Fri, 08 May 2026 20:31:28 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.9-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:ebc8ceed9be5a00fc758a033fe53a59bbfecee3e162dce6206586f202460bbe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4699071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095a3869b3e0fa239ae77fd0cae50b0a6c692c1de4c98abc538dfc9163b09687`

```dockerfile
```

-	Layers:
	-	`sha256:9062516ed121d018d8e87175cfe7bb058a04f605c6139fab0cec84e9c008d3f9`  
		Last Modified: Fri, 08 May 2026 20:31:27 GMT  
		Size: 4.7 MB (4684406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bc34dbc5f340362b9f0be81242eca95ba37ba516c306b0a9e00989fd77c29cd`  
		Last Modified: Fri, 08 May 2026 20:31:26 GMT  
		Size: 14.7 KB (14665 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.9-data-alpine`

```console
$ docker pull influxdb@sha256:2c730e49a113a126b1281048b9c98c5373f3b3ed9c57a99bdca5af87c064c3bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.9-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:0671e00fc1703a2335d7d8ccec6d5c3fc877a7b655e445dbb4d9b7eff7de5466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (46961715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a2c871250391b6e26e632188146322a8300af32771a450554299b21f6a95ce5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:26 GMT
ADD alpine-minirootfs-3.20.10-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:26 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:23:28 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 00:29:35 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:29:40 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Fri, 17 Apr 2026 00:29:40 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 17 Apr 2026 00:29:40 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 17 Apr 2026 00:29:40 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 17 Apr 2026 00:29:40 GMT
VOLUME [/var/lib/influxdb]
# Fri, 17 Apr 2026 00:29:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:29:40 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 17 Apr 2026 00:29:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:29:40 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:25f1d6b1951ac8eb3740558fe94cb83d377bdadf95fd9f98b50d2e1b96130471`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.6 MB (3630321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16e69077797f1a90c5b8946765d6547bd0bbe62c5edf87016fc687d8691b62a`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af57cce8ae005f5a40607aad79b1ddb8723ac2ed76151ffcc1a72c328acacc7d`  
		Last Modified: Fri, 17 Apr 2026 00:29:51 GMT  
		Size: 1.2 MB (1223405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d046eafdb2a4db7f864b62f3ab9ed93e3cd1553bda6057bc02efb3f740c1306d`  
		Last Modified: Fri, 17 Apr 2026 00:29:52 GMT  
		Size: 42.1 MB (42105941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d9ccf75a23a13dff950bb929cd6a60c7208cf7a1699d7c546576a049220dd0`  
		Last Modified: Fri, 17 Apr 2026 00:29:51 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d083a439c971ab903b7be1cd6b575d9ee65e56179ae9825601147ea925a137b`  
		Last Modified: Fri, 17 Apr 2026 00:29:51 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a380e4d1db8548c3b44fce44aa833ff6cdc0b8ca30c39f0d3128651c073c66d`  
		Last Modified: Fri, 17 Apr 2026 00:29:52 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.9-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:165efda98c84959e51ced992a98d0cbacdefc15c74a015c0e6dc3b0e0e310660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **784.9 KB (784902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67062268e78fc070e07f5bad9381325bde8f0cabae65bf623ee76e4492cd1b7e`

```dockerfile
```

-	Layers:
	-	`sha256:3ee75c0665dafeeb249371bbbf9d57fcea7ba80183e5d44744949922acfbd7d5`  
		Last Modified: Fri, 17 Apr 2026 00:29:51 GMT  
		Size: 768.3 KB (768306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b01deace176bb6b1fb0eb0ed1ecd4c734ce2a20e172d872b40a93997108554a2`  
		Last Modified: Fri, 17 Apr 2026 00:29:51 GMT  
		Size: 16.6 KB (16596 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.9-meta`

```console
$ docker pull influxdb@sha256:3c5b2e0bd5581e3d8cbb67e1c5172d38a1e0b42df58445d0605820ab3665a1ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.9-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:ea1593b619759437437bc5be1d9a35ddaed80c62d29c89f55d21c059cc4ef8b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91132630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e419949d2b367440de707c7b722cdbe914853b53cf924d90156f735335801ad8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:31:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Fri, 08 May 2026 20:31:10 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Fri, 08 May 2026 20:31:10 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Fri, 08 May 2026 20:31:10 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Fri, 08 May 2026 20:31:10 GMT
EXPOSE map[8091/tcp:{}]
# Fri, 08 May 2026 20:31:10 GMT
VOLUME [/var/lib/influxdb]
# Fri, 08 May 2026 20:31:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 20:31:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 20:31:10 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d055cea50c88c57fc27fcd44845ebabfe5b830ea8a0a621b89d38a2b650b7ff3`  
		Last Modified: Fri, 08 May 2026 19:40:29 GMT  
		Size: 24.0 MB (24042180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78bfb5e8d1f9fc3a8975eab40ee71dc7620fc203bc375dbb0b9534aaf417d706`  
		Last Modified: Fri, 08 May 2026 20:31:19 GMT  
		Size: 5.1 KB (5056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b896672d5b689b4a7343388d5f3a4e1a9cef918fc14ef0a990e66803b809e4f`  
		Last Modified: Fri, 08 May 2026 20:31:20 GMT  
		Size: 18.6 MB (18596153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ba7b2860167f73d9d2bdd430d7fc23e349b04da41894f4b0418fa9085b5460`  
		Last Modified: Fri, 08 May 2026 20:31:19 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b4e45f64d1c0baacdce9da58e0d4f6d02f11d4fab80d842ce692c8de20b635`  
		Last Modified: Fri, 08 May 2026 20:31:19 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.9-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:43ff505dc544042e4176c136e9385cccc3350eb8beb287d190c53fa191a08ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4604273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4af004f40cae2f2f1f1a3c3d4042881fddb3cbc235cb19973538e203843e220`

```dockerfile
```

-	Layers:
	-	`sha256:d25a540e1080daefdd6b2b80c5c601e76308413dec5d677a40ff5ae13e494430`  
		Last Modified: Fri, 08 May 2026 20:31:19 GMT  
		Size: 4.6 MB (4591249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cfa85d48bc765a776682977fd3d546cd44783a7e6f6d0912e07869847b41290`  
		Last Modified: Fri, 08 May 2026 20:31:19 GMT  
		Size: 13.0 KB (13024 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.9-meta-alpine`

```console
$ docker pull influxdb@sha256:daddca33674d6c64b22a7b6c8c2de2eacaf080740cd6af5fd19a3e72bb137c5c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.9-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:862b7bf142bd9364711341e8f1f3d2520a18116170d0ffae6efd549f8c97f283
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23404458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ea1bdcd315b61c5f93e52bf43f255d6783fb267040bfce52c7db27d36b06c5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:26 GMT
ADD alpine-minirootfs-3.20.10-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:26 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:23:28 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 00:29:48 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:29:51 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Fri, 17 Apr 2026 00:29:51 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Fri, 17 Apr 2026 00:29:51 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Fri, 17 Apr 2026 00:29:51 GMT
EXPOSE map[8091/tcp:{}]
# Fri, 17 Apr 2026 00:29:51 GMT
VOLUME [/var/lib/influxdb]
# Fri, 17 Apr 2026 00:29:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:29:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:29:51 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:25f1d6b1951ac8eb3740558fe94cb83d377bdadf95fd9f98b50d2e1b96130471`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.6 MB (3630321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16e69077797f1a90c5b8946765d6547bd0bbe62c5edf87016fc687d8691b62a`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9955919308d229699ac49bbc72bab580fd288f1af2f3b6cc66a957c6d3d24885`  
		Last Modified: Fri, 17 Apr 2026 00:29:58 GMT  
		Size: 1.2 MB (1223402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7a220e4724731871c74b6b012d6715930a5bb3565f1efdffd443db33f3376b`  
		Last Modified: Fri, 17 Apr 2026 00:29:58 GMT  
		Size: 18.5 MB (18549892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d5be0b517eeb7c96c4a09e24f86e5a307ad93bd508d312c16c7e06c47898e4a`  
		Last Modified: Fri, 17 Apr 2026 00:29:58 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:505381ed372988e41482fe95507ecec0af5458d244367e5eb52e8434076157cb`  
		Last Modified: Fri, 17 Apr 2026 00:29:58 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.9-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:db9d12f0b4dc24b7138485d50373557147062d696e39c6f45f4bc5af0bac03ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **690.9 KB (690902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88402e2c7be6cf4b869598e08df66f57a37e996b8401a0fb858d27613087a3dc`

```dockerfile
```

-	Layers:
	-	`sha256:f111903fd5464752b27291f2048e29a6a47be84533209ad5256fe7bec19799e9`  
		Last Modified: Fri, 17 Apr 2026 00:29:58 GMT  
		Size: 675.9 KB (675935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28f1a7f75df23b853dcd0246a4244377266683be022a9f0d9df941570b16edc0`  
		Last Modified: Fri, 17 Apr 2026 00:29:58 GMT  
		Size: 15.0 KB (14967 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12`

```console
$ docker pull influxdb@sha256:e9363fd88d67f8ae6f019f37a30cc136e3644f2cbaea5abd71ad63c96dc6ae08
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.12` - linux; amd64

```console
$ docker pull influxdb@sha256:70fb0d2c004f475439e044abee282bcdca40dd5bf07c7da48d5eeeb757f9f7a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114660034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df1f9a737bfa342065b155fb4c75b90f5befe474c912b2046a7a6b7c615351f9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:30:41 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Fri, 08 May 2026 20:30:47 GMT
ENV INFLUXDB_VERSION=1.12.4
# Fri, 08 May 2026 20:30:47 GMT
ENV INFLUXDB_PR=-1
# Fri, 08 May 2026 20:30:47 GMT
ENV INFLUXDB_PV=1.12.4-1
# Fri, 08 May 2026 20:30:47 GMT
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_PV}_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:30:47 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 08 May 2026 20:30:47 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 08 May 2026 20:30:47 GMT
VOLUME [/var/lib/influxdb]
# Fri, 08 May 2026 20:30:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 20:30:47 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 08 May 2026 20:30:47 GMT
USER influxdb
# Fri, 08 May 2026 20:30:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 20:30:47 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d055cea50c88c57fc27fcd44845ebabfe5b830ea8a0a621b89d38a2b650b7ff3`  
		Last Modified: Fri, 08 May 2026 19:40:29 GMT  
		Size: 24.0 MB (24042180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9aef9dd3ee15ba56d1914e858a632db3a0757d6ff96d35dc9b99cbf8993f478`  
		Last Modified: Fri, 08 May 2026 20:31:00 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da6117c0a9c02803c1efba4749beb78cd3bda41777c5cc0b85d03cad31d5dab`  
		Last Modified: Fri, 08 May 2026 20:31:01 GMT  
		Size: 42.1 MB (42126263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe387fe968ddd644052b75d259bd582b2657ec49465d2bb692f19594e50c3cb`  
		Last Modified: Fri, 08 May 2026 20:31:00 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffd3eaffded54f5f83c427977d48d7f5695e2ade4839b4cd12cbd9dd76bf8a9`  
		Last Modified: Fri, 08 May 2026 20:31:00 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee0b030e056e99d9b6567b858be0294a0581eecdfb22859e4002fcedf2efc61`  
		Last Modified: Fri, 08 May 2026 20:31:01 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:7ccfb4c3ae7ebf72835eff1dedafdbfb7dc0d209d109c33d87413dc263711802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add224f63b95fe755d2e01b0ab6173162af166aefd7b793206f972fe99b2cb0a`

```dockerfile
```

-	Layers:
	-	`sha256:05e0b1fbf88be7d164e95925c79caf7d55a0149f074aace0a8e0baf95e13c82e`  
		Last Modified: Fri, 08 May 2026 20:31:00 GMT  
		Size: 4.7 MB (4678133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ad32ce71f4e40c81a6717f78e88f22e0cfa5cc834d6a32aaf1a021987d851fa`  
		Last Modified: Fri, 08 May 2026 20:31:00 GMT  
		Size: 16.5 KB (16529 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.12` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:d78d2de9e52ce053bd436726acf103389fa9a946d9a586d448c0aeb388486654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110739824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a950ec6a38ecb85c83329bad98813d8c7d6e0f456fd70d16fe949a619d63c77b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:42:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:36:19 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Fri, 08 May 2026 20:36:24 GMT
ENV INFLUXDB_VERSION=1.12.4
# Fri, 08 May 2026 20:36:24 GMT
ENV INFLUXDB_PR=-1
# Fri, 08 May 2026 20:36:24 GMT
ENV INFLUXDB_PV=1.12.4-1
# Fri, 08 May 2026 20:36:24 GMT
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_PV}_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:36:24 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 08 May 2026 20:36:24 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 08 May 2026 20:36:24 GMT
VOLUME [/var/lib/influxdb]
# Fri, 08 May 2026 20:36:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 20:36:24 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 08 May 2026 20:36:24 GMT
USER influxdb
# Fri, 08 May 2026 20:36:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 20:36:24 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f56578c9577bd69a05b2319baacd770a986ae61a8568047ddd91db1a1893b4`  
		Last Modified: Fri, 08 May 2026 19:42:30 GMT  
		Size: 23.6 MB (23609357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f10c9d0130b02a8e2ea0a143fd27ce60fe500311296bbcd0d15d8e32f35556`  
		Last Modified: Fri, 08 May 2026 20:36:36 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aeba6a20528127046d8b3ac86a7cbefcf861b5fe33ae1cdae95620cddfbaf1f`  
		Last Modified: Fri, 08 May 2026 20:36:38 GMT  
		Size: 38.8 MB (38754404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4a6ddab59dba6cab64122213b1869b06b4ab7c2fda5e06a91c9ae0dbe93837`  
		Last Modified: Fri, 08 May 2026 20:36:36 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582e132768c9ee3ea54b802cc9d8d194551eabe13fb6e99bdfd1a285480b9717`  
		Last Modified: Fri, 08 May 2026 20:36:36 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb64ce9e7c9c0e20d3c938b58adac70efb8c18c0f16924e4239e7ed9e9a78ca`  
		Last Modified: Fri, 08 May 2026 20:36:37 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:355c8890f84743039e8f984faa378f99f837127c8cd6728c68ed01077b73025a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3615ae43b3e91b51bf55e19554a4bfcfa36b8a639dd21c9dd58f1def6509b48`

```dockerfile
```

-	Layers:
	-	`sha256:51038de8fb83e459cd04466595bf42c9930f5f8d74b9fb1c86563eb4ff0610c1`  
		Last Modified: Fri, 08 May 2026 20:36:36 GMT  
		Size: 4.7 MB (4677589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5132a7ad8fc5e69b55152f613d964315e042386848699b949424f2be9fc9b6e7`  
		Last Modified: Fri, 08 May 2026 20:36:36 GMT  
		Size: 16.6 KB (16624 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12-alpine`

```console
$ docker pull influxdb@sha256:7d08136634b8da51fbb5a651b4b0127c1527d9f35c0fd1b8761ee9c5ce258889
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.12-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:a3b8600eeb02763008ec656caba8be042a8afeacf4c747cb5fd3a522710d8ce2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46928702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab5a726f0cdc6866a5cf7c5ffccb246a1de116c7f474e8948b6df86552e3d99`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:29:10 GMT
RUN apk add --no-cache bash ca-certificates tzdata &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:29:15 GMT
ENV INFLUXDB_VERSION=1.12.4
# Fri, 17 Apr 2026 00:29:15 GMT
ENV INFLUXDB_PR=
# Fri, 17 Apr 2026 00:29:15 GMT
ENV INFLUXDB_PV=1.12.4
# Fri, 17 Apr 2026 00:29:15 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     case "$(apk --print-arch)" in         x86_64)  ARCH=amd64 ;;         aarch64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz.asc"         "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz" &&     tar -xvf "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz"         -C /usr/bin --strip-components 1 --wildcards             'influxdb-*/influx'             'influxdb-*/influx_inspect'             'influxdb-*/influxd' &&     rm "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz.asc"        "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz" &&     apk del .build-deps # buildkit
# Fri, 17 Apr 2026 00:29:15 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 17 Apr 2026 00:29:15 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Fri, 17 Apr 2026 00:29:15 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 17 Apr 2026 00:29:15 GMT
VOLUME [/var/lib/influxdb]
# Fri, 17 Apr 2026 00:29:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:29:15 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 17 Apr 2026 00:29:15 GMT
USER influxdb
# Fri, 17 Apr 2026 00:29:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:29:15 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5f5636135d43d03ecba2495c5be87f500f43e984887a726c5c982823c7df06`  
		Last Modified: Fri, 17 Apr 2026 00:29:24 GMT  
		Size: 1.2 MB (1224161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa7021fe11ae352a5ff9638340af993261c1412280f47c594bc06b23ad0f5a8e`  
		Last Modified: Fri, 17 Apr 2026 00:29:25 GMT  
		Size: 42.1 MB (42054959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1988b8bbb2be28ed54089649c9630841ae6e10f93ccee10b9c97a696a7e75cb5`  
		Last Modified: Fri, 17 Apr 2026 00:29:24 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06fc58ca41b83f65d0150d3693907ee7dffddef2831c8f4c8ba655c96de54d07`  
		Last Modified: Fri, 17 Apr 2026 00:29:24 GMT  
		Size: 992.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875b13ef487fbbfa7cbd658e9c4db087d9d35bdd978ac347dfda7ea976b61939`  
		Last Modified: Fri, 17 Apr 2026 00:29:25 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13ae692fa73a5ed1e111faaaa566b7290a52c0dc7b6239615571ada027e9f8a`  
		Last Modified: Fri, 17 Apr 2026 00:29:25 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:c18639da4ee3aa318651f04dc1850176a200484f3ea250724f48178354c9c6ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **779.9 KB (779910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d6b567f557b018dd00e41e6d773f38568fb6fb462abfb9ac8dace8e85163faa`

```dockerfile
```

-	Layers:
	-	`sha256:34675433092d7051c2568a2a49060a8bce5f3378b26b1d62d05e04d421062879`  
		Last Modified: Fri, 17 Apr 2026 00:29:24 GMT  
		Size: 761.2 KB (761192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:523fdb60f8ce8cd1d7ea153f5f56308503862bc1673a2051efec78452ef2cfd9`  
		Last Modified: Fri, 17 Apr 2026 00:29:23 GMT  
		Size: 18.7 KB (18718 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.12-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:24d700526b0ddf4784407f81c8dad61cd96bf707fe24360f12c9d669effcb2b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (43966338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da4c763f3e1f947a6ab02b45b6d56257a131850f32d8d004749a52161f09342c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:13 GMT
ADD alpine-minirootfs-3.21.7-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:13 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:30:04 GMT
RUN apk add --no-cache bash ca-certificates tzdata &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:30:09 GMT
ENV INFLUXDB_VERSION=1.12.4
# Fri, 17 Apr 2026 00:30:09 GMT
ENV INFLUXDB_PR=
# Fri, 17 Apr 2026 00:30:09 GMT
ENV INFLUXDB_PV=1.12.4
# Fri, 17 Apr 2026 00:30:09 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     case "$(apk --print-arch)" in         x86_64)  ARCH=amd64 ;;         aarch64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz.asc"         "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz" &&     tar -xvf "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz"         -C /usr/bin --strip-components 1 --wildcards             'influxdb-*/influx'             'influxdb-*/influx_inspect'             'influxdb-*/influxd' &&     rm "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz.asc"        "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz" &&     apk del .build-deps # buildkit
# Fri, 17 Apr 2026 00:30:09 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 17 Apr 2026 00:30:09 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Fri, 17 Apr 2026 00:30:09 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 17 Apr 2026 00:30:09 GMT
VOLUME [/var/lib/influxdb]
# Fri, 17 Apr 2026 00:30:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:30:09 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 17 Apr 2026 00:30:09 GMT
USER influxdb
# Fri, 17 Apr 2026 00:30:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:30:09 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:2dd7199cff98a7400e801cbfad6de906972a4e3dd0a749d4c1b80f5a1e3e4108`  
		Last Modified: Thu, 16 Apr 2026 05:32:50 GMT  
		Size: 4.0 MB (3994465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6485fbe4c86c7beea4454c9beac448c9bc2d15418646bd15f5804deb9250e2de`  
		Last Modified: Fri, 17 Apr 2026 00:30:19 GMT  
		Size: 1.3 MB (1288257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57f0cc6d9f8a6c327d9726a8a6af67bb058645e70743b6892991a1adb98c294`  
		Last Modified: Fri, 17 Apr 2026 00:30:19 GMT  
		Size: 38.7 MB (38680908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30dec3520d50f59e9d1064c02eeb05af6b5960b514355331ed6425ddd686ded5`  
		Last Modified: Fri, 17 Apr 2026 00:30:18 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7e5247083153c5218c789e42f35fea3782be687f56d7636c3fb3aaedea298ea`  
		Last Modified: Fri, 17 Apr 2026 00:30:18 GMT  
		Size: 991.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3582776f3ccf5bb7a6a37d053ac30411dfce856b6f3ff6599626e7a3bf1441`  
		Last Modified: Fri, 17 Apr 2026 00:30:19 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c75eb759c4ceeed5e525aacc2876e85dc22d0bfa9326a91ab91215c6df153a`  
		Last Modified: Fri, 17 Apr 2026 00:30:20 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:55f4dff83f5c7f0fd1e714ae092d77cd3fa55e5a3d2557d7d76363a3901eba53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **779.2 KB (779247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9c649fcdce8d00652e0e92aefb077cb6ddf48ac55255f3c891d9292d2d00cfc`

```dockerfile
```

-	Layers:
	-	`sha256:6ea75a35ef586313f9ae9c658a2b0170872bd5de591e4d51e1641d2c1458b258`  
		Last Modified: Fri, 17 Apr 2026 00:30:18 GMT  
		Size: 760.4 KB (760419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8702f37fef178cf8529101088eb230fa6f264a1a72f46b605176fdbb591453e5`  
		Last Modified: Fri, 17 Apr 2026 00:30:18 GMT  
		Size: 18.8 KB (18828 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12-data`

```console
$ docker pull influxdb@sha256:e6398d43e07f280786f433bf80f8639b750bfb50e5c747ffc4ddc9e2a60c5b7c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12-data` - linux; amd64

```console
$ docker pull influxdb@sha256:0f1cd7dc2417b33893cf37d0c221c1d141fea39c7e6f3d75987d2ce2f39c7379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115722571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90e946c6558e16f25290a65d9cacce4a62fb96fa1e024c32df5af02a52dce8e0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:30:41 GMT
ENV INFLUXDB_VERSION=1.12.4-c1.12.4
# Fri, 08 May 2026 20:30:41 GMT
ENV INFLUXDB_PR=
# Fri, 08 May 2026 20:30:41 GMT
ENV INFLUXDB_PV=1.12.4-c1.12.4
# Fri, 08 May 2026 20:30:41 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"          -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"         "influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     rm -r "influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"           "influxdb-data_${INFLUXDB_PV}_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:30:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 08 May 2026 20:30:41 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 08 May 2026 20:30:41 GMT
VOLUME [/var/lib/influxdb]
# Fri, 08 May 2026 20:30:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 20:30:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 08 May 2026 20:30:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 20:30:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d055cea50c88c57fc27fcd44845ebabfe5b830ea8a0a621b89d38a2b650b7ff3`  
		Last Modified: Fri, 08 May 2026 19:40:29 GMT  
		Size: 24.0 MB (24042180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:962acf40db3a7d5df88755121d66b97b074e6fa7af51182c3582c3fbb65fdfb2`  
		Last Modified: Fri, 08 May 2026 20:30:56 GMT  
		Size: 43.2 MB (43189938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fcb508adabb85feb56df9db23493b1b85833909a099c96a55ee681b41293c99`  
		Last Modified: Fri, 08 May 2026 20:30:55 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f6c1227d43a6d82ff41b8ef79cb08bab47864e59f8c6884a2a263d146821d3`  
		Last Modified: Fri, 08 May 2026 20:30:55 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db63a3ea8649aa33914a2860a788be1b9e77252249952311c7ba20c888f8b43`  
		Last Modified: Fri, 08 May 2026 20:30:55 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:3a80b17123ca1905ae253c10601c1a1906b0f118b45e3254adebf76cc7782238
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4707277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a478a44f1e471ed0a0b7184d1ededb0817c5a7f997b34f0fa4b76f3cf8b5003e`

```dockerfile
```

-	Layers:
	-	`sha256:43aec9720ab4169c00241c51f14a8db53355c107f19b19a1e1fc4897ce1db8b8`  
		Last Modified: Fri, 08 May 2026 20:30:55 GMT  
		Size: 4.7 MB (4693123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c013f1c88633b1a08bb7a4ffa1463dd4ac279bf38bfb418977e5426907519d6`  
		Last Modified: Fri, 08 May 2026 20:30:55 GMT  
		Size: 14.2 KB (14154 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12-data-alpine`

```console
$ docker pull influxdb@sha256:97455dc1763d0603ac9b2c08bb015eeafa3a4293efdb6da2dcac20989499411b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:9e565c7fd49e5d8f35ed01c97673730f73fe99480f2bcc42df2ebaeb6670e25f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47997256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63094d0e7597666e3a6319a4c087f71fe682814c16de22d762b1de6dd9c5cca7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:29:12 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:29:15 GMT
ENV INFLUXDB_VERSION=1.12.4-c1.12.4
# Fri, 17 Apr 2026 00:29:15 GMT
ENV INFLUXDB_PR=
# Fri, 17 Apr 2026 00:29:15 GMT
ENV INFLUXDB_PV=1.12.4-c1.12.4
# Fri, 17 Apr 2026 00:29:15 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"         "influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     tar -xvf "influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz"         -C /usr/bin --strip-components 1 --wildcards             'influxdb-*/influx'             'influxdb-*/influx_inspect'             'influxdb-*/influxd' &&     rm "influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"        "influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     apk del .build-deps # buildkit
# Fri, 17 Apr 2026 00:29:15 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 17 Apr 2026 00:29:15 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 17 Apr 2026 00:29:15 GMT
VOLUME [/var/lib/influxdb]
# Fri, 17 Apr 2026 00:29:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:29:15 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 17 Apr 2026 00:29:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:29:15 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc9611369db3ecb1526937d9f72c04921aa31dc4ba3d99a4e3b9c15767aa38c`  
		Last Modified: Fri, 17 Apr 2026 00:29:25 GMT  
		Size: 1.2 MB (1224170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88fc8e5058960e45aee8b6cac82ff2bd50d7e2137e6cf885c0b4d623ae175b8`  
		Last Modified: Fri, 17 Apr 2026 00:29:26 GMT  
		Size: 43.1 MB (43124440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada70a5a02afde6bb6c3f103fa9ec3a499488396461d706bd57a9bac54ad1dbf`  
		Last Modified: Fri, 17 Apr 2026 00:29:25 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d47be05a8626fbeb060a3ac42397eec5b9faff395d564ed99c70f443120850`  
		Last Modified: Fri, 17 Apr 2026 00:29:25 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2249338bf3d212a5f9560aae8dae54182f0232814622fe938e2ea878e279faab`  
		Last Modified: Fri, 17 Apr 2026 00:29:26 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:78a86aa0d4d8e27d8e0afc24b8bac506e70b8877e920a0b0d532fad2c24f6d91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **796.1 KB (796066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eaafdeb7f35414723ace5c8693058a60536ee236f09cb0b7ee8cd56812f99a5`

```dockerfile
```

-	Layers:
	-	`sha256:2c95497e066bdcad88af076d5632e15c891f1c90d79ccc0cfc2ab77eac05e7bb`  
		Last Modified: Fri, 17 Apr 2026 00:29:25 GMT  
		Size: 780.5 KB (780536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:329b5b66f2e9143f7d74aaad874558e3fea3758d13aaf5008df91e8d3021223c`  
		Last Modified: Fri, 17 Apr 2026 00:29:25 GMT  
		Size: 15.5 KB (15530 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12-meta`

```console
$ docker pull influxdb@sha256:fa416351c64988902901b3c3e3e95b78760e4b64d8537a6953bb506642e80ba4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:b1ef1ea5f5c5fb9423f07a34691b7341a98b8edfecb170cc13c5c72c8feb2fcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91916620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3045502ba23a95adfb8f7d6a59cf783fd370ea250146a00d8985f015bbf88464`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:30:52 GMT
ENV INFLUXDB_VERSION=1.12.4-c1.12.4
# Fri, 08 May 2026 20:30:52 GMT
ENV INFLUXDB_PR=
# Fri, 08 May 2026 20:30:52 GMT
ENV INFLUXDB_PV=1.12.4-c1.12.4
# Fri, 08 May 2026 20:30:52 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"          -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"         "influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     rm -r "influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"           "influxdb-meta_${INFLUXDB_PV}_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:30:52 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Fri, 08 May 2026 20:30:52 GMT
EXPOSE map[8091/tcp:{}]
# Fri, 08 May 2026 20:30:52 GMT
VOLUME [/var/lib/influxdb]
# Fri, 08 May 2026 20:30:52 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 20:30:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 20:30:52 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d055cea50c88c57fc27fcd44845ebabfe5b830ea8a0a621b89d38a2b650b7ff3`  
		Last Modified: Fri, 08 May 2026 19:40:29 GMT  
		Size: 24.0 MB (24042180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b058c7f6dfb8da15a4a0b773a7c4c7059f9b5e4f6b82db7424793cf8cea072aa`  
		Last Modified: Fri, 08 May 2026 20:31:02 GMT  
		Size: 19.4 MB (19385193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5794176de2edc35b4dc3032ace26da68f9eec0ff629b42b1c68d97af7d7c4a`  
		Last Modified: Fri, 08 May 2026 20:31:01 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7d46c4bdbd2d99069aecc0673097fdc4f2d690f90831ab9767ae1f0a7c080b`  
		Last Modified: Fri, 08 May 2026 20:31:01 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:e8c2b5bac24fa5471bf3dfe6af346c57367722bc2084aa1f1848d16d0acd596c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4605854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e02b4f902aa1d98d78b949b707dc7e11e98ca677360c6102f0c52507bb6e677`

```dockerfile
```

-	Layers:
	-	`sha256:7e6306732f4bf984511ea6ba4d8028686ba7a12977d0460e9515b17e763f1a97`  
		Last Modified: Fri, 08 May 2026 20:31:01 GMT  
		Size: 4.6 MB (4593191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0782c7a7748da881c618af0865368527f37ef032d843b1aa0d258633ba71c89`  
		Last Modified: Fri, 08 May 2026 20:31:01 GMT  
		Size: 12.7 KB (12663 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12-meta-alpine`

```console
$ docker pull influxdb@sha256:c1609e4b1a9966a278cbc63e39637d62a3798895d5f9dffb16f56642c345a470
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:0c2d58c85a4eeef69b1067b8385427653ccd49a3c18b2fa5c406ecc061a3eff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.2 MB (24201677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c996d394ebe8422efb6cd5313a8b6d659f4361c8783ba7e2765a3495d82bf9a9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:29:31 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:29:34 GMT
ENV INFLUXDB_VERSION=1.12.4-c1.12.4
# Fri, 17 Apr 2026 00:29:34 GMT
ENV INFLUXDB_PR=
# Fri, 17 Apr 2026 00:29:34 GMT
ENV INFLUXDB_PV=1.12.4-c1.12.4
# Fri, 17 Apr 2026 00:29:34 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"         "influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     tar -xvf "influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz"         -C /usr/bin --strip-components 1 --wildcards             'influxdb-*/influxd-ctl'             'influxdb-*/influxd-meta' &&     rm "influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"        "influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     apk del .build-deps # buildkit
# Fri, 17 Apr 2026 00:29:34 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Fri, 17 Apr 2026 00:29:34 GMT
EXPOSE map[8091/tcp:{}]
# Fri, 17 Apr 2026 00:29:34 GMT
VOLUME [/var/lib/influxdb]
# Fri, 17 Apr 2026 00:29:34 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:29:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:29:34 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fce14c04b1498e08f014d63ade6e29799ca92f77d6d5aee2e26f723fa47632`  
		Last Modified: Fri, 17 Apr 2026 00:29:41 GMT  
		Size: 1.2 MB (1224167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e592b60a790f783fefc22026e6f186aec24b3fb81e56fe43bc3ad4dfbccf3b`  
		Last Modified: Fri, 17 Apr 2026 00:29:42 GMT  
		Size: 19.3 MB (19330070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1f2ec0dd69b272c781c7c30754b98f78b843600b12cddc731b02a3b58f888a1`  
		Last Modified: Fri, 17 Apr 2026 00:29:41 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc5145a28bfcd9c82912556bd7085dee977090f80a54a3c6ee097e29382fcbf`  
		Last Modified: Fri, 17 Apr 2026 00:29:41 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:667228df4c2fe4090dfa788f0b272b45189b51414433b171b53980323a0ef648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **695.3 KB (695321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b92baa71c20ea018ab004a2abf41df19c1368d9bff15dcda5fa2415c18b67e4`

```dockerfile
```

-	Layers:
	-	`sha256:0b0a0c460b5f111deb27700ed49900ddbe4a0e118ad09843c430e91a8668f979`  
		Last Modified: Fri, 17 Apr 2026 00:29:41 GMT  
		Size: 681.4 KB (681390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7168d592346505ecf69732a4af5308278302c2ca1cc6966560e75037b25b940c`  
		Last Modified: Fri, 17 Apr 2026 00:29:41 GMT  
		Size: 13.9 KB (13931 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12.4`

```console
$ docker pull influxdb@sha256:e9363fd88d67f8ae6f019f37a30cc136e3644f2cbaea5abd71ad63c96dc6ae08
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.12.4` - linux; amd64

```console
$ docker pull influxdb@sha256:70fb0d2c004f475439e044abee282bcdca40dd5bf07c7da48d5eeeb757f9f7a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114660034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df1f9a737bfa342065b155fb4c75b90f5befe474c912b2046a7a6b7c615351f9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:30:41 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Fri, 08 May 2026 20:30:47 GMT
ENV INFLUXDB_VERSION=1.12.4
# Fri, 08 May 2026 20:30:47 GMT
ENV INFLUXDB_PR=-1
# Fri, 08 May 2026 20:30:47 GMT
ENV INFLUXDB_PV=1.12.4-1
# Fri, 08 May 2026 20:30:47 GMT
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_PV}_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:30:47 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 08 May 2026 20:30:47 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 08 May 2026 20:30:47 GMT
VOLUME [/var/lib/influxdb]
# Fri, 08 May 2026 20:30:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 20:30:47 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 08 May 2026 20:30:47 GMT
USER influxdb
# Fri, 08 May 2026 20:30:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 20:30:47 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d055cea50c88c57fc27fcd44845ebabfe5b830ea8a0a621b89d38a2b650b7ff3`  
		Last Modified: Fri, 08 May 2026 19:40:29 GMT  
		Size: 24.0 MB (24042180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9aef9dd3ee15ba56d1914e858a632db3a0757d6ff96d35dc9b99cbf8993f478`  
		Last Modified: Fri, 08 May 2026 20:31:00 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da6117c0a9c02803c1efba4749beb78cd3bda41777c5cc0b85d03cad31d5dab`  
		Last Modified: Fri, 08 May 2026 20:31:01 GMT  
		Size: 42.1 MB (42126263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe387fe968ddd644052b75d259bd582b2657ec49465d2bb692f19594e50c3cb`  
		Last Modified: Fri, 08 May 2026 20:31:00 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffd3eaffded54f5f83c427977d48d7f5695e2ade4839b4cd12cbd9dd76bf8a9`  
		Last Modified: Fri, 08 May 2026 20:31:00 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee0b030e056e99d9b6567b858be0294a0581eecdfb22859e4002fcedf2efc61`  
		Last Modified: Fri, 08 May 2026 20:31:01 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.4` - unknown; unknown

```console
$ docker pull influxdb@sha256:7ccfb4c3ae7ebf72835eff1dedafdbfb7dc0d209d109c33d87413dc263711802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add224f63b95fe755d2e01b0ab6173162af166aefd7b793206f972fe99b2cb0a`

```dockerfile
```

-	Layers:
	-	`sha256:05e0b1fbf88be7d164e95925c79caf7d55a0149f074aace0a8e0baf95e13c82e`  
		Last Modified: Fri, 08 May 2026 20:31:00 GMT  
		Size: 4.7 MB (4678133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ad32ce71f4e40c81a6717f78e88f22e0cfa5cc834d6a32aaf1a021987d851fa`  
		Last Modified: Fri, 08 May 2026 20:31:00 GMT  
		Size: 16.5 KB (16529 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.12.4` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:d78d2de9e52ce053bd436726acf103389fa9a946d9a586d448c0aeb388486654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110739824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a950ec6a38ecb85c83329bad98813d8c7d6e0f456fd70d16fe949a619d63c77b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:42:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:36:19 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Fri, 08 May 2026 20:36:24 GMT
ENV INFLUXDB_VERSION=1.12.4
# Fri, 08 May 2026 20:36:24 GMT
ENV INFLUXDB_PR=-1
# Fri, 08 May 2026 20:36:24 GMT
ENV INFLUXDB_PV=1.12.4-1
# Fri, 08 May 2026 20:36:24 GMT
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_PV}_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:36:24 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 08 May 2026 20:36:24 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 08 May 2026 20:36:24 GMT
VOLUME [/var/lib/influxdb]
# Fri, 08 May 2026 20:36:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 20:36:24 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 08 May 2026 20:36:24 GMT
USER influxdb
# Fri, 08 May 2026 20:36:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 20:36:24 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f56578c9577bd69a05b2319baacd770a986ae61a8568047ddd91db1a1893b4`  
		Last Modified: Fri, 08 May 2026 19:42:30 GMT  
		Size: 23.6 MB (23609357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f10c9d0130b02a8e2ea0a143fd27ce60fe500311296bbcd0d15d8e32f35556`  
		Last Modified: Fri, 08 May 2026 20:36:36 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aeba6a20528127046d8b3ac86a7cbefcf861b5fe33ae1cdae95620cddfbaf1f`  
		Last Modified: Fri, 08 May 2026 20:36:38 GMT  
		Size: 38.8 MB (38754404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4a6ddab59dba6cab64122213b1869b06b4ab7c2fda5e06a91c9ae0dbe93837`  
		Last Modified: Fri, 08 May 2026 20:36:36 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582e132768c9ee3ea54b802cc9d8d194551eabe13fb6e99bdfd1a285480b9717`  
		Last Modified: Fri, 08 May 2026 20:36:36 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb64ce9e7c9c0e20d3c938b58adac70efb8c18c0f16924e4239e7ed9e9a78ca`  
		Last Modified: Fri, 08 May 2026 20:36:37 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.4` - unknown; unknown

```console
$ docker pull influxdb@sha256:355c8890f84743039e8f984faa378f99f837127c8cd6728c68ed01077b73025a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3615ae43b3e91b51bf55e19554a4bfcfa36b8a639dd21c9dd58f1def6509b48`

```dockerfile
```

-	Layers:
	-	`sha256:51038de8fb83e459cd04466595bf42c9930f5f8d74b9fb1c86563eb4ff0610c1`  
		Last Modified: Fri, 08 May 2026 20:36:36 GMT  
		Size: 4.7 MB (4677589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5132a7ad8fc5e69b55152f613d964315e042386848699b949424f2be9fc9b6e7`  
		Last Modified: Fri, 08 May 2026 20:36:36 GMT  
		Size: 16.6 KB (16624 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12.4-alpine`

```console
$ docker pull influxdb@sha256:7d08136634b8da51fbb5a651b4b0127c1527d9f35c0fd1b8761ee9c5ce258889
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.12.4-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:a3b8600eeb02763008ec656caba8be042a8afeacf4c747cb5fd3a522710d8ce2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46928702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab5a726f0cdc6866a5cf7c5ffccb246a1de116c7f474e8948b6df86552e3d99`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:29:10 GMT
RUN apk add --no-cache bash ca-certificates tzdata &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:29:15 GMT
ENV INFLUXDB_VERSION=1.12.4
# Fri, 17 Apr 2026 00:29:15 GMT
ENV INFLUXDB_PR=
# Fri, 17 Apr 2026 00:29:15 GMT
ENV INFLUXDB_PV=1.12.4
# Fri, 17 Apr 2026 00:29:15 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     case "$(apk --print-arch)" in         x86_64)  ARCH=amd64 ;;         aarch64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz.asc"         "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz" &&     tar -xvf "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz"         -C /usr/bin --strip-components 1 --wildcards             'influxdb-*/influx'             'influxdb-*/influx_inspect'             'influxdb-*/influxd' &&     rm "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz.asc"        "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz" &&     apk del .build-deps # buildkit
# Fri, 17 Apr 2026 00:29:15 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 17 Apr 2026 00:29:15 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Fri, 17 Apr 2026 00:29:15 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 17 Apr 2026 00:29:15 GMT
VOLUME [/var/lib/influxdb]
# Fri, 17 Apr 2026 00:29:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:29:15 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 17 Apr 2026 00:29:15 GMT
USER influxdb
# Fri, 17 Apr 2026 00:29:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:29:15 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5f5636135d43d03ecba2495c5be87f500f43e984887a726c5c982823c7df06`  
		Last Modified: Fri, 17 Apr 2026 00:29:24 GMT  
		Size: 1.2 MB (1224161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa7021fe11ae352a5ff9638340af993261c1412280f47c594bc06b23ad0f5a8e`  
		Last Modified: Fri, 17 Apr 2026 00:29:25 GMT  
		Size: 42.1 MB (42054959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1988b8bbb2be28ed54089649c9630841ae6e10f93ccee10b9c97a696a7e75cb5`  
		Last Modified: Fri, 17 Apr 2026 00:29:24 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06fc58ca41b83f65d0150d3693907ee7dffddef2831c8f4c8ba655c96de54d07`  
		Last Modified: Fri, 17 Apr 2026 00:29:24 GMT  
		Size: 992.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875b13ef487fbbfa7cbd658e9c4db087d9d35bdd978ac347dfda7ea976b61939`  
		Last Modified: Fri, 17 Apr 2026 00:29:25 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13ae692fa73a5ed1e111faaaa566b7290a52c0dc7b6239615571ada027e9f8a`  
		Last Modified: Fri, 17 Apr 2026 00:29:25 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.4-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:c18639da4ee3aa318651f04dc1850176a200484f3ea250724f48178354c9c6ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **779.9 KB (779910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d6b567f557b018dd00e41e6d773f38568fb6fb462abfb9ac8dace8e85163faa`

```dockerfile
```

-	Layers:
	-	`sha256:34675433092d7051c2568a2a49060a8bce5f3378b26b1d62d05e04d421062879`  
		Last Modified: Fri, 17 Apr 2026 00:29:24 GMT  
		Size: 761.2 KB (761192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:523fdb60f8ce8cd1d7ea153f5f56308503862bc1673a2051efec78452ef2cfd9`  
		Last Modified: Fri, 17 Apr 2026 00:29:23 GMT  
		Size: 18.7 KB (18718 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.12.4-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:24d700526b0ddf4784407f81c8dad61cd96bf707fe24360f12c9d669effcb2b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (43966338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da4c763f3e1f947a6ab02b45b6d56257a131850f32d8d004749a52161f09342c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:13 GMT
ADD alpine-minirootfs-3.21.7-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:13 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:30:04 GMT
RUN apk add --no-cache bash ca-certificates tzdata &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:30:09 GMT
ENV INFLUXDB_VERSION=1.12.4
# Fri, 17 Apr 2026 00:30:09 GMT
ENV INFLUXDB_PR=
# Fri, 17 Apr 2026 00:30:09 GMT
ENV INFLUXDB_PV=1.12.4
# Fri, 17 Apr 2026 00:30:09 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     case "$(apk --print-arch)" in         x86_64)  ARCH=amd64 ;;         aarch64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz.asc"         "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz" &&     tar -xvf "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz"         -C /usr/bin --strip-components 1 --wildcards             'influxdb-*/influx'             'influxdb-*/influx_inspect'             'influxdb-*/influxd' &&     rm "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz.asc"        "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz" &&     apk del .build-deps # buildkit
# Fri, 17 Apr 2026 00:30:09 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 17 Apr 2026 00:30:09 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Fri, 17 Apr 2026 00:30:09 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 17 Apr 2026 00:30:09 GMT
VOLUME [/var/lib/influxdb]
# Fri, 17 Apr 2026 00:30:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:30:09 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 17 Apr 2026 00:30:09 GMT
USER influxdb
# Fri, 17 Apr 2026 00:30:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:30:09 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:2dd7199cff98a7400e801cbfad6de906972a4e3dd0a749d4c1b80f5a1e3e4108`  
		Last Modified: Thu, 16 Apr 2026 05:32:50 GMT  
		Size: 4.0 MB (3994465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6485fbe4c86c7beea4454c9beac448c9bc2d15418646bd15f5804deb9250e2de`  
		Last Modified: Fri, 17 Apr 2026 00:30:19 GMT  
		Size: 1.3 MB (1288257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57f0cc6d9f8a6c327d9726a8a6af67bb058645e70743b6892991a1adb98c294`  
		Last Modified: Fri, 17 Apr 2026 00:30:19 GMT  
		Size: 38.7 MB (38680908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30dec3520d50f59e9d1064c02eeb05af6b5960b514355331ed6425ddd686ded5`  
		Last Modified: Fri, 17 Apr 2026 00:30:18 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7e5247083153c5218c789e42f35fea3782be687f56d7636c3fb3aaedea298ea`  
		Last Modified: Fri, 17 Apr 2026 00:30:18 GMT  
		Size: 991.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3582776f3ccf5bb7a6a37d053ac30411dfce856b6f3ff6599626e7a3bf1441`  
		Last Modified: Fri, 17 Apr 2026 00:30:19 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c75eb759c4ceeed5e525aacc2876e85dc22d0bfa9326a91ab91215c6df153a`  
		Last Modified: Fri, 17 Apr 2026 00:30:20 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.4-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:55f4dff83f5c7f0fd1e714ae092d77cd3fa55e5a3d2557d7d76363a3901eba53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **779.2 KB (779247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9c649fcdce8d00652e0e92aefb077cb6ddf48ac55255f3c891d9292d2d00cfc`

```dockerfile
```

-	Layers:
	-	`sha256:6ea75a35ef586313f9ae9c658a2b0170872bd5de591e4d51e1641d2c1458b258`  
		Last Modified: Fri, 17 Apr 2026 00:30:18 GMT  
		Size: 760.4 KB (760419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8702f37fef178cf8529101088eb230fa6f264a1a72f46b605176fdbb591453e5`  
		Last Modified: Fri, 17 Apr 2026 00:30:18 GMT  
		Size: 18.8 KB (18828 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12.4-data`

```console
$ docker pull influxdb@sha256:e6398d43e07f280786f433bf80f8639b750bfb50e5c747ffc4ddc9e2a60c5b7c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12.4-data` - linux; amd64

```console
$ docker pull influxdb@sha256:0f1cd7dc2417b33893cf37d0c221c1d141fea39c7e6f3d75987d2ce2f39c7379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115722571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90e946c6558e16f25290a65d9cacce4a62fb96fa1e024c32df5af02a52dce8e0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:30:41 GMT
ENV INFLUXDB_VERSION=1.12.4-c1.12.4
# Fri, 08 May 2026 20:30:41 GMT
ENV INFLUXDB_PR=
# Fri, 08 May 2026 20:30:41 GMT
ENV INFLUXDB_PV=1.12.4-c1.12.4
# Fri, 08 May 2026 20:30:41 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"          -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"         "influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     rm -r "influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"           "influxdb-data_${INFLUXDB_PV}_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:30:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 08 May 2026 20:30:41 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 08 May 2026 20:30:41 GMT
VOLUME [/var/lib/influxdb]
# Fri, 08 May 2026 20:30:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 20:30:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 08 May 2026 20:30:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 20:30:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d055cea50c88c57fc27fcd44845ebabfe5b830ea8a0a621b89d38a2b650b7ff3`  
		Last Modified: Fri, 08 May 2026 19:40:29 GMT  
		Size: 24.0 MB (24042180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:962acf40db3a7d5df88755121d66b97b074e6fa7af51182c3582c3fbb65fdfb2`  
		Last Modified: Fri, 08 May 2026 20:30:56 GMT  
		Size: 43.2 MB (43189938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fcb508adabb85feb56df9db23493b1b85833909a099c96a55ee681b41293c99`  
		Last Modified: Fri, 08 May 2026 20:30:55 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f6c1227d43a6d82ff41b8ef79cb08bab47864e59f8c6884a2a263d146821d3`  
		Last Modified: Fri, 08 May 2026 20:30:55 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db63a3ea8649aa33914a2860a788be1b9e77252249952311c7ba20c888f8b43`  
		Last Modified: Fri, 08 May 2026 20:30:55 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.4-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:3a80b17123ca1905ae253c10601c1a1906b0f118b45e3254adebf76cc7782238
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4707277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a478a44f1e471ed0a0b7184d1ededb0817c5a7f997b34f0fa4b76f3cf8b5003e`

```dockerfile
```

-	Layers:
	-	`sha256:43aec9720ab4169c00241c51f14a8db53355c107f19b19a1e1fc4897ce1db8b8`  
		Last Modified: Fri, 08 May 2026 20:30:55 GMT  
		Size: 4.7 MB (4693123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c013f1c88633b1a08bb7a4ffa1463dd4ac279bf38bfb418977e5426907519d6`  
		Last Modified: Fri, 08 May 2026 20:30:55 GMT  
		Size: 14.2 KB (14154 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12.4-data-alpine`

```console
$ docker pull influxdb@sha256:97455dc1763d0603ac9b2c08bb015eeafa3a4293efdb6da2dcac20989499411b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12.4-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:9e565c7fd49e5d8f35ed01c97673730f73fe99480f2bcc42df2ebaeb6670e25f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47997256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63094d0e7597666e3a6319a4c087f71fe682814c16de22d762b1de6dd9c5cca7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:29:12 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:29:15 GMT
ENV INFLUXDB_VERSION=1.12.4-c1.12.4
# Fri, 17 Apr 2026 00:29:15 GMT
ENV INFLUXDB_PR=
# Fri, 17 Apr 2026 00:29:15 GMT
ENV INFLUXDB_PV=1.12.4-c1.12.4
# Fri, 17 Apr 2026 00:29:15 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"         "influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     tar -xvf "influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz"         -C /usr/bin --strip-components 1 --wildcards             'influxdb-*/influx'             'influxdb-*/influx_inspect'             'influxdb-*/influxd' &&     rm "influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"        "influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     apk del .build-deps # buildkit
# Fri, 17 Apr 2026 00:29:15 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 17 Apr 2026 00:29:15 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 17 Apr 2026 00:29:15 GMT
VOLUME [/var/lib/influxdb]
# Fri, 17 Apr 2026 00:29:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:29:15 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 17 Apr 2026 00:29:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:29:15 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc9611369db3ecb1526937d9f72c04921aa31dc4ba3d99a4e3b9c15767aa38c`  
		Last Modified: Fri, 17 Apr 2026 00:29:25 GMT  
		Size: 1.2 MB (1224170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88fc8e5058960e45aee8b6cac82ff2bd50d7e2137e6cf885c0b4d623ae175b8`  
		Last Modified: Fri, 17 Apr 2026 00:29:26 GMT  
		Size: 43.1 MB (43124440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada70a5a02afde6bb6c3f103fa9ec3a499488396461d706bd57a9bac54ad1dbf`  
		Last Modified: Fri, 17 Apr 2026 00:29:25 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d47be05a8626fbeb060a3ac42397eec5b9faff395d564ed99c70f443120850`  
		Last Modified: Fri, 17 Apr 2026 00:29:25 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2249338bf3d212a5f9560aae8dae54182f0232814622fe938e2ea878e279faab`  
		Last Modified: Fri, 17 Apr 2026 00:29:26 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.4-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:78a86aa0d4d8e27d8e0afc24b8bac506e70b8877e920a0b0d532fad2c24f6d91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **796.1 KB (796066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eaafdeb7f35414723ace5c8693058a60536ee236f09cb0b7ee8cd56812f99a5`

```dockerfile
```

-	Layers:
	-	`sha256:2c95497e066bdcad88af076d5632e15c891f1c90d79ccc0cfc2ab77eac05e7bb`  
		Last Modified: Fri, 17 Apr 2026 00:29:25 GMT  
		Size: 780.5 KB (780536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:329b5b66f2e9143f7d74aaad874558e3fea3758d13aaf5008df91e8d3021223c`  
		Last Modified: Fri, 17 Apr 2026 00:29:25 GMT  
		Size: 15.5 KB (15530 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12.4-meta`

```console
$ docker pull influxdb@sha256:fa416351c64988902901b3c3e3e95b78760e4b64d8537a6953bb506642e80ba4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12.4-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:b1ef1ea5f5c5fb9423f07a34691b7341a98b8edfecb170cc13c5c72c8feb2fcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91916620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3045502ba23a95adfb8f7d6a59cf783fd370ea250146a00d8985f015bbf88464`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:30:52 GMT
ENV INFLUXDB_VERSION=1.12.4-c1.12.4
# Fri, 08 May 2026 20:30:52 GMT
ENV INFLUXDB_PR=
# Fri, 08 May 2026 20:30:52 GMT
ENV INFLUXDB_PV=1.12.4-c1.12.4
# Fri, 08 May 2026 20:30:52 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"          -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"         "influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     rm -r "influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"           "influxdb-meta_${INFLUXDB_PV}_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:30:52 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Fri, 08 May 2026 20:30:52 GMT
EXPOSE map[8091/tcp:{}]
# Fri, 08 May 2026 20:30:52 GMT
VOLUME [/var/lib/influxdb]
# Fri, 08 May 2026 20:30:52 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 20:30:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 20:30:52 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d055cea50c88c57fc27fcd44845ebabfe5b830ea8a0a621b89d38a2b650b7ff3`  
		Last Modified: Fri, 08 May 2026 19:40:29 GMT  
		Size: 24.0 MB (24042180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b058c7f6dfb8da15a4a0b773a7c4c7059f9b5e4f6b82db7424793cf8cea072aa`  
		Last Modified: Fri, 08 May 2026 20:31:02 GMT  
		Size: 19.4 MB (19385193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5794176de2edc35b4dc3032ace26da68f9eec0ff629b42b1c68d97af7d7c4a`  
		Last Modified: Fri, 08 May 2026 20:31:01 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7d46c4bdbd2d99069aecc0673097fdc4f2d690f90831ab9767ae1f0a7c080b`  
		Last Modified: Fri, 08 May 2026 20:31:01 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.4-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:e8c2b5bac24fa5471bf3dfe6af346c57367722bc2084aa1f1848d16d0acd596c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4605854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e02b4f902aa1d98d78b949b707dc7e11e98ca677360c6102f0c52507bb6e677`

```dockerfile
```

-	Layers:
	-	`sha256:7e6306732f4bf984511ea6ba4d8028686ba7a12977d0460e9515b17e763f1a97`  
		Last Modified: Fri, 08 May 2026 20:31:01 GMT  
		Size: 4.6 MB (4593191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0782c7a7748da881c618af0865368527f37ef032d843b1aa0d258633ba71c89`  
		Last Modified: Fri, 08 May 2026 20:31:01 GMT  
		Size: 12.7 KB (12663 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12.4-meta-alpine`

```console
$ docker pull influxdb@sha256:c1609e4b1a9966a278cbc63e39637d62a3798895d5f9dffb16f56642c345a470
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12.4-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:0c2d58c85a4eeef69b1067b8385427653ccd49a3c18b2fa5c406ecc061a3eff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.2 MB (24201677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c996d394ebe8422efb6cd5313a8b6d659f4361c8783ba7e2765a3495d82bf9a9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:29:31 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:29:34 GMT
ENV INFLUXDB_VERSION=1.12.4-c1.12.4
# Fri, 17 Apr 2026 00:29:34 GMT
ENV INFLUXDB_PR=
# Fri, 17 Apr 2026 00:29:34 GMT
ENV INFLUXDB_PV=1.12.4-c1.12.4
# Fri, 17 Apr 2026 00:29:34 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"         "influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     tar -xvf "influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz"         -C /usr/bin --strip-components 1 --wildcards             'influxdb-*/influxd-ctl'             'influxdb-*/influxd-meta' &&     rm "influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"        "influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     apk del .build-deps # buildkit
# Fri, 17 Apr 2026 00:29:34 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Fri, 17 Apr 2026 00:29:34 GMT
EXPOSE map[8091/tcp:{}]
# Fri, 17 Apr 2026 00:29:34 GMT
VOLUME [/var/lib/influxdb]
# Fri, 17 Apr 2026 00:29:34 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:29:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:29:34 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fce14c04b1498e08f014d63ade6e29799ca92f77d6d5aee2e26f723fa47632`  
		Last Modified: Fri, 17 Apr 2026 00:29:41 GMT  
		Size: 1.2 MB (1224167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e592b60a790f783fefc22026e6f186aec24b3fb81e56fe43bc3ad4dfbccf3b`  
		Last Modified: Fri, 17 Apr 2026 00:29:42 GMT  
		Size: 19.3 MB (19330070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1f2ec0dd69b272c781c7c30754b98f78b843600b12cddc731b02a3b58f888a1`  
		Last Modified: Fri, 17 Apr 2026 00:29:41 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc5145a28bfcd9c82912556bd7085dee977090f80a54a3c6ee097e29382fcbf`  
		Last Modified: Fri, 17 Apr 2026 00:29:41 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.4-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:667228df4c2fe4090dfa788f0b272b45189b51414433b171b53980323a0ef648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **695.3 KB (695321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b92baa71c20ea018ab004a2abf41df19c1368d9bff15dcda5fa2415c18b67e4`

```dockerfile
```

-	Layers:
	-	`sha256:0b0a0c460b5f111deb27700ed49900ddbe4a0e118ad09843c430e91a8668f979`  
		Last Modified: Fri, 17 Apr 2026 00:29:41 GMT  
		Size: 681.4 KB (681390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7168d592346505ecf69732a4af5308278302c2ca1cc6966560e75037b25b940c`  
		Last Modified: Fri, 17 Apr 2026 00:29:41 GMT  
		Size: 13.9 KB (13931 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2`

```console
$ docker pull influxdb@sha256:044d60447880093b9837d5de56ea0699b0db79a3e48fb94edf0f9e0eb9f4b95c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2` - linux; amd64

```console
$ docker pull influxdb@sha256:82cd8aa54e7a82a3a006af30e3a31488b73a24f664677ba63782a9343302f1bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.8 MB (110800813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:373cd1bc99e1a9c96598fe115410634b5c8730eb6745f041f9203f1b3291ec8f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Mon, 11 May 2026 23:06:14 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg       util-linux &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:06:14 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Mon, 11 May 2026 23:06:14 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Mon, 11 May 2026 23:06:18 GMT
ENV INFLUXDB_VERSION=2.9.1
# Mon, 11 May 2026 23:06:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 11 May 2026 23:06:18 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Mon, 11 May 2026 23:06:20 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 11 May 2026 23:06:20 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 11 May 2026 23:06:20 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 11 May 2026 23:06:20 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 11 May 2026 23:06:20 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 11 May 2026 23:06:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 May 2026 23:06:20 GMT
CMD ["influxd"]
# Mon, 11 May 2026 23:06:20 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 11 May 2026 23:06:20 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 11 May 2026 23:06:20 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 11 May 2026 23:06:20 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 11 May 2026 23:06:20 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6306d75e2dc4ba2680cb2722b624ffd58658aea8bd7eb42637befbd5f956dc64`  
		Last Modified: Mon, 11 May 2026 23:06:33 GMT  
		Size: 9.8 MB (9799055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a82281c39f9f067b4235800d0e007670159c80542159a4450563d989fcb6563`  
		Last Modified: Mon, 11 May 2026 23:06:33 GMT  
		Size: 3.8 MB (3822784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a116ed37df3620df292451a9d9a04e82e56d60335cf27224a67219ed22cc038`  
		Last Modified: Mon, 11 May 2026 23:06:33 GMT  
		Size: 3.2 KB (3235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af303914f43bdf518bb8cfc5c3c8f4ce2f6e39e7424c012c140aca8689925373`  
		Last Modified: Mon, 11 May 2026 23:06:34 GMT  
		Size: 56.5 MB (56510687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080fd8044aff2f969b124bf1847f066b663e5b2f6cae5eb4a2fe39fd84b9ca8a`  
		Last Modified: Mon, 11 May 2026 23:06:34 GMT  
		Size: 12.4 MB (12421826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c8bdb93dd525adb082fe977c42446a606867cb0876486414590f483bdb16e5`  
		Last Modified: Mon, 11 May 2026 23:06:34 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec61169a51e436a25adf019845e2b06c2a2f667604bdaa2f3ce7d6c242b7e2d3`  
		Last Modified: Mon, 11 May 2026 23:06:35 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c8475bae289926b70499ba7275b48cf710950a5c1745f1047e5cea27687ae7`  
		Last Modified: Mon, 11 May 2026 23:06:35 GMT  
		Size: 6.5 KB (6500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:3b4cdef18045a438e84e562f34e5593ba983944ada9400c448b23087fef4b9a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2988025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c263006991641cd34e84386b46b2189a3f22c0342ad8433ea93de78b3c101a59`

```dockerfile
```

-	Layers:
	-	`sha256:1eaa89e6c29ca38c8ea88162e378052dd323f1b5ccec9fbe77da9e5df39808c7`  
		Last Modified: Mon, 11 May 2026 23:06:33 GMT  
		Size: 3.0 MB (2959411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4126e96a3d9f757323087f196a105f67cb780972bf33fd5a38e7808989145600`  
		Last Modified: Mon, 11 May 2026 23:06:32 GMT  
		Size: 28.6 KB (28614 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:3bce906f5cd366a1d7f1386e355e51c87c6192fcc4d71c68a2edd3297a0192df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106330754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53cf7d95c5904cc95a6940f0d1154b73162e38d225ef133b2450a48ca219c096`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Mon, 11 May 2026 23:06:05 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg       util-linux &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:06:05 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Mon, 11 May 2026 23:06:05 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Mon, 11 May 2026 23:06:09 GMT
ENV INFLUXDB_VERSION=2.9.1
# Mon, 11 May 2026 23:06:09 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 11 May 2026 23:06:09 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Mon, 11 May 2026 23:06:11 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 11 May 2026 23:06:11 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 11 May 2026 23:06:11 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 11 May 2026 23:06:11 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 11 May 2026 23:06:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 11 May 2026 23:06:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 May 2026 23:06:11 GMT
CMD ["influxd"]
# Mon, 11 May 2026 23:06:11 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 11 May 2026 23:06:11 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 11 May 2026 23:06:11 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 11 May 2026 23:06:11 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 11 May 2026 23:06:11 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f23bbe568e43c569b84c86a9c06acb37a65383eef9d7a41c3493f2fc439b23`  
		Last Modified: Mon, 11 May 2026 23:06:23 GMT  
		Size: 9.6 MB (9628121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf21f16acbfdf9cb08e177f4e24e660aef286d9b0246883ca9ccac7f3423ef5`  
		Last Modified: Mon, 11 May 2026 23:06:23 GMT  
		Size: 3.5 MB (3459172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7651cdf91299714e33bee7297dbf293d680c2046377416bbec761092b53fbff`  
		Last Modified: Mon, 11 May 2026 23:06:23 GMT  
		Size: 3.2 KB (3233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93251acc80816de10b80ad59732e2112e724a1d77bc28e4943715d5a298725e`  
		Last Modified: Mon, 11 May 2026 23:06:25 GMT  
		Size: 53.6 MB (53636817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb61f007cdfb2efe51d7353b061d5dc88228555a0565832e7f4798bcf9c4bc05`  
		Last Modified: Mon, 11 May 2026 23:06:25 GMT  
		Size: 11.5 MB (11480302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d795a7febcb13431d839fb4382b6e22f5debf58e787deaeb34da45464289ba10`  
		Last Modified: Mon, 11 May 2026 23:06:25 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e57e263f59e437119c3be99d4d6e7ef67e658750db5b34f3c5307bb8d3d583`  
		Last Modified: Mon, 11 May 2026 23:06:25 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f0fde88bd7e8e0fef0640c7e8be480e6b382f511e2da3d9129a50466da3d55`  
		Last Modified: Mon, 11 May 2026 23:06:26 GMT  
		Size: 6.5 KB (6500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:eb708288bfdc461e6c7c5c7346d5a1d11ba930ebf51cd162c10e023a7e3b89cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed727a90b15a758f20fe1ecb27f8186e0638b8cd670f3eb6052b11f07a9dde9c`

```dockerfile
```

-	Layers:
	-	`sha256:64fc4525aa7a436f50908c48554e8f5bd8b3b56e903570d96d434ea2183135f7`  
		Last Modified: Mon, 11 May 2026 23:06:23 GMT  
		Size: 3.0 MB (2958889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c1611d06ea9793b05207e6377419833d4f183dd192845527a8be765b2d3d5e9`  
		Last Modified: Mon, 11 May 2026 23:06:23 GMT  
		Size: 28.8 KB (28793 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2-alpine`

```console
$ docker pull influxdb@sha256:1cb8fa92ff9d13518d8198dae872b7ea523757a03c655d12a67175b1ab7a72f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:99e216544ab6f8f8d4180d06bcc8deb61a676971c63e31faae24fc169945c4d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86902190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:343b7e7e34cb3b0c8e6c7a44f74f147f01f7ab4022ad1aa3c99ee43701d261f0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 11 May 2026 23:06:21 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 11 May 2026 23:06:23 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       setpriv       tzdata &&     update-ca-certificates # buildkit
# Mon, 11 May 2026 23:06:23 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Mon, 11 May 2026 23:06:23 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Mon, 11 May 2026 23:06:26 GMT
ENV INFLUXDB_VERSION=2.9.1
# Mon, 11 May 2026 23:06:26 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 11 May 2026 23:06:26 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Mon, 11 May 2026 23:06:27 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 11 May 2026 23:06:27 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 11 May 2026 23:06:27 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 11 May 2026 23:06:27 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 11 May 2026 23:06:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 11 May 2026 23:06:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 May 2026 23:06:27 GMT
CMD ["influxd"]
# Mon, 11 May 2026 23:06:27 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 11 May 2026 23:06:27 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 11 May 2026 23:06:27 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 11 May 2026 23:06:27 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 11 May 2026 23:06:27 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298fb8d3d07e69a02cd49af0883ae79a93c4625bc43501293daf0d954698afb5`  
		Last Modified: Mon, 11 May 2026 23:06:38 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896207ace1714281476706f02a38f5bafa2e8b0d466910e59c4abe1f0ef217a3`  
		Last Modified: Mon, 11 May 2026 23:06:38 GMT  
		Size: 10.3 MB (10274619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2fcd4f5629f0c11692de5d63652eda9a1de734dedd342a70ef1a8c1915d6e3`  
		Last Modified: Mon, 11 May 2026 23:06:38 GMT  
		Size: 3.8 MB (3822787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7399422b7a7b047fd9f9ae6a7b1b3c379169c0320d8c89787c7e57e378c95d46`  
		Last Modified: Mon, 11 May 2026 23:06:38 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a421d960302e6e78e3497cecdfbf7e68f9f87afb9c264f7efd238f037129c2`  
		Last Modified: Mon, 11 May 2026 23:06:41 GMT  
		Size: 56.5 MB (56510610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af09c2df41ffda41b4df2fd992fb0be316e613c2f08ecac1733e26e530fd6fb`  
		Last Modified: Mon, 11 May 2026 23:06:40 GMT  
		Size: 12.4 MB (12421822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141bbaa5308a2f1112e696cb9e82bc575508bf3fdba5b192f4c5017ed1ff0345`  
		Last Modified: Mon, 11 May 2026 23:06:40 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8db14735975847fbcb27a366734a994b19e81b52f37258eb95514dd7f2e7403`  
		Last Modified: Mon, 11 May 2026 23:06:41 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e66dbce9517e43a94af04ed7171b8a8c4174f59aeedd523604e88ced95a82de`  
		Last Modified: Mon, 11 May 2026 23:06:41 GMT  
		Size: 6.5 KB (6493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:45ebd475ac2880a68c21896d4cb1186238df70770b3318fdfcc83ac0f437a337
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **982.6 KB (982563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d587a6c839e8fdba54a6798485c7788dea62d5dc23bb982ddb676468b555f2e2`

```dockerfile
```

-	Layers:
	-	`sha256:00fb4b7e94546950e1d396936b5d2b235f6b34d79341a38bea451349ae4e71ad`  
		Last Modified: Mon, 11 May 2026 23:06:38 GMT  
		Size: 952.0 KB (951954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87c7670b411083afd6e9eee2031e773c5f9c80d7684afade5ae50a6602f99766`  
		Last Modified: Mon, 11 May 2026 23:06:38 GMT  
		Size: 30.6 KB (30609 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:02a1ea25d55126eb4d17a75d949f6939f995ee716a38d5cf87dacbfcbc43b5f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.0 MB (83028837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc4487542a8db6296883e5107322a4eeb7ac2f72cf6251e1b284eb9f8ba30ad0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 11 May 2026 23:06:28 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 11 May 2026 23:06:29 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       setpriv       tzdata &&     update-ca-certificates # buildkit
# Mon, 11 May 2026 23:06:30 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Mon, 11 May 2026 23:06:30 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Mon, 11 May 2026 23:06:32 GMT
ENV INFLUXDB_VERSION=2.9.1
# Mon, 11 May 2026 23:06:32 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 11 May 2026 23:06:32 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Mon, 11 May 2026 23:06:33 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 11 May 2026 23:06:33 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 11 May 2026 23:06:33 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 11 May 2026 23:06:33 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 11 May 2026 23:06:33 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 11 May 2026 23:06:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 May 2026 23:06:33 GMT
CMD ["influxd"]
# Mon, 11 May 2026 23:06:33 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 11 May 2026 23:06:33 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 11 May 2026 23:06:33 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 11 May 2026 23:06:33 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 11 May 2026 23:06:33 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4647b3db14cecf9d1d3425f0c3d71e29d76706a4ba687c996add84a9e46d7ac`  
		Last Modified: Mon, 11 May 2026 23:06:44 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fff389d9cde97293c698f3913f18598979f35d0502a8e50385bda21328b81c4`  
		Last Modified: Mon, 11 May 2026 23:06:44 GMT  
		Size: 10.2 MB (10244532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b6866a06fadef09561556d16e7b2b3e0279d4ca952ac2e3675803c00008dbc`  
		Last Modified: Mon, 11 May 2026 23:06:44 GMT  
		Size: 3.5 MB (3459165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9f34a583141b546c821a5ff21181240e09fa803803fe707d8da1b354084a33`  
		Last Modified: Mon, 11 May 2026 23:06:44 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a88da843f8eafbaedc72d393269a63b69eba46cd5780a319eee812b3428b8cc`  
		Last Modified: Mon, 11 May 2026 23:06:47 GMT  
		Size: 53.6 MB (53636820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd2e861c1ced42fa6d0ba182a983a7cf3b6d02f861f36efcfbe429b15544c4b`  
		Last Modified: Mon, 11 May 2026 23:06:46 GMT  
		Size: 11.5 MB (11480281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a31d56e532ff265b275aae709861e82df693b3c0e28e467fbd828aee0eb0d88`  
		Last Modified: Mon, 11 May 2026 23:06:46 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54b8df16388dbc099806c1c1818c3a2bde146ee08ff812e31237dd89b42b910`  
		Last Modified: Mon, 11 May 2026 23:06:46 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b97561ea1445f287f13425e0d8c6cc555dda4521823c070aee98a51e1ca95aa`  
		Last Modified: Mon, 11 May 2026 23:06:47 GMT  
		Size: 6.5 KB (6492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:93902ca0265dee33a0a0ecae116ee8a0737de7a4b93bba1f8cadd54423063670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **981.4 KB (981356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ec019bd514eb7e1cda009f18e83ee9eb4242bf44eccda3b8f5330ee187a1a0`

```dockerfile
```

-	Layers:
	-	`sha256:b6b9ccdbf33b901df2b0084d3c64070e298e28ab046116b504914e56b831cb5d`  
		Last Modified: Mon, 11 May 2026 23:06:44 GMT  
		Size: 950.6 KB (950553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79b372300ad917b42bbf5b0f86f143b26dbe1d2b21c384a53e3a0fd0c0c2b4c6`  
		Last Modified: Mon, 11 May 2026 23:06:44 GMT  
		Size: 30.8 KB (30803 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.8`

```console
$ docker pull influxdb@sha256:d54f5c2028952aa407e3dca1d041ddd3416e64643b44096d39db41cb78721b90
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.8` - linux; amd64

```console
$ docker pull influxdb@sha256:3caf968c36db4203526d6888d827e47005b82cf2897ea245caac5c5d309fe9c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107241471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c196dda07efd74a544b14751d7e16da8920758ec1c9e47d10b003de6da829ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:42:06 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:42:06 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 08 May 2026 19:42:07 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Fri, 08 May 2026 19:42:08 GMT
ENV GOSU_VER=1.19
# Fri, 08 May 2026 19:42:08 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Fri, 08 May 2026 19:42:08 GMT
ENV INFLUXDB_VERSION=2.8.0
# Fri, 08 May 2026 19:42:08 GMT
ENV INFLUXDB_PR=-2
# Fri, 08 May 2026 19:42:08 GMT
ENV INFLUXDB_PV=2.8.0-2
# Fri, 08 May 2026 19:42:11 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Fri, 08 May 2026 19:42:11 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Fri, 08 May 2026 19:42:13 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 08 May 2026 19:42:13 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 08 May 2026 19:42:13 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 08 May 2026 19:42:13 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 08 May 2026 19:42:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 19:42:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 19:42:13 GMT
CMD ["influxd"]
# Fri, 08 May 2026 19:42:13 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 08 May 2026 19:42:13 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 08 May 2026 19:42:13 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 08 May 2026 19:42:13 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 08 May 2026 19:42:13 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5419d59ac905bf3776ddf9d322a917e1dea92efa2a25013b50bf37d79576b995`  
		Last Modified: Fri, 08 May 2026 19:42:24 GMT  
		Size: 9.8 MB (9799024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873cc6026d3f10bf3fd20ba4d9e1ed6d5658f60d6bd7be53d254754085563b31`  
		Last Modified: Fri, 08 May 2026 19:42:24 GMT  
		Size: 6.2 MB (6156974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b894acf519ad470390025a1a00fa97ac6a6b0d59d43ea1eaef872024a37e1d4e`  
		Last Modified: Fri, 08 May 2026 19:42:24 GMT  
		Size: 3.2 KB (3237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fce2d476bbb82bf725eb89b5f9d850d075e98cb2abf1abf9947870f03ea132a0`  
		Last Modified: Fri, 08 May 2026 19:42:24 GMT  
		Size: 811.5 KB (811475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f02aa765109be7224595a67b9e98faa952380a5fa1f1dc694d2054b6a27d0a`  
		Last Modified: Fri, 08 May 2026 19:42:27 GMT  
		Size: 50.5 MB (50451873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55e443aeec78cc9ac5eeb6ef90e9f2329651e4e367633563c9bf20f9af69942`  
		Last Modified: Fri, 08 May 2026 19:42:26 GMT  
		Size: 11.8 MB (11775877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882318f828a60133c97290606bf6ee422bfa888d323d852d653da07a0b7e1dc9`  
		Last Modified: Fri, 08 May 2026 19:42:26 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3d46a6ac3a1a7daecac827bcd9770a071e14a29a5e2bfc5020fb501925a558`  
		Last Modified: Fri, 08 May 2026 19:42:26 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c58ca0921ed5592f2f72e1ea39ef8be7368da833a40a75d5b071a7e70b3ba0`  
		Last Modified: Fri, 08 May 2026 19:42:27 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:02544f5c283632cb60ee19370461ddbb1f41031187a17f8838d6d84109e0c874
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2966670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59e9e467abcca7abfa0a89046a18858d367eb758420c9cfde9de24a2ecbc35a4`

```dockerfile
```

-	Layers:
	-	`sha256:ac661d6e1ebd732617626c1b6f7066268606dd7dbb123cf49875e6399049bb2a`  
		Last Modified: Fri, 08 May 2026 19:42:24 GMT  
		Size: 2.9 MB (2933643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0714435e3b2014eae105878d6b0dabc4555aeffbd47857f2a40331fac62e969`  
		Last Modified: Fri, 08 May 2026 19:42:24 GMT  
		Size: 33.0 KB (33027 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:31e54ac5d723e5e89a245a59e0449fa42f05afc6eabb80069cefe3db969cead2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103640917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:594e53651410f61840faee122635ff5569f999a811f222b772e671c8c8950e85`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:43:51 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:43:52 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 08 May 2026 19:43:52 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Fri, 08 May 2026 19:43:54 GMT
ENV GOSU_VER=1.19
# Fri, 08 May 2026 19:43:54 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Fri, 08 May 2026 19:43:54 GMT
ENV INFLUXDB_VERSION=2.8.0
# Fri, 08 May 2026 19:43:54 GMT
ENV INFLUXDB_PR=-2
# Fri, 08 May 2026 19:43:54 GMT
ENV INFLUXDB_PV=2.8.0-2
# Fri, 08 May 2026 19:43:57 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Fri, 08 May 2026 19:43:57 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Fri, 08 May 2026 19:43:59 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 08 May 2026 19:43:59 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 08 May 2026 19:43:59 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 08 May 2026 19:43:59 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 08 May 2026 19:43:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 19:43:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 19:43:59 GMT
CMD ["influxd"]
# Fri, 08 May 2026 19:43:59 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 08 May 2026 19:43:59 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 08 May 2026 19:43:59 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 08 May 2026 19:43:59 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 08 May 2026 19:43:59 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:947e85f6f9b14ae86257c598354512902b92d66affe0f135bcf3d046aa93b3d7`  
		Last Modified: Fri, 08 May 2026 19:44:10 GMT  
		Size: 9.6 MB (9628074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ec8e18de824b9849430d8d198c18302a0ecacf5d79bce199ebfc8b167626c7`  
		Last Modified: Fri, 08 May 2026 19:44:10 GMT  
		Size: 5.8 MB (5790425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1822d825c1e8a6ce305b404f0e672e4d1affca5fe1f00a0e5e3c8ce43cbf54c`  
		Last Modified: Fri, 08 May 2026 19:44:10 GMT  
		Size: 3.2 KB (3231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f7c78e6d67ffa39bb33dd5da6fbbbf9ab0ba4d031ff74280b74948a21e04eb`  
		Last Modified: Fri, 08 May 2026 19:44:10 GMT  
		Size: 766.4 KB (766366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61954b10bb9d67d8cc7fdd819aee43a574698710fdce0be52d1ec2d33659ab4b`  
		Last Modified: Fri, 08 May 2026 19:44:13 GMT  
		Size: 48.2 MB (48229553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c430a9db8de2dcf694eebd2ae181655006af2cba702a5b66c2d9e74d3c9453`  
		Last Modified: Fri, 08 May 2026 19:44:13 GMT  
		Size: 11.1 MB (11100373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1704e5bc01c6ad2912530f2ef763163b5ed08bbfc99fb2b9d8ac1b29d78a0e3a`  
		Last Modified: Fri, 08 May 2026 19:44:12 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001c31a94a84715d4d255becfbecbe3961ea62c2854fdf3e4de9568f47aa0601`  
		Last Modified: Fri, 08 May 2026 19:44:12 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e635b657af89a8e2130093e28c12cd17c9283c5af9bec398b4588e0ccebd1eb5`  
		Last Modified: Fri, 08 May 2026 19:44:13 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:c2dc4c93bfcc480d4e73949ffb58c0b237a64b9c57ef97473e2a10cdd60cd7f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2966296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de73f70f95fbf73966d530c8567921e0f30d67bfe07c5c16dd35ff623307d03`

```dockerfile
```

-	Layers:
	-	`sha256:66f9f4270290be667bd51b227f16aad8864f1f5f66ed5d30f184d2b68d18ebb1`  
		Last Modified: Fri, 08 May 2026 19:44:10 GMT  
		Size: 2.9 MB (2933099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:716cfee7b969bfa6e52cbc11fc245222524fca8e4ec3a3fa10176c37f80e71c5`  
		Last Modified: Fri, 08 May 2026 19:44:10 GMT  
		Size: 33.2 KB (33197 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.8-alpine`

```console
$ docker pull influxdb@sha256:41dd20908d395acc7b839b64e4350e2b5f41a368beb2a1368ca52e8c76c94b3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.8-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:3f404b91defd8c01462d057d44587bbdd546a9318d8ca366faaa7468d638a81a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82513535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:619efccec88d0d48782c928996db6c574990252fbf53b9fd930c5087bf49b7b3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 04 May 2026 19:24:53 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 04 May 2026 19:24:54 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Mon, 04 May 2026 19:24:55 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 04 May 2026 19:24:55 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Mon, 04 May 2026 19:24:58 GMT
ENV INFLUXDB_VERSION=2.8.0
# Mon, 04 May 2026 19:24:58 GMT
ENV INFLUXDB_PR=-2
# Mon, 04 May 2026 19:24:58 GMT
ENV INFLUXDB_PV=2.8.0-2
# Mon, 04 May 2026 19:24:58 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 04 May 2026 19:24:58 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 04 May 2026 19:24:59 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 04 May 2026 19:24:59 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 04 May 2026 19:24:59 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 04 May 2026 19:24:59 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 04 May 2026 19:24:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 04 May 2026 19:24:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 19:24:59 GMT
CMD ["influxd"]
# Mon, 04 May 2026 19:24:59 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 04 May 2026 19:24:59 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 04 May 2026 19:24:59 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 04 May 2026 19:24:59 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 04 May 2026 19:24:59 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2a13f00c9e25a577d0e7db67a69e5f306c605370a8dec0e497d024648585cc`  
		Last Modified: Mon, 04 May 2026 19:25:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c36b34b857cc72e8b17924102300f4d1e0b805cb7f26a64b396bc57cef99e6`  
		Last Modified: Mon, 04 May 2026 19:25:09 GMT  
		Size: 10.3 MB (10256715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80cd0cf192f513cad40625f345a0e918e179f5f39a9f4216f2ba7a029b0ba45`  
		Last Modified: Mon, 04 May 2026 19:25:08 GMT  
		Size: 6.2 MB (6156988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6979c5162c5b276272cb3564173208c2b96b611beb6ae2f1632ec7a96b93fa8`  
		Last Modified: Mon, 04 May 2026 19:25:08 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05cbe6af81003faa3a881f17e88b95dd2d60ed199b539a729f6a42a69d659b2`  
		Last Modified: Mon, 04 May 2026 19:25:11 GMT  
		Size: 50.5 MB (50451815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524f983f6e0756b970192c5c005927ec8015f0dd037940b402e9f34ac25001ac`  
		Last Modified: Mon, 04 May 2026 19:25:10 GMT  
		Size: 11.8 MB (11775875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6355824be7ea94633d3879b23f8f1921059dddad278e6065823cf950058b152f`  
		Last Modified: Mon, 04 May 2026 19:25:10 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:692a76cbc8005b70d601e64f1fdae9068feb261c8aa7c7e2f807e945d510baca`  
		Last Modified: Mon, 04 May 2026 19:25:10 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c96464a562d572ffff64a598ebd5d9ee461c2a9f16a4babf7e24462097c0e1`  
		Last Modified: Mon, 04 May 2026 19:25:11 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:dda9fc6d5d354addeb1d4b4e56524b4aecb06fd30bc59344e71f3fe781accc87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **950.3 KB (950334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9193e76f2cea5534115c717c0245c66ce5eff44c87285eedf5df4ce37984524f`

```dockerfile
```

-	Layers:
	-	`sha256:a0d882621340a7bdcda574c4739cc11b13ebd6f2e655fb5a5698a02226d4a46a`  
		Last Modified: Mon, 04 May 2026 19:25:08 GMT  
		Size: 919.5 KB (919479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d50076762614be90fec916e38425d5756a50d65274827a3d3c18ea750222e382`  
		Last Modified: Mon, 04 May 2026 19:25:08 GMT  
		Size: 30.9 KB (30855 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.8-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:9a45f57bab26507490970d9693c1ee4636bbda47b51a4548c3151432ca97d8fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79551691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:665b984f6fa94fab273917c84f5d1e41308f92acc108d34c5d58b5bd2767defc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 04 May 2026 19:25:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 04 May 2026 19:25:09 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Mon, 04 May 2026 19:25:09 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 04 May 2026 19:25:09 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Mon, 04 May 2026 19:25:12 GMT
ENV INFLUXDB_VERSION=2.8.0
# Mon, 04 May 2026 19:25:12 GMT
ENV INFLUXDB_PR=-2
# Mon, 04 May 2026 19:25:12 GMT
ENV INFLUXDB_PV=2.8.0-2
# Mon, 04 May 2026 19:25:12 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 04 May 2026 19:25:12 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 04 May 2026 19:25:13 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 04 May 2026 19:25:13 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 04 May 2026 19:25:13 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 04 May 2026 19:25:13 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 04 May 2026 19:25:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 04 May 2026 19:25:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 19:25:13 GMT
CMD ["influxd"]
# Mon, 04 May 2026 19:25:13 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 04 May 2026 19:25:13 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 04 May 2026 19:25:13 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 04 May 2026 19:25:13 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 04 May 2026 19:25:13 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4386c3398ae404c3540b4525a958fc9e31ebd8766a9fde64c0eb48c47a82b3f5`  
		Last Modified: Mon, 04 May 2026 19:25:23 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be54a4b3b97cdaafcf772bf0961664df00d6b88b5b0837d1a9373a8754b90893`  
		Last Modified: Mon, 04 May 2026 19:25:23 GMT  
		Size: 10.2 MB (10223491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74da88063d91843af2e82ba63cee5041c68a9a2f1be476ab9a01acada4a6d48f`  
		Last Modified: Mon, 04 May 2026 19:25:23 GMT  
		Size: 5.8 MB (5790431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d697444c8fbdcefe0897e2aa13400fe43bb855aab373b0e3d083c648f60d557`  
		Last Modified: Mon, 04 May 2026 19:25:23 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0616fa7080c6f424270564b2f256272c9cf01ed6ae62e3d2d32d73d822959f0d`  
		Last Modified: Mon, 04 May 2026 19:25:25 GMT  
		Size: 48.2 MB (48229534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f485e2c91079cd39cb7e4ea83e14263347b0f516e45a4eb4f90c118829f68f`  
		Last Modified: Mon, 04 May 2026 19:25:25 GMT  
		Size: 11.1 MB (11100412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b5d177042371e3ed653567402afc5f81f3ae14a6822fa4c6c67aa0566ffe809`  
		Last Modified: Mon, 04 May 2026 19:25:24 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0172bb0812fd93a7eba4d87db2999b21c2408fc38a661b288119a41c318ca2`  
		Last Modified: Mon, 04 May 2026 19:25:25 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539c90580d970ff60c09191930bf47bf2723b1fdb9991363aca087e0c10395da`  
		Last Modified: Mon, 04 May 2026 19:25:26 GMT  
		Size: 6.3 KB (6280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:87bf8c3f9414553407e04b3ab15af77e8112c17e304e6581269224e20bc3f71d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **949.1 KB (949129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c1f2b013744e021e3b9ecff03c6ed7db669dc448f7194cb6ae53cc8f4489914`

```dockerfile
```

-	Layers:
	-	`sha256:a21e15400842bdec049aedd115554726aaeb4c5fc72fe83f027ae4cf94dc0b83`  
		Last Modified: Mon, 04 May 2026 19:25:23 GMT  
		Size: 918.1 KB (918080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9558444eedc144a914b41b0c7ac259c6cb898a785a1f47da7f639ebbedfb7e9`  
		Last Modified: Mon, 04 May 2026 19:25:23 GMT  
		Size: 31.0 KB (31049 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.8.0`

```console
$ docker pull influxdb@sha256:d54f5c2028952aa407e3dca1d041ddd3416e64643b44096d39db41cb78721b90
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.8.0` - linux; amd64

```console
$ docker pull influxdb@sha256:3caf968c36db4203526d6888d827e47005b82cf2897ea245caac5c5d309fe9c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107241471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c196dda07efd74a544b14751d7e16da8920758ec1c9e47d10b003de6da829ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:42:06 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:42:06 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 08 May 2026 19:42:07 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Fri, 08 May 2026 19:42:08 GMT
ENV GOSU_VER=1.19
# Fri, 08 May 2026 19:42:08 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Fri, 08 May 2026 19:42:08 GMT
ENV INFLUXDB_VERSION=2.8.0
# Fri, 08 May 2026 19:42:08 GMT
ENV INFLUXDB_PR=-2
# Fri, 08 May 2026 19:42:08 GMT
ENV INFLUXDB_PV=2.8.0-2
# Fri, 08 May 2026 19:42:11 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Fri, 08 May 2026 19:42:11 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Fri, 08 May 2026 19:42:13 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 08 May 2026 19:42:13 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 08 May 2026 19:42:13 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 08 May 2026 19:42:13 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 08 May 2026 19:42:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 19:42:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 19:42:13 GMT
CMD ["influxd"]
# Fri, 08 May 2026 19:42:13 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 08 May 2026 19:42:13 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 08 May 2026 19:42:13 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 08 May 2026 19:42:13 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 08 May 2026 19:42:13 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5419d59ac905bf3776ddf9d322a917e1dea92efa2a25013b50bf37d79576b995`  
		Last Modified: Fri, 08 May 2026 19:42:24 GMT  
		Size: 9.8 MB (9799024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873cc6026d3f10bf3fd20ba4d9e1ed6d5658f60d6bd7be53d254754085563b31`  
		Last Modified: Fri, 08 May 2026 19:42:24 GMT  
		Size: 6.2 MB (6156974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b894acf519ad470390025a1a00fa97ac6a6b0d59d43ea1eaef872024a37e1d4e`  
		Last Modified: Fri, 08 May 2026 19:42:24 GMT  
		Size: 3.2 KB (3237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fce2d476bbb82bf725eb89b5f9d850d075e98cb2abf1abf9947870f03ea132a0`  
		Last Modified: Fri, 08 May 2026 19:42:24 GMT  
		Size: 811.5 KB (811475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f02aa765109be7224595a67b9e98faa952380a5fa1f1dc694d2054b6a27d0a`  
		Last Modified: Fri, 08 May 2026 19:42:27 GMT  
		Size: 50.5 MB (50451873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55e443aeec78cc9ac5eeb6ef90e9f2329651e4e367633563c9bf20f9af69942`  
		Last Modified: Fri, 08 May 2026 19:42:26 GMT  
		Size: 11.8 MB (11775877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882318f828a60133c97290606bf6ee422bfa888d323d852d653da07a0b7e1dc9`  
		Last Modified: Fri, 08 May 2026 19:42:26 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3d46a6ac3a1a7daecac827bcd9770a071e14a29a5e2bfc5020fb501925a558`  
		Last Modified: Fri, 08 May 2026 19:42:26 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c58ca0921ed5592f2f72e1ea39ef8be7368da833a40a75d5b071a7e70b3ba0`  
		Last Modified: Fri, 08 May 2026 19:42:27 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8.0` - unknown; unknown

```console
$ docker pull influxdb@sha256:02544f5c283632cb60ee19370461ddbb1f41031187a17f8838d6d84109e0c874
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2966670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59e9e467abcca7abfa0a89046a18858d367eb758420c9cfde9de24a2ecbc35a4`

```dockerfile
```

-	Layers:
	-	`sha256:ac661d6e1ebd732617626c1b6f7066268606dd7dbb123cf49875e6399049bb2a`  
		Last Modified: Fri, 08 May 2026 19:42:24 GMT  
		Size: 2.9 MB (2933643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0714435e3b2014eae105878d6b0dabc4555aeffbd47857f2a40331fac62e969`  
		Last Modified: Fri, 08 May 2026 19:42:24 GMT  
		Size: 33.0 KB (33027 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.8.0` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:31e54ac5d723e5e89a245a59e0449fa42f05afc6eabb80069cefe3db969cead2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103640917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:594e53651410f61840faee122635ff5569f999a811f222b772e671c8c8950e85`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:43:51 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:43:52 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 08 May 2026 19:43:52 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Fri, 08 May 2026 19:43:54 GMT
ENV GOSU_VER=1.19
# Fri, 08 May 2026 19:43:54 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Fri, 08 May 2026 19:43:54 GMT
ENV INFLUXDB_VERSION=2.8.0
# Fri, 08 May 2026 19:43:54 GMT
ENV INFLUXDB_PR=-2
# Fri, 08 May 2026 19:43:54 GMT
ENV INFLUXDB_PV=2.8.0-2
# Fri, 08 May 2026 19:43:57 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Fri, 08 May 2026 19:43:57 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Fri, 08 May 2026 19:43:59 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 08 May 2026 19:43:59 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 08 May 2026 19:43:59 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 08 May 2026 19:43:59 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 08 May 2026 19:43:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 19:43:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 19:43:59 GMT
CMD ["influxd"]
# Fri, 08 May 2026 19:43:59 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 08 May 2026 19:43:59 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 08 May 2026 19:43:59 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 08 May 2026 19:43:59 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 08 May 2026 19:43:59 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:947e85f6f9b14ae86257c598354512902b92d66affe0f135bcf3d046aa93b3d7`  
		Last Modified: Fri, 08 May 2026 19:44:10 GMT  
		Size: 9.6 MB (9628074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ec8e18de824b9849430d8d198c18302a0ecacf5d79bce199ebfc8b167626c7`  
		Last Modified: Fri, 08 May 2026 19:44:10 GMT  
		Size: 5.8 MB (5790425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1822d825c1e8a6ce305b404f0e672e4d1affca5fe1f00a0e5e3c8ce43cbf54c`  
		Last Modified: Fri, 08 May 2026 19:44:10 GMT  
		Size: 3.2 KB (3231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f7c78e6d67ffa39bb33dd5da6fbbbf9ab0ba4d031ff74280b74948a21e04eb`  
		Last Modified: Fri, 08 May 2026 19:44:10 GMT  
		Size: 766.4 KB (766366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61954b10bb9d67d8cc7fdd819aee43a574698710fdce0be52d1ec2d33659ab4b`  
		Last Modified: Fri, 08 May 2026 19:44:13 GMT  
		Size: 48.2 MB (48229553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c430a9db8de2dcf694eebd2ae181655006af2cba702a5b66c2d9e74d3c9453`  
		Last Modified: Fri, 08 May 2026 19:44:13 GMT  
		Size: 11.1 MB (11100373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1704e5bc01c6ad2912530f2ef763163b5ed08bbfc99fb2b9d8ac1b29d78a0e3a`  
		Last Modified: Fri, 08 May 2026 19:44:12 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001c31a94a84715d4d255becfbecbe3961ea62c2854fdf3e4de9568f47aa0601`  
		Last Modified: Fri, 08 May 2026 19:44:12 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e635b657af89a8e2130093e28c12cd17c9283c5af9bec398b4588e0ccebd1eb5`  
		Last Modified: Fri, 08 May 2026 19:44:13 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8.0` - unknown; unknown

```console
$ docker pull influxdb@sha256:c2dc4c93bfcc480d4e73949ffb58c0b237a64b9c57ef97473e2a10cdd60cd7f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2966296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de73f70f95fbf73966d530c8567921e0f30d67bfe07c5c16dd35ff623307d03`

```dockerfile
```

-	Layers:
	-	`sha256:66f9f4270290be667bd51b227f16aad8864f1f5f66ed5d30f184d2b68d18ebb1`  
		Last Modified: Fri, 08 May 2026 19:44:10 GMT  
		Size: 2.9 MB (2933099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:716cfee7b969bfa6e52cbc11fc245222524fca8e4ec3a3fa10176c37f80e71c5`  
		Last Modified: Fri, 08 May 2026 19:44:10 GMT  
		Size: 33.2 KB (33197 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.8.0-alpine`

```console
$ docker pull influxdb@sha256:41dd20908d395acc7b839b64e4350e2b5f41a368beb2a1368ca52e8c76c94b3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.8.0-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:3f404b91defd8c01462d057d44587bbdd546a9318d8ca366faaa7468d638a81a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82513535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:619efccec88d0d48782c928996db6c574990252fbf53b9fd930c5087bf49b7b3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 04 May 2026 19:24:53 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 04 May 2026 19:24:54 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Mon, 04 May 2026 19:24:55 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 04 May 2026 19:24:55 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Mon, 04 May 2026 19:24:58 GMT
ENV INFLUXDB_VERSION=2.8.0
# Mon, 04 May 2026 19:24:58 GMT
ENV INFLUXDB_PR=-2
# Mon, 04 May 2026 19:24:58 GMT
ENV INFLUXDB_PV=2.8.0-2
# Mon, 04 May 2026 19:24:58 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 04 May 2026 19:24:58 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 04 May 2026 19:24:59 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 04 May 2026 19:24:59 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 04 May 2026 19:24:59 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 04 May 2026 19:24:59 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 04 May 2026 19:24:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 04 May 2026 19:24:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 19:24:59 GMT
CMD ["influxd"]
# Mon, 04 May 2026 19:24:59 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 04 May 2026 19:24:59 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 04 May 2026 19:24:59 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 04 May 2026 19:24:59 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 04 May 2026 19:24:59 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2a13f00c9e25a577d0e7db67a69e5f306c605370a8dec0e497d024648585cc`  
		Last Modified: Mon, 04 May 2026 19:25:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c36b34b857cc72e8b17924102300f4d1e0b805cb7f26a64b396bc57cef99e6`  
		Last Modified: Mon, 04 May 2026 19:25:09 GMT  
		Size: 10.3 MB (10256715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80cd0cf192f513cad40625f345a0e918e179f5f39a9f4216f2ba7a029b0ba45`  
		Last Modified: Mon, 04 May 2026 19:25:08 GMT  
		Size: 6.2 MB (6156988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6979c5162c5b276272cb3564173208c2b96b611beb6ae2f1632ec7a96b93fa8`  
		Last Modified: Mon, 04 May 2026 19:25:08 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05cbe6af81003faa3a881f17e88b95dd2d60ed199b539a729f6a42a69d659b2`  
		Last Modified: Mon, 04 May 2026 19:25:11 GMT  
		Size: 50.5 MB (50451815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524f983f6e0756b970192c5c005927ec8015f0dd037940b402e9f34ac25001ac`  
		Last Modified: Mon, 04 May 2026 19:25:10 GMT  
		Size: 11.8 MB (11775875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6355824be7ea94633d3879b23f8f1921059dddad278e6065823cf950058b152f`  
		Last Modified: Mon, 04 May 2026 19:25:10 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:692a76cbc8005b70d601e64f1fdae9068feb261c8aa7c7e2f807e945d510baca`  
		Last Modified: Mon, 04 May 2026 19:25:10 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c96464a562d572ffff64a598ebd5d9ee461c2a9f16a4babf7e24462097c0e1`  
		Last Modified: Mon, 04 May 2026 19:25:11 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8.0-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:dda9fc6d5d354addeb1d4b4e56524b4aecb06fd30bc59344e71f3fe781accc87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **950.3 KB (950334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9193e76f2cea5534115c717c0245c66ce5eff44c87285eedf5df4ce37984524f`

```dockerfile
```

-	Layers:
	-	`sha256:a0d882621340a7bdcda574c4739cc11b13ebd6f2e655fb5a5698a02226d4a46a`  
		Last Modified: Mon, 04 May 2026 19:25:08 GMT  
		Size: 919.5 KB (919479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d50076762614be90fec916e38425d5756a50d65274827a3d3c18ea750222e382`  
		Last Modified: Mon, 04 May 2026 19:25:08 GMT  
		Size: 30.9 KB (30855 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.8.0-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:9a45f57bab26507490970d9693c1ee4636bbda47b51a4548c3151432ca97d8fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79551691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:665b984f6fa94fab273917c84f5d1e41308f92acc108d34c5d58b5bd2767defc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 04 May 2026 19:25:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 04 May 2026 19:25:09 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Mon, 04 May 2026 19:25:09 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 04 May 2026 19:25:09 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Mon, 04 May 2026 19:25:12 GMT
ENV INFLUXDB_VERSION=2.8.0
# Mon, 04 May 2026 19:25:12 GMT
ENV INFLUXDB_PR=-2
# Mon, 04 May 2026 19:25:12 GMT
ENV INFLUXDB_PV=2.8.0-2
# Mon, 04 May 2026 19:25:12 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 04 May 2026 19:25:12 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 04 May 2026 19:25:13 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 04 May 2026 19:25:13 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 04 May 2026 19:25:13 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 04 May 2026 19:25:13 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 04 May 2026 19:25:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 04 May 2026 19:25:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 19:25:13 GMT
CMD ["influxd"]
# Mon, 04 May 2026 19:25:13 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 04 May 2026 19:25:13 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 04 May 2026 19:25:13 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 04 May 2026 19:25:13 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 04 May 2026 19:25:13 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4386c3398ae404c3540b4525a958fc9e31ebd8766a9fde64c0eb48c47a82b3f5`  
		Last Modified: Mon, 04 May 2026 19:25:23 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be54a4b3b97cdaafcf772bf0961664df00d6b88b5b0837d1a9373a8754b90893`  
		Last Modified: Mon, 04 May 2026 19:25:23 GMT  
		Size: 10.2 MB (10223491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74da88063d91843af2e82ba63cee5041c68a9a2f1be476ab9a01acada4a6d48f`  
		Last Modified: Mon, 04 May 2026 19:25:23 GMT  
		Size: 5.8 MB (5790431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d697444c8fbdcefe0897e2aa13400fe43bb855aab373b0e3d083c648f60d557`  
		Last Modified: Mon, 04 May 2026 19:25:23 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0616fa7080c6f424270564b2f256272c9cf01ed6ae62e3d2d32d73d822959f0d`  
		Last Modified: Mon, 04 May 2026 19:25:25 GMT  
		Size: 48.2 MB (48229534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f485e2c91079cd39cb7e4ea83e14263347b0f516e45a4eb4f90c118829f68f`  
		Last Modified: Mon, 04 May 2026 19:25:25 GMT  
		Size: 11.1 MB (11100412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b5d177042371e3ed653567402afc5f81f3ae14a6822fa4c6c67aa0566ffe809`  
		Last Modified: Mon, 04 May 2026 19:25:24 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0172bb0812fd93a7eba4d87db2999b21c2408fc38a661b288119a41c318ca2`  
		Last Modified: Mon, 04 May 2026 19:25:25 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539c90580d970ff60c09191930bf47bf2723b1fdb9991363aca087e0c10395da`  
		Last Modified: Mon, 04 May 2026 19:25:26 GMT  
		Size: 6.3 KB (6280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8.0-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:87bf8c3f9414553407e04b3ab15af77e8112c17e304e6581269224e20bc3f71d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **949.1 KB (949129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c1f2b013744e021e3b9ecff03c6ed7db669dc448f7194cb6ae53cc8f4489914`

```dockerfile
```

-	Layers:
	-	`sha256:a21e15400842bdec049aedd115554726aaeb4c5fc72fe83f027ae4cf94dc0b83`  
		Last Modified: Mon, 04 May 2026 19:25:23 GMT  
		Size: 918.1 KB (918080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9558444eedc144a914b41b0c7ac259c6cb898a785a1f47da7f639ebbedfb7e9`  
		Last Modified: Mon, 04 May 2026 19:25:23 GMT  
		Size: 31.0 KB (31049 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.9`

```console
$ docker pull influxdb@sha256:044d60447880093b9837d5de56ea0699b0db79a3e48fb94edf0f9e0eb9f4b95c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.9` - linux; amd64

```console
$ docker pull influxdb@sha256:82cd8aa54e7a82a3a006af30e3a31488b73a24f664677ba63782a9343302f1bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.8 MB (110800813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:373cd1bc99e1a9c96598fe115410634b5c8730eb6745f041f9203f1b3291ec8f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Mon, 11 May 2026 23:06:14 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg       util-linux &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:06:14 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Mon, 11 May 2026 23:06:14 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Mon, 11 May 2026 23:06:18 GMT
ENV INFLUXDB_VERSION=2.9.1
# Mon, 11 May 2026 23:06:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 11 May 2026 23:06:18 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Mon, 11 May 2026 23:06:20 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 11 May 2026 23:06:20 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 11 May 2026 23:06:20 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 11 May 2026 23:06:20 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 11 May 2026 23:06:20 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 11 May 2026 23:06:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 May 2026 23:06:20 GMT
CMD ["influxd"]
# Mon, 11 May 2026 23:06:20 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 11 May 2026 23:06:20 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 11 May 2026 23:06:20 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 11 May 2026 23:06:20 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 11 May 2026 23:06:20 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6306d75e2dc4ba2680cb2722b624ffd58658aea8bd7eb42637befbd5f956dc64`  
		Last Modified: Mon, 11 May 2026 23:06:33 GMT  
		Size: 9.8 MB (9799055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a82281c39f9f067b4235800d0e007670159c80542159a4450563d989fcb6563`  
		Last Modified: Mon, 11 May 2026 23:06:33 GMT  
		Size: 3.8 MB (3822784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a116ed37df3620df292451a9d9a04e82e56d60335cf27224a67219ed22cc038`  
		Last Modified: Mon, 11 May 2026 23:06:33 GMT  
		Size: 3.2 KB (3235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af303914f43bdf518bb8cfc5c3c8f4ce2f6e39e7424c012c140aca8689925373`  
		Last Modified: Mon, 11 May 2026 23:06:34 GMT  
		Size: 56.5 MB (56510687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080fd8044aff2f969b124bf1847f066b663e5b2f6cae5eb4a2fe39fd84b9ca8a`  
		Last Modified: Mon, 11 May 2026 23:06:34 GMT  
		Size: 12.4 MB (12421826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c8bdb93dd525adb082fe977c42446a606867cb0876486414590f483bdb16e5`  
		Last Modified: Mon, 11 May 2026 23:06:34 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec61169a51e436a25adf019845e2b06c2a2f667604bdaa2f3ce7d6c242b7e2d3`  
		Last Modified: Mon, 11 May 2026 23:06:35 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c8475bae289926b70499ba7275b48cf710950a5c1745f1047e5cea27687ae7`  
		Last Modified: Mon, 11 May 2026 23:06:35 GMT  
		Size: 6.5 KB (6500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.9` - unknown; unknown

```console
$ docker pull influxdb@sha256:3b4cdef18045a438e84e562f34e5593ba983944ada9400c448b23087fef4b9a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2988025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c263006991641cd34e84386b46b2189a3f22c0342ad8433ea93de78b3c101a59`

```dockerfile
```

-	Layers:
	-	`sha256:1eaa89e6c29ca38c8ea88162e378052dd323f1b5ccec9fbe77da9e5df39808c7`  
		Last Modified: Mon, 11 May 2026 23:06:33 GMT  
		Size: 3.0 MB (2959411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4126e96a3d9f757323087f196a105f67cb780972bf33fd5a38e7808989145600`  
		Last Modified: Mon, 11 May 2026 23:06:32 GMT  
		Size: 28.6 KB (28614 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.9` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:3bce906f5cd366a1d7f1386e355e51c87c6192fcc4d71c68a2edd3297a0192df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106330754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53cf7d95c5904cc95a6940f0d1154b73162e38d225ef133b2450a48ca219c096`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Mon, 11 May 2026 23:06:05 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg       util-linux &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:06:05 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Mon, 11 May 2026 23:06:05 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Mon, 11 May 2026 23:06:09 GMT
ENV INFLUXDB_VERSION=2.9.1
# Mon, 11 May 2026 23:06:09 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 11 May 2026 23:06:09 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Mon, 11 May 2026 23:06:11 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 11 May 2026 23:06:11 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 11 May 2026 23:06:11 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 11 May 2026 23:06:11 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 11 May 2026 23:06:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 11 May 2026 23:06:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 May 2026 23:06:11 GMT
CMD ["influxd"]
# Mon, 11 May 2026 23:06:11 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 11 May 2026 23:06:11 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 11 May 2026 23:06:11 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 11 May 2026 23:06:11 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 11 May 2026 23:06:11 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f23bbe568e43c569b84c86a9c06acb37a65383eef9d7a41c3493f2fc439b23`  
		Last Modified: Mon, 11 May 2026 23:06:23 GMT  
		Size: 9.6 MB (9628121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf21f16acbfdf9cb08e177f4e24e660aef286d9b0246883ca9ccac7f3423ef5`  
		Last Modified: Mon, 11 May 2026 23:06:23 GMT  
		Size: 3.5 MB (3459172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7651cdf91299714e33bee7297dbf293d680c2046377416bbec761092b53fbff`  
		Last Modified: Mon, 11 May 2026 23:06:23 GMT  
		Size: 3.2 KB (3233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93251acc80816de10b80ad59732e2112e724a1d77bc28e4943715d5a298725e`  
		Last Modified: Mon, 11 May 2026 23:06:25 GMT  
		Size: 53.6 MB (53636817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb61f007cdfb2efe51d7353b061d5dc88228555a0565832e7f4798bcf9c4bc05`  
		Last Modified: Mon, 11 May 2026 23:06:25 GMT  
		Size: 11.5 MB (11480302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d795a7febcb13431d839fb4382b6e22f5debf58e787deaeb34da45464289ba10`  
		Last Modified: Mon, 11 May 2026 23:06:25 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e57e263f59e437119c3be99d4d6e7ef67e658750db5b34f3c5307bb8d3d583`  
		Last Modified: Mon, 11 May 2026 23:06:25 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f0fde88bd7e8e0fef0640c7e8be480e6b382f511e2da3d9129a50466da3d55`  
		Last Modified: Mon, 11 May 2026 23:06:26 GMT  
		Size: 6.5 KB (6500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.9` - unknown; unknown

```console
$ docker pull influxdb@sha256:eb708288bfdc461e6c7c5c7346d5a1d11ba930ebf51cd162c10e023a7e3b89cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed727a90b15a758f20fe1ecb27f8186e0638b8cd670f3eb6052b11f07a9dde9c`

```dockerfile
```

-	Layers:
	-	`sha256:64fc4525aa7a436f50908c48554e8f5bd8b3b56e903570d96d434ea2183135f7`  
		Last Modified: Mon, 11 May 2026 23:06:23 GMT  
		Size: 3.0 MB (2958889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c1611d06ea9793b05207e6377419833d4f183dd192845527a8be765b2d3d5e9`  
		Last Modified: Mon, 11 May 2026 23:06:23 GMT  
		Size: 28.8 KB (28793 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.9-alpine`

```console
$ docker pull influxdb@sha256:1cb8fa92ff9d13518d8198dae872b7ea523757a03c655d12a67175b1ab7a72f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.9-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:99e216544ab6f8f8d4180d06bcc8deb61a676971c63e31faae24fc169945c4d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86902190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:343b7e7e34cb3b0c8e6c7a44f74f147f01f7ab4022ad1aa3c99ee43701d261f0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 11 May 2026 23:06:21 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 11 May 2026 23:06:23 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       setpriv       tzdata &&     update-ca-certificates # buildkit
# Mon, 11 May 2026 23:06:23 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Mon, 11 May 2026 23:06:23 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Mon, 11 May 2026 23:06:26 GMT
ENV INFLUXDB_VERSION=2.9.1
# Mon, 11 May 2026 23:06:26 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 11 May 2026 23:06:26 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Mon, 11 May 2026 23:06:27 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 11 May 2026 23:06:27 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 11 May 2026 23:06:27 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 11 May 2026 23:06:27 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 11 May 2026 23:06:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 11 May 2026 23:06:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 May 2026 23:06:27 GMT
CMD ["influxd"]
# Mon, 11 May 2026 23:06:27 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 11 May 2026 23:06:27 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 11 May 2026 23:06:27 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 11 May 2026 23:06:27 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 11 May 2026 23:06:27 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298fb8d3d07e69a02cd49af0883ae79a93c4625bc43501293daf0d954698afb5`  
		Last Modified: Mon, 11 May 2026 23:06:38 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896207ace1714281476706f02a38f5bafa2e8b0d466910e59c4abe1f0ef217a3`  
		Last Modified: Mon, 11 May 2026 23:06:38 GMT  
		Size: 10.3 MB (10274619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2fcd4f5629f0c11692de5d63652eda9a1de734dedd342a70ef1a8c1915d6e3`  
		Last Modified: Mon, 11 May 2026 23:06:38 GMT  
		Size: 3.8 MB (3822787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7399422b7a7b047fd9f9ae6a7b1b3c379169c0320d8c89787c7e57e378c95d46`  
		Last Modified: Mon, 11 May 2026 23:06:38 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a421d960302e6e78e3497cecdfbf7e68f9f87afb9c264f7efd238f037129c2`  
		Last Modified: Mon, 11 May 2026 23:06:41 GMT  
		Size: 56.5 MB (56510610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af09c2df41ffda41b4df2fd992fb0be316e613c2f08ecac1733e26e530fd6fb`  
		Last Modified: Mon, 11 May 2026 23:06:40 GMT  
		Size: 12.4 MB (12421822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141bbaa5308a2f1112e696cb9e82bc575508bf3fdba5b192f4c5017ed1ff0345`  
		Last Modified: Mon, 11 May 2026 23:06:40 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8db14735975847fbcb27a366734a994b19e81b52f37258eb95514dd7f2e7403`  
		Last Modified: Mon, 11 May 2026 23:06:41 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e66dbce9517e43a94af04ed7171b8a8c4174f59aeedd523604e88ced95a82de`  
		Last Modified: Mon, 11 May 2026 23:06:41 GMT  
		Size: 6.5 KB (6493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.9-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:45ebd475ac2880a68c21896d4cb1186238df70770b3318fdfcc83ac0f437a337
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **982.6 KB (982563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d587a6c839e8fdba54a6798485c7788dea62d5dc23bb982ddb676468b555f2e2`

```dockerfile
```

-	Layers:
	-	`sha256:00fb4b7e94546950e1d396936b5d2b235f6b34d79341a38bea451349ae4e71ad`  
		Last Modified: Mon, 11 May 2026 23:06:38 GMT  
		Size: 952.0 KB (951954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87c7670b411083afd6e9eee2031e773c5f9c80d7684afade5ae50a6602f99766`  
		Last Modified: Mon, 11 May 2026 23:06:38 GMT  
		Size: 30.6 KB (30609 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.9-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:02a1ea25d55126eb4d17a75d949f6939f995ee716a38d5cf87dacbfcbc43b5f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.0 MB (83028837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc4487542a8db6296883e5107322a4eeb7ac2f72cf6251e1b284eb9f8ba30ad0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 11 May 2026 23:06:28 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 11 May 2026 23:06:29 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       setpriv       tzdata &&     update-ca-certificates # buildkit
# Mon, 11 May 2026 23:06:30 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Mon, 11 May 2026 23:06:30 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Mon, 11 May 2026 23:06:32 GMT
ENV INFLUXDB_VERSION=2.9.1
# Mon, 11 May 2026 23:06:32 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 11 May 2026 23:06:32 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Mon, 11 May 2026 23:06:33 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 11 May 2026 23:06:33 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 11 May 2026 23:06:33 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 11 May 2026 23:06:33 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 11 May 2026 23:06:33 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 11 May 2026 23:06:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 May 2026 23:06:33 GMT
CMD ["influxd"]
# Mon, 11 May 2026 23:06:33 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 11 May 2026 23:06:33 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 11 May 2026 23:06:33 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 11 May 2026 23:06:33 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 11 May 2026 23:06:33 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4647b3db14cecf9d1d3425f0c3d71e29d76706a4ba687c996add84a9e46d7ac`  
		Last Modified: Mon, 11 May 2026 23:06:44 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fff389d9cde97293c698f3913f18598979f35d0502a8e50385bda21328b81c4`  
		Last Modified: Mon, 11 May 2026 23:06:44 GMT  
		Size: 10.2 MB (10244532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b6866a06fadef09561556d16e7b2b3e0279d4ca952ac2e3675803c00008dbc`  
		Last Modified: Mon, 11 May 2026 23:06:44 GMT  
		Size: 3.5 MB (3459165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9f34a583141b546c821a5ff21181240e09fa803803fe707d8da1b354084a33`  
		Last Modified: Mon, 11 May 2026 23:06:44 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a88da843f8eafbaedc72d393269a63b69eba46cd5780a319eee812b3428b8cc`  
		Last Modified: Mon, 11 May 2026 23:06:47 GMT  
		Size: 53.6 MB (53636820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd2e861c1ced42fa6d0ba182a983a7cf3b6d02f861f36efcfbe429b15544c4b`  
		Last Modified: Mon, 11 May 2026 23:06:46 GMT  
		Size: 11.5 MB (11480281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a31d56e532ff265b275aae709861e82df693b3c0e28e467fbd828aee0eb0d88`  
		Last Modified: Mon, 11 May 2026 23:06:46 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54b8df16388dbc099806c1c1818c3a2bde146ee08ff812e31237dd89b42b910`  
		Last Modified: Mon, 11 May 2026 23:06:46 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b97561ea1445f287f13425e0d8c6cc555dda4521823c070aee98a51e1ca95aa`  
		Last Modified: Mon, 11 May 2026 23:06:47 GMT  
		Size: 6.5 KB (6492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.9-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:93902ca0265dee33a0a0ecae116ee8a0737de7a4b93bba1f8cadd54423063670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **981.4 KB (981356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ec019bd514eb7e1cda009f18e83ee9eb4242bf44eccda3b8f5330ee187a1a0`

```dockerfile
```

-	Layers:
	-	`sha256:b6b9ccdbf33b901df2b0084d3c64070e298e28ab046116b504914e56b831cb5d`  
		Last Modified: Mon, 11 May 2026 23:06:44 GMT  
		Size: 950.6 KB (950553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79b372300ad917b42bbf5b0f86f143b26dbe1d2b21c384a53e3a0fd0c0c2b4c6`  
		Last Modified: Mon, 11 May 2026 23:06:44 GMT  
		Size: 30.8 KB (30803 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.9.1`

```console
$ docker pull influxdb@sha256:044d60447880093b9837d5de56ea0699b0db79a3e48fb94edf0f9e0eb9f4b95c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.9.1` - linux; amd64

```console
$ docker pull influxdb@sha256:82cd8aa54e7a82a3a006af30e3a31488b73a24f664677ba63782a9343302f1bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.8 MB (110800813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:373cd1bc99e1a9c96598fe115410634b5c8730eb6745f041f9203f1b3291ec8f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Mon, 11 May 2026 23:06:14 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg       util-linux &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:06:14 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Mon, 11 May 2026 23:06:14 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Mon, 11 May 2026 23:06:18 GMT
ENV INFLUXDB_VERSION=2.9.1
# Mon, 11 May 2026 23:06:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 11 May 2026 23:06:18 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Mon, 11 May 2026 23:06:20 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 11 May 2026 23:06:20 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 11 May 2026 23:06:20 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 11 May 2026 23:06:20 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 11 May 2026 23:06:20 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 11 May 2026 23:06:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 May 2026 23:06:20 GMT
CMD ["influxd"]
# Mon, 11 May 2026 23:06:20 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 11 May 2026 23:06:20 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 11 May 2026 23:06:20 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 11 May 2026 23:06:20 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 11 May 2026 23:06:20 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6306d75e2dc4ba2680cb2722b624ffd58658aea8bd7eb42637befbd5f956dc64`  
		Last Modified: Mon, 11 May 2026 23:06:33 GMT  
		Size: 9.8 MB (9799055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a82281c39f9f067b4235800d0e007670159c80542159a4450563d989fcb6563`  
		Last Modified: Mon, 11 May 2026 23:06:33 GMT  
		Size: 3.8 MB (3822784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a116ed37df3620df292451a9d9a04e82e56d60335cf27224a67219ed22cc038`  
		Last Modified: Mon, 11 May 2026 23:06:33 GMT  
		Size: 3.2 KB (3235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af303914f43bdf518bb8cfc5c3c8f4ce2f6e39e7424c012c140aca8689925373`  
		Last Modified: Mon, 11 May 2026 23:06:34 GMT  
		Size: 56.5 MB (56510687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080fd8044aff2f969b124bf1847f066b663e5b2f6cae5eb4a2fe39fd84b9ca8a`  
		Last Modified: Mon, 11 May 2026 23:06:34 GMT  
		Size: 12.4 MB (12421826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c8bdb93dd525adb082fe977c42446a606867cb0876486414590f483bdb16e5`  
		Last Modified: Mon, 11 May 2026 23:06:34 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec61169a51e436a25adf019845e2b06c2a2f667604bdaa2f3ce7d6c242b7e2d3`  
		Last Modified: Mon, 11 May 2026 23:06:35 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c8475bae289926b70499ba7275b48cf710950a5c1745f1047e5cea27687ae7`  
		Last Modified: Mon, 11 May 2026 23:06:35 GMT  
		Size: 6.5 KB (6500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.9.1` - unknown; unknown

```console
$ docker pull influxdb@sha256:3b4cdef18045a438e84e562f34e5593ba983944ada9400c448b23087fef4b9a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2988025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c263006991641cd34e84386b46b2189a3f22c0342ad8433ea93de78b3c101a59`

```dockerfile
```

-	Layers:
	-	`sha256:1eaa89e6c29ca38c8ea88162e378052dd323f1b5ccec9fbe77da9e5df39808c7`  
		Last Modified: Mon, 11 May 2026 23:06:33 GMT  
		Size: 3.0 MB (2959411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4126e96a3d9f757323087f196a105f67cb780972bf33fd5a38e7808989145600`  
		Last Modified: Mon, 11 May 2026 23:06:32 GMT  
		Size: 28.6 KB (28614 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.9.1` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:3bce906f5cd366a1d7f1386e355e51c87c6192fcc4d71c68a2edd3297a0192df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106330754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53cf7d95c5904cc95a6940f0d1154b73162e38d225ef133b2450a48ca219c096`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Mon, 11 May 2026 23:06:05 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg       util-linux &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:06:05 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Mon, 11 May 2026 23:06:05 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Mon, 11 May 2026 23:06:09 GMT
ENV INFLUXDB_VERSION=2.9.1
# Mon, 11 May 2026 23:06:09 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 11 May 2026 23:06:09 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Mon, 11 May 2026 23:06:11 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 11 May 2026 23:06:11 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 11 May 2026 23:06:11 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 11 May 2026 23:06:11 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 11 May 2026 23:06:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 11 May 2026 23:06:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 May 2026 23:06:11 GMT
CMD ["influxd"]
# Mon, 11 May 2026 23:06:11 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 11 May 2026 23:06:11 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 11 May 2026 23:06:11 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 11 May 2026 23:06:11 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 11 May 2026 23:06:11 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f23bbe568e43c569b84c86a9c06acb37a65383eef9d7a41c3493f2fc439b23`  
		Last Modified: Mon, 11 May 2026 23:06:23 GMT  
		Size: 9.6 MB (9628121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf21f16acbfdf9cb08e177f4e24e660aef286d9b0246883ca9ccac7f3423ef5`  
		Last Modified: Mon, 11 May 2026 23:06:23 GMT  
		Size: 3.5 MB (3459172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7651cdf91299714e33bee7297dbf293d680c2046377416bbec761092b53fbff`  
		Last Modified: Mon, 11 May 2026 23:06:23 GMT  
		Size: 3.2 KB (3233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93251acc80816de10b80ad59732e2112e724a1d77bc28e4943715d5a298725e`  
		Last Modified: Mon, 11 May 2026 23:06:25 GMT  
		Size: 53.6 MB (53636817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb61f007cdfb2efe51d7353b061d5dc88228555a0565832e7f4798bcf9c4bc05`  
		Last Modified: Mon, 11 May 2026 23:06:25 GMT  
		Size: 11.5 MB (11480302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d795a7febcb13431d839fb4382b6e22f5debf58e787deaeb34da45464289ba10`  
		Last Modified: Mon, 11 May 2026 23:06:25 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e57e263f59e437119c3be99d4d6e7ef67e658750db5b34f3c5307bb8d3d583`  
		Last Modified: Mon, 11 May 2026 23:06:25 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f0fde88bd7e8e0fef0640c7e8be480e6b382f511e2da3d9129a50466da3d55`  
		Last Modified: Mon, 11 May 2026 23:06:26 GMT  
		Size: 6.5 KB (6500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.9.1` - unknown; unknown

```console
$ docker pull influxdb@sha256:eb708288bfdc461e6c7c5c7346d5a1d11ba930ebf51cd162c10e023a7e3b89cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed727a90b15a758f20fe1ecb27f8186e0638b8cd670f3eb6052b11f07a9dde9c`

```dockerfile
```

-	Layers:
	-	`sha256:64fc4525aa7a436f50908c48554e8f5bd8b3b56e903570d96d434ea2183135f7`  
		Last Modified: Mon, 11 May 2026 23:06:23 GMT  
		Size: 3.0 MB (2958889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c1611d06ea9793b05207e6377419833d4f183dd192845527a8be765b2d3d5e9`  
		Last Modified: Mon, 11 May 2026 23:06:23 GMT  
		Size: 28.8 KB (28793 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.9.1-alpine`

```console
$ docker pull influxdb@sha256:1cb8fa92ff9d13518d8198dae872b7ea523757a03c655d12a67175b1ab7a72f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.9.1-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:99e216544ab6f8f8d4180d06bcc8deb61a676971c63e31faae24fc169945c4d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86902190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:343b7e7e34cb3b0c8e6c7a44f74f147f01f7ab4022ad1aa3c99ee43701d261f0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 11 May 2026 23:06:21 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 11 May 2026 23:06:23 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       setpriv       tzdata &&     update-ca-certificates # buildkit
# Mon, 11 May 2026 23:06:23 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Mon, 11 May 2026 23:06:23 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Mon, 11 May 2026 23:06:26 GMT
ENV INFLUXDB_VERSION=2.9.1
# Mon, 11 May 2026 23:06:26 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 11 May 2026 23:06:26 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Mon, 11 May 2026 23:06:27 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 11 May 2026 23:06:27 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 11 May 2026 23:06:27 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 11 May 2026 23:06:27 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 11 May 2026 23:06:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 11 May 2026 23:06:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 May 2026 23:06:27 GMT
CMD ["influxd"]
# Mon, 11 May 2026 23:06:27 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 11 May 2026 23:06:27 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 11 May 2026 23:06:27 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 11 May 2026 23:06:27 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 11 May 2026 23:06:27 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298fb8d3d07e69a02cd49af0883ae79a93c4625bc43501293daf0d954698afb5`  
		Last Modified: Mon, 11 May 2026 23:06:38 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896207ace1714281476706f02a38f5bafa2e8b0d466910e59c4abe1f0ef217a3`  
		Last Modified: Mon, 11 May 2026 23:06:38 GMT  
		Size: 10.3 MB (10274619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2fcd4f5629f0c11692de5d63652eda9a1de734dedd342a70ef1a8c1915d6e3`  
		Last Modified: Mon, 11 May 2026 23:06:38 GMT  
		Size: 3.8 MB (3822787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7399422b7a7b047fd9f9ae6a7b1b3c379169c0320d8c89787c7e57e378c95d46`  
		Last Modified: Mon, 11 May 2026 23:06:38 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a421d960302e6e78e3497cecdfbf7e68f9f87afb9c264f7efd238f037129c2`  
		Last Modified: Mon, 11 May 2026 23:06:41 GMT  
		Size: 56.5 MB (56510610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af09c2df41ffda41b4df2fd992fb0be316e613c2f08ecac1733e26e530fd6fb`  
		Last Modified: Mon, 11 May 2026 23:06:40 GMT  
		Size: 12.4 MB (12421822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141bbaa5308a2f1112e696cb9e82bc575508bf3fdba5b192f4c5017ed1ff0345`  
		Last Modified: Mon, 11 May 2026 23:06:40 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8db14735975847fbcb27a366734a994b19e81b52f37258eb95514dd7f2e7403`  
		Last Modified: Mon, 11 May 2026 23:06:41 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e66dbce9517e43a94af04ed7171b8a8c4174f59aeedd523604e88ced95a82de`  
		Last Modified: Mon, 11 May 2026 23:06:41 GMT  
		Size: 6.5 KB (6493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.9.1-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:45ebd475ac2880a68c21896d4cb1186238df70770b3318fdfcc83ac0f437a337
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **982.6 KB (982563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d587a6c839e8fdba54a6798485c7788dea62d5dc23bb982ddb676468b555f2e2`

```dockerfile
```

-	Layers:
	-	`sha256:00fb4b7e94546950e1d396936b5d2b235f6b34d79341a38bea451349ae4e71ad`  
		Last Modified: Mon, 11 May 2026 23:06:38 GMT  
		Size: 952.0 KB (951954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87c7670b411083afd6e9eee2031e773c5f9c80d7684afade5ae50a6602f99766`  
		Last Modified: Mon, 11 May 2026 23:06:38 GMT  
		Size: 30.6 KB (30609 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.9.1-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:02a1ea25d55126eb4d17a75d949f6939f995ee716a38d5cf87dacbfcbc43b5f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.0 MB (83028837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc4487542a8db6296883e5107322a4eeb7ac2f72cf6251e1b284eb9f8ba30ad0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 11 May 2026 23:06:28 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 11 May 2026 23:06:29 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       setpriv       tzdata &&     update-ca-certificates # buildkit
# Mon, 11 May 2026 23:06:30 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Mon, 11 May 2026 23:06:30 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Mon, 11 May 2026 23:06:32 GMT
ENV INFLUXDB_VERSION=2.9.1
# Mon, 11 May 2026 23:06:32 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 11 May 2026 23:06:32 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Mon, 11 May 2026 23:06:33 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 11 May 2026 23:06:33 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 11 May 2026 23:06:33 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 11 May 2026 23:06:33 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 11 May 2026 23:06:33 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 11 May 2026 23:06:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 May 2026 23:06:33 GMT
CMD ["influxd"]
# Mon, 11 May 2026 23:06:33 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 11 May 2026 23:06:33 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 11 May 2026 23:06:33 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 11 May 2026 23:06:33 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 11 May 2026 23:06:33 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4647b3db14cecf9d1d3425f0c3d71e29d76706a4ba687c996add84a9e46d7ac`  
		Last Modified: Mon, 11 May 2026 23:06:44 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fff389d9cde97293c698f3913f18598979f35d0502a8e50385bda21328b81c4`  
		Last Modified: Mon, 11 May 2026 23:06:44 GMT  
		Size: 10.2 MB (10244532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b6866a06fadef09561556d16e7b2b3e0279d4ca952ac2e3675803c00008dbc`  
		Last Modified: Mon, 11 May 2026 23:06:44 GMT  
		Size: 3.5 MB (3459165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9f34a583141b546c821a5ff21181240e09fa803803fe707d8da1b354084a33`  
		Last Modified: Mon, 11 May 2026 23:06:44 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a88da843f8eafbaedc72d393269a63b69eba46cd5780a319eee812b3428b8cc`  
		Last Modified: Mon, 11 May 2026 23:06:47 GMT  
		Size: 53.6 MB (53636820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd2e861c1ced42fa6d0ba182a983a7cf3b6d02f861f36efcfbe429b15544c4b`  
		Last Modified: Mon, 11 May 2026 23:06:46 GMT  
		Size: 11.5 MB (11480281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a31d56e532ff265b275aae709861e82df693b3c0e28e467fbd828aee0eb0d88`  
		Last Modified: Mon, 11 May 2026 23:06:46 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54b8df16388dbc099806c1c1818c3a2bde146ee08ff812e31237dd89b42b910`  
		Last Modified: Mon, 11 May 2026 23:06:46 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b97561ea1445f287f13425e0d8c6cc555dda4521823c070aee98a51e1ca95aa`  
		Last Modified: Mon, 11 May 2026 23:06:47 GMT  
		Size: 6.5 KB (6492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.9.1-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:93902ca0265dee33a0a0ecae116ee8a0737de7a4b93bba1f8cadd54423063670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **981.4 KB (981356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ec019bd514eb7e1cda009f18e83ee9eb4242bf44eccda3b8f5330ee187a1a0`

```dockerfile
```

-	Layers:
	-	`sha256:b6b9ccdbf33b901df2b0084d3c64070e298e28ab046116b504914e56b831cb5d`  
		Last Modified: Mon, 11 May 2026 23:06:44 GMT  
		Size: 950.6 KB (950553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79b372300ad917b42bbf5b0f86f143b26dbe1d2b21c384a53e3a0fd0c0c2b4c6`  
		Last Modified: Mon, 11 May 2026 23:06:44 GMT  
		Size: 30.8 KB (30803 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3-core`

```console
$ docker pull influxdb@sha256:31ad94df2248134989b2cf73d965e51dd5f35dfae22d7ed8f4776b12e6f69f4e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-core` - linux; amd64

```console
$ docker pull influxdb@sha256:2a33df848aa7e3110aa16d53642e9a0049413bc3549800aa30f3524a4cf6604d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149127978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30799fe936a4c3feda6e44ed98270c5f1eb40430c1a340a6675165c646941f58`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 19:30:14 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Mon, 04 May 2026 19:30:14 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Mon, 04 May 2026 19:30:19 GMT
ENV INFLUXDB_VERSION=3.9.2
# Mon, 04 May 2026 19:30:19 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Mon, 04 May 2026 19:30:19 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Mon, 04 May 2026 19:30:19 GMT
USER influxdb3
# Mon, 04 May 2026 19:30:19 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Mon, 04 May 2026 19:30:19 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Mon, 04 May 2026 19:30:19 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Mon, 04 May 2026 19:30:19 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Mon, 04 May 2026 19:30:19 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Mon, 04 May 2026 19:30:19 GMT
ENV LOG_FILTER=info
# Mon, 04 May 2026 19:30:19 GMT
EXPOSE map[8181/tcp:{}]
# Mon, 04 May 2026 19:30:19 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Mon, 04 May 2026 19:30:19 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0150fdeaff076406fcb3a0c4aa18adf46fb2fbb198e2232890493f8fee6c0bd`  
		Last Modified: Mon, 04 May 2026 19:30:37 GMT  
		Size: 6.7 MB (6672455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d0a189ea13679d8de8790c8207bb78913300cef22bf6c22dca410a226b9f08`  
		Last Modified: Mon, 04 May 2026 19:30:37 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fdd7d5e6bee01c1e036187795eda83e4de4724db84c3313152063861e927cb`  
		Last Modified: Mon, 04 May 2026 19:30:40 GMT  
		Size: 112.7 MB (112718222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43ebd3cb97923e17f7d330643a76d1b460fe10f7b30af7d2d3c1750cc672975`  
		Last Modified: Mon, 04 May 2026 19:30:37 GMT  
		Size: 519.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede128c13a48993b91017a4040191e412a2b84a1b360f498d6f494a36df1ba2b`  
		Last Modified: Mon, 04 May 2026 19:30:38 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:49664c981cea3b12231c6dcf35f5b9ea94fcade463b25febf6a944359da3a564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de9630edcca1790e79f0afb1d5e18a21fee2f33172c92521ed5cce8c3a110dd`

```dockerfile
```

-	Layers:
	-	`sha256:f55f07cbe1ba319f4fb641561ce3b8c04caaf4e83764e4ca7f9032b649920b88`  
		Last Modified: Mon, 04 May 2026 19:30:37 GMT  
		Size: 2.3 MB (2310597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09dbe94fe189d04cc2285f2ccff91d7f69338f6afbd7f000e681371e6532bd87`  
		Last Modified: Mon, 04 May 2026 19:30:37 GMT  
		Size: 17.6 KB (17620 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:52d9872ab1e55a055dd3f7b5268f5c6c2b029cb8b68f858c23f0aad0b79831a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140106553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19979a9a1a5887ca0db7a0955919bfef6d9fa32db9c94087e5f504fb83d5af85`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 19:24:42 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Mon, 04 May 2026 19:24:42 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Mon, 04 May 2026 19:24:47 GMT
ENV INFLUXDB_VERSION=3.9.2
# Mon, 04 May 2026 19:24:47 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Mon, 04 May 2026 19:24:47 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Mon, 04 May 2026 19:24:47 GMT
USER influxdb3
# Mon, 04 May 2026 19:24:47 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Mon, 04 May 2026 19:24:47 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Mon, 04 May 2026 19:24:47 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Mon, 04 May 2026 19:24:47 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Mon, 04 May 2026 19:24:47 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Mon, 04 May 2026 19:24:47 GMT
ENV LOG_FILTER=info
# Mon, 04 May 2026 19:24:47 GMT
EXPOSE map[8181/tcp:{}]
# Mon, 04 May 2026 19:24:47 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Mon, 04 May 2026 19:24:47 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86122c5ae2f33c5829b37b51c97108e5d0affc9a8df38a2520c2547957be231`  
		Last Modified: Mon, 04 May 2026 19:25:04 GMT  
		Size: 6.7 MB (6682327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9912325bdc1215b07db51f9c07ae6e8820f419585f5b9887242a1fe13c7613d6`  
		Last Modified: Mon, 04 May 2026 19:25:03 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b125a45984c5269b6fa91084249fabb15107023aa0b6b970da45b12c244f228`  
		Last Modified: Mon, 04 May 2026 19:25:06 GMT  
		Size: 104.5 MB (104544117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8864d3ce3dc01bc91806893665a5b7fc0a8b446a18b11dab323970528b26f0c`  
		Last Modified: Mon, 04 May 2026 19:25:03 GMT  
		Size: 521.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba1d612389a4091467addf28fb0d3c3d2403a29bb18848dd001ec6e3e032fb9`  
		Last Modified: Mon, 04 May 2026 19:25:04 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:a18ae06ad6d18c7f881a4b49c8d07d0cb3230600e42b332e69f8de458933da8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e147252f5eea6b419a730b9f59f8f268481a1395aa6b563d14563c918a6d5f8b`

```dockerfile
```

-	Layers:
	-	`sha256:f5e73fadd1e444f21baa13cf65d30006e79055f47e5fdee04f18b8c6941a04a3`  
		Last Modified: Mon, 04 May 2026 19:25:04 GMT  
		Size: 2.3 MB (2311679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9efa154e53131da2dc68d5b78f59fc7828711e79ff576b57b71b56c777b161c`  
		Last Modified: Mon, 04 May 2026 19:25:03 GMT  
		Size: 17.8 KB (17768 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3-enterprise`

```console
$ docker pull influxdb@sha256:358c82dce3772e483184ec1acd6b3571819996264a0c6cffcd2398371d6147f2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:6d4a1152a25f15c7c0f79509879af7b8e6e6c4ead39701f8b861e6f319469a7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.9 MB (159913248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68aa326322ac34c5534cc776f18b712958bbeb3ad2965bc0b97734e41241d920`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 19:32:39 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Mon, 04 May 2026 19:32:39 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Mon, 04 May 2026 19:32:45 GMT
ENV INFLUXDB_VERSION=3.9.2
# Mon, 04 May 2026 19:32:45 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Mon, 04 May 2026 19:32:45 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Mon, 04 May 2026 19:32:45 GMT
USER influxdb3
# Mon, 04 May 2026 19:32:45 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Mon, 04 May 2026 19:32:45 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Mon, 04 May 2026 19:32:45 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Mon, 04 May 2026 19:32:45 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Mon, 04 May 2026 19:32:45 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Mon, 04 May 2026 19:32:45 GMT
ENV LOG_FILTER=info
# Mon, 04 May 2026 19:32:45 GMT
EXPOSE map[8181/tcp:{}]
# Mon, 04 May 2026 19:32:45 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Mon, 04 May 2026 19:32:45 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35d8f1f66ee449437f42b2c20cc6370539b21981f7fe4b600041b02873f30cd`  
		Last Modified: Mon, 04 May 2026 19:33:05 GMT  
		Size: 6.7 MB (6672522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5269437d2b975134ce7f74a1f7939103033cf78c221de1bc63baaa714e82645`  
		Last Modified: Mon, 04 May 2026 19:33:05 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c75ef02653df55bbae0bc226f10bfa24eed141084f7cb5cbdab3cd7d0e5813`  
		Last Modified: Mon, 04 May 2026 19:33:08 GMT  
		Size: 123.5 MB (123503421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b421193e1bc6d530da0ca9c62059309564df29ef793eacb9921153d6478bbac`  
		Last Modified: Mon, 04 May 2026 19:33:05 GMT  
		Size: 523.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14bb906d01a393178b6d80cdee8f560c5aac7db2c8045f2f0931dcb04ada0bf8`  
		Last Modified: Mon, 04 May 2026 19:33:06 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:a3b3021ed521d9f9d53e3a7eb742cec3e30c6226c942b1ffa7a5401749c7b870
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1460a0fd76dfcb9bc844b4be1121a59d3da09daac7c44b7cd4ac79beca4bbfd9`

```dockerfile
```

-	Layers:
	-	`sha256:bfbfbdf1abe1a2935c1f66e68c46f03b7a53310be04982b56e1de99c1cb050fe`  
		Last Modified: Mon, 04 May 2026 19:33:05 GMT  
		Size: 2.3 MB (2310645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce512bf114d10d645b772ed385e73462aa7f8c89560aa2f169ea851461a323ed`  
		Last Modified: Mon, 04 May 2026 19:33:05 GMT  
		Size: 17.8 KB (17800 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:3750f19aa7e14906adc446335d9a9ab7f132d3e89497255f64d2834c4cb9aca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.7 MB (150709333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac4e26b527de2a11705829ca2661397204d09e368b0ad02369fad7d5994fb780`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 19:25:22 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Mon, 04 May 2026 19:25:22 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Mon, 04 May 2026 19:25:28 GMT
ENV INFLUXDB_VERSION=3.9.2
# Mon, 04 May 2026 19:25:28 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Mon, 04 May 2026 19:25:28 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Mon, 04 May 2026 19:25:28 GMT
USER influxdb3
# Mon, 04 May 2026 19:25:28 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Mon, 04 May 2026 19:25:28 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Mon, 04 May 2026 19:25:28 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Mon, 04 May 2026 19:25:28 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Mon, 04 May 2026 19:25:28 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Mon, 04 May 2026 19:25:28 GMT
ENV LOG_FILTER=info
# Mon, 04 May 2026 19:25:28 GMT
EXPOSE map[8181/tcp:{}]
# Mon, 04 May 2026 19:25:28 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Mon, 04 May 2026 19:25:28 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9e93e4bc5af617de342495cefd816d6ea3b1e47a9d0525d6bba17800dfe6f1`  
		Last Modified: Mon, 04 May 2026 19:25:45 GMT  
		Size: 6.7 MB (6682319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55d6c43df9d1b0b687412810604131e85819992a314de97d358a54dc0de899e`  
		Last Modified: Mon, 04 May 2026 19:25:45 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feba211f9bf3663dc5a64e9aaf491c8d04501281015e7d261176d09c3fc3280d`  
		Last Modified: Mon, 04 May 2026 19:25:48 GMT  
		Size: 115.1 MB (115146903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b31f11ffdb15964895b1830588c2ca47aa1c740f4ac77aa6d2142f20542543`  
		Last Modified: Mon, 04 May 2026 19:25:45 GMT  
		Size: 520.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baaf4d5e1f4596459dbbee4d8d09205c6de08fd9fc6626aa4b7c9971bca2db77`  
		Last Modified: Mon, 04 May 2026 19:25:46 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:b9f8d5b54641ebef9a6aecaca1c2c676181dd5902fe213001d42e5ea6d9c7fdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87996fd97d3a29be0e191bff3ed856e2c59ec34976e1cef9b82b3463e29f383e`

```dockerfile
```

-	Layers:
	-	`sha256:2d2e8117fb38299a365e12bebb3f57a26cc8c547bf2aa9bb4494ad539f1feafb`  
		Last Modified: Mon, 04 May 2026 19:25:45 GMT  
		Size: 2.3 MB (2311727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28fd98d7646d9de54953525aba2e5944a6ccd1eb921b35732bf39ca85139bca9`  
		Last Modified: Mon, 04 May 2026 19:25:45 GMT  
		Size: 17.9 KB (17947 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.9-core`

```console
$ docker pull influxdb@sha256:31ad94df2248134989b2cf73d965e51dd5f35dfae22d7ed8f4776b12e6f69f4e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.9-core` - linux; amd64

```console
$ docker pull influxdb@sha256:2a33df848aa7e3110aa16d53642e9a0049413bc3549800aa30f3524a4cf6604d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149127978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30799fe936a4c3feda6e44ed98270c5f1eb40430c1a340a6675165c646941f58`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 19:30:14 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Mon, 04 May 2026 19:30:14 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Mon, 04 May 2026 19:30:19 GMT
ENV INFLUXDB_VERSION=3.9.2
# Mon, 04 May 2026 19:30:19 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Mon, 04 May 2026 19:30:19 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Mon, 04 May 2026 19:30:19 GMT
USER influxdb3
# Mon, 04 May 2026 19:30:19 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Mon, 04 May 2026 19:30:19 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Mon, 04 May 2026 19:30:19 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Mon, 04 May 2026 19:30:19 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Mon, 04 May 2026 19:30:19 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Mon, 04 May 2026 19:30:19 GMT
ENV LOG_FILTER=info
# Mon, 04 May 2026 19:30:19 GMT
EXPOSE map[8181/tcp:{}]
# Mon, 04 May 2026 19:30:19 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Mon, 04 May 2026 19:30:19 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0150fdeaff076406fcb3a0c4aa18adf46fb2fbb198e2232890493f8fee6c0bd`  
		Last Modified: Mon, 04 May 2026 19:30:37 GMT  
		Size: 6.7 MB (6672455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d0a189ea13679d8de8790c8207bb78913300cef22bf6c22dca410a226b9f08`  
		Last Modified: Mon, 04 May 2026 19:30:37 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fdd7d5e6bee01c1e036187795eda83e4de4724db84c3313152063861e927cb`  
		Last Modified: Mon, 04 May 2026 19:30:40 GMT  
		Size: 112.7 MB (112718222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43ebd3cb97923e17f7d330643a76d1b460fe10f7b30af7d2d3c1750cc672975`  
		Last Modified: Mon, 04 May 2026 19:30:37 GMT  
		Size: 519.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede128c13a48993b91017a4040191e412a2b84a1b360f498d6f494a36df1ba2b`  
		Last Modified: Mon, 04 May 2026 19:30:38 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.9-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:49664c981cea3b12231c6dcf35f5b9ea94fcade463b25febf6a944359da3a564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de9630edcca1790e79f0afb1d5e18a21fee2f33172c92521ed5cce8c3a110dd`

```dockerfile
```

-	Layers:
	-	`sha256:f55f07cbe1ba319f4fb641561ce3b8c04caaf4e83764e4ca7f9032b649920b88`  
		Last Modified: Mon, 04 May 2026 19:30:37 GMT  
		Size: 2.3 MB (2310597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09dbe94fe189d04cc2285f2ccff91d7f69338f6afbd7f000e681371e6532bd87`  
		Last Modified: Mon, 04 May 2026 19:30:37 GMT  
		Size: 17.6 KB (17620 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.9-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:52d9872ab1e55a055dd3f7b5268f5c6c2b029cb8b68f858c23f0aad0b79831a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140106553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19979a9a1a5887ca0db7a0955919bfef6d9fa32db9c94087e5f504fb83d5af85`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 19:24:42 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Mon, 04 May 2026 19:24:42 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Mon, 04 May 2026 19:24:47 GMT
ENV INFLUXDB_VERSION=3.9.2
# Mon, 04 May 2026 19:24:47 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Mon, 04 May 2026 19:24:47 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Mon, 04 May 2026 19:24:47 GMT
USER influxdb3
# Mon, 04 May 2026 19:24:47 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Mon, 04 May 2026 19:24:47 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Mon, 04 May 2026 19:24:47 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Mon, 04 May 2026 19:24:47 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Mon, 04 May 2026 19:24:47 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Mon, 04 May 2026 19:24:47 GMT
ENV LOG_FILTER=info
# Mon, 04 May 2026 19:24:47 GMT
EXPOSE map[8181/tcp:{}]
# Mon, 04 May 2026 19:24:47 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Mon, 04 May 2026 19:24:47 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86122c5ae2f33c5829b37b51c97108e5d0affc9a8df38a2520c2547957be231`  
		Last Modified: Mon, 04 May 2026 19:25:04 GMT  
		Size: 6.7 MB (6682327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9912325bdc1215b07db51f9c07ae6e8820f419585f5b9887242a1fe13c7613d6`  
		Last Modified: Mon, 04 May 2026 19:25:03 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b125a45984c5269b6fa91084249fabb15107023aa0b6b970da45b12c244f228`  
		Last Modified: Mon, 04 May 2026 19:25:06 GMT  
		Size: 104.5 MB (104544117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8864d3ce3dc01bc91806893665a5b7fc0a8b446a18b11dab323970528b26f0c`  
		Last Modified: Mon, 04 May 2026 19:25:03 GMT  
		Size: 521.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba1d612389a4091467addf28fb0d3c3d2403a29bb18848dd001ec6e3e032fb9`  
		Last Modified: Mon, 04 May 2026 19:25:04 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.9-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:a18ae06ad6d18c7f881a4b49c8d07d0cb3230600e42b332e69f8de458933da8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e147252f5eea6b419a730b9f59f8f268481a1395aa6b563d14563c918a6d5f8b`

```dockerfile
```

-	Layers:
	-	`sha256:f5e73fadd1e444f21baa13cf65d30006e79055f47e5fdee04f18b8c6941a04a3`  
		Last Modified: Mon, 04 May 2026 19:25:04 GMT  
		Size: 2.3 MB (2311679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9efa154e53131da2dc68d5b78f59fc7828711e79ff576b57b71b56c777b161c`  
		Last Modified: Mon, 04 May 2026 19:25:03 GMT  
		Size: 17.8 KB (17768 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.9-enterprise`

```console
$ docker pull influxdb@sha256:358c82dce3772e483184ec1acd6b3571819996264a0c6cffcd2398371d6147f2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.9-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:6d4a1152a25f15c7c0f79509879af7b8e6e6c4ead39701f8b861e6f319469a7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.9 MB (159913248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68aa326322ac34c5534cc776f18b712958bbeb3ad2965bc0b97734e41241d920`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 19:32:39 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Mon, 04 May 2026 19:32:39 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Mon, 04 May 2026 19:32:45 GMT
ENV INFLUXDB_VERSION=3.9.2
# Mon, 04 May 2026 19:32:45 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Mon, 04 May 2026 19:32:45 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Mon, 04 May 2026 19:32:45 GMT
USER influxdb3
# Mon, 04 May 2026 19:32:45 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Mon, 04 May 2026 19:32:45 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Mon, 04 May 2026 19:32:45 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Mon, 04 May 2026 19:32:45 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Mon, 04 May 2026 19:32:45 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Mon, 04 May 2026 19:32:45 GMT
ENV LOG_FILTER=info
# Mon, 04 May 2026 19:32:45 GMT
EXPOSE map[8181/tcp:{}]
# Mon, 04 May 2026 19:32:45 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Mon, 04 May 2026 19:32:45 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35d8f1f66ee449437f42b2c20cc6370539b21981f7fe4b600041b02873f30cd`  
		Last Modified: Mon, 04 May 2026 19:33:05 GMT  
		Size: 6.7 MB (6672522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5269437d2b975134ce7f74a1f7939103033cf78c221de1bc63baaa714e82645`  
		Last Modified: Mon, 04 May 2026 19:33:05 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c75ef02653df55bbae0bc226f10bfa24eed141084f7cb5cbdab3cd7d0e5813`  
		Last Modified: Mon, 04 May 2026 19:33:08 GMT  
		Size: 123.5 MB (123503421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b421193e1bc6d530da0ca9c62059309564df29ef793eacb9921153d6478bbac`  
		Last Modified: Mon, 04 May 2026 19:33:05 GMT  
		Size: 523.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14bb906d01a393178b6d80cdee8f560c5aac7db2c8045f2f0931dcb04ada0bf8`  
		Last Modified: Mon, 04 May 2026 19:33:06 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.9-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:a3b3021ed521d9f9d53e3a7eb742cec3e30c6226c942b1ffa7a5401749c7b870
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1460a0fd76dfcb9bc844b4be1121a59d3da09daac7c44b7cd4ac79beca4bbfd9`

```dockerfile
```

-	Layers:
	-	`sha256:bfbfbdf1abe1a2935c1f66e68c46f03b7a53310be04982b56e1de99c1cb050fe`  
		Last Modified: Mon, 04 May 2026 19:33:05 GMT  
		Size: 2.3 MB (2310645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce512bf114d10d645b772ed385e73462aa7f8c89560aa2f169ea851461a323ed`  
		Last Modified: Mon, 04 May 2026 19:33:05 GMT  
		Size: 17.8 KB (17800 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.9-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:3750f19aa7e14906adc446335d9a9ab7f132d3e89497255f64d2834c4cb9aca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.7 MB (150709333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac4e26b527de2a11705829ca2661397204d09e368b0ad02369fad7d5994fb780`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 19:25:22 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Mon, 04 May 2026 19:25:22 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Mon, 04 May 2026 19:25:28 GMT
ENV INFLUXDB_VERSION=3.9.2
# Mon, 04 May 2026 19:25:28 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Mon, 04 May 2026 19:25:28 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Mon, 04 May 2026 19:25:28 GMT
USER influxdb3
# Mon, 04 May 2026 19:25:28 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Mon, 04 May 2026 19:25:28 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Mon, 04 May 2026 19:25:28 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Mon, 04 May 2026 19:25:28 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Mon, 04 May 2026 19:25:28 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Mon, 04 May 2026 19:25:28 GMT
ENV LOG_FILTER=info
# Mon, 04 May 2026 19:25:28 GMT
EXPOSE map[8181/tcp:{}]
# Mon, 04 May 2026 19:25:28 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Mon, 04 May 2026 19:25:28 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9e93e4bc5af617de342495cefd816d6ea3b1e47a9d0525d6bba17800dfe6f1`  
		Last Modified: Mon, 04 May 2026 19:25:45 GMT  
		Size: 6.7 MB (6682319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55d6c43df9d1b0b687412810604131e85819992a314de97d358a54dc0de899e`  
		Last Modified: Mon, 04 May 2026 19:25:45 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feba211f9bf3663dc5a64e9aaf491c8d04501281015e7d261176d09c3fc3280d`  
		Last Modified: Mon, 04 May 2026 19:25:48 GMT  
		Size: 115.1 MB (115146903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b31f11ffdb15964895b1830588c2ca47aa1c740f4ac77aa6d2142f20542543`  
		Last Modified: Mon, 04 May 2026 19:25:45 GMT  
		Size: 520.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baaf4d5e1f4596459dbbee4d8d09205c6de08fd9fc6626aa4b7c9971bca2db77`  
		Last Modified: Mon, 04 May 2026 19:25:46 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.9-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:b9f8d5b54641ebef9a6aecaca1c2c676181dd5902fe213001d42e5ea6d9c7fdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87996fd97d3a29be0e191bff3ed856e2c59ec34976e1cef9b82b3463e29f383e`

```dockerfile
```

-	Layers:
	-	`sha256:2d2e8117fb38299a365e12bebb3f57a26cc8c547bf2aa9bb4494ad539f1feafb`  
		Last Modified: Mon, 04 May 2026 19:25:45 GMT  
		Size: 2.3 MB (2311727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28fd98d7646d9de54953525aba2e5944a6ccd1eb921b35732bf39ca85139bca9`  
		Last Modified: Mon, 04 May 2026 19:25:45 GMT  
		Size: 17.9 KB (17947 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.9.2-core`

```console
$ docker pull influxdb@sha256:31ad94df2248134989b2cf73d965e51dd5f35dfae22d7ed8f4776b12e6f69f4e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.9.2-core` - linux; amd64

```console
$ docker pull influxdb@sha256:2a33df848aa7e3110aa16d53642e9a0049413bc3549800aa30f3524a4cf6604d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149127978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30799fe936a4c3feda6e44ed98270c5f1eb40430c1a340a6675165c646941f58`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 19:30:14 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Mon, 04 May 2026 19:30:14 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Mon, 04 May 2026 19:30:19 GMT
ENV INFLUXDB_VERSION=3.9.2
# Mon, 04 May 2026 19:30:19 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Mon, 04 May 2026 19:30:19 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Mon, 04 May 2026 19:30:19 GMT
USER influxdb3
# Mon, 04 May 2026 19:30:19 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Mon, 04 May 2026 19:30:19 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Mon, 04 May 2026 19:30:19 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Mon, 04 May 2026 19:30:19 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Mon, 04 May 2026 19:30:19 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Mon, 04 May 2026 19:30:19 GMT
ENV LOG_FILTER=info
# Mon, 04 May 2026 19:30:19 GMT
EXPOSE map[8181/tcp:{}]
# Mon, 04 May 2026 19:30:19 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Mon, 04 May 2026 19:30:19 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0150fdeaff076406fcb3a0c4aa18adf46fb2fbb198e2232890493f8fee6c0bd`  
		Last Modified: Mon, 04 May 2026 19:30:37 GMT  
		Size: 6.7 MB (6672455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d0a189ea13679d8de8790c8207bb78913300cef22bf6c22dca410a226b9f08`  
		Last Modified: Mon, 04 May 2026 19:30:37 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fdd7d5e6bee01c1e036187795eda83e4de4724db84c3313152063861e927cb`  
		Last Modified: Mon, 04 May 2026 19:30:40 GMT  
		Size: 112.7 MB (112718222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43ebd3cb97923e17f7d330643a76d1b460fe10f7b30af7d2d3c1750cc672975`  
		Last Modified: Mon, 04 May 2026 19:30:37 GMT  
		Size: 519.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede128c13a48993b91017a4040191e412a2b84a1b360f498d6f494a36df1ba2b`  
		Last Modified: Mon, 04 May 2026 19:30:38 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.9.2-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:49664c981cea3b12231c6dcf35f5b9ea94fcade463b25febf6a944359da3a564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de9630edcca1790e79f0afb1d5e18a21fee2f33172c92521ed5cce8c3a110dd`

```dockerfile
```

-	Layers:
	-	`sha256:f55f07cbe1ba319f4fb641561ce3b8c04caaf4e83764e4ca7f9032b649920b88`  
		Last Modified: Mon, 04 May 2026 19:30:37 GMT  
		Size: 2.3 MB (2310597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09dbe94fe189d04cc2285f2ccff91d7f69338f6afbd7f000e681371e6532bd87`  
		Last Modified: Mon, 04 May 2026 19:30:37 GMT  
		Size: 17.6 KB (17620 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.9.2-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:52d9872ab1e55a055dd3f7b5268f5c6c2b029cb8b68f858c23f0aad0b79831a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140106553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19979a9a1a5887ca0db7a0955919bfef6d9fa32db9c94087e5f504fb83d5af85`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 19:24:42 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Mon, 04 May 2026 19:24:42 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Mon, 04 May 2026 19:24:47 GMT
ENV INFLUXDB_VERSION=3.9.2
# Mon, 04 May 2026 19:24:47 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Mon, 04 May 2026 19:24:47 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Mon, 04 May 2026 19:24:47 GMT
USER influxdb3
# Mon, 04 May 2026 19:24:47 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Mon, 04 May 2026 19:24:47 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Mon, 04 May 2026 19:24:47 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Mon, 04 May 2026 19:24:47 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Mon, 04 May 2026 19:24:47 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Mon, 04 May 2026 19:24:47 GMT
ENV LOG_FILTER=info
# Mon, 04 May 2026 19:24:47 GMT
EXPOSE map[8181/tcp:{}]
# Mon, 04 May 2026 19:24:47 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Mon, 04 May 2026 19:24:47 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86122c5ae2f33c5829b37b51c97108e5d0affc9a8df38a2520c2547957be231`  
		Last Modified: Mon, 04 May 2026 19:25:04 GMT  
		Size: 6.7 MB (6682327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9912325bdc1215b07db51f9c07ae6e8820f419585f5b9887242a1fe13c7613d6`  
		Last Modified: Mon, 04 May 2026 19:25:03 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b125a45984c5269b6fa91084249fabb15107023aa0b6b970da45b12c244f228`  
		Last Modified: Mon, 04 May 2026 19:25:06 GMT  
		Size: 104.5 MB (104544117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8864d3ce3dc01bc91806893665a5b7fc0a8b446a18b11dab323970528b26f0c`  
		Last Modified: Mon, 04 May 2026 19:25:03 GMT  
		Size: 521.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba1d612389a4091467addf28fb0d3c3d2403a29bb18848dd001ec6e3e032fb9`  
		Last Modified: Mon, 04 May 2026 19:25:04 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.9.2-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:a18ae06ad6d18c7f881a4b49c8d07d0cb3230600e42b332e69f8de458933da8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e147252f5eea6b419a730b9f59f8f268481a1395aa6b563d14563c918a6d5f8b`

```dockerfile
```

-	Layers:
	-	`sha256:f5e73fadd1e444f21baa13cf65d30006e79055f47e5fdee04f18b8c6941a04a3`  
		Last Modified: Mon, 04 May 2026 19:25:04 GMT  
		Size: 2.3 MB (2311679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9efa154e53131da2dc68d5b78f59fc7828711e79ff576b57b71b56c777b161c`  
		Last Modified: Mon, 04 May 2026 19:25:03 GMT  
		Size: 17.8 KB (17768 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.9.2-enterprise`

```console
$ docker pull influxdb@sha256:358c82dce3772e483184ec1acd6b3571819996264a0c6cffcd2398371d6147f2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.9.2-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:6d4a1152a25f15c7c0f79509879af7b8e6e6c4ead39701f8b861e6f319469a7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.9 MB (159913248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68aa326322ac34c5534cc776f18b712958bbeb3ad2965bc0b97734e41241d920`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 19:32:39 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Mon, 04 May 2026 19:32:39 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Mon, 04 May 2026 19:32:45 GMT
ENV INFLUXDB_VERSION=3.9.2
# Mon, 04 May 2026 19:32:45 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Mon, 04 May 2026 19:32:45 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Mon, 04 May 2026 19:32:45 GMT
USER influxdb3
# Mon, 04 May 2026 19:32:45 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Mon, 04 May 2026 19:32:45 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Mon, 04 May 2026 19:32:45 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Mon, 04 May 2026 19:32:45 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Mon, 04 May 2026 19:32:45 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Mon, 04 May 2026 19:32:45 GMT
ENV LOG_FILTER=info
# Mon, 04 May 2026 19:32:45 GMT
EXPOSE map[8181/tcp:{}]
# Mon, 04 May 2026 19:32:45 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Mon, 04 May 2026 19:32:45 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35d8f1f66ee449437f42b2c20cc6370539b21981f7fe4b600041b02873f30cd`  
		Last Modified: Mon, 04 May 2026 19:33:05 GMT  
		Size: 6.7 MB (6672522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5269437d2b975134ce7f74a1f7939103033cf78c221de1bc63baaa714e82645`  
		Last Modified: Mon, 04 May 2026 19:33:05 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c75ef02653df55bbae0bc226f10bfa24eed141084f7cb5cbdab3cd7d0e5813`  
		Last Modified: Mon, 04 May 2026 19:33:08 GMT  
		Size: 123.5 MB (123503421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b421193e1bc6d530da0ca9c62059309564df29ef793eacb9921153d6478bbac`  
		Last Modified: Mon, 04 May 2026 19:33:05 GMT  
		Size: 523.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14bb906d01a393178b6d80cdee8f560c5aac7db2c8045f2f0931dcb04ada0bf8`  
		Last Modified: Mon, 04 May 2026 19:33:06 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.9.2-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:a3b3021ed521d9f9d53e3a7eb742cec3e30c6226c942b1ffa7a5401749c7b870
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1460a0fd76dfcb9bc844b4be1121a59d3da09daac7c44b7cd4ac79beca4bbfd9`

```dockerfile
```

-	Layers:
	-	`sha256:bfbfbdf1abe1a2935c1f66e68c46f03b7a53310be04982b56e1de99c1cb050fe`  
		Last Modified: Mon, 04 May 2026 19:33:05 GMT  
		Size: 2.3 MB (2310645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce512bf114d10d645b772ed385e73462aa7f8c89560aa2f169ea851461a323ed`  
		Last Modified: Mon, 04 May 2026 19:33:05 GMT  
		Size: 17.8 KB (17800 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.9.2-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:3750f19aa7e14906adc446335d9a9ab7f132d3e89497255f64d2834c4cb9aca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.7 MB (150709333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac4e26b527de2a11705829ca2661397204d09e368b0ad02369fad7d5994fb780`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 19:25:22 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Mon, 04 May 2026 19:25:22 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Mon, 04 May 2026 19:25:28 GMT
ENV INFLUXDB_VERSION=3.9.2
# Mon, 04 May 2026 19:25:28 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Mon, 04 May 2026 19:25:28 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Mon, 04 May 2026 19:25:28 GMT
USER influxdb3
# Mon, 04 May 2026 19:25:28 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Mon, 04 May 2026 19:25:28 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Mon, 04 May 2026 19:25:28 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Mon, 04 May 2026 19:25:28 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Mon, 04 May 2026 19:25:28 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Mon, 04 May 2026 19:25:28 GMT
ENV LOG_FILTER=info
# Mon, 04 May 2026 19:25:28 GMT
EXPOSE map[8181/tcp:{}]
# Mon, 04 May 2026 19:25:28 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Mon, 04 May 2026 19:25:28 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9e93e4bc5af617de342495cefd816d6ea3b1e47a9d0525d6bba17800dfe6f1`  
		Last Modified: Mon, 04 May 2026 19:25:45 GMT  
		Size: 6.7 MB (6682319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55d6c43df9d1b0b687412810604131e85819992a314de97d358a54dc0de899e`  
		Last Modified: Mon, 04 May 2026 19:25:45 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feba211f9bf3663dc5a64e9aaf491c8d04501281015e7d261176d09c3fc3280d`  
		Last Modified: Mon, 04 May 2026 19:25:48 GMT  
		Size: 115.1 MB (115146903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b31f11ffdb15964895b1830588c2ca47aa1c740f4ac77aa6d2142f20542543`  
		Last Modified: Mon, 04 May 2026 19:25:45 GMT  
		Size: 520.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baaf4d5e1f4596459dbbee4d8d09205c6de08fd9fc6626aa4b7c9971bca2db77`  
		Last Modified: Mon, 04 May 2026 19:25:46 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.9.2-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:b9f8d5b54641ebef9a6aecaca1c2c676181dd5902fe213001d42e5ea6d9c7fdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87996fd97d3a29be0e191bff3ed856e2c59ec34976e1cef9b82b3463e29f383e`

```dockerfile
```

-	Layers:
	-	`sha256:2d2e8117fb38299a365e12bebb3f57a26cc8c547bf2aa9bb4494ad539f1feafb`  
		Last Modified: Mon, 04 May 2026 19:25:45 GMT  
		Size: 2.3 MB (2311727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28fd98d7646d9de54953525aba2e5944a6ccd1eb921b35732bf39ca85139bca9`  
		Last Modified: Mon, 04 May 2026 19:25:45 GMT  
		Size: 17.9 KB (17947 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:1cb8fa92ff9d13518d8198dae872b7ea523757a03c655d12a67175b1ab7a72f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:99e216544ab6f8f8d4180d06bcc8deb61a676971c63e31faae24fc169945c4d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86902190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:343b7e7e34cb3b0c8e6c7a44f74f147f01f7ab4022ad1aa3c99ee43701d261f0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 11 May 2026 23:06:21 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 11 May 2026 23:06:23 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       setpriv       tzdata &&     update-ca-certificates # buildkit
# Mon, 11 May 2026 23:06:23 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Mon, 11 May 2026 23:06:23 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Mon, 11 May 2026 23:06:26 GMT
ENV INFLUXDB_VERSION=2.9.1
# Mon, 11 May 2026 23:06:26 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 11 May 2026 23:06:26 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Mon, 11 May 2026 23:06:27 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 11 May 2026 23:06:27 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 11 May 2026 23:06:27 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 11 May 2026 23:06:27 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 11 May 2026 23:06:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 11 May 2026 23:06:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 May 2026 23:06:27 GMT
CMD ["influxd"]
# Mon, 11 May 2026 23:06:27 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 11 May 2026 23:06:27 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 11 May 2026 23:06:27 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 11 May 2026 23:06:27 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 11 May 2026 23:06:27 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298fb8d3d07e69a02cd49af0883ae79a93c4625bc43501293daf0d954698afb5`  
		Last Modified: Mon, 11 May 2026 23:06:38 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896207ace1714281476706f02a38f5bafa2e8b0d466910e59c4abe1f0ef217a3`  
		Last Modified: Mon, 11 May 2026 23:06:38 GMT  
		Size: 10.3 MB (10274619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2fcd4f5629f0c11692de5d63652eda9a1de734dedd342a70ef1a8c1915d6e3`  
		Last Modified: Mon, 11 May 2026 23:06:38 GMT  
		Size: 3.8 MB (3822787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7399422b7a7b047fd9f9ae6a7b1b3c379169c0320d8c89787c7e57e378c95d46`  
		Last Modified: Mon, 11 May 2026 23:06:38 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a421d960302e6e78e3497cecdfbf7e68f9f87afb9c264f7efd238f037129c2`  
		Last Modified: Mon, 11 May 2026 23:06:41 GMT  
		Size: 56.5 MB (56510610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af09c2df41ffda41b4df2fd992fb0be316e613c2f08ecac1733e26e530fd6fb`  
		Last Modified: Mon, 11 May 2026 23:06:40 GMT  
		Size: 12.4 MB (12421822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141bbaa5308a2f1112e696cb9e82bc575508bf3fdba5b192f4c5017ed1ff0345`  
		Last Modified: Mon, 11 May 2026 23:06:40 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8db14735975847fbcb27a366734a994b19e81b52f37258eb95514dd7f2e7403`  
		Last Modified: Mon, 11 May 2026 23:06:41 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e66dbce9517e43a94af04ed7171b8a8c4174f59aeedd523604e88ced95a82de`  
		Last Modified: Mon, 11 May 2026 23:06:41 GMT  
		Size: 6.5 KB (6493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:45ebd475ac2880a68c21896d4cb1186238df70770b3318fdfcc83ac0f437a337
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **982.6 KB (982563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d587a6c839e8fdba54a6798485c7788dea62d5dc23bb982ddb676468b555f2e2`

```dockerfile
```

-	Layers:
	-	`sha256:00fb4b7e94546950e1d396936b5d2b235f6b34d79341a38bea451349ae4e71ad`  
		Last Modified: Mon, 11 May 2026 23:06:38 GMT  
		Size: 952.0 KB (951954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87c7670b411083afd6e9eee2031e773c5f9c80d7684afade5ae50a6602f99766`  
		Last Modified: Mon, 11 May 2026 23:06:38 GMT  
		Size: 30.6 KB (30609 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:02a1ea25d55126eb4d17a75d949f6939f995ee716a38d5cf87dacbfcbc43b5f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.0 MB (83028837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc4487542a8db6296883e5107322a4eeb7ac2f72cf6251e1b284eb9f8ba30ad0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 11 May 2026 23:06:28 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 11 May 2026 23:06:29 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       setpriv       tzdata &&     update-ca-certificates # buildkit
# Mon, 11 May 2026 23:06:30 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Mon, 11 May 2026 23:06:30 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Mon, 11 May 2026 23:06:32 GMT
ENV INFLUXDB_VERSION=2.9.1
# Mon, 11 May 2026 23:06:32 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 11 May 2026 23:06:32 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Mon, 11 May 2026 23:06:33 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 11 May 2026 23:06:33 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 11 May 2026 23:06:33 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 11 May 2026 23:06:33 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 11 May 2026 23:06:33 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 11 May 2026 23:06:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 May 2026 23:06:33 GMT
CMD ["influxd"]
# Mon, 11 May 2026 23:06:33 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 11 May 2026 23:06:33 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 11 May 2026 23:06:33 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 11 May 2026 23:06:33 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 11 May 2026 23:06:33 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4647b3db14cecf9d1d3425f0c3d71e29d76706a4ba687c996add84a9e46d7ac`  
		Last Modified: Mon, 11 May 2026 23:06:44 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fff389d9cde97293c698f3913f18598979f35d0502a8e50385bda21328b81c4`  
		Last Modified: Mon, 11 May 2026 23:06:44 GMT  
		Size: 10.2 MB (10244532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b6866a06fadef09561556d16e7b2b3e0279d4ca952ac2e3675803c00008dbc`  
		Last Modified: Mon, 11 May 2026 23:06:44 GMT  
		Size: 3.5 MB (3459165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9f34a583141b546c821a5ff21181240e09fa803803fe707d8da1b354084a33`  
		Last Modified: Mon, 11 May 2026 23:06:44 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a88da843f8eafbaedc72d393269a63b69eba46cd5780a319eee812b3428b8cc`  
		Last Modified: Mon, 11 May 2026 23:06:47 GMT  
		Size: 53.6 MB (53636820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd2e861c1ced42fa6d0ba182a983a7cf3b6d02f861f36efcfbe429b15544c4b`  
		Last Modified: Mon, 11 May 2026 23:06:46 GMT  
		Size: 11.5 MB (11480281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a31d56e532ff265b275aae709861e82df693b3c0e28e467fbd828aee0eb0d88`  
		Last Modified: Mon, 11 May 2026 23:06:46 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54b8df16388dbc099806c1c1818c3a2bde146ee08ff812e31237dd89b42b910`  
		Last Modified: Mon, 11 May 2026 23:06:46 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b97561ea1445f287f13425e0d8c6cc555dda4521823c070aee98a51e1ca95aa`  
		Last Modified: Mon, 11 May 2026 23:06:47 GMT  
		Size: 6.5 KB (6492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:93902ca0265dee33a0a0ecae116ee8a0737de7a4b93bba1f8cadd54423063670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **981.4 KB (981356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ec019bd514eb7e1cda009f18e83ee9eb4242bf44eccda3b8f5330ee187a1a0`

```dockerfile
```

-	Layers:
	-	`sha256:b6b9ccdbf33b901df2b0084d3c64070e298e28ab046116b504914e56b831cb5d`  
		Last Modified: Mon, 11 May 2026 23:06:44 GMT  
		Size: 950.6 KB (950553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79b372300ad917b42bbf5b0f86f143b26dbe1d2b21c384a53e3a0fd0c0c2b4c6`  
		Last Modified: Mon, 11 May 2026 23:06:44 GMT  
		Size: 30.8 KB (30803 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:core`

```console
$ docker pull influxdb@sha256:31ad94df2248134989b2cf73d965e51dd5f35dfae22d7ed8f4776b12e6f69f4e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:core` - linux; amd64

```console
$ docker pull influxdb@sha256:2a33df848aa7e3110aa16d53642e9a0049413bc3549800aa30f3524a4cf6604d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149127978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30799fe936a4c3feda6e44ed98270c5f1eb40430c1a340a6675165c646941f58`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 19:30:14 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Mon, 04 May 2026 19:30:14 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Mon, 04 May 2026 19:30:19 GMT
ENV INFLUXDB_VERSION=3.9.2
# Mon, 04 May 2026 19:30:19 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Mon, 04 May 2026 19:30:19 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Mon, 04 May 2026 19:30:19 GMT
USER influxdb3
# Mon, 04 May 2026 19:30:19 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Mon, 04 May 2026 19:30:19 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Mon, 04 May 2026 19:30:19 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Mon, 04 May 2026 19:30:19 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Mon, 04 May 2026 19:30:19 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Mon, 04 May 2026 19:30:19 GMT
ENV LOG_FILTER=info
# Mon, 04 May 2026 19:30:19 GMT
EXPOSE map[8181/tcp:{}]
# Mon, 04 May 2026 19:30:19 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Mon, 04 May 2026 19:30:19 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0150fdeaff076406fcb3a0c4aa18adf46fb2fbb198e2232890493f8fee6c0bd`  
		Last Modified: Mon, 04 May 2026 19:30:37 GMT  
		Size: 6.7 MB (6672455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d0a189ea13679d8de8790c8207bb78913300cef22bf6c22dca410a226b9f08`  
		Last Modified: Mon, 04 May 2026 19:30:37 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fdd7d5e6bee01c1e036187795eda83e4de4724db84c3313152063861e927cb`  
		Last Modified: Mon, 04 May 2026 19:30:40 GMT  
		Size: 112.7 MB (112718222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43ebd3cb97923e17f7d330643a76d1b460fe10f7b30af7d2d3c1750cc672975`  
		Last Modified: Mon, 04 May 2026 19:30:37 GMT  
		Size: 519.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede128c13a48993b91017a4040191e412a2b84a1b360f498d6f494a36df1ba2b`  
		Last Modified: Mon, 04 May 2026 19:30:38 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:49664c981cea3b12231c6dcf35f5b9ea94fcade463b25febf6a944359da3a564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de9630edcca1790e79f0afb1d5e18a21fee2f33172c92521ed5cce8c3a110dd`

```dockerfile
```

-	Layers:
	-	`sha256:f55f07cbe1ba319f4fb641561ce3b8c04caaf4e83764e4ca7f9032b649920b88`  
		Last Modified: Mon, 04 May 2026 19:30:37 GMT  
		Size: 2.3 MB (2310597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09dbe94fe189d04cc2285f2ccff91d7f69338f6afbd7f000e681371e6532bd87`  
		Last Modified: Mon, 04 May 2026 19:30:37 GMT  
		Size: 17.6 KB (17620 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:52d9872ab1e55a055dd3f7b5268f5c6c2b029cb8b68f858c23f0aad0b79831a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140106553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19979a9a1a5887ca0db7a0955919bfef6d9fa32db9c94087e5f504fb83d5af85`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 19:24:42 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Mon, 04 May 2026 19:24:42 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Mon, 04 May 2026 19:24:47 GMT
ENV INFLUXDB_VERSION=3.9.2
# Mon, 04 May 2026 19:24:47 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Mon, 04 May 2026 19:24:47 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Mon, 04 May 2026 19:24:47 GMT
USER influxdb3
# Mon, 04 May 2026 19:24:47 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Mon, 04 May 2026 19:24:47 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Mon, 04 May 2026 19:24:47 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Mon, 04 May 2026 19:24:47 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Mon, 04 May 2026 19:24:47 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Mon, 04 May 2026 19:24:47 GMT
ENV LOG_FILTER=info
# Mon, 04 May 2026 19:24:47 GMT
EXPOSE map[8181/tcp:{}]
# Mon, 04 May 2026 19:24:47 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Mon, 04 May 2026 19:24:47 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86122c5ae2f33c5829b37b51c97108e5d0affc9a8df38a2520c2547957be231`  
		Last Modified: Mon, 04 May 2026 19:25:04 GMT  
		Size: 6.7 MB (6682327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9912325bdc1215b07db51f9c07ae6e8820f419585f5b9887242a1fe13c7613d6`  
		Last Modified: Mon, 04 May 2026 19:25:03 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b125a45984c5269b6fa91084249fabb15107023aa0b6b970da45b12c244f228`  
		Last Modified: Mon, 04 May 2026 19:25:06 GMT  
		Size: 104.5 MB (104544117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8864d3ce3dc01bc91806893665a5b7fc0a8b446a18b11dab323970528b26f0c`  
		Last Modified: Mon, 04 May 2026 19:25:03 GMT  
		Size: 521.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba1d612389a4091467addf28fb0d3c3d2403a29bb18848dd001ec6e3e032fb9`  
		Last Modified: Mon, 04 May 2026 19:25:04 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:a18ae06ad6d18c7f881a4b49c8d07d0cb3230600e42b332e69f8de458933da8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e147252f5eea6b419a730b9f59f8f268481a1395aa6b563d14563c918a6d5f8b`

```dockerfile
```

-	Layers:
	-	`sha256:f5e73fadd1e444f21baa13cf65d30006e79055f47e5fdee04f18b8c6941a04a3`  
		Last Modified: Mon, 04 May 2026 19:25:04 GMT  
		Size: 2.3 MB (2311679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9efa154e53131da2dc68d5b78f59fc7828711e79ff576b57b71b56c777b161c`  
		Last Modified: Mon, 04 May 2026 19:25:03 GMT  
		Size: 17.8 KB (17768 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:data`

```console
$ docker pull influxdb@sha256:e6398d43e07f280786f433bf80f8639b750bfb50e5c747ffc4ddc9e2a60c5b7c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:data` - linux; amd64

```console
$ docker pull influxdb@sha256:0f1cd7dc2417b33893cf37d0c221c1d141fea39c7e6f3d75987d2ce2f39c7379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115722571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90e946c6558e16f25290a65d9cacce4a62fb96fa1e024c32df5af02a52dce8e0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:30:41 GMT
ENV INFLUXDB_VERSION=1.12.4-c1.12.4
# Fri, 08 May 2026 20:30:41 GMT
ENV INFLUXDB_PR=
# Fri, 08 May 2026 20:30:41 GMT
ENV INFLUXDB_PV=1.12.4-c1.12.4
# Fri, 08 May 2026 20:30:41 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"          -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"         "influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     rm -r "influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"           "influxdb-data_${INFLUXDB_PV}_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:30:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 08 May 2026 20:30:41 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 08 May 2026 20:30:41 GMT
VOLUME [/var/lib/influxdb]
# Fri, 08 May 2026 20:30:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 20:30:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 08 May 2026 20:30:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 20:30:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d055cea50c88c57fc27fcd44845ebabfe5b830ea8a0a621b89d38a2b650b7ff3`  
		Last Modified: Fri, 08 May 2026 19:40:29 GMT  
		Size: 24.0 MB (24042180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:962acf40db3a7d5df88755121d66b97b074e6fa7af51182c3582c3fbb65fdfb2`  
		Last Modified: Fri, 08 May 2026 20:30:56 GMT  
		Size: 43.2 MB (43189938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fcb508adabb85feb56df9db23493b1b85833909a099c96a55ee681b41293c99`  
		Last Modified: Fri, 08 May 2026 20:30:55 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f6c1227d43a6d82ff41b8ef79cb08bab47864e59f8c6884a2a263d146821d3`  
		Last Modified: Fri, 08 May 2026 20:30:55 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db63a3ea8649aa33914a2860a788be1b9e77252249952311c7ba20c888f8b43`  
		Last Modified: Fri, 08 May 2026 20:30:55 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:data` - unknown; unknown

```console
$ docker pull influxdb@sha256:3a80b17123ca1905ae253c10601c1a1906b0f118b45e3254adebf76cc7782238
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4707277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a478a44f1e471ed0a0b7184d1ededb0817c5a7f997b34f0fa4b76f3cf8b5003e`

```dockerfile
```

-	Layers:
	-	`sha256:43aec9720ab4169c00241c51f14a8db53355c107f19b19a1e1fc4897ce1db8b8`  
		Last Modified: Fri, 08 May 2026 20:30:55 GMT  
		Size: 4.7 MB (4693123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c013f1c88633b1a08bb7a4ffa1463dd4ac279bf38bfb418977e5426907519d6`  
		Last Modified: Fri, 08 May 2026 20:30:55 GMT  
		Size: 14.2 KB (14154 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:data-alpine`

```console
$ docker pull influxdb@sha256:97455dc1763d0603ac9b2c08bb015eeafa3a4293efdb6da2dcac20989499411b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:9e565c7fd49e5d8f35ed01c97673730f73fe99480f2bcc42df2ebaeb6670e25f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47997256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63094d0e7597666e3a6319a4c087f71fe682814c16de22d762b1de6dd9c5cca7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:29:12 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:29:15 GMT
ENV INFLUXDB_VERSION=1.12.4-c1.12.4
# Fri, 17 Apr 2026 00:29:15 GMT
ENV INFLUXDB_PR=
# Fri, 17 Apr 2026 00:29:15 GMT
ENV INFLUXDB_PV=1.12.4-c1.12.4
# Fri, 17 Apr 2026 00:29:15 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"         "influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     tar -xvf "influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz"         -C /usr/bin --strip-components 1 --wildcards             'influxdb-*/influx'             'influxdb-*/influx_inspect'             'influxdb-*/influxd' &&     rm "influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"        "influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     apk del .build-deps # buildkit
# Fri, 17 Apr 2026 00:29:15 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Fri, 17 Apr 2026 00:29:15 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 17 Apr 2026 00:29:15 GMT
VOLUME [/var/lib/influxdb]
# Fri, 17 Apr 2026 00:29:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:29:15 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Fri, 17 Apr 2026 00:29:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:29:15 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc9611369db3ecb1526937d9f72c04921aa31dc4ba3d99a4e3b9c15767aa38c`  
		Last Modified: Fri, 17 Apr 2026 00:29:25 GMT  
		Size: 1.2 MB (1224170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88fc8e5058960e45aee8b6cac82ff2bd50d7e2137e6cf885c0b4d623ae175b8`  
		Last Modified: Fri, 17 Apr 2026 00:29:26 GMT  
		Size: 43.1 MB (43124440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada70a5a02afde6bb6c3f103fa9ec3a499488396461d706bd57a9bac54ad1dbf`  
		Last Modified: Fri, 17 Apr 2026 00:29:25 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d47be05a8626fbeb060a3ac42397eec5b9faff395d564ed99c70f443120850`  
		Last Modified: Fri, 17 Apr 2026 00:29:25 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2249338bf3d212a5f9560aae8dae54182f0232814622fe938e2ea878e279faab`  
		Last Modified: Fri, 17 Apr 2026 00:29:26 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:78a86aa0d4d8e27d8e0afc24b8bac506e70b8877e920a0b0d532fad2c24f6d91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **796.1 KB (796066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eaafdeb7f35414723ace5c8693058a60536ee236f09cb0b7ee8cd56812f99a5`

```dockerfile
```

-	Layers:
	-	`sha256:2c95497e066bdcad88af076d5632e15c891f1c90d79ccc0cfc2ab77eac05e7bb`  
		Last Modified: Fri, 17 Apr 2026 00:29:25 GMT  
		Size: 780.5 KB (780536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:329b5b66f2e9143f7d74aaad874558e3fea3758d13aaf5008df91e8d3021223c`  
		Last Modified: Fri, 17 Apr 2026 00:29:25 GMT  
		Size: 15.5 KB (15530 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:enterprise`

```console
$ docker pull influxdb@sha256:358c82dce3772e483184ec1acd6b3571819996264a0c6cffcd2398371d6147f2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:6d4a1152a25f15c7c0f79509879af7b8e6e6c4ead39701f8b861e6f319469a7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.9 MB (159913248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68aa326322ac34c5534cc776f18b712958bbeb3ad2965bc0b97734e41241d920`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 19:32:39 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Mon, 04 May 2026 19:32:39 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Mon, 04 May 2026 19:32:45 GMT
ENV INFLUXDB_VERSION=3.9.2
# Mon, 04 May 2026 19:32:45 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Mon, 04 May 2026 19:32:45 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Mon, 04 May 2026 19:32:45 GMT
USER influxdb3
# Mon, 04 May 2026 19:32:45 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Mon, 04 May 2026 19:32:45 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Mon, 04 May 2026 19:32:45 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Mon, 04 May 2026 19:32:45 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Mon, 04 May 2026 19:32:45 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Mon, 04 May 2026 19:32:45 GMT
ENV LOG_FILTER=info
# Mon, 04 May 2026 19:32:45 GMT
EXPOSE map[8181/tcp:{}]
# Mon, 04 May 2026 19:32:45 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Mon, 04 May 2026 19:32:45 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35d8f1f66ee449437f42b2c20cc6370539b21981f7fe4b600041b02873f30cd`  
		Last Modified: Mon, 04 May 2026 19:33:05 GMT  
		Size: 6.7 MB (6672522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5269437d2b975134ce7f74a1f7939103033cf78c221de1bc63baaa714e82645`  
		Last Modified: Mon, 04 May 2026 19:33:05 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c75ef02653df55bbae0bc226f10bfa24eed141084f7cb5cbdab3cd7d0e5813`  
		Last Modified: Mon, 04 May 2026 19:33:08 GMT  
		Size: 123.5 MB (123503421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b421193e1bc6d530da0ca9c62059309564df29ef793eacb9921153d6478bbac`  
		Last Modified: Mon, 04 May 2026 19:33:05 GMT  
		Size: 523.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14bb906d01a393178b6d80cdee8f560c5aac7db2c8045f2f0931dcb04ada0bf8`  
		Last Modified: Mon, 04 May 2026 19:33:06 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:a3b3021ed521d9f9d53e3a7eb742cec3e30c6226c942b1ffa7a5401749c7b870
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1460a0fd76dfcb9bc844b4be1121a59d3da09daac7c44b7cd4ac79beca4bbfd9`

```dockerfile
```

-	Layers:
	-	`sha256:bfbfbdf1abe1a2935c1f66e68c46f03b7a53310be04982b56e1de99c1cb050fe`  
		Last Modified: Mon, 04 May 2026 19:33:05 GMT  
		Size: 2.3 MB (2310645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce512bf114d10d645b772ed385e73462aa7f8c89560aa2f169ea851461a323ed`  
		Last Modified: Mon, 04 May 2026 19:33:05 GMT  
		Size: 17.8 KB (17800 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:3750f19aa7e14906adc446335d9a9ab7f132d3e89497255f64d2834c4cb9aca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.7 MB (150709333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac4e26b527de2a11705829ca2661397204d09e368b0ad02369fad7d5994fb780`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 19:25:22 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Mon, 04 May 2026 19:25:22 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Mon, 04 May 2026 19:25:28 GMT
ENV INFLUXDB_VERSION=3.9.2
# Mon, 04 May 2026 19:25:28 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Mon, 04 May 2026 19:25:28 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Mon, 04 May 2026 19:25:28 GMT
USER influxdb3
# Mon, 04 May 2026 19:25:28 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Mon, 04 May 2026 19:25:28 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Mon, 04 May 2026 19:25:28 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Mon, 04 May 2026 19:25:28 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Mon, 04 May 2026 19:25:28 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Mon, 04 May 2026 19:25:28 GMT
ENV LOG_FILTER=info
# Mon, 04 May 2026 19:25:28 GMT
EXPOSE map[8181/tcp:{}]
# Mon, 04 May 2026 19:25:28 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Mon, 04 May 2026 19:25:28 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9e93e4bc5af617de342495cefd816d6ea3b1e47a9d0525d6bba17800dfe6f1`  
		Last Modified: Mon, 04 May 2026 19:25:45 GMT  
		Size: 6.7 MB (6682319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55d6c43df9d1b0b687412810604131e85819992a314de97d358a54dc0de899e`  
		Last Modified: Mon, 04 May 2026 19:25:45 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feba211f9bf3663dc5a64e9aaf491c8d04501281015e7d261176d09c3fc3280d`  
		Last Modified: Mon, 04 May 2026 19:25:48 GMT  
		Size: 115.1 MB (115146903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b31f11ffdb15964895b1830588c2ca47aa1c740f4ac77aa6d2142f20542543`  
		Last Modified: Mon, 04 May 2026 19:25:45 GMT  
		Size: 520.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baaf4d5e1f4596459dbbee4d8d09205c6de08fd9fc6626aa4b7c9971bca2db77`  
		Last Modified: Mon, 04 May 2026 19:25:46 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:b9f8d5b54641ebef9a6aecaca1c2c676181dd5902fe213001d42e5ea6d9c7fdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87996fd97d3a29be0e191bff3ed856e2c59ec34976e1cef9b82b3463e29f383e`

```dockerfile
```

-	Layers:
	-	`sha256:2d2e8117fb38299a365e12bebb3f57a26cc8c547bf2aa9bb4494ad539f1feafb`  
		Last Modified: Mon, 04 May 2026 19:25:45 GMT  
		Size: 2.3 MB (2311727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28fd98d7646d9de54953525aba2e5944a6ccd1eb921b35732bf39ca85139bca9`  
		Last Modified: Mon, 04 May 2026 19:25:45 GMT  
		Size: 17.9 KB (17947 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:latest`

```console
$ docker pull influxdb@sha256:044d60447880093b9837d5de56ea0699b0db79a3e48fb94edf0f9e0eb9f4b95c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:82cd8aa54e7a82a3a006af30e3a31488b73a24f664677ba63782a9343302f1bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.8 MB (110800813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:373cd1bc99e1a9c96598fe115410634b5c8730eb6745f041f9203f1b3291ec8f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Mon, 11 May 2026 23:06:14 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg       util-linux &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:06:14 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Mon, 11 May 2026 23:06:14 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Mon, 11 May 2026 23:06:18 GMT
ENV INFLUXDB_VERSION=2.9.1
# Mon, 11 May 2026 23:06:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 11 May 2026 23:06:18 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Mon, 11 May 2026 23:06:20 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 11 May 2026 23:06:20 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 11 May 2026 23:06:20 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 11 May 2026 23:06:20 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 11 May 2026 23:06:20 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 11 May 2026 23:06:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 May 2026 23:06:20 GMT
CMD ["influxd"]
# Mon, 11 May 2026 23:06:20 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 11 May 2026 23:06:20 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 11 May 2026 23:06:20 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 11 May 2026 23:06:20 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 11 May 2026 23:06:20 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6306d75e2dc4ba2680cb2722b624ffd58658aea8bd7eb42637befbd5f956dc64`  
		Last Modified: Mon, 11 May 2026 23:06:33 GMT  
		Size: 9.8 MB (9799055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a82281c39f9f067b4235800d0e007670159c80542159a4450563d989fcb6563`  
		Last Modified: Mon, 11 May 2026 23:06:33 GMT  
		Size: 3.8 MB (3822784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a116ed37df3620df292451a9d9a04e82e56d60335cf27224a67219ed22cc038`  
		Last Modified: Mon, 11 May 2026 23:06:33 GMT  
		Size: 3.2 KB (3235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af303914f43bdf518bb8cfc5c3c8f4ce2f6e39e7424c012c140aca8689925373`  
		Last Modified: Mon, 11 May 2026 23:06:34 GMT  
		Size: 56.5 MB (56510687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080fd8044aff2f969b124bf1847f066b663e5b2f6cae5eb4a2fe39fd84b9ca8a`  
		Last Modified: Mon, 11 May 2026 23:06:34 GMT  
		Size: 12.4 MB (12421826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c8bdb93dd525adb082fe977c42446a606867cb0876486414590f483bdb16e5`  
		Last Modified: Mon, 11 May 2026 23:06:34 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec61169a51e436a25adf019845e2b06c2a2f667604bdaa2f3ce7d6c242b7e2d3`  
		Last Modified: Mon, 11 May 2026 23:06:35 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c8475bae289926b70499ba7275b48cf710950a5c1745f1047e5cea27687ae7`  
		Last Modified: Mon, 11 May 2026 23:06:35 GMT  
		Size: 6.5 KB (6500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:3b4cdef18045a438e84e562f34e5593ba983944ada9400c448b23087fef4b9a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2988025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c263006991641cd34e84386b46b2189a3f22c0342ad8433ea93de78b3c101a59`

```dockerfile
```

-	Layers:
	-	`sha256:1eaa89e6c29ca38c8ea88162e378052dd323f1b5ccec9fbe77da9e5df39808c7`  
		Last Modified: Mon, 11 May 2026 23:06:33 GMT  
		Size: 3.0 MB (2959411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4126e96a3d9f757323087f196a105f67cb780972bf33fd5a38e7808989145600`  
		Last Modified: Mon, 11 May 2026 23:06:32 GMT  
		Size: 28.6 KB (28614 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:3bce906f5cd366a1d7f1386e355e51c87c6192fcc4d71c68a2edd3297a0192df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106330754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53cf7d95c5904cc95a6940f0d1154b73162e38d225ef133b2450a48ca219c096`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Mon, 11 May 2026 23:06:05 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg       util-linux &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:06:05 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Mon, 11 May 2026 23:06:05 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Mon, 11 May 2026 23:06:09 GMT
ENV INFLUXDB_VERSION=2.9.1
# Mon, 11 May 2026 23:06:09 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 11 May 2026 23:06:09 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Mon, 11 May 2026 23:06:11 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 11 May 2026 23:06:11 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 11 May 2026 23:06:11 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 11 May 2026 23:06:11 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 11 May 2026 23:06:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 11 May 2026 23:06:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 11 May 2026 23:06:11 GMT
CMD ["influxd"]
# Mon, 11 May 2026 23:06:11 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 11 May 2026 23:06:11 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 11 May 2026 23:06:11 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 11 May 2026 23:06:11 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 11 May 2026 23:06:11 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f23bbe568e43c569b84c86a9c06acb37a65383eef9d7a41c3493f2fc439b23`  
		Last Modified: Mon, 11 May 2026 23:06:23 GMT  
		Size: 9.6 MB (9628121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf21f16acbfdf9cb08e177f4e24e660aef286d9b0246883ca9ccac7f3423ef5`  
		Last Modified: Mon, 11 May 2026 23:06:23 GMT  
		Size: 3.5 MB (3459172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7651cdf91299714e33bee7297dbf293d680c2046377416bbec761092b53fbff`  
		Last Modified: Mon, 11 May 2026 23:06:23 GMT  
		Size: 3.2 KB (3233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93251acc80816de10b80ad59732e2112e724a1d77bc28e4943715d5a298725e`  
		Last Modified: Mon, 11 May 2026 23:06:25 GMT  
		Size: 53.6 MB (53636817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb61f007cdfb2efe51d7353b061d5dc88228555a0565832e7f4798bcf9c4bc05`  
		Last Modified: Mon, 11 May 2026 23:06:25 GMT  
		Size: 11.5 MB (11480302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d795a7febcb13431d839fb4382b6e22f5debf58e787deaeb34da45464289ba10`  
		Last Modified: Mon, 11 May 2026 23:06:25 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e57e263f59e437119c3be99d4d6e7ef67e658750db5b34f3c5307bb8d3d583`  
		Last Modified: Mon, 11 May 2026 23:06:25 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f0fde88bd7e8e0fef0640c7e8be480e6b382f511e2da3d9129a50466da3d55`  
		Last Modified: Mon, 11 May 2026 23:06:26 GMT  
		Size: 6.5 KB (6500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:eb708288bfdc461e6c7c5c7346d5a1d11ba930ebf51cd162c10e023a7e3b89cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed727a90b15a758f20fe1ecb27f8186e0638b8cd670f3eb6052b11f07a9dde9c`

```dockerfile
```

-	Layers:
	-	`sha256:64fc4525aa7a436f50908c48554e8f5bd8b3b56e903570d96d434ea2183135f7`  
		Last Modified: Mon, 11 May 2026 23:06:23 GMT  
		Size: 3.0 MB (2958889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c1611d06ea9793b05207e6377419833d4f183dd192845527a8be765b2d3d5e9`  
		Last Modified: Mon, 11 May 2026 23:06:23 GMT  
		Size: 28.8 KB (28793 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:meta`

```console
$ docker pull influxdb@sha256:fa416351c64988902901b3c3e3e95b78760e4b64d8537a6953bb506642e80ba4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:meta` - linux; amd64

```console
$ docker pull influxdb@sha256:b1ef1ea5f5c5fb9423f07a34691b7341a98b8edfecb170cc13c5c72c8feb2fcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91916620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3045502ba23a95adfb8f7d6a59cf783fd370ea250146a00d8985f015bbf88464`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:30:52 GMT
ENV INFLUXDB_VERSION=1.12.4-c1.12.4
# Fri, 08 May 2026 20:30:52 GMT
ENV INFLUXDB_PR=
# Fri, 08 May 2026 20:30:52 GMT
ENV INFLUXDB_PV=1.12.4-c1.12.4
# Fri, 08 May 2026 20:30:52 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"          -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"         "influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     rm -r "influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"           "influxdb-meta_${INFLUXDB_PV}_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:30:52 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Fri, 08 May 2026 20:30:52 GMT
EXPOSE map[8091/tcp:{}]
# Fri, 08 May 2026 20:30:52 GMT
VOLUME [/var/lib/influxdb]
# Fri, 08 May 2026 20:30:52 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 08 May 2026 20:30:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 20:30:52 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d055cea50c88c57fc27fcd44845ebabfe5b830ea8a0a621b89d38a2b650b7ff3`  
		Last Modified: Fri, 08 May 2026 19:40:29 GMT  
		Size: 24.0 MB (24042180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b058c7f6dfb8da15a4a0b773a7c4c7059f9b5e4f6b82db7424793cf8cea072aa`  
		Last Modified: Fri, 08 May 2026 20:31:02 GMT  
		Size: 19.4 MB (19385193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5794176de2edc35b4dc3032ace26da68f9eec0ff629b42b1c68d97af7d7c4a`  
		Last Modified: Fri, 08 May 2026 20:31:01 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7d46c4bdbd2d99069aecc0673097fdc4f2d690f90831ab9767ae1f0a7c080b`  
		Last Modified: Fri, 08 May 2026 20:31:01 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:e8c2b5bac24fa5471bf3dfe6af346c57367722bc2084aa1f1848d16d0acd596c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4605854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e02b4f902aa1d98d78b949b707dc7e11e98ca677360c6102f0c52507bb6e677`

```dockerfile
```

-	Layers:
	-	`sha256:7e6306732f4bf984511ea6ba4d8028686ba7a12977d0460e9515b17e763f1a97`  
		Last Modified: Fri, 08 May 2026 20:31:01 GMT  
		Size: 4.6 MB (4593191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0782c7a7748da881c618af0865368527f37ef032d843b1aa0d258633ba71c89`  
		Last Modified: Fri, 08 May 2026 20:31:01 GMT  
		Size: 12.7 KB (12663 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:meta-alpine`

```console
$ docker pull influxdb@sha256:c1609e4b1a9966a278cbc63e39637d62a3798895d5f9dffb16f56642c345a470
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:0c2d58c85a4eeef69b1067b8385427653ccd49a3c18b2fa5c406ecc061a3eff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.2 MB (24201677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c996d394ebe8422efb6cd5313a8b6d659f4361c8783ba7e2765a3495d82bf9a9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:29:31 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:29:34 GMT
ENV INFLUXDB_VERSION=1.12.4-c1.12.4
# Fri, 17 Apr 2026 00:29:34 GMT
ENV INFLUXDB_PR=
# Fri, 17 Apr 2026 00:29:34 GMT
ENV INFLUXDB_PV=1.12.4-c1.12.4
# Fri, 17 Apr 2026 00:29:34 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"         "influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     tar -xvf "influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz"         -C /usr/bin --strip-components 1 --wildcards             'influxdb-*/influxd-ctl'             'influxdb-*/influxd-meta' &&     rm "influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"        "influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     apk del .build-deps # buildkit
# Fri, 17 Apr 2026 00:29:34 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Fri, 17 Apr 2026 00:29:34 GMT
EXPOSE map[8091/tcp:{}]
# Fri, 17 Apr 2026 00:29:34 GMT
VOLUME [/var/lib/influxdb]
# Fri, 17 Apr 2026 00:29:34 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:29:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:29:34 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fce14c04b1498e08f014d63ade6e29799ca92f77d6d5aee2e26f723fa47632`  
		Last Modified: Fri, 17 Apr 2026 00:29:41 GMT  
		Size: 1.2 MB (1224167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e592b60a790f783fefc22026e6f186aec24b3fb81e56fe43bc3ad4dfbccf3b`  
		Last Modified: Fri, 17 Apr 2026 00:29:42 GMT  
		Size: 19.3 MB (19330070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1f2ec0dd69b272c781c7c30754b98f78b843600b12cddc731b02a3b58f888a1`  
		Last Modified: Fri, 17 Apr 2026 00:29:41 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc5145a28bfcd9c82912556bd7085dee977090f80a54a3c6ee097e29382fcbf`  
		Last Modified: Fri, 17 Apr 2026 00:29:41 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:667228df4c2fe4090dfa788f0b272b45189b51414433b171b53980323a0ef648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **695.3 KB (695321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b92baa71c20ea018ab004a2abf41df19c1368d9bff15dcda5fa2415c18b67e4`

```dockerfile
```

-	Layers:
	-	`sha256:0b0a0c460b5f111deb27700ed49900ddbe4a0e118ad09843c430e91a8668f979`  
		Last Modified: Fri, 17 Apr 2026 00:29:41 GMT  
		Size: 681.4 KB (681390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7168d592346505ecf69732a4af5308278302c2ca1cc6966560e75037b25b940c`  
		Last Modified: Fri, 17 Apr 2026 00:29:41 GMT  
		Size: 13.9 KB (13931 bytes)  
		MIME: application/vnd.in-toto+json
