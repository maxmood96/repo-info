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
-	[`influxdb:3.9.3-core`](#influxdb393-core)
-	[`influxdb:3.9.3-enterprise`](#influxdb393-enterprise)
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
$ docker pull influxdb@sha256:6e9190e218fc460c4b215c0827080dc03c040e1b27ce28d060b9437d1e22a661
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11` - linux; amd64

```console
$ docker pull influxdb@sha256:19cc9690900d65a642195040901b6f9ff963f06f52bea6e142dbc631e6657d15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117551104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08e51fb88f02c5a7417b4bac714e6619b616ea70b9884ba99d96c0cdb47cacb4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:29:47 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Wed, 20 May 2026 00:29:54 GMT
ARG INFLUXDB_VERSION=1.11.8
# Wed, 20 May 2026 00:29:54 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:29:54 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 20 May 2026 00:29:54 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 20 May 2026 00:29:54 GMT
VOLUME [/var/lib/influxdb]
# Wed, 20 May 2026 00:29:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:29:54 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 20 May 2026 00:29:54 GMT
USER influxdb
# Wed, 20 May 2026 00:29:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:29:54 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e51c50554dce9c9549d76c40bfea45780a8342aea81ba8b270ba1bf46a2aec5`  
		Last Modified: Tue, 19 May 2026 23:23:20 GMT  
		Size: 24.0 MB (24043374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f337adb3bc8da7397cf0460555e6e6a43df976fa683ac31e04d9eda95ac95aa5`  
		Last Modified: Wed, 20 May 2026 00:30:06 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82c3fef4cd9ed8e0cc53efb0a3c6563120b37ed51b98af095ca123440beb02b`  
		Last Modified: Wed, 20 May 2026 00:30:07 GMT  
		Size: 45.0 MB (45009386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44cd58dc536d239bd951db20c348e8a91705fbf2b2d66a126e2612c53b1eb342`  
		Last Modified: Wed, 20 May 2026 00:30:06 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e55c77a6007b8080bf7610af150727b8e48a81d1d299c5272781f66ca701a0a`  
		Last Modified: Wed, 20 May 2026 00:30:06 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e15bc91c95f94825083917d416de10ba61aa9cdd8cd7a084e95e146462457f`  
		Last Modified: Wed, 20 May 2026 00:30:07 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11` - unknown; unknown

```console
$ docker pull influxdb@sha256:d7942c8f8fcbb36555b2b0e01d50faee36f7492485b0f1f648a991833e0b2e87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:866a6d086f48d15ae4fc84e5324f6885445a54906aa78ce93ee4dc0ab186c202`

```dockerfile
```

-	Layers:
	-	`sha256:22feb2ba9f12b44e8960a1b730c3fbb29080ab4b550b72d285f2d4eb2d5bef0a`  
		Last Modified: Wed, 20 May 2026 00:30:06 GMT  
		Size: 5.1 MB (5079281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c24d5080902db16be96ec0e8bedef2cd09c3995632533ee7d8f092039c23bc95`  
		Last Modified: Wed, 20 May 2026 00:30:06 GMT  
		Size: 15.5 KB (15485 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:bc5729389a158c0d30656254e27b874f98bb0772b45376661fcb8626a4a33076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.4 MB (114426987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7707685419abd5440d0895a5698b6efe9b9d0bab62a3cb09952eadeef0dd0270`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:31:44 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Wed, 20 May 2026 00:31:51 GMT
ARG INFLUXDB_VERSION=1.11.8
# Wed, 20 May 2026 00:31:51 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:31:51 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 20 May 2026 00:31:51 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 20 May 2026 00:31:51 GMT
VOLUME [/var/lib/influxdb]
# Wed, 20 May 2026 00:31:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:31:51 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 20 May 2026 00:31:51 GMT
USER influxdb
# Wed, 20 May 2026 00:31:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:31:51 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3daebbc198bd7b84bdd72840d7f4ded251896f03b9a9f880894e95e926bc543`  
		Last Modified: Tue, 19 May 2026 23:26:38 GMT  
		Size: 23.6 MB (23613394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c222752bcced6996c802bc035941d4911cd9dffa7b5addd5f46af9660f4d4b8`  
		Last Modified: Wed, 20 May 2026 00:32:05 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b1d0e5e24c6a10710499572b4d85e868375d46a8be5153dac9e11728edd74d`  
		Last Modified: Wed, 20 May 2026 00:32:07 GMT  
		Size: 42.4 MB (42431253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e4e61c18a45dfd158b8e7bd58e87ff7395c56f6598f155373c62bf3dac3da5`  
		Last Modified: Wed, 20 May 2026 00:32:05 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ec42ddbcf22446d81960e9f8883b5466c8ab1d8ac7dd3be3f300dbd2cea21e`  
		Last Modified: Wed, 20 May 2026 00:32:05 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dcbd9d8c864b0a154373f0f2c1b09137074c26d7416ec753acc4c497142cd81`  
		Last Modified: Wed, 20 May 2026 00:32:06 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11` - unknown; unknown

```console
$ docker pull influxdb@sha256:c48f9916007127e66c29f053c16751464e30f9a31c12c783979d81f6ce91cd38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36312913da5dc136113269d6cf39da5ce2fb611e198184b95a2c5c5fdddcb86b`

```dockerfile
```

-	Layers:
	-	`sha256:c4f3cb12e5c960ffe84ffa78f452851c69a412bec2c43adf8417ac00aacce5ac`  
		Last Modified: Wed, 20 May 2026 00:32:06 GMT  
		Size: 5.1 MB (5078746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de2ade0a11dfdc71f777800d1d42e5ad83690c89e8d1bb137fcc95b4132092e3`  
		Last Modified: Wed, 20 May 2026 00:32:05 GMT  
		Size: 15.6 KB (15581 bytes)  
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
$ docker pull influxdb@sha256:5d450b564ae9a330a5b25b0a93dfdcdcfe8363ffc089ed8d05d95e6e56bb9c8e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data` - linux; amd64

```console
$ docker pull influxdb@sha256:b615a6c612f251aebaed9de6702048285116215a616ad8656ce0d42f38d58238
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114711304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8637a5db607c1da6c3acc9492c9a0a98d769e2beaf345d9170af6c3e5e8c75f0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:29:57 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 20 May 2026 00:30:00 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Wed, 20 May 2026 00:30:00 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Wed, 20 May 2026 00:30:00 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 20 May 2026 00:30:00 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 20 May 2026 00:30:00 GMT
VOLUME [/var/lib/influxdb]
# Wed, 20 May 2026 00:30:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:30:00 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 20 May 2026 00:30:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:30:00 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e51c50554dce9c9549d76c40bfea45780a8342aea81ba8b270ba1bf46a2aec5`  
		Last Modified: Tue, 19 May 2026 23:23:20 GMT  
		Size: 24.0 MB (24043374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b2766f3d9e46adc1446fa2859b95b3d25133f7e79c93bb5f2329daf4ed1d8a`  
		Last Modified: Wed, 20 May 2026 00:30:10 GMT  
		Size: 5.1 KB (5054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1efb5366b429829b85a57b14d74c93d82b97409f0fbb88f5699610bed5b87a5`  
		Last Modified: Wed, 20 May 2026 00:30:12 GMT  
		Size: 42.2 MB (42165672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d506fbbd4d951998e71974269ed2f65d12565e55870fa4198310e788744c56`  
		Last Modified: Wed, 20 May 2026 00:30:11 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b0e6b82dc60a952ce66099814052c3c535cfaec64ec43d254e1eea4f5e429f`  
		Last Modified: Wed, 20 May 2026 00:30:11 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd61e28c1a3e961e980d5bc69df2c1b499647c19ffa50f18ac146b91cfd30ce`  
		Last Modified: Wed, 20 May 2026 00:30:12 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:7dfcb5a7a1847c56f46fc4ca954d1573a161c94605d67aa4faa60f59ab7054db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4699089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dae5ccf0c8de83c6ed7933e838eceb1c27e4133707a3215cf1c20dd6f878ab7b`

```dockerfile
```

-	Layers:
	-	`sha256:07a4640486eca69b880c7bfa500524117f507446395b96e33e20c666ebdbc2ca`  
		Last Modified: Wed, 20 May 2026 00:30:11 GMT  
		Size: 4.7 MB (4684424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:824fa47846859316701c9207f5dde80287eb5fb8ed4ae68d91c16bd323473267`  
		Last Modified: Wed, 20 May 2026 00:30:10 GMT  
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
$ docker pull influxdb@sha256:d4933947e588c43fe64df2ccc556e5a91d49ae2320d43d97833f29a141f1b192
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:73853e64190409539c9a64f10f68531136d93dae6de093123c664c227ab61532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91140554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05633fac51a8d71141ef0bf82cf18942a6389cecbf123b566691dad53f32b930`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:30:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 20 May 2026 00:30:04 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Wed, 20 May 2026 00:30:04 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Wed, 20 May 2026 00:30:04 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Wed, 20 May 2026 00:30:04 GMT
EXPOSE map[8091/tcp:{}]
# Wed, 20 May 2026 00:30:04 GMT
VOLUME [/var/lib/influxdb]
# Wed, 20 May 2026 00:30:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:30:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:30:04 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e51c50554dce9c9549d76c40bfea45780a8342aea81ba8b270ba1bf46a2aec5`  
		Last Modified: Tue, 19 May 2026 23:23:20 GMT  
		Size: 24.0 MB (24043374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59cd9de8aa6946930e99155e744849133cb1e5c03fa6198fa025077d5083c10`  
		Last Modified: Wed, 20 May 2026 00:30:12 GMT  
		Size: 5.1 KB (5068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a179aa039cec8a243a2d701abb23333a818392d54351a3ca4cb63c4956102f2f`  
		Last Modified: Wed, 20 May 2026 00:30:13 GMT  
		Size: 18.6 MB (18596114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fe31e893e9f7068cd045162118fc0a2f765c7e9d0187c7a3db0a39722b3b5a`  
		Last Modified: Wed, 20 May 2026 00:30:12 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f2f6e8be368b93ff67d7e5620e0c74bb704286de293380a1120a23f663afd8`  
		Last Modified: Wed, 20 May 2026 00:30:12 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:fce2f83150f69750b4e4d537e421354bde4c893d2cc603ded7f94e8c9f3d3706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4604290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0553606145ac4f9ab70cf61710ea0359b780d3d3d52b9bad5088ae4bb12795b`

```dockerfile
```

-	Layers:
	-	`sha256:a07d3bd66e7368e1c9a82f598f0578a9fb9fded00d96ee2988338e68b638e63a`  
		Last Modified: Wed, 20 May 2026 00:30:13 GMT  
		Size: 4.6 MB (4591267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:253940034186cc643194dd25c05eceb2e6d155609462b114a68228675d72aca4`  
		Last Modified: Wed, 20 May 2026 00:30:12 GMT  
		Size: 13.0 KB (13023 bytes)  
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
$ docker pull influxdb@sha256:6e9190e218fc460c4b215c0827080dc03c040e1b27ce28d060b9437d1e22a661
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11.8` - linux; amd64

```console
$ docker pull influxdb@sha256:19cc9690900d65a642195040901b6f9ff963f06f52bea6e142dbc631e6657d15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117551104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08e51fb88f02c5a7417b4bac714e6619b616ea70b9884ba99d96c0cdb47cacb4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:29:47 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Wed, 20 May 2026 00:29:54 GMT
ARG INFLUXDB_VERSION=1.11.8
# Wed, 20 May 2026 00:29:54 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:29:54 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 20 May 2026 00:29:54 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 20 May 2026 00:29:54 GMT
VOLUME [/var/lib/influxdb]
# Wed, 20 May 2026 00:29:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:29:54 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 20 May 2026 00:29:54 GMT
USER influxdb
# Wed, 20 May 2026 00:29:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:29:54 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e51c50554dce9c9549d76c40bfea45780a8342aea81ba8b270ba1bf46a2aec5`  
		Last Modified: Tue, 19 May 2026 23:23:20 GMT  
		Size: 24.0 MB (24043374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f337adb3bc8da7397cf0460555e6e6a43df976fa683ac31e04d9eda95ac95aa5`  
		Last Modified: Wed, 20 May 2026 00:30:06 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82c3fef4cd9ed8e0cc53efb0a3c6563120b37ed51b98af095ca123440beb02b`  
		Last Modified: Wed, 20 May 2026 00:30:07 GMT  
		Size: 45.0 MB (45009386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44cd58dc536d239bd951db20c348e8a91705fbf2b2d66a126e2612c53b1eb342`  
		Last Modified: Wed, 20 May 2026 00:30:06 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e55c77a6007b8080bf7610af150727b8e48a81d1d299c5272781f66ca701a0a`  
		Last Modified: Wed, 20 May 2026 00:30:06 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e15bc91c95f94825083917d416de10ba61aa9cdd8cd7a084e95e146462457f`  
		Last Modified: Wed, 20 May 2026 00:30:07 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:d7942c8f8fcbb36555b2b0e01d50faee36f7492485b0f1f648a991833e0b2e87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:866a6d086f48d15ae4fc84e5324f6885445a54906aa78ce93ee4dc0ab186c202`

```dockerfile
```

-	Layers:
	-	`sha256:22feb2ba9f12b44e8960a1b730c3fbb29080ab4b550b72d285f2d4eb2d5bef0a`  
		Last Modified: Wed, 20 May 2026 00:30:06 GMT  
		Size: 5.1 MB (5079281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c24d5080902db16be96ec0e8bedef2cd09c3995632533ee7d8f092039c23bc95`  
		Last Modified: Wed, 20 May 2026 00:30:06 GMT  
		Size: 15.5 KB (15485 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:bc5729389a158c0d30656254e27b874f98bb0772b45376661fcb8626a4a33076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.4 MB (114426987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7707685419abd5440d0895a5698b6efe9b9d0bab62a3cb09952eadeef0dd0270`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:31:44 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Wed, 20 May 2026 00:31:51 GMT
ARG INFLUXDB_VERSION=1.11.8
# Wed, 20 May 2026 00:31:51 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:31:51 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 20 May 2026 00:31:51 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 20 May 2026 00:31:51 GMT
VOLUME [/var/lib/influxdb]
# Wed, 20 May 2026 00:31:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:31:51 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 20 May 2026 00:31:51 GMT
USER influxdb
# Wed, 20 May 2026 00:31:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:31:51 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3daebbc198bd7b84bdd72840d7f4ded251896f03b9a9f880894e95e926bc543`  
		Last Modified: Tue, 19 May 2026 23:26:38 GMT  
		Size: 23.6 MB (23613394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c222752bcced6996c802bc035941d4911cd9dffa7b5addd5f46af9660f4d4b8`  
		Last Modified: Wed, 20 May 2026 00:32:05 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b1d0e5e24c6a10710499572b4d85e868375d46a8be5153dac9e11728edd74d`  
		Last Modified: Wed, 20 May 2026 00:32:07 GMT  
		Size: 42.4 MB (42431253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e4e61c18a45dfd158b8e7bd58e87ff7395c56f6598f155373c62bf3dac3da5`  
		Last Modified: Wed, 20 May 2026 00:32:05 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ec42ddbcf22446d81960e9f8883b5466c8ab1d8ac7dd3be3f300dbd2cea21e`  
		Last Modified: Wed, 20 May 2026 00:32:05 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dcbd9d8c864b0a154373f0f2c1b09137074c26d7416ec753acc4c497142cd81`  
		Last Modified: Wed, 20 May 2026 00:32:06 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:c48f9916007127e66c29f053c16751464e30f9a31c12c783979d81f6ce91cd38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36312913da5dc136113269d6cf39da5ce2fb611e198184b95a2c5c5fdddcb86b`

```dockerfile
```

-	Layers:
	-	`sha256:c4f3cb12e5c960ffe84ffa78f452851c69a412bec2c43adf8417ac00aacce5ac`  
		Last Modified: Wed, 20 May 2026 00:32:06 GMT  
		Size: 5.1 MB (5078746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de2ade0a11dfdc71f777800d1d42e5ad83690c89e8d1bb137fcc95b4132092e3`  
		Last Modified: Wed, 20 May 2026 00:32:05 GMT  
		Size: 15.6 KB (15581 bytes)  
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
$ docker pull influxdb@sha256:5d450b564ae9a330a5b25b0a93dfdcdcfe8363ffc089ed8d05d95e6e56bb9c8e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.9-data` - linux; amd64

```console
$ docker pull influxdb@sha256:b615a6c612f251aebaed9de6702048285116215a616ad8656ce0d42f38d58238
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114711304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8637a5db607c1da6c3acc9492c9a0a98d769e2beaf345d9170af6c3e5e8c75f0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:29:57 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 20 May 2026 00:30:00 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Wed, 20 May 2026 00:30:00 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Wed, 20 May 2026 00:30:00 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 20 May 2026 00:30:00 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 20 May 2026 00:30:00 GMT
VOLUME [/var/lib/influxdb]
# Wed, 20 May 2026 00:30:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:30:00 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 20 May 2026 00:30:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:30:00 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e51c50554dce9c9549d76c40bfea45780a8342aea81ba8b270ba1bf46a2aec5`  
		Last Modified: Tue, 19 May 2026 23:23:20 GMT  
		Size: 24.0 MB (24043374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b2766f3d9e46adc1446fa2859b95b3d25133f7e79c93bb5f2329daf4ed1d8a`  
		Last Modified: Wed, 20 May 2026 00:30:10 GMT  
		Size: 5.1 KB (5054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1efb5366b429829b85a57b14d74c93d82b97409f0fbb88f5699610bed5b87a5`  
		Last Modified: Wed, 20 May 2026 00:30:12 GMT  
		Size: 42.2 MB (42165672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d506fbbd4d951998e71974269ed2f65d12565e55870fa4198310e788744c56`  
		Last Modified: Wed, 20 May 2026 00:30:11 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b0e6b82dc60a952ce66099814052c3c535cfaec64ec43d254e1eea4f5e429f`  
		Last Modified: Wed, 20 May 2026 00:30:11 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd61e28c1a3e961e980d5bc69df2c1b499647c19ffa50f18ac146b91cfd30ce`  
		Last Modified: Wed, 20 May 2026 00:30:12 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.9-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:7dfcb5a7a1847c56f46fc4ca954d1573a161c94605d67aa4faa60f59ab7054db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4699089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dae5ccf0c8de83c6ed7933e838eceb1c27e4133707a3215cf1c20dd6f878ab7b`

```dockerfile
```

-	Layers:
	-	`sha256:07a4640486eca69b880c7bfa500524117f507446395b96e33e20c666ebdbc2ca`  
		Last Modified: Wed, 20 May 2026 00:30:11 GMT  
		Size: 4.7 MB (4684424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:824fa47846859316701c9207f5dde80287eb5fb8ed4ae68d91c16bd323473267`  
		Last Modified: Wed, 20 May 2026 00:30:10 GMT  
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
$ docker pull influxdb@sha256:d4933947e588c43fe64df2ccc556e5a91d49ae2320d43d97833f29a141f1b192
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.9-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:73853e64190409539c9a64f10f68531136d93dae6de093123c664c227ab61532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91140554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05633fac51a8d71141ef0bf82cf18942a6389cecbf123b566691dad53f32b930`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:30:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 20 May 2026 00:30:04 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Wed, 20 May 2026 00:30:04 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Wed, 20 May 2026 00:30:04 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Wed, 20 May 2026 00:30:04 GMT
EXPOSE map[8091/tcp:{}]
# Wed, 20 May 2026 00:30:04 GMT
VOLUME [/var/lib/influxdb]
# Wed, 20 May 2026 00:30:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:30:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:30:04 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e51c50554dce9c9549d76c40bfea45780a8342aea81ba8b270ba1bf46a2aec5`  
		Last Modified: Tue, 19 May 2026 23:23:20 GMT  
		Size: 24.0 MB (24043374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59cd9de8aa6946930e99155e744849133cb1e5c03fa6198fa025077d5083c10`  
		Last Modified: Wed, 20 May 2026 00:30:12 GMT  
		Size: 5.1 KB (5068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a179aa039cec8a243a2d701abb23333a818392d54351a3ca4cb63c4956102f2f`  
		Last Modified: Wed, 20 May 2026 00:30:13 GMT  
		Size: 18.6 MB (18596114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5fe31e893e9f7068cd045162118fc0a2f765c7e9d0187c7a3db0a39722b3b5a`  
		Last Modified: Wed, 20 May 2026 00:30:12 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f2f6e8be368b93ff67d7e5620e0c74bb704286de293380a1120a23f663afd8`  
		Last Modified: Wed, 20 May 2026 00:30:12 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.9-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:fce2f83150f69750b4e4d537e421354bde4c893d2cc603ded7f94e8c9f3d3706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4604290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0553606145ac4f9ab70cf61710ea0359b780d3d3d52b9bad5088ae4bb12795b`

```dockerfile
```

-	Layers:
	-	`sha256:a07d3bd66e7368e1c9a82f598f0578a9fb9fded00d96ee2988338e68b638e63a`  
		Last Modified: Wed, 20 May 2026 00:30:13 GMT  
		Size: 4.6 MB (4591267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:253940034186cc643194dd25c05eceb2e6d155609462b114a68228675d72aca4`  
		Last Modified: Wed, 20 May 2026 00:30:12 GMT  
		Size: 13.0 KB (13023 bytes)  
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
$ docker pull influxdb@sha256:67e0b53c29cd4bd17d7633ad83399af86f8f131c063a785db4f7e3aa4d0a6bdf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.12` - linux; amd64

```console
$ docker pull influxdb@sha256:949e2f3b7b23e88c0f85f51a0f56b92f72f6fdb327ab185ec4299d515bc3d9ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114668090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd8876a6ed3b4c7e0602fe327f00f3a792017c4b6ff3c22a53daa11f41538dc1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:29:33 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Wed, 20 May 2026 00:29:38 GMT
ENV INFLUXDB_VERSION=1.12.4
# Wed, 20 May 2026 00:29:38 GMT
ENV INFLUXDB_PR=-1
# Wed, 20 May 2026 00:29:38 GMT
ENV INFLUXDB_PV=1.12.4-1
# Wed, 20 May 2026 00:29:38 GMT
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_PV}_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:29:38 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 20 May 2026 00:29:38 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 20 May 2026 00:29:38 GMT
VOLUME [/var/lib/influxdb]
# Wed, 20 May 2026 00:29:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:29:38 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 20 May 2026 00:29:38 GMT
USER influxdb
# Wed, 20 May 2026 00:29:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:29:38 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e51c50554dce9c9549d76c40bfea45780a8342aea81ba8b270ba1bf46a2aec5`  
		Last Modified: Tue, 19 May 2026 23:23:20 GMT  
		Size: 24.0 MB (24043374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300525e978958bc009f1604e662f5450d8601291957b031029e471ab910e8ae9`  
		Last Modified: Wed, 20 May 2026 00:29:49 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6dfe9783caa36ea1666ed94de8e4d3d620944c7165ffadca95a2bab3226c1e`  
		Last Modified: Wed, 20 May 2026 00:29:51 GMT  
		Size: 42.1 MB (42126377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a835a41f8df1903759160d2c2aeae67eea461949d1169a93d6c70613f47898ef`  
		Last Modified: Wed, 20 May 2026 00:29:49 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326a3964c37889c39857c9e95d359d92c54ebdf6d615de3710bc8e19c59c8746`  
		Last Modified: Wed, 20 May 2026 00:29:49 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e618dbdd730d57b0c9b328ede82c564a9d45a87eccaad7389de602894afbb6`  
		Last Modified: Wed, 20 May 2026 00:29:50 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:628c5845f057d4e8959adc67895602974cd3553e6a251ca8068d81d1d1510061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31e8935915f60becdee0dc8e076487fff2a9a0d9383907275d50dd2d94bf4c18`

```dockerfile
```

-	Layers:
	-	`sha256:061b43c2b6fde2db35fd1335dc3a699611d39bac55c1a1b624e4a6960d453d23`  
		Last Modified: Wed, 20 May 2026 00:29:50 GMT  
		Size: 4.7 MB (4678151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea4c75c171fa8256e6c4c7ffae7f85bfbbdd87daebd41743aead9449110c203e`  
		Last Modified: Wed, 20 May 2026 00:29:49 GMT  
		Size: 16.5 KB (16529 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.12` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:fc922499dc0a946d413e0f8d23481bd01e9540caf47131d8e51649b0e9d4dcdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.8 MB (110750067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03b8de319bf50482a9916d294ab03a0dedaf358fadb657a210ee719f29a80d4d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:31:43 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Wed, 20 May 2026 00:31:49 GMT
ENV INFLUXDB_VERSION=1.12.4
# Wed, 20 May 2026 00:31:49 GMT
ENV INFLUXDB_PR=-1
# Wed, 20 May 2026 00:31:49 GMT
ENV INFLUXDB_PV=1.12.4-1
# Wed, 20 May 2026 00:31:49 GMT
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_PV}_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:31:49 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 20 May 2026 00:31:49 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 20 May 2026 00:31:49 GMT
VOLUME [/var/lib/influxdb]
# Wed, 20 May 2026 00:31:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:31:49 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 20 May 2026 00:31:49 GMT
USER influxdb
# Wed, 20 May 2026 00:31:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:31:49 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3daebbc198bd7b84bdd72840d7f4ded251896f03b9a9f880894e95e926bc543`  
		Last Modified: Tue, 19 May 2026 23:26:38 GMT  
		Size: 23.6 MB (23613394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12521174fcc638716b3ee36ba5034fc26f9f84615c5a373ac4500a87d417cffd`  
		Last Modified: Wed, 20 May 2026 00:32:00 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33dcd3bea41d053d3320da0f102557e1e6ad14ff3ce13efb489b553112122f0f`  
		Last Modified: Wed, 20 May 2026 00:32:01 GMT  
		Size: 38.8 MB (38754336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee4659542b6cbbedf8682f5bd1d227e58913636107fb54bc5601df3b00d8856`  
		Last Modified: Wed, 20 May 2026 00:32:00 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c72664a5db2c1d1b9cf55181797467ed7b29404adc1c7933bb4d9799f7c927`  
		Last Modified: Wed, 20 May 2026 00:32:00 GMT  
		Size: 207.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74d05d1d98041a739e75ef8b6af16805bd050917a93609c688a9708560c8a77`  
		Last Modified: Wed, 20 May 2026 00:32:02 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:2e42bd89d063ed8dafc685620648ea74b6c88a01af16f75e1fa612f5c5f377b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d66b0787788828ab4ef331bd5f9e0c28af22cd3558cf35c31e67565895e6efd6`

```dockerfile
```

-	Layers:
	-	`sha256:78e7da9818b2499203fa01c2819fb15ce2580acd4d45806a59704124cf2815ef`  
		Last Modified: Wed, 20 May 2026 00:32:00 GMT  
		Size: 4.7 MB (4677607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3860dc9befefff2f6bc7c084dfe8d0e2518dcb487573857d977cbc7c6a389415`  
		Last Modified: Wed, 20 May 2026 00:32:00 GMT  
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
$ docker pull influxdb@sha256:9319bb876d60b6611d7314e40ced0a9093badec94380fd788d26fd2ae2258e7f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12-data` - linux; amd64

```console
$ docker pull influxdb@sha256:579ca334f033a171c682d34b1c340d2fe8880c3dea2edb1b861f32cbd8a4ab9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115730454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c666f3a65cbb37594d2787f9802d5d13604d24770dd4ac72f6ff5254ed4f02`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:29:41 GMT
ENV INFLUXDB_VERSION=1.12.4-c1.12.4
# Wed, 20 May 2026 00:29:41 GMT
ENV INFLUXDB_PR=
# Wed, 20 May 2026 00:29:41 GMT
ENV INFLUXDB_PV=1.12.4-c1.12.4
# Wed, 20 May 2026 00:29:41 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"          -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"         "influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     rm -r "influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"           "influxdb-data_${INFLUXDB_PV}_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:29:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 20 May 2026 00:29:41 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 20 May 2026 00:29:41 GMT
VOLUME [/var/lib/influxdb]
# Wed, 20 May 2026 00:29:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:29:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 20 May 2026 00:29:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:29:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e51c50554dce9c9549d76c40bfea45780a8342aea81ba8b270ba1bf46a2aec5`  
		Last Modified: Tue, 19 May 2026 23:23:20 GMT  
		Size: 24.0 MB (24043374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122828ed9828493a392d3bbd9540521410cf9cf21e14801d4368427ab3cd94b3`  
		Last Modified: Wed, 20 May 2026 00:29:55 GMT  
		Size: 43.2 MB (43189878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de91331488774fe9e2d09549cd5a5d1e4d157b3accfc4f111eb66f7e8a78ec4`  
		Last Modified: Wed, 20 May 2026 00:29:54 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c650389a0929f427ce6e58d1ef4b9e97645e7409a49c8eae0691bb95ccf3d10`  
		Last Modified: Wed, 20 May 2026 00:29:54 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f5de10629d35972965ab74df4e979631016090bf6e698d40b7bfb3c9399125`  
		Last Modified: Wed, 20 May 2026 00:29:54 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:c0e349314838ec27086c03fedc8033ce30c3a691cfe1c4bb0d22ee06c43435d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4707295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb1fc2a0bec89acfd2cad38c8f018acc50a6fd978d2be2f8502e23fecf642dab`

```dockerfile
```

-	Layers:
	-	`sha256:5493b0b0c59fe03e660e43bf5164927cb17f7eaa8fb42fa6778eb7409226336c`  
		Last Modified: Wed, 20 May 2026 00:29:54 GMT  
		Size: 4.7 MB (4693141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3c95869539703cb6ec78b80a3a4fe4b11f4db2ccdf8b38cb792807c5a67dbe2`  
		Last Modified: Wed, 20 May 2026 00:29:54 GMT  
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
$ docker pull influxdb@sha256:eb1275d9a00d3d902dd398f2eff0c8255039191767cea04c0007f41b22500756
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:57a044b67fbcc59869345506b2c3e911a8f5f0917bbef96777c10469d6f82d1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91924518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b463ccdbb88aeddac659fe2cb6f4bf528d2fa31712966603f303ce742a8c90e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:29:46 GMT
ENV INFLUXDB_VERSION=1.12.4-c1.12.4
# Wed, 20 May 2026 00:29:46 GMT
ENV INFLUXDB_PR=
# Wed, 20 May 2026 00:29:46 GMT
ENV INFLUXDB_PV=1.12.4-c1.12.4
# Wed, 20 May 2026 00:29:46 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"          -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"         "influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     rm -r "influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"           "influxdb-meta_${INFLUXDB_PV}_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:29:46 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Wed, 20 May 2026 00:29:46 GMT
EXPOSE map[8091/tcp:{}]
# Wed, 20 May 2026 00:29:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 20 May 2026 00:29:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:29:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:29:46 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e51c50554dce9c9549d76c40bfea45780a8342aea81ba8b270ba1bf46a2aec5`  
		Last Modified: Tue, 19 May 2026 23:23:20 GMT  
		Size: 24.0 MB (24043374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231a6a12e39a684b8ef400973532085455b3543f371d1bb90f45442900340a6b`  
		Last Modified: Wed, 20 May 2026 00:29:56 GMT  
		Size: 19.4 MB (19385146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c88a42d2f3e78083f3422ab9fee7830022e74612847d646975dc0e445f467b`  
		Last Modified: Wed, 20 May 2026 00:29:55 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f6fcdeed90a4e263d4d42f8469c6a2f871ea40910010f73940c93664a9bd45`  
		Last Modified: Wed, 20 May 2026 00:29:55 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:6262a32495c2a4fff37a1137f8904b95d7aa4f6d6c66a4190ae73ae7052d82ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4605873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:517704ae2ac63a1323353df03f5108b0356a0a9eb2898e249df613a4d7cf2031`

```dockerfile
```

-	Layers:
	-	`sha256:0a7f7f23c71460ad60a701c4198a800a0f496f8dd4e1b4cc08f25b1ba5cfea80`  
		Last Modified: Wed, 20 May 2026 00:29:56 GMT  
		Size: 4.6 MB (4593209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:534a176d731bc426208fe21876a10f5f82a0dacb9772e2443aaeaaa1ecc6ed18`  
		Last Modified: Wed, 20 May 2026 00:29:56 GMT  
		Size: 12.7 KB (12664 bytes)  
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
$ docker pull influxdb@sha256:67e0b53c29cd4bd17d7633ad83399af86f8f131c063a785db4f7e3aa4d0a6bdf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.12.4` - linux; amd64

```console
$ docker pull influxdb@sha256:949e2f3b7b23e88c0f85f51a0f56b92f72f6fdb327ab185ec4299d515bc3d9ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114668090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd8876a6ed3b4c7e0602fe327f00f3a792017c4b6ff3c22a53daa11f41538dc1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:29:33 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Wed, 20 May 2026 00:29:38 GMT
ENV INFLUXDB_VERSION=1.12.4
# Wed, 20 May 2026 00:29:38 GMT
ENV INFLUXDB_PR=-1
# Wed, 20 May 2026 00:29:38 GMT
ENV INFLUXDB_PV=1.12.4-1
# Wed, 20 May 2026 00:29:38 GMT
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_PV}_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:29:38 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 20 May 2026 00:29:38 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 20 May 2026 00:29:38 GMT
VOLUME [/var/lib/influxdb]
# Wed, 20 May 2026 00:29:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:29:38 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 20 May 2026 00:29:38 GMT
USER influxdb
# Wed, 20 May 2026 00:29:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:29:38 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e51c50554dce9c9549d76c40bfea45780a8342aea81ba8b270ba1bf46a2aec5`  
		Last Modified: Tue, 19 May 2026 23:23:20 GMT  
		Size: 24.0 MB (24043374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300525e978958bc009f1604e662f5450d8601291957b031029e471ab910e8ae9`  
		Last Modified: Wed, 20 May 2026 00:29:49 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6dfe9783caa36ea1666ed94de8e4d3d620944c7165ffadca95a2bab3226c1e`  
		Last Modified: Wed, 20 May 2026 00:29:51 GMT  
		Size: 42.1 MB (42126377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a835a41f8df1903759160d2c2aeae67eea461949d1169a93d6c70613f47898ef`  
		Last Modified: Wed, 20 May 2026 00:29:49 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326a3964c37889c39857c9e95d359d92c54ebdf6d615de3710bc8e19c59c8746`  
		Last Modified: Wed, 20 May 2026 00:29:49 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e618dbdd730d57b0c9b328ede82c564a9d45a87eccaad7389de602894afbb6`  
		Last Modified: Wed, 20 May 2026 00:29:50 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.4` - unknown; unknown

```console
$ docker pull influxdb@sha256:628c5845f057d4e8959adc67895602974cd3553e6a251ca8068d81d1d1510061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31e8935915f60becdee0dc8e076487fff2a9a0d9383907275d50dd2d94bf4c18`

```dockerfile
```

-	Layers:
	-	`sha256:061b43c2b6fde2db35fd1335dc3a699611d39bac55c1a1b624e4a6960d453d23`  
		Last Modified: Wed, 20 May 2026 00:29:50 GMT  
		Size: 4.7 MB (4678151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea4c75c171fa8256e6c4c7ffae7f85bfbbdd87daebd41743aead9449110c203e`  
		Last Modified: Wed, 20 May 2026 00:29:49 GMT  
		Size: 16.5 KB (16529 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.12.4` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:fc922499dc0a946d413e0f8d23481bd01e9540caf47131d8e51649b0e9d4dcdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.8 MB (110750067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03b8de319bf50482a9916d294ab03a0dedaf358fadb657a210ee719f29a80d4d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:31:43 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Wed, 20 May 2026 00:31:49 GMT
ENV INFLUXDB_VERSION=1.12.4
# Wed, 20 May 2026 00:31:49 GMT
ENV INFLUXDB_PR=-1
# Wed, 20 May 2026 00:31:49 GMT
ENV INFLUXDB_PV=1.12.4-1
# Wed, 20 May 2026 00:31:49 GMT
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_PV}_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:31:49 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 20 May 2026 00:31:49 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 20 May 2026 00:31:49 GMT
VOLUME [/var/lib/influxdb]
# Wed, 20 May 2026 00:31:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:31:49 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 20 May 2026 00:31:49 GMT
USER influxdb
# Wed, 20 May 2026 00:31:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:31:49 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3daebbc198bd7b84bdd72840d7f4ded251896f03b9a9f880894e95e926bc543`  
		Last Modified: Tue, 19 May 2026 23:26:38 GMT  
		Size: 23.6 MB (23613394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12521174fcc638716b3ee36ba5034fc26f9f84615c5a373ac4500a87d417cffd`  
		Last Modified: Wed, 20 May 2026 00:32:00 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33dcd3bea41d053d3320da0f102557e1e6ad14ff3ce13efb489b553112122f0f`  
		Last Modified: Wed, 20 May 2026 00:32:01 GMT  
		Size: 38.8 MB (38754336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee4659542b6cbbedf8682f5bd1d227e58913636107fb54bc5601df3b00d8856`  
		Last Modified: Wed, 20 May 2026 00:32:00 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c72664a5db2c1d1b9cf55181797467ed7b29404adc1c7933bb4d9799f7c927`  
		Last Modified: Wed, 20 May 2026 00:32:00 GMT  
		Size: 207.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74d05d1d98041a739e75ef8b6af16805bd050917a93609c688a9708560c8a77`  
		Last Modified: Wed, 20 May 2026 00:32:02 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.4` - unknown; unknown

```console
$ docker pull influxdb@sha256:2e42bd89d063ed8dafc685620648ea74b6c88a01af16f75e1fa612f5c5f377b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d66b0787788828ab4ef331bd5f9e0c28af22cd3558cf35c31e67565895e6efd6`

```dockerfile
```

-	Layers:
	-	`sha256:78e7da9818b2499203fa01c2819fb15ce2580acd4d45806a59704124cf2815ef`  
		Last Modified: Wed, 20 May 2026 00:32:00 GMT  
		Size: 4.7 MB (4677607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3860dc9befefff2f6bc7c084dfe8d0e2518dcb487573857d977cbc7c6a389415`  
		Last Modified: Wed, 20 May 2026 00:32:00 GMT  
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
$ docker pull influxdb@sha256:9319bb876d60b6611d7314e40ced0a9093badec94380fd788d26fd2ae2258e7f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12.4-data` - linux; amd64

```console
$ docker pull influxdb@sha256:579ca334f033a171c682d34b1c340d2fe8880c3dea2edb1b861f32cbd8a4ab9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115730454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c666f3a65cbb37594d2787f9802d5d13604d24770dd4ac72f6ff5254ed4f02`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:29:41 GMT
ENV INFLUXDB_VERSION=1.12.4-c1.12.4
# Wed, 20 May 2026 00:29:41 GMT
ENV INFLUXDB_PR=
# Wed, 20 May 2026 00:29:41 GMT
ENV INFLUXDB_PV=1.12.4-c1.12.4
# Wed, 20 May 2026 00:29:41 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"          -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"         "influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     rm -r "influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"           "influxdb-data_${INFLUXDB_PV}_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:29:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 20 May 2026 00:29:41 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 20 May 2026 00:29:41 GMT
VOLUME [/var/lib/influxdb]
# Wed, 20 May 2026 00:29:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:29:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 20 May 2026 00:29:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:29:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e51c50554dce9c9549d76c40bfea45780a8342aea81ba8b270ba1bf46a2aec5`  
		Last Modified: Tue, 19 May 2026 23:23:20 GMT  
		Size: 24.0 MB (24043374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122828ed9828493a392d3bbd9540521410cf9cf21e14801d4368427ab3cd94b3`  
		Last Modified: Wed, 20 May 2026 00:29:55 GMT  
		Size: 43.2 MB (43189878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de91331488774fe9e2d09549cd5a5d1e4d157b3accfc4f111eb66f7e8a78ec4`  
		Last Modified: Wed, 20 May 2026 00:29:54 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c650389a0929f427ce6e58d1ef4b9e97645e7409a49c8eae0691bb95ccf3d10`  
		Last Modified: Wed, 20 May 2026 00:29:54 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f5de10629d35972965ab74df4e979631016090bf6e698d40b7bfb3c9399125`  
		Last Modified: Wed, 20 May 2026 00:29:54 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.4-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:c0e349314838ec27086c03fedc8033ce30c3a691cfe1c4bb0d22ee06c43435d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4707295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb1fc2a0bec89acfd2cad38c8f018acc50a6fd978d2be2f8502e23fecf642dab`

```dockerfile
```

-	Layers:
	-	`sha256:5493b0b0c59fe03e660e43bf5164927cb17f7eaa8fb42fa6778eb7409226336c`  
		Last Modified: Wed, 20 May 2026 00:29:54 GMT  
		Size: 4.7 MB (4693141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3c95869539703cb6ec78b80a3a4fe4b11f4db2ccdf8b38cb792807c5a67dbe2`  
		Last Modified: Wed, 20 May 2026 00:29:54 GMT  
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
$ docker pull influxdb@sha256:eb1275d9a00d3d902dd398f2eff0c8255039191767cea04c0007f41b22500756
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12.4-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:57a044b67fbcc59869345506b2c3e911a8f5f0917bbef96777c10469d6f82d1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91924518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b463ccdbb88aeddac659fe2cb6f4bf528d2fa31712966603f303ce742a8c90e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:29:46 GMT
ENV INFLUXDB_VERSION=1.12.4-c1.12.4
# Wed, 20 May 2026 00:29:46 GMT
ENV INFLUXDB_PR=
# Wed, 20 May 2026 00:29:46 GMT
ENV INFLUXDB_PV=1.12.4-c1.12.4
# Wed, 20 May 2026 00:29:46 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"          -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"         "influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     rm -r "influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"           "influxdb-meta_${INFLUXDB_PV}_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:29:46 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Wed, 20 May 2026 00:29:46 GMT
EXPOSE map[8091/tcp:{}]
# Wed, 20 May 2026 00:29:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 20 May 2026 00:29:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:29:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:29:46 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e51c50554dce9c9549d76c40bfea45780a8342aea81ba8b270ba1bf46a2aec5`  
		Last Modified: Tue, 19 May 2026 23:23:20 GMT  
		Size: 24.0 MB (24043374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231a6a12e39a684b8ef400973532085455b3543f371d1bb90f45442900340a6b`  
		Last Modified: Wed, 20 May 2026 00:29:56 GMT  
		Size: 19.4 MB (19385146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c88a42d2f3e78083f3422ab9fee7830022e74612847d646975dc0e445f467b`  
		Last Modified: Wed, 20 May 2026 00:29:55 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f6fcdeed90a4e263d4d42f8469c6a2f871ea40910010f73940c93664a9bd45`  
		Last Modified: Wed, 20 May 2026 00:29:55 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.4-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:6262a32495c2a4fff37a1137f8904b95d7aa4f6d6c66a4190ae73ae7052d82ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4605873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:517704ae2ac63a1323353df03f5108b0356a0a9eb2898e249df613a4d7cf2031`

```dockerfile
```

-	Layers:
	-	`sha256:0a7f7f23c71460ad60a701c4198a800a0f496f8dd4e1b4cc08f25b1ba5cfea80`  
		Last Modified: Wed, 20 May 2026 00:29:56 GMT  
		Size: 4.6 MB (4593209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:534a176d731bc426208fe21876a10f5f82a0dacb9772e2443aaeaaa1ecc6ed18`  
		Last Modified: Wed, 20 May 2026 00:29:56 GMT  
		Size: 12.7 KB (12664 bytes)  
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
$ docker pull influxdb@sha256:c9acb506f536915c97ff71c971970ad9c2a38b2b8a0d54200ef0ef430f7a37f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2` - linux; amd64

```console
$ docker pull influxdb@sha256:a6f9bf39c55260644b8d92fda430cdb035553e240e9457fcb7e688714ddd58a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.8 MB (110799736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06abeab9b64ea2bcd9a872dbcfbae45956540fd9e5dda9126d43dd9df66536d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:24:55 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg       util-linux &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:24:55 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Tue, 19 May 2026 23:24:56 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 19 May 2026 23:24:58 GMT
ENV INFLUXDB_VERSION=2.9.1
# Tue, 19 May 2026 23:24:58 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 19 May 2026 23:24:58 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Tue, 19 May 2026 23:25:00 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 19 May 2026 23:25:00 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 19 May 2026 23:25:00 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 19 May 2026 23:25:00 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 19 May 2026 23:25:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 May 2026 23:25:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 May 2026 23:25:00 GMT
CMD ["influxd"]
# Tue, 19 May 2026 23:25:00 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 19 May 2026 23:25:00 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 19 May 2026 23:25:00 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 19 May 2026 23:25:00 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 19 May 2026 23:25:00 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c71a21b19bd6c649ea1e324c4d701c55fb5dad2603879df10dc7afaa323d50`  
		Last Modified: Tue, 19 May 2026 23:25:13 GMT  
		Size: 9.8 MB (9800832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717bcf11cb3cc23b0cff75de4a1c15cc7d26323472f95ba3479c845395c59fb1`  
		Last Modified: Tue, 19 May 2026 23:25:12 GMT  
		Size: 3.8 MB (3822787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0d6975a8cc10b47a2b313757955d26198aef78ac28389bf2f456e96f320ca6`  
		Last Modified: Tue, 19 May 2026 23:25:12 GMT  
		Size: 3.2 KB (3235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41371aff054c12f24015975eb32925ecdbe6cd9dabd561244871778f50a16d2b`  
		Last Modified: Tue, 19 May 2026 23:25:14 GMT  
		Size: 56.5 MB (56510574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90cd044c089a7210079f32826689d04869dbaff450297593e1f61877e9d1847`  
		Last Modified: Tue, 19 May 2026 23:25:14 GMT  
		Size: 12.4 MB (12421825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46d8268bc61e87ea71b79fade2d60c9d8f0884a4858f1f24593ca1f188c133b`  
		Last Modified: Tue, 19 May 2026 23:25:14 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9374c3e54ff0378b9306cccc8b9ca7b75fed4a52791bca44370842bc8aa395`  
		Last Modified: Tue, 19 May 2026 23:25:14 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15861eb3c0e7ac9aa7eebb79d91dc4503d36d432b5391d5c79e420b2d8059a64`  
		Last Modified: Tue, 19 May 2026 23:25:15 GMT  
		Size: 6.5 KB (6497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:4cd7dd0ab43920355f0ee88d7fb4896b9243fd07caa0842158c88d9c4af127f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2988043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b77346806c1383c545a78b619c7d6eb2d4d5b513519152c2a4c83484e338a456`

```dockerfile
```

-	Layers:
	-	`sha256:b3126195e2521ecbed67a65602733863692c0969bcfdbd618638132dbebfaead`  
		Last Modified: Tue, 19 May 2026 23:25:12 GMT  
		Size: 3.0 MB (2959429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b288657180483275616cb5620206f8d0a09327d49de6dc37fab5eaeb3b38c28b`  
		Last Modified: Tue, 19 May 2026 23:25:12 GMT  
		Size: 28.6 KB (28614 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:d6fc942f1fae5ff590d663642865f594b48a0756071c498be8eb38b0d6770574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106330815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea2fc64efaf734880bc89ce2fed2ad2396ea48636bcd90f7b135f7e85fefd70f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:28:14 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg       util-linux &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:28:15 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Tue, 19 May 2026 23:28:15 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 19 May 2026 23:28:18 GMT
ENV INFLUXDB_VERSION=2.9.1
# Tue, 19 May 2026 23:28:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 19 May 2026 23:28:18 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Tue, 19 May 2026 23:28:19 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 19 May 2026 23:28:20 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 19 May 2026 23:28:20 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 19 May 2026 23:28:20 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 19 May 2026 23:28:20 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 May 2026 23:28:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 May 2026 23:28:20 GMT
CMD ["influxd"]
# Tue, 19 May 2026 23:28:20 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 19 May 2026 23:28:20 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 19 May 2026 23:28:20 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 19 May 2026 23:28:20 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 19 May 2026 23:28:20 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a3e4fdf0759b602cc83eee55bb98191a184bf47394c125416bad56fd14cf2e`  
		Last Modified: Tue, 19 May 2026 23:28:31 GMT  
		Size: 9.6 MB (9629316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69d1631bd9b1dc8d27a448997e0d90af077c96a2041f16eb89751cd7a188383`  
		Last Modified: Tue, 19 May 2026 23:28:31 GMT  
		Size: 3.5 MB (3459173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3843f9e7c58fc79d623603a0448fe5eb8b646c9acb86278e08024e28e90e6e1a`  
		Last Modified: Tue, 19 May 2026 23:28:31 GMT  
		Size: 3.2 KB (3227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b748a12a94328f10d7c957a9ef02934ab7b468161e7f3274c68923d716de920d`  
		Last Modified: Tue, 19 May 2026 23:28:33 GMT  
		Size: 53.6 MB (53636820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40bad5774d9135c6e7eabc80742652a79641e86bd6a0f05b13a385c47764bc20`  
		Last Modified: Tue, 19 May 2026 23:28:32 GMT  
		Size: 11.5 MB (11480296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e4221fc8c1ab93c69cafbc88cb0214ea6877c204266846e6add1891ea58a891`  
		Last Modified: Tue, 19 May 2026 23:28:32 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129703821150bfc0ff6995ffa921aaca455ba27668ec104ae6ff73b58cfbba8c`  
		Last Modified: Tue, 19 May 2026 23:28:32 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7424fffba09e6f72ae806428342ccfd9cf858d0dfa3e1acbf6111cf5603a85fe`  
		Last Modified: Tue, 19 May 2026 23:28:33 GMT  
		Size: 6.5 KB (6499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:ba793f9c250c21d96c0eccc2bf682b93706548fcc7def232da980c3ce77bd9b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca7a7141b9565f983497bde826dc595445dbd26abef6d664c30cd7d78280717f`

```dockerfile
```

-	Layers:
	-	`sha256:b176ade03bf084e3c8722d038d297af9345b5ff626542e7bb237a7adc6b1b5aa`  
		Last Modified: Tue, 19 May 2026 23:28:31 GMT  
		Size: 3.0 MB (2958907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a53002c50db871c40a28faf2f74b6de4d013e714ecc96cbbfcbc68704f320026`  
		Last Modified: Tue, 19 May 2026 23:28:31 GMT  
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
$ docker pull influxdb@sha256:e3e7ee6476007edc0577e9114c78028112e92e48ead3545865d35187cd9a5eda
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.8` - linux; amd64

```console
$ docker pull influxdb@sha256:e0748f1c9ac1b5aa31284131f1578837f14df2d6a49add0fb3f3fb7ddd600214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107240537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d53a1e67679b448f53023064effe1d3734a83f717508bc352982771d5cf5780`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:24:38 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:24:39 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 19 May 2026 23:24:39 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 19 May 2026 23:24:40 GMT
ENV GOSU_VER=1.19
# Tue, 19 May 2026 23:24:40 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 19 May 2026 23:24:40 GMT
ENV INFLUXDB_VERSION=2.8.0
# Tue, 19 May 2026 23:24:40 GMT
ENV INFLUXDB_PR=-2
# Tue, 19 May 2026 23:24:40 GMT
ENV INFLUXDB_PV=2.8.0-2
# Tue, 19 May 2026 23:24:43 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 19 May 2026 23:24:43 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 19 May 2026 23:24:44 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 19 May 2026 23:24:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 19 May 2026 23:24:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 19 May 2026 23:24:45 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 19 May 2026 23:24:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 May 2026 23:24:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 May 2026 23:24:45 GMT
CMD ["influxd"]
# Tue, 19 May 2026 23:24:45 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 19 May 2026 23:24:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 19 May 2026 23:24:45 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 19 May 2026 23:24:45 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 19 May 2026 23:24:45 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e5d12c6dd969145911fae915d76edd102e60a6860a938ac79f015de2584856`  
		Last Modified: Tue, 19 May 2026 23:24:57 GMT  
		Size: 9.8 MB (9800878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0e730458f6901c3a76665ef2df9354c666d64a0c8e90ce98675d3a693d9973`  
		Last Modified: Tue, 19 May 2026 23:24:57 GMT  
		Size: 6.2 MB (6156987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5353d7907bb719af55f3d2c731f2918052b7a5ebd34c8abb5328ffb8cbce0b`  
		Last Modified: Tue, 19 May 2026 23:24:56 GMT  
		Size: 3.2 KB (3230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:052a614289a5ed934350b9bd416e5e1173182416fa6681bae3430c8c49143d64`  
		Last Modified: Tue, 19 May 2026 23:24:56 GMT  
		Size: 811.5 KB (811478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e22e845481dd6b6fd1b55c5861b1fadcf4cf4b1d0e4ce59b1f9772bd2fd71c0`  
		Last Modified: Tue, 19 May 2026 23:24:59 GMT  
		Size: 50.5 MB (50451820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c9b5f15ba22a5e5c0b7a7b56859a2b9d5aeedc2f00372530f7266cfa0e260f`  
		Last Modified: Tue, 19 May 2026 23:24:58 GMT  
		Size: 11.8 MB (11775871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ae5ddc70b016958e3141531da4aab65e35dd1678fd88bfbf46fe0da8f5b0a3`  
		Last Modified: Tue, 19 May 2026 23:24:58 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e37bb687da9bad85e40934fbbaad1263c8ba6ad83e61fc0ac40f9ea66f0a748`  
		Last Modified: Tue, 19 May 2026 23:24:58 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2656cf71b3edd5cefb78c9b26e753636817e07be03a195e27c0de982e2dc616`  
		Last Modified: Tue, 19 May 2026 23:24:59 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:c3fcaf7e4924ff0b2d69020af7738f2e39c6021b4c675f9612314bd56cb565c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2966688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6621518eb9a248b769ddbcfb2ad19377283bb774a430a02ae0017a96dcf2583d`

```dockerfile
```

-	Layers:
	-	`sha256:1ba5923db566df9d998e6d02fbf63a42708e560ea67e0b741abcfc8361c7f0b0`  
		Last Modified: Tue, 19 May 2026 23:24:56 GMT  
		Size: 2.9 MB (2933661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ceacf3841c0ff564df7e20d883c579696cbb901e9a954f0ccbf1a5b4dd411f92`  
		Last Modified: Tue, 19 May 2026 23:24:56 GMT  
		Size: 33.0 KB (33027 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:f29ad5d197f4f347febe490a45cd8784f0a13d794ebce3cc6d1299ef2436fc58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103641016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d966bd63c5d9d97e54c46e79e2106df64f4776435f5551e81a2d8989d72d333d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:28:14 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:28:15 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 19 May 2026 23:28:15 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 19 May 2026 23:28:16 GMT
ENV GOSU_VER=1.19
# Tue, 19 May 2026 23:28:16 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 19 May 2026 23:28:16 GMT
ENV INFLUXDB_VERSION=2.8.0
# Tue, 19 May 2026 23:28:16 GMT
ENV INFLUXDB_PR=-2
# Tue, 19 May 2026 23:28:16 GMT
ENV INFLUXDB_PV=2.8.0-2
# Tue, 19 May 2026 23:28:19 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 19 May 2026 23:28:19 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 19 May 2026 23:28:21 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 19 May 2026 23:28:21 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 19 May 2026 23:28:21 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 19 May 2026 23:28:21 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 19 May 2026 23:28:21 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 May 2026 23:28:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 May 2026 23:28:21 GMT
CMD ["influxd"]
# Tue, 19 May 2026 23:28:21 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 19 May 2026 23:28:21 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 19 May 2026 23:28:21 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 19 May 2026 23:28:21 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 19 May 2026 23:28:21 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1171077eae0c65e97236090e15f5e2956ce7a1e983290c6ca3e3f98eb8d41422`  
		Last Modified: Tue, 19 May 2026 23:28:31 GMT  
		Size: 9.6 MB (9629303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb52ee1ec12ede3fad76db17206195cf6cd586935f42e83a926c7bfd0e875a89`  
		Last Modified: Tue, 19 May 2026 23:28:31 GMT  
		Size: 5.8 MB (5790415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3843f9e7c58fc79d623603a0448fe5eb8b646c9acb86278e08024e28e90e6e1a`  
		Last Modified: Tue, 19 May 2026 23:28:31 GMT  
		Size: 3.2 KB (3227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3a4bdd7e03d9a1f7abdd3b3cab2eff1dea6591c281cf92affb864105893880`  
		Last Modified: Tue, 19 May 2026 23:28:31 GMT  
		Size: 766.4 KB (766373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8edcd831045a7aab8bb482b80ee511b3eb54b5446cfe139b1b078f49a39794ef`  
		Last Modified: Tue, 19 May 2026 23:28:33 GMT  
		Size: 48.2 MB (48229548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b1a60cf6b9e7a044609057cc08e6206c19a4b64b83949836f237ba6064032e`  
		Last Modified: Tue, 19 May 2026 23:28:33 GMT  
		Size: 11.1 MB (11100379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c097f884af83e415cce15751e2cc0a58770650fe74614aa55954e457e57041c`  
		Last Modified: Tue, 19 May 2026 23:28:33 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b99ec4f6285a23aca0579bca06393ff6195e0299ccc0f30648dbe487ca235c`  
		Last Modified: Tue, 19 May 2026 23:28:33 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549cfc61bdf91571c70d20a186217f821c8d44fa22fc4d0b5ba997e3d25b7464`  
		Last Modified: Tue, 19 May 2026 23:28:34 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:ef11a6c58c724392a8c240f310e7b3fdab64e7c547b9d49d7cf237d9a80235a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2966314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2b974b8f96465e52b757bd13b0042502cc1c4ee06079302df2f363d821191cc`

```dockerfile
```

-	Layers:
	-	`sha256:6adf10a69785902404386f887f81c6e9ddde1819a2f97371e363ca21fe5e7201`  
		Last Modified: Tue, 19 May 2026 23:28:31 GMT  
		Size: 2.9 MB (2933117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6cfbc57127f46060e7a4345cdfda534a3359581314de467ee0543e8fe3dc15e`  
		Last Modified: Tue, 19 May 2026 23:28:31 GMT  
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
$ docker pull influxdb@sha256:e3e7ee6476007edc0577e9114c78028112e92e48ead3545865d35187cd9a5eda
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.8.0` - linux; amd64

```console
$ docker pull influxdb@sha256:e0748f1c9ac1b5aa31284131f1578837f14df2d6a49add0fb3f3fb7ddd600214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107240537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d53a1e67679b448f53023064effe1d3734a83f717508bc352982771d5cf5780`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:24:38 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:24:39 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 19 May 2026 23:24:39 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 19 May 2026 23:24:40 GMT
ENV GOSU_VER=1.19
# Tue, 19 May 2026 23:24:40 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 19 May 2026 23:24:40 GMT
ENV INFLUXDB_VERSION=2.8.0
# Tue, 19 May 2026 23:24:40 GMT
ENV INFLUXDB_PR=-2
# Tue, 19 May 2026 23:24:40 GMT
ENV INFLUXDB_PV=2.8.0-2
# Tue, 19 May 2026 23:24:43 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 19 May 2026 23:24:43 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 19 May 2026 23:24:44 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 19 May 2026 23:24:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 19 May 2026 23:24:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 19 May 2026 23:24:45 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 19 May 2026 23:24:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 May 2026 23:24:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 May 2026 23:24:45 GMT
CMD ["influxd"]
# Tue, 19 May 2026 23:24:45 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 19 May 2026 23:24:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 19 May 2026 23:24:45 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 19 May 2026 23:24:45 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 19 May 2026 23:24:45 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e5d12c6dd969145911fae915d76edd102e60a6860a938ac79f015de2584856`  
		Last Modified: Tue, 19 May 2026 23:24:57 GMT  
		Size: 9.8 MB (9800878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0e730458f6901c3a76665ef2df9354c666d64a0c8e90ce98675d3a693d9973`  
		Last Modified: Tue, 19 May 2026 23:24:57 GMT  
		Size: 6.2 MB (6156987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5353d7907bb719af55f3d2c731f2918052b7a5ebd34c8abb5328ffb8cbce0b`  
		Last Modified: Tue, 19 May 2026 23:24:56 GMT  
		Size: 3.2 KB (3230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:052a614289a5ed934350b9bd416e5e1173182416fa6681bae3430c8c49143d64`  
		Last Modified: Tue, 19 May 2026 23:24:56 GMT  
		Size: 811.5 KB (811478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e22e845481dd6b6fd1b55c5861b1fadcf4cf4b1d0e4ce59b1f9772bd2fd71c0`  
		Last Modified: Tue, 19 May 2026 23:24:59 GMT  
		Size: 50.5 MB (50451820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c9b5f15ba22a5e5c0b7a7b56859a2b9d5aeedc2f00372530f7266cfa0e260f`  
		Last Modified: Tue, 19 May 2026 23:24:58 GMT  
		Size: 11.8 MB (11775871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ae5ddc70b016958e3141531da4aab65e35dd1678fd88bfbf46fe0da8f5b0a3`  
		Last Modified: Tue, 19 May 2026 23:24:58 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e37bb687da9bad85e40934fbbaad1263c8ba6ad83e61fc0ac40f9ea66f0a748`  
		Last Modified: Tue, 19 May 2026 23:24:58 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2656cf71b3edd5cefb78c9b26e753636817e07be03a195e27c0de982e2dc616`  
		Last Modified: Tue, 19 May 2026 23:24:59 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8.0` - unknown; unknown

```console
$ docker pull influxdb@sha256:c3fcaf7e4924ff0b2d69020af7738f2e39c6021b4c675f9612314bd56cb565c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2966688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6621518eb9a248b769ddbcfb2ad19377283bb774a430a02ae0017a96dcf2583d`

```dockerfile
```

-	Layers:
	-	`sha256:1ba5923db566df9d998e6d02fbf63a42708e560ea67e0b741abcfc8361c7f0b0`  
		Last Modified: Tue, 19 May 2026 23:24:56 GMT  
		Size: 2.9 MB (2933661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ceacf3841c0ff564df7e20d883c579696cbb901e9a954f0ccbf1a5b4dd411f92`  
		Last Modified: Tue, 19 May 2026 23:24:56 GMT  
		Size: 33.0 KB (33027 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.8.0` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:f29ad5d197f4f347febe490a45cd8784f0a13d794ebce3cc6d1299ef2436fc58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103641016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d966bd63c5d9d97e54c46e79e2106df64f4776435f5551e81a2d8989d72d333d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:28:14 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:28:15 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 19 May 2026 23:28:15 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 19 May 2026 23:28:16 GMT
ENV GOSU_VER=1.19
# Tue, 19 May 2026 23:28:16 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 19 May 2026 23:28:16 GMT
ENV INFLUXDB_VERSION=2.8.0
# Tue, 19 May 2026 23:28:16 GMT
ENV INFLUXDB_PR=-2
# Tue, 19 May 2026 23:28:16 GMT
ENV INFLUXDB_PV=2.8.0-2
# Tue, 19 May 2026 23:28:19 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 19 May 2026 23:28:19 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 19 May 2026 23:28:21 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 19 May 2026 23:28:21 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 19 May 2026 23:28:21 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 19 May 2026 23:28:21 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 19 May 2026 23:28:21 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 May 2026 23:28:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 May 2026 23:28:21 GMT
CMD ["influxd"]
# Tue, 19 May 2026 23:28:21 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 19 May 2026 23:28:21 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 19 May 2026 23:28:21 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 19 May 2026 23:28:21 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 19 May 2026 23:28:21 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1171077eae0c65e97236090e15f5e2956ce7a1e983290c6ca3e3f98eb8d41422`  
		Last Modified: Tue, 19 May 2026 23:28:31 GMT  
		Size: 9.6 MB (9629303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb52ee1ec12ede3fad76db17206195cf6cd586935f42e83a926c7bfd0e875a89`  
		Last Modified: Tue, 19 May 2026 23:28:31 GMT  
		Size: 5.8 MB (5790415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3843f9e7c58fc79d623603a0448fe5eb8b646c9acb86278e08024e28e90e6e1a`  
		Last Modified: Tue, 19 May 2026 23:28:31 GMT  
		Size: 3.2 KB (3227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3a4bdd7e03d9a1f7abdd3b3cab2eff1dea6591c281cf92affb864105893880`  
		Last Modified: Tue, 19 May 2026 23:28:31 GMT  
		Size: 766.4 KB (766373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8edcd831045a7aab8bb482b80ee511b3eb54b5446cfe139b1b078f49a39794ef`  
		Last Modified: Tue, 19 May 2026 23:28:33 GMT  
		Size: 48.2 MB (48229548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b1a60cf6b9e7a044609057cc08e6206c19a4b64b83949836f237ba6064032e`  
		Last Modified: Tue, 19 May 2026 23:28:33 GMT  
		Size: 11.1 MB (11100379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c097f884af83e415cce15751e2cc0a58770650fe74614aa55954e457e57041c`  
		Last Modified: Tue, 19 May 2026 23:28:33 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b99ec4f6285a23aca0579bca06393ff6195e0299ccc0f30648dbe487ca235c`  
		Last Modified: Tue, 19 May 2026 23:28:33 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549cfc61bdf91571c70d20a186217f821c8d44fa22fc4d0b5ba997e3d25b7464`  
		Last Modified: Tue, 19 May 2026 23:28:34 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8.0` - unknown; unknown

```console
$ docker pull influxdb@sha256:ef11a6c58c724392a8c240f310e7b3fdab64e7c547b9d49d7cf237d9a80235a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2966314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2b974b8f96465e52b757bd13b0042502cc1c4ee06079302df2f363d821191cc`

```dockerfile
```

-	Layers:
	-	`sha256:6adf10a69785902404386f887f81c6e9ddde1819a2f97371e363ca21fe5e7201`  
		Last Modified: Tue, 19 May 2026 23:28:31 GMT  
		Size: 2.9 MB (2933117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6cfbc57127f46060e7a4345cdfda534a3359581314de467ee0543e8fe3dc15e`  
		Last Modified: Tue, 19 May 2026 23:28:31 GMT  
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
$ docker pull influxdb@sha256:c9acb506f536915c97ff71c971970ad9c2a38b2b8a0d54200ef0ef430f7a37f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.9` - linux; amd64

```console
$ docker pull influxdb@sha256:a6f9bf39c55260644b8d92fda430cdb035553e240e9457fcb7e688714ddd58a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.8 MB (110799736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06abeab9b64ea2bcd9a872dbcfbae45956540fd9e5dda9126d43dd9df66536d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:24:55 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg       util-linux &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:24:55 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Tue, 19 May 2026 23:24:56 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 19 May 2026 23:24:58 GMT
ENV INFLUXDB_VERSION=2.9.1
# Tue, 19 May 2026 23:24:58 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 19 May 2026 23:24:58 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Tue, 19 May 2026 23:25:00 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 19 May 2026 23:25:00 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 19 May 2026 23:25:00 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 19 May 2026 23:25:00 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 19 May 2026 23:25:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 May 2026 23:25:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 May 2026 23:25:00 GMT
CMD ["influxd"]
# Tue, 19 May 2026 23:25:00 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 19 May 2026 23:25:00 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 19 May 2026 23:25:00 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 19 May 2026 23:25:00 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 19 May 2026 23:25:00 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c71a21b19bd6c649ea1e324c4d701c55fb5dad2603879df10dc7afaa323d50`  
		Last Modified: Tue, 19 May 2026 23:25:13 GMT  
		Size: 9.8 MB (9800832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717bcf11cb3cc23b0cff75de4a1c15cc7d26323472f95ba3479c845395c59fb1`  
		Last Modified: Tue, 19 May 2026 23:25:12 GMT  
		Size: 3.8 MB (3822787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0d6975a8cc10b47a2b313757955d26198aef78ac28389bf2f456e96f320ca6`  
		Last Modified: Tue, 19 May 2026 23:25:12 GMT  
		Size: 3.2 KB (3235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41371aff054c12f24015975eb32925ecdbe6cd9dabd561244871778f50a16d2b`  
		Last Modified: Tue, 19 May 2026 23:25:14 GMT  
		Size: 56.5 MB (56510574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90cd044c089a7210079f32826689d04869dbaff450297593e1f61877e9d1847`  
		Last Modified: Tue, 19 May 2026 23:25:14 GMT  
		Size: 12.4 MB (12421825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46d8268bc61e87ea71b79fade2d60c9d8f0884a4858f1f24593ca1f188c133b`  
		Last Modified: Tue, 19 May 2026 23:25:14 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9374c3e54ff0378b9306cccc8b9ca7b75fed4a52791bca44370842bc8aa395`  
		Last Modified: Tue, 19 May 2026 23:25:14 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15861eb3c0e7ac9aa7eebb79d91dc4503d36d432b5391d5c79e420b2d8059a64`  
		Last Modified: Tue, 19 May 2026 23:25:15 GMT  
		Size: 6.5 KB (6497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.9` - unknown; unknown

```console
$ docker pull influxdb@sha256:4cd7dd0ab43920355f0ee88d7fb4896b9243fd07caa0842158c88d9c4af127f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2988043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b77346806c1383c545a78b619c7d6eb2d4d5b513519152c2a4c83484e338a456`

```dockerfile
```

-	Layers:
	-	`sha256:b3126195e2521ecbed67a65602733863692c0969bcfdbd618638132dbebfaead`  
		Last Modified: Tue, 19 May 2026 23:25:12 GMT  
		Size: 3.0 MB (2959429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b288657180483275616cb5620206f8d0a09327d49de6dc37fab5eaeb3b38c28b`  
		Last Modified: Tue, 19 May 2026 23:25:12 GMT  
		Size: 28.6 KB (28614 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.9` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:d6fc942f1fae5ff590d663642865f594b48a0756071c498be8eb38b0d6770574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106330815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea2fc64efaf734880bc89ce2fed2ad2396ea48636bcd90f7b135f7e85fefd70f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:28:14 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg       util-linux &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:28:15 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Tue, 19 May 2026 23:28:15 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 19 May 2026 23:28:18 GMT
ENV INFLUXDB_VERSION=2.9.1
# Tue, 19 May 2026 23:28:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 19 May 2026 23:28:18 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Tue, 19 May 2026 23:28:19 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 19 May 2026 23:28:20 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 19 May 2026 23:28:20 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 19 May 2026 23:28:20 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 19 May 2026 23:28:20 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 May 2026 23:28:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 May 2026 23:28:20 GMT
CMD ["influxd"]
# Tue, 19 May 2026 23:28:20 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 19 May 2026 23:28:20 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 19 May 2026 23:28:20 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 19 May 2026 23:28:20 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 19 May 2026 23:28:20 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a3e4fdf0759b602cc83eee55bb98191a184bf47394c125416bad56fd14cf2e`  
		Last Modified: Tue, 19 May 2026 23:28:31 GMT  
		Size: 9.6 MB (9629316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69d1631bd9b1dc8d27a448997e0d90af077c96a2041f16eb89751cd7a188383`  
		Last Modified: Tue, 19 May 2026 23:28:31 GMT  
		Size: 3.5 MB (3459173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3843f9e7c58fc79d623603a0448fe5eb8b646c9acb86278e08024e28e90e6e1a`  
		Last Modified: Tue, 19 May 2026 23:28:31 GMT  
		Size: 3.2 KB (3227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b748a12a94328f10d7c957a9ef02934ab7b468161e7f3274c68923d716de920d`  
		Last Modified: Tue, 19 May 2026 23:28:33 GMT  
		Size: 53.6 MB (53636820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40bad5774d9135c6e7eabc80742652a79641e86bd6a0f05b13a385c47764bc20`  
		Last Modified: Tue, 19 May 2026 23:28:32 GMT  
		Size: 11.5 MB (11480296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e4221fc8c1ab93c69cafbc88cb0214ea6877c204266846e6add1891ea58a891`  
		Last Modified: Tue, 19 May 2026 23:28:32 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129703821150bfc0ff6995ffa921aaca455ba27668ec104ae6ff73b58cfbba8c`  
		Last Modified: Tue, 19 May 2026 23:28:32 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7424fffba09e6f72ae806428342ccfd9cf858d0dfa3e1acbf6111cf5603a85fe`  
		Last Modified: Tue, 19 May 2026 23:28:33 GMT  
		Size: 6.5 KB (6499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.9` - unknown; unknown

```console
$ docker pull influxdb@sha256:ba793f9c250c21d96c0eccc2bf682b93706548fcc7def232da980c3ce77bd9b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca7a7141b9565f983497bde826dc595445dbd26abef6d664c30cd7d78280717f`

```dockerfile
```

-	Layers:
	-	`sha256:b176ade03bf084e3c8722d038d297af9345b5ff626542e7bb237a7adc6b1b5aa`  
		Last Modified: Tue, 19 May 2026 23:28:31 GMT  
		Size: 3.0 MB (2958907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a53002c50db871c40a28faf2f74b6de4d013e714ecc96cbbfcbc68704f320026`  
		Last Modified: Tue, 19 May 2026 23:28:31 GMT  
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
$ docker pull influxdb@sha256:c9acb506f536915c97ff71c971970ad9c2a38b2b8a0d54200ef0ef430f7a37f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.9.1` - linux; amd64

```console
$ docker pull influxdb@sha256:a6f9bf39c55260644b8d92fda430cdb035553e240e9457fcb7e688714ddd58a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.8 MB (110799736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06abeab9b64ea2bcd9a872dbcfbae45956540fd9e5dda9126d43dd9df66536d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:24:55 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg       util-linux &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:24:55 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Tue, 19 May 2026 23:24:56 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 19 May 2026 23:24:58 GMT
ENV INFLUXDB_VERSION=2.9.1
# Tue, 19 May 2026 23:24:58 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 19 May 2026 23:24:58 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Tue, 19 May 2026 23:25:00 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 19 May 2026 23:25:00 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 19 May 2026 23:25:00 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 19 May 2026 23:25:00 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 19 May 2026 23:25:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 May 2026 23:25:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 May 2026 23:25:00 GMT
CMD ["influxd"]
# Tue, 19 May 2026 23:25:00 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 19 May 2026 23:25:00 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 19 May 2026 23:25:00 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 19 May 2026 23:25:00 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 19 May 2026 23:25:00 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c71a21b19bd6c649ea1e324c4d701c55fb5dad2603879df10dc7afaa323d50`  
		Last Modified: Tue, 19 May 2026 23:25:13 GMT  
		Size: 9.8 MB (9800832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717bcf11cb3cc23b0cff75de4a1c15cc7d26323472f95ba3479c845395c59fb1`  
		Last Modified: Tue, 19 May 2026 23:25:12 GMT  
		Size: 3.8 MB (3822787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0d6975a8cc10b47a2b313757955d26198aef78ac28389bf2f456e96f320ca6`  
		Last Modified: Tue, 19 May 2026 23:25:12 GMT  
		Size: 3.2 KB (3235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41371aff054c12f24015975eb32925ecdbe6cd9dabd561244871778f50a16d2b`  
		Last Modified: Tue, 19 May 2026 23:25:14 GMT  
		Size: 56.5 MB (56510574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90cd044c089a7210079f32826689d04869dbaff450297593e1f61877e9d1847`  
		Last Modified: Tue, 19 May 2026 23:25:14 GMT  
		Size: 12.4 MB (12421825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46d8268bc61e87ea71b79fade2d60c9d8f0884a4858f1f24593ca1f188c133b`  
		Last Modified: Tue, 19 May 2026 23:25:14 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9374c3e54ff0378b9306cccc8b9ca7b75fed4a52791bca44370842bc8aa395`  
		Last Modified: Tue, 19 May 2026 23:25:14 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15861eb3c0e7ac9aa7eebb79d91dc4503d36d432b5391d5c79e420b2d8059a64`  
		Last Modified: Tue, 19 May 2026 23:25:15 GMT  
		Size: 6.5 KB (6497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.9.1` - unknown; unknown

```console
$ docker pull influxdb@sha256:4cd7dd0ab43920355f0ee88d7fb4896b9243fd07caa0842158c88d9c4af127f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2988043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b77346806c1383c545a78b619c7d6eb2d4d5b513519152c2a4c83484e338a456`

```dockerfile
```

-	Layers:
	-	`sha256:b3126195e2521ecbed67a65602733863692c0969bcfdbd618638132dbebfaead`  
		Last Modified: Tue, 19 May 2026 23:25:12 GMT  
		Size: 3.0 MB (2959429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b288657180483275616cb5620206f8d0a09327d49de6dc37fab5eaeb3b38c28b`  
		Last Modified: Tue, 19 May 2026 23:25:12 GMT  
		Size: 28.6 KB (28614 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.9.1` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:d6fc942f1fae5ff590d663642865f594b48a0756071c498be8eb38b0d6770574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106330815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea2fc64efaf734880bc89ce2fed2ad2396ea48636bcd90f7b135f7e85fefd70f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:28:14 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg       util-linux &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:28:15 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Tue, 19 May 2026 23:28:15 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 19 May 2026 23:28:18 GMT
ENV INFLUXDB_VERSION=2.9.1
# Tue, 19 May 2026 23:28:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 19 May 2026 23:28:18 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Tue, 19 May 2026 23:28:19 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 19 May 2026 23:28:20 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 19 May 2026 23:28:20 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 19 May 2026 23:28:20 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 19 May 2026 23:28:20 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 May 2026 23:28:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 May 2026 23:28:20 GMT
CMD ["influxd"]
# Tue, 19 May 2026 23:28:20 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 19 May 2026 23:28:20 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 19 May 2026 23:28:20 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 19 May 2026 23:28:20 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 19 May 2026 23:28:20 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a3e4fdf0759b602cc83eee55bb98191a184bf47394c125416bad56fd14cf2e`  
		Last Modified: Tue, 19 May 2026 23:28:31 GMT  
		Size: 9.6 MB (9629316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69d1631bd9b1dc8d27a448997e0d90af077c96a2041f16eb89751cd7a188383`  
		Last Modified: Tue, 19 May 2026 23:28:31 GMT  
		Size: 3.5 MB (3459173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3843f9e7c58fc79d623603a0448fe5eb8b646c9acb86278e08024e28e90e6e1a`  
		Last Modified: Tue, 19 May 2026 23:28:31 GMT  
		Size: 3.2 KB (3227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b748a12a94328f10d7c957a9ef02934ab7b468161e7f3274c68923d716de920d`  
		Last Modified: Tue, 19 May 2026 23:28:33 GMT  
		Size: 53.6 MB (53636820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40bad5774d9135c6e7eabc80742652a79641e86bd6a0f05b13a385c47764bc20`  
		Last Modified: Tue, 19 May 2026 23:28:32 GMT  
		Size: 11.5 MB (11480296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e4221fc8c1ab93c69cafbc88cb0214ea6877c204266846e6add1891ea58a891`  
		Last Modified: Tue, 19 May 2026 23:28:32 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129703821150bfc0ff6995ffa921aaca455ba27668ec104ae6ff73b58cfbba8c`  
		Last Modified: Tue, 19 May 2026 23:28:32 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7424fffba09e6f72ae806428342ccfd9cf858d0dfa3e1acbf6111cf5603a85fe`  
		Last Modified: Tue, 19 May 2026 23:28:33 GMT  
		Size: 6.5 KB (6499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.9.1` - unknown; unknown

```console
$ docker pull influxdb@sha256:ba793f9c250c21d96c0eccc2bf682b93706548fcc7def232da980c3ce77bd9b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca7a7141b9565f983497bde826dc595445dbd26abef6d664c30cd7d78280717f`

```dockerfile
```

-	Layers:
	-	`sha256:b176ade03bf084e3c8722d038d297af9345b5ff626542e7bb237a7adc6b1b5aa`  
		Last Modified: Tue, 19 May 2026 23:28:31 GMT  
		Size: 3.0 MB (2958907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a53002c50db871c40a28faf2f74b6de4d013e714ecc96cbbfcbc68704f320026`  
		Last Modified: Tue, 19 May 2026 23:28:31 GMT  
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
$ docker pull influxdb@sha256:c27c9b2ca2625b5b6966f0b09baa448102310e63a471fd60dff22646a2522e29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-core` - linux; amd64

```console
$ docker pull influxdb@sha256:c7fd6ab41537a64efa0c1086fa319537013bbe95207c3481a72288556d89ace5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148828426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d3505bfb53281388e25180b07f9eb7cd1c1d688af4b6736a93bc6aca1aff2da`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:17:58 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 02 Jun 2026 08:17:58 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 02 Jun 2026 08:18:03 GMT
ENV INFLUXDB_VERSION=3.9.3
# Tue, 02 Jun 2026 08:18:03 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 02 Jun 2026 08:18:03 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:18:03 GMT
USER influxdb3
# Tue, 02 Jun 2026 08:18:03 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 02 Jun 2026 08:18:03 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 02 Jun 2026 08:18:03 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 02 Jun 2026 08:18:03 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Tue, 02 Jun 2026 08:18:03 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 02 Jun 2026 08:18:03 GMT
ENV LOG_FILTER=info
# Tue, 02 Jun 2026 08:18:03 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 02 Jun 2026 08:18:03 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 02 Jun 2026 08:18:03 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade8c505837de120705feefca71ae19ba5a4999cf9621298e5babc7c06c76e89`  
		Last Modified: Tue, 02 Jun 2026 08:18:21 GMT  
		Size: 6.7 MB (6672925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6c98dbf06904987967684c82fc531600afe85f092a228192c720e6b140d47a`  
		Last Modified: Tue, 02 Jun 2026 08:18:21 GMT  
		Size: 3.6 KB (3649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3fc616b313f8b79b71693d92a507ddbc4448bea1d78cb9a6938793b3d2615d`  
		Last Modified: Tue, 02 Jun 2026 08:18:23 GMT  
		Size: 112.4 MB (112418377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969790be85663fe104269a6e942fabb2b199bedc896cfc3b99de25a052a7fb86`  
		Last Modified: Tue, 02 Jun 2026 08:18:21 GMT  
		Size: 521.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4daa696f40c046e331c8dc0dbcc5de500eda957934079b505ef9ce7e1ac8ea49`  
		Last Modified: Tue, 02 Jun 2026 08:18:22 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:f5bc0ba8d4ed3a0e3af46246e855ce46f5a77c65c2fd14bf97da768eee1c3034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cf5a9948dac3dda6a8b08111978a67d65ce896f265d45d4d3dbdca21915018b`

```dockerfile
```

-	Layers:
	-	`sha256:cb25b6eed079349b38a9d32f651ca9ce6ddeac149983f4f3a395ad3c0181af3e`  
		Last Modified: Tue, 02 Jun 2026 08:18:21 GMT  
		Size: 2.3 MB (2310615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcbf97d4871dcbcb20923a6a4329b867ac8ea561b42e32210f0d3f463390ac35`  
		Last Modified: Tue, 02 Jun 2026 08:18:21 GMT  
		Size: 17.6 KB (17620 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:30a0a93fa38fb80a32386999fc04d3da2b257b941fdafb9e70c9061c79bc09c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.0 MB (140020883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:524a258898e9483f652c29166efb0db1c1546aba05ddf13584458b316d4615f1`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:18:31 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 02 Jun 2026 08:18:31 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 02 Jun 2026 08:18:36 GMT
ENV INFLUXDB_VERSION=3.9.3
# Tue, 02 Jun 2026 08:18:36 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 02 Jun 2026 08:18:36 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:18:36 GMT
USER influxdb3
# Tue, 02 Jun 2026 08:18:36 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 02 Jun 2026 08:18:36 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 02 Jun 2026 08:18:36 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 02 Jun 2026 08:18:36 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Tue, 02 Jun 2026 08:18:36 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 02 Jun 2026 08:18:36 GMT
ENV LOG_FILTER=info
# Tue, 02 Jun 2026 08:18:36 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 02 Jun 2026 08:18:36 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 02 Jun 2026 08:18:36 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8192048613ede57b06877b77b5b15c760702a460e00a9765562011f8400eb0bb`  
		Last Modified: Tue, 02 Jun 2026 08:18:53 GMT  
		Size: 6.7 MB (6682530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27ed7b1a518af169037891be86d878895b7227f145c781aebd36f74ad9fcd7d`  
		Last Modified: Tue, 02 Jun 2026 08:18:52 GMT  
		Size: 3.6 KB (3650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb2d6904a22f4fb7087f1f2c30a6e23bd2073a9ee2dab956d0cd30f5947abcd`  
		Last Modified: Tue, 02 Jun 2026 08:18:55 GMT  
		Size: 104.5 MB (104457628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:074caea2353dc9a4845bb7c86ee19e2a8f73f84e90977346ee563b1151cdd090`  
		Last Modified: Tue, 02 Jun 2026 08:18:52 GMT  
		Size: 520.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b39f4df680d32c2cc4a8b4972bc5bb7ccf34344fd92f563674f3edf84db5b4`  
		Last Modified: Tue, 02 Jun 2026 08:18:54 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:2f816d70eced4289a87ff05c535f2b9bfec2ced85b2963e8151aaf7257ee86a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:109d1990ca3ddb26414e25474d80bd5aa0bec2eb53ac24685b91cc44e0de471b`

```dockerfile
```

-	Layers:
	-	`sha256:5750b7d30243168512f6683ab5cdbd26406e419466579cf5426987b9205d6688`  
		Last Modified: Tue, 02 Jun 2026 08:18:53 GMT  
		Size: 2.3 MB (2311697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f98e29d0a3a997b74ea7619ee1a8a6b09b6d11903643126afce417921633da11`  
		Last Modified: Tue, 02 Jun 2026 08:18:52 GMT  
		Size: 17.8 KB (17769 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3-enterprise`

```console
$ docker pull influxdb@sha256:835229f278ea2dd7e139450d90ffa5af00dc731cb3dd9379ba42faa250b8a697
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:72a786b354966a3f05b6906464d2f76beb84db58cecc24cb0e54912b7f182215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.5 MB (159473195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58ab121ae6a1686d392793a96e1403a5dc1d919c930c266ed405e801f89f8da2`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:18:35 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 02 Jun 2026 08:18:35 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 02 Jun 2026 08:18:40 GMT
ENV INFLUXDB_VERSION=3.9.3
# Tue, 02 Jun 2026 08:18:40 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 02 Jun 2026 08:18:40 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:18:40 GMT
USER influxdb3
# Tue, 02 Jun 2026 08:18:40 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 02 Jun 2026 08:18:40 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 02 Jun 2026 08:18:40 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 02 Jun 2026 08:18:40 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Tue, 02 Jun 2026 08:18:40 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 02 Jun 2026 08:18:40 GMT
ENV LOG_FILTER=info
# Tue, 02 Jun 2026 08:18:40 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 02 Jun 2026 08:18:40 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 02 Jun 2026 08:18:40 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a93cc4ed173c2d653d9d05b7d7a395ba4b81eb1928e9519e27de5e7c5c512a`  
		Last Modified: Tue, 02 Jun 2026 08:19:00 GMT  
		Size: 6.7 MB (6672941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ec311104fc1c8b0457287201d08b27f8e0e0d998ec499ec0176c11dbb80711`  
		Last Modified: Tue, 02 Jun 2026 08:19:00 GMT  
		Size: 3.7 KB (3651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4f55416553b1818707f5256d494948439a6e118f1f89be90daacda21fe165e`  
		Last Modified: Tue, 02 Jun 2026 08:19:03 GMT  
		Size: 123.1 MB (123063129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312b7602e21e8e22bfd0fe497ee8ddaa5ed6d2be3da38c63da9e77bd19ef3941`  
		Last Modified: Tue, 02 Jun 2026 08:19:00 GMT  
		Size: 521.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:321a561e097c78a830035cdb9bdae97ee44fa5c1100fef65c7c014696b18eab4`  
		Last Modified: Tue, 02 Jun 2026 08:19:01 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:6277afcfb1fcf8ff0d4292c2117da607eeb263195e596f1ddb7b4f6afdb34c6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc4029b765694577339e6cb3c73e3603c3b2f86e7d2c01ffbc263750e971aec7`

```dockerfile
```

-	Layers:
	-	`sha256:8680a032214d875ea9856434d5e294e96f11a911ce1817715039896a28c90baa`  
		Last Modified: Tue, 02 Jun 2026 08:19:00 GMT  
		Size: 2.3 MB (2310663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44b1302e98b859d594b9f6da2289a1b4bf0847f933025e6af94e37bd87a94b1c`  
		Last Modified: Tue, 02 Jun 2026 08:19:00 GMT  
		Size: 17.8 KB (17800 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:a75ee42f999ea6d313c79f36782a188c508560f27a7d53ece147ddcb2f0b41fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.5 MB (150491979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6208cf7be57cdc24eef049f2a862a47216bbea93f0c6836da844dbc85e2fbed9`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:18:42 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 02 Jun 2026 08:18:42 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 02 Jun 2026 08:18:47 GMT
ENV INFLUXDB_VERSION=3.9.3
# Tue, 02 Jun 2026 08:18:47 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 02 Jun 2026 08:18:47 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:18:47 GMT
USER influxdb3
# Tue, 02 Jun 2026 08:18:47 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 02 Jun 2026 08:18:47 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 02 Jun 2026 08:18:47 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 02 Jun 2026 08:18:47 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Tue, 02 Jun 2026 08:18:47 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 02 Jun 2026 08:18:47 GMT
ENV LOG_FILTER=info
# Tue, 02 Jun 2026 08:18:47 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 02 Jun 2026 08:18:47 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 02 Jun 2026 08:18:47 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233d54f9dc825b34a82ea91bcc0754b7d4c154fc7517c9c2962fd01782faeb5d`  
		Last Modified: Tue, 02 Jun 2026 08:19:05 GMT  
		Size: 6.7 MB (6682535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a2cc1e1d488c31fdbbe6a21443745ac798b9b704fbd24811571310ee5430bb`  
		Last Modified: Tue, 02 Jun 2026 08:19:04 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f77332c2036a26b34d8ca49077225fae7607d919bed80b94976639bb3761f5`  
		Last Modified: Tue, 02 Jun 2026 08:19:07 GMT  
		Size: 114.9 MB (114928715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b25c39ebd758c2acb6e101baba666437493a8e1fc5099e4f87c5bf7d94ac02d`  
		Last Modified: Tue, 02 Jun 2026 08:19:04 GMT  
		Size: 520.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d711546eec3630af6fef47c499afbd8c137014757a448713939d2d9d296ae430`  
		Last Modified: Tue, 02 Jun 2026 08:19:06 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:f908b92dfeb8950758d8b9792d421afeeb07f8a58bc34eed302c2944074893c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b51ea865b515f3357856e492f9177f9d6ce02f5d2b9d79d78d1163fda0ba9d7`

```dockerfile
```

-	Layers:
	-	`sha256:ad48a8a10e7cf0a4a543c2ae930eb4d5c84f93d51d7466b7f4251e0bd4710071`  
		Last Modified: Tue, 02 Jun 2026 08:19:04 GMT  
		Size: 2.3 MB (2311745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25ae3771136afb25ff27f8f451c6b2ba3295aaa02db431cd3a00f0da4b5f61a0`  
		Last Modified: Tue, 02 Jun 2026 08:19:04 GMT  
		Size: 17.9 KB (17949 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.9-core`

```console
$ docker pull influxdb@sha256:c27c9b2ca2625b5b6966f0b09baa448102310e63a471fd60dff22646a2522e29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.9-core` - linux; amd64

```console
$ docker pull influxdb@sha256:c7fd6ab41537a64efa0c1086fa319537013bbe95207c3481a72288556d89ace5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148828426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d3505bfb53281388e25180b07f9eb7cd1c1d688af4b6736a93bc6aca1aff2da`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:17:58 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 02 Jun 2026 08:17:58 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 02 Jun 2026 08:18:03 GMT
ENV INFLUXDB_VERSION=3.9.3
# Tue, 02 Jun 2026 08:18:03 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 02 Jun 2026 08:18:03 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:18:03 GMT
USER influxdb3
# Tue, 02 Jun 2026 08:18:03 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 02 Jun 2026 08:18:03 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 02 Jun 2026 08:18:03 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 02 Jun 2026 08:18:03 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Tue, 02 Jun 2026 08:18:03 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 02 Jun 2026 08:18:03 GMT
ENV LOG_FILTER=info
# Tue, 02 Jun 2026 08:18:03 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 02 Jun 2026 08:18:03 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 02 Jun 2026 08:18:03 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade8c505837de120705feefca71ae19ba5a4999cf9621298e5babc7c06c76e89`  
		Last Modified: Tue, 02 Jun 2026 08:18:21 GMT  
		Size: 6.7 MB (6672925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6c98dbf06904987967684c82fc531600afe85f092a228192c720e6b140d47a`  
		Last Modified: Tue, 02 Jun 2026 08:18:21 GMT  
		Size: 3.6 KB (3649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3fc616b313f8b79b71693d92a507ddbc4448bea1d78cb9a6938793b3d2615d`  
		Last Modified: Tue, 02 Jun 2026 08:18:23 GMT  
		Size: 112.4 MB (112418377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969790be85663fe104269a6e942fabb2b199bedc896cfc3b99de25a052a7fb86`  
		Last Modified: Tue, 02 Jun 2026 08:18:21 GMT  
		Size: 521.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4daa696f40c046e331c8dc0dbcc5de500eda957934079b505ef9ce7e1ac8ea49`  
		Last Modified: Tue, 02 Jun 2026 08:18:22 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.9-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:f5bc0ba8d4ed3a0e3af46246e855ce46f5a77c65c2fd14bf97da768eee1c3034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cf5a9948dac3dda6a8b08111978a67d65ce896f265d45d4d3dbdca21915018b`

```dockerfile
```

-	Layers:
	-	`sha256:cb25b6eed079349b38a9d32f651ca9ce6ddeac149983f4f3a395ad3c0181af3e`  
		Last Modified: Tue, 02 Jun 2026 08:18:21 GMT  
		Size: 2.3 MB (2310615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcbf97d4871dcbcb20923a6a4329b867ac8ea561b42e32210f0d3f463390ac35`  
		Last Modified: Tue, 02 Jun 2026 08:18:21 GMT  
		Size: 17.6 KB (17620 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.9-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:30a0a93fa38fb80a32386999fc04d3da2b257b941fdafb9e70c9061c79bc09c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.0 MB (140020883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:524a258898e9483f652c29166efb0db1c1546aba05ddf13584458b316d4615f1`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:18:31 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 02 Jun 2026 08:18:31 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 02 Jun 2026 08:18:36 GMT
ENV INFLUXDB_VERSION=3.9.3
# Tue, 02 Jun 2026 08:18:36 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 02 Jun 2026 08:18:36 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:18:36 GMT
USER influxdb3
# Tue, 02 Jun 2026 08:18:36 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 02 Jun 2026 08:18:36 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 02 Jun 2026 08:18:36 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 02 Jun 2026 08:18:36 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Tue, 02 Jun 2026 08:18:36 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 02 Jun 2026 08:18:36 GMT
ENV LOG_FILTER=info
# Tue, 02 Jun 2026 08:18:36 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 02 Jun 2026 08:18:36 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 02 Jun 2026 08:18:36 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8192048613ede57b06877b77b5b15c760702a460e00a9765562011f8400eb0bb`  
		Last Modified: Tue, 02 Jun 2026 08:18:53 GMT  
		Size: 6.7 MB (6682530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27ed7b1a518af169037891be86d878895b7227f145c781aebd36f74ad9fcd7d`  
		Last Modified: Tue, 02 Jun 2026 08:18:52 GMT  
		Size: 3.6 KB (3650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb2d6904a22f4fb7087f1f2c30a6e23bd2073a9ee2dab956d0cd30f5947abcd`  
		Last Modified: Tue, 02 Jun 2026 08:18:55 GMT  
		Size: 104.5 MB (104457628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:074caea2353dc9a4845bb7c86ee19e2a8f73f84e90977346ee563b1151cdd090`  
		Last Modified: Tue, 02 Jun 2026 08:18:52 GMT  
		Size: 520.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b39f4df680d32c2cc4a8b4972bc5bb7ccf34344fd92f563674f3edf84db5b4`  
		Last Modified: Tue, 02 Jun 2026 08:18:54 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.9-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:2f816d70eced4289a87ff05c535f2b9bfec2ced85b2963e8151aaf7257ee86a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:109d1990ca3ddb26414e25474d80bd5aa0bec2eb53ac24685b91cc44e0de471b`

```dockerfile
```

-	Layers:
	-	`sha256:5750b7d30243168512f6683ab5cdbd26406e419466579cf5426987b9205d6688`  
		Last Modified: Tue, 02 Jun 2026 08:18:53 GMT  
		Size: 2.3 MB (2311697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f98e29d0a3a997b74ea7619ee1a8a6b09b6d11903643126afce417921633da11`  
		Last Modified: Tue, 02 Jun 2026 08:18:52 GMT  
		Size: 17.8 KB (17769 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.9-enterprise`

```console
$ docker pull influxdb@sha256:835229f278ea2dd7e139450d90ffa5af00dc731cb3dd9379ba42faa250b8a697
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.9-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:72a786b354966a3f05b6906464d2f76beb84db58cecc24cb0e54912b7f182215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.5 MB (159473195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58ab121ae6a1686d392793a96e1403a5dc1d919c930c266ed405e801f89f8da2`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:18:35 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 02 Jun 2026 08:18:35 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 02 Jun 2026 08:18:40 GMT
ENV INFLUXDB_VERSION=3.9.3
# Tue, 02 Jun 2026 08:18:40 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 02 Jun 2026 08:18:40 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:18:40 GMT
USER influxdb3
# Tue, 02 Jun 2026 08:18:40 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 02 Jun 2026 08:18:40 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 02 Jun 2026 08:18:40 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 02 Jun 2026 08:18:40 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Tue, 02 Jun 2026 08:18:40 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 02 Jun 2026 08:18:40 GMT
ENV LOG_FILTER=info
# Tue, 02 Jun 2026 08:18:40 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 02 Jun 2026 08:18:40 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 02 Jun 2026 08:18:40 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a93cc4ed173c2d653d9d05b7d7a395ba4b81eb1928e9519e27de5e7c5c512a`  
		Last Modified: Tue, 02 Jun 2026 08:19:00 GMT  
		Size: 6.7 MB (6672941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ec311104fc1c8b0457287201d08b27f8e0e0d998ec499ec0176c11dbb80711`  
		Last Modified: Tue, 02 Jun 2026 08:19:00 GMT  
		Size: 3.7 KB (3651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4f55416553b1818707f5256d494948439a6e118f1f89be90daacda21fe165e`  
		Last Modified: Tue, 02 Jun 2026 08:19:03 GMT  
		Size: 123.1 MB (123063129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312b7602e21e8e22bfd0fe497ee8ddaa5ed6d2be3da38c63da9e77bd19ef3941`  
		Last Modified: Tue, 02 Jun 2026 08:19:00 GMT  
		Size: 521.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:321a561e097c78a830035cdb9bdae97ee44fa5c1100fef65c7c014696b18eab4`  
		Last Modified: Tue, 02 Jun 2026 08:19:01 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.9-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:6277afcfb1fcf8ff0d4292c2117da607eeb263195e596f1ddb7b4f6afdb34c6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc4029b765694577339e6cb3c73e3603c3b2f86e7d2c01ffbc263750e971aec7`

```dockerfile
```

-	Layers:
	-	`sha256:8680a032214d875ea9856434d5e294e96f11a911ce1817715039896a28c90baa`  
		Last Modified: Tue, 02 Jun 2026 08:19:00 GMT  
		Size: 2.3 MB (2310663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44b1302e98b859d594b9f6da2289a1b4bf0847f933025e6af94e37bd87a94b1c`  
		Last Modified: Tue, 02 Jun 2026 08:19:00 GMT  
		Size: 17.8 KB (17800 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.9-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:a75ee42f999ea6d313c79f36782a188c508560f27a7d53ece147ddcb2f0b41fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.5 MB (150491979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6208cf7be57cdc24eef049f2a862a47216bbea93f0c6836da844dbc85e2fbed9`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:18:42 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 02 Jun 2026 08:18:42 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 02 Jun 2026 08:18:47 GMT
ENV INFLUXDB_VERSION=3.9.3
# Tue, 02 Jun 2026 08:18:47 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 02 Jun 2026 08:18:47 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:18:47 GMT
USER influxdb3
# Tue, 02 Jun 2026 08:18:47 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 02 Jun 2026 08:18:47 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 02 Jun 2026 08:18:47 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 02 Jun 2026 08:18:47 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Tue, 02 Jun 2026 08:18:47 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 02 Jun 2026 08:18:47 GMT
ENV LOG_FILTER=info
# Tue, 02 Jun 2026 08:18:47 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 02 Jun 2026 08:18:47 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 02 Jun 2026 08:18:47 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233d54f9dc825b34a82ea91bcc0754b7d4c154fc7517c9c2962fd01782faeb5d`  
		Last Modified: Tue, 02 Jun 2026 08:19:05 GMT  
		Size: 6.7 MB (6682535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a2cc1e1d488c31fdbbe6a21443745ac798b9b704fbd24811571310ee5430bb`  
		Last Modified: Tue, 02 Jun 2026 08:19:04 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f77332c2036a26b34d8ca49077225fae7607d919bed80b94976639bb3761f5`  
		Last Modified: Tue, 02 Jun 2026 08:19:07 GMT  
		Size: 114.9 MB (114928715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b25c39ebd758c2acb6e101baba666437493a8e1fc5099e4f87c5bf7d94ac02d`  
		Last Modified: Tue, 02 Jun 2026 08:19:04 GMT  
		Size: 520.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d711546eec3630af6fef47c499afbd8c137014757a448713939d2d9d296ae430`  
		Last Modified: Tue, 02 Jun 2026 08:19:06 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.9-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:f908b92dfeb8950758d8b9792d421afeeb07f8a58bc34eed302c2944074893c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b51ea865b515f3357856e492f9177f9d6ce02f5d2b9d79d78d1163fda0ba9d7`

```dockerfile
```

-	Layers:
	-	`sha256:ad48a8a10e7cf0a4a543c2ae930eb4d5c84f93d51d7466b7f4251e0bd4710071`  
		Last Modified: Tue, 02 Jun 2026 08:19:04 GMT  
		Size: 2.3 MB (2311745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25ae3771136afb25ff27f8f451c6b2ba3295aaa02db431cd3a00f0da4b5f61a0`  
		Last Modified: Tue, 02 Jun 2026 08:19:04 GMT  
		Size: 17.9 KB (17949 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.9.3-core`

```console
$ docker pull influxdb@sha256:c27c9b2ca2625b5b6966f0b09baa448102310e63a471fd60dff22646a2522e29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.9.3-core` - linux; amd64

```console
$ docker pull influxdb@sha256:c7fd6ab41537a64efa0c1086fa319537013bbe95207c3481a72288556d89ace5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148828426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d3505bfb53281388e25180b07f9eb7cd1c1d688af4b6736a93bc6aca1aff2da`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:17:58 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 02 Jun 2026 08:17:58 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 02 Jun 2026 08:18:03 GMT
ENV INFLUXDB_VERSION=3.9.3
# Tue, 02 Jun 2026 08:18:03 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 02 Jun 2026 08:18:03 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:18:03 GMT
USER influxdb3
# Tue, 02 Jun 2026 08:18:03 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 02 Jun 2026 08:18:03 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 02 Jun 2026 08:18:03 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 02 Jun 2026 08:18:03 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Tue, 02 Jun 2026 08:18:03 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 02 Jun 2026 08:18:03 GMT
ENV LOG_FILTER=info
# Tue, 02 Jun 2026 08:18:03 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 02 Jun 2026 08:18:03 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 02 Jun 2026 08:18:03 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade8c505837de120705feefca71ae19ba5a4999cf9621298e5babc7c06c76e89`  
		Last Modified: Tue, 02 Jun 2026 08:18:21 GMT  
		Size: 6.7 MB (6672925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6c98dbf06904987967684c82fc531600afe85f092a228192c720e6b140d47a`  
		Last Modified: Tue, 02 Jun 2026 08:18:21 GMT  
		Size: 3.6 KB (3649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3fc616b313f8b79b71693d92a507ddbc4448bea1d78cb9a6938793b3d2615d`  
		Last Modified: Tue, 02 Jun 2026 08:18:23 GMT  
		Size: 112.4 MB (112418377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969790be85663fe104269a6e942fabb2b199bedc896cfc3b99de25a052a7fb86`  
		Last Modified: Tue, 02 Jun 2026 08:18:21 GMT  
		Size: 521.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4daa696f40c046e331c8dc0dbcc5de500eda957934079b505ef9ce7e1ac8ea49`  
		Last Modified: Tue, 02 Jun 2026 08:18:22 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.9.3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:f5bc0ba8d4ed3a0e3af46246e855ce46f5a77c65c2fd14bf97da768eee1c3034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cf5a9948dac3dda6a8b08111978a67d65ce896f265d45d4d3dbdca21915018b`

```dockerfile
```

-	Layers:
	-	`sha256:cb25b6eed079349b38a9d32f651ca9ce6ddeac149983f4f3a395ad3c0181af3e`  
		Last Modified: Tue, 02 Jun 2026 08:18:21 GMT  
		Size: 2.3 MB (2310615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcbf97d4871dcbcb20923a6a4329b867ac8ea561b42e32210f0d3f463390ac35`  
		Last Modified: Tue, 02 Jun 2026 08:18:21 GMT  
		Size: 17.6 KB (17620 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.9.3-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:30a0a93fa38fb80a32386999fc04d3da2b257b941fdafb9e70c9061c79bc09c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.0 MB (140020883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:524a258898e9483f652c29166efb0db1c1546aba05ddf13584458b316d4615f1`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:18:31 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 02 Jun 2026 08:18:31 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 02 Jun 2026 08:18:36 GMT
ENV INFLUXDB_VERSION=3.9.3
# Tue, 02 Jun 2026 08:18:36 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 02 Jun 2026 08:18:36 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:18:36 GMT
USER influxdb3
# Tue, 02 Jun 2026 08:18:36 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 02 Jun 2026 08:18:36 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 02 Jun 2026 08:18:36 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 02 Jun 2026 08:18:36 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Tue, 02 Jun 2026 08:18:36 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 02 Jun 2026 08:18:36 GMT
ENV LOG_FILTER=info
# Tue, 02 Jun 2026 08:18:36 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 02 Jun 2026 08:18:36 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 02 Jun 2026 08:18:36 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8192048613ede57b06877b77b5b15c760702a460e00a9765562011f8400eb0bb`  
		Last Modified: Tue, 02 Jun 2026 08:18:53 GMT  
		Size: 6.7 MB (6682530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27ed7b1a518af169037891be86d878895b7227f145c781aebd36f74ad9fcd7d`  
		Last Modified: Tue, 02 Jun 2026 08:18:52 GMT  
		Size: 3.6 KB (3650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb2d6904a22f4fb7087f1f2c30a6e23bd2073a9ee2dab956d0cd30f5947abcd`  
		Last Modified: Tue, 02 Jun 2026 08:18:55 GMT  
		Size: 104.5 MB (104457628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:074caea2353dc9a4845bb7c86ee19e2a8f73f84e90977346ee563b1151cdd090`  
		Last Modified: Tue, 02 Jun 2026 08:18:52 GMT  
		Size: 520.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b39f4df680d32c2cc4a8b4972bc5bb7ccf34344fd92f563674f3edf84db5b4`  
		Last Modified: Tue, 02 Jun 2026 08:18:54 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.9.3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:2f816d70eced4289a87ff05c535f2b9bfec2ced85b2963e8151aaf7257ee86a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:109d1990ca3ddb26414e25474d80bd5aa0bec2eb53ac24685b91cc44e0de471b`

```dockerfile
```

-	Layers:
	-	`sha256:5750b7d30243168512f6683ab5cdbd26406e419466579cf5426987b9205d6688`  
		Last Modified: Tue, 02 Jun 2026 08:18:53 GMT  
		Size: 2.3 MB (2311697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f98e29d0a3a997b74ea7619ee1a8a6b09b6d11903643126afce417921633da11`  
		Last Modified: Tue, 02 Jun 2026 08:18:52 GMT  
		Size: 17.8 KB (17769 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.9.3-enterprise`

```console
$ docker pull influxdb@sha256:835229f278ea2dd7e139450d90ffa5af00dc731cb3dd9379ba42faa250b8a697
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.9.3-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:72a786b354966a3f05b6906464d2f76beb84db58cecc24cb0e54912b7f182215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.5 MB (159473195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58ab121ae6a1686d392793a96e1403a5dc1d919c930c266ed405e801f89f8da2`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:18:35 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 02 Jun 2026 08:18:35 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 02 Jun 2026 08:18:40 GMT
ENV INFLUXDB_VERSION=3.9.3
# Tue, 02 Jun 2026 08:18:40 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 02 Jun 2026 08:18:40 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:18:40 GMT
USER influxdb3
# Tue, 02 Jun 2026 08:18:40 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 02 Jun 2026 08:18:40 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 02 Jun 2026 08:18:40 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 02 Jun 2026 08:18:40 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Tue, 02 Jun 2026 08:18:40 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 02 Jun 2026 08:18:40 GMT
ENV LOG_FILTER=info
# Tue, 02 Jun 2026 08:18:40 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 02 Jun 2026 08:18:40 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 02 Jun 2026 08:18:40 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a93cc4ed173c2d653d9d05b7d7a395ba4b81eb1928e9519e27de5e7c5c512a`  
		Last Modified: Tue, 02 Jun 2026 08:19:00 GMT  
		Size: 6.7 MB (6672941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ec311104fc1c8b0457287201d08b27f8e0e0d998ec499ec0176c11dbb80711`  
		Last Modified: Tue, 02 Jun 2026 08:19:00 GMT  
		Size: 3.7 KB (3651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4f55416553b1818707f5256d494948439a6e118f1f89be90daacda21fe165e`  
		Last Modified: Tue, 02 Jun 2026 08:19:03 GMT  
		Size: 123.1 MB (123063129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312b7602e21e8e22bfd0fe497ee8ddaa5ed6d2be3da38c63da9e77bd19ef3941`  
		Last Modified: Tue, 02 Jun 2026 08:19:00 GMT  
		Size: 521.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:321a561e097c78a830035cdb9bdae97ee44fa5c1100fef65c7c014696b18eab4`  
		Last Modified: Tue, 02 Jun 2026 08:19:01 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.9.3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:6277afcfb1fcf8ff0d4292c2117da607eeb263195e596f1ddb7b4f6afdb34c6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc4029b765694577339e6cb3c73e3603c3b2f86e7d2c01ffbc263750e971aec7`

```dockerfile
```

-	Layers:
	-	`sha256:8680a032214d875ea9856434d5e294e96f11a911ce1817715039896a28c90baa`  
		Last Modified: Tue, 02 Jun 2026 08:19:00 GMT  
		Size: 2.3 MB (2310663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44b1302e98b859d594b9f6da2289a1b4bf0847f933025e6af94e37bd87a94b1c`  
		Last Modified: Tue, 02 Jun 2026 08:19:00 GMT  
		Size: 17.8 KB (17800 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.9.3-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:a75ee42f999ea6d313c79f36782a188c508560f27a7d53ece147ddcb2f0b41fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.5 MB (150491979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6208cf7be57cdc24eef049f2a862a47216bbea93f0c6836da844dbc85e2fbed9`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:18:42 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 02 Jun 2026 08:18:42 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 02 Jun 2026 08:18:47 GMT
ENV INFLUXDB_VERSION=3.9.3
# Tue, 02 Jun 2026 08:18:47 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 02 Jun 2026 08:18:47 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:18:47 GMT
USER influxdb3
# Tue, 02 Jun 2026 08:18:47 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 02 Jun 2026 08:18:47 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 02 Jun 2026 08:18:47 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 02 Jun 2026 08:18:47 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Tue, 02 Jun 2026 08:18:47 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 02 Jun 2026 08:18:47 GMT
ENV LOG_FILTER=info
# Tue, 02 Jun 2026 08:18:47 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 02 Jun 2026 08:18:47 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 02 Jun 2026 08:18:47 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233d54f9dc825b34a82ea91bcc0754b7d4c154fc7517c9c2962fd01782faeb5d`  
		Last Modified: Tue, 02 Jun 2026 08:19:05 GMT  
		Size: 6.7 MB (6682535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a2cc1e1d488c31fdbbe6a21443745ac798b9b704fbd24811571310ee5430bb`  
		Last Modified: Tue, 02 Jun 2026 08:19:04 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f77332c2036a26b34d8ca49077225fae7607d919bed80b94976639bb3761f5`  
		Last Modified: Tue, 02 Jun 2026 08:19:07 GMT  
		Size: 114.9 MB (114928715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b25c39ebd758c2acb6e101baba666437493a8e1fc5099e4f87c5bf7d94ac02d`  
		Last Modified: Tue, 02 Jun 2026 08:19:04 GMT  
		Size: 520.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d711546eec3630af6fef47c499afbd8c137014757a448713939d2d9d296ae430`  
		Last Modified: Tue, 02 Jun 2026 08:19:06 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.9.3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:f908b92dfeb8950758d8b9792d421afeeb07f8a58bc34eed302c2944074893c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b51ea865b515f3357856e492f9177f9d6ce02f5d2b9d79d78d1163fda0ba9d7`

```dockerfile
```

-	Layers:
	-	`sha256:ad48a8a10e7cf0a4a543c2ae930eb4d5c84f93d51d7466b7f4251e0bd4710071`  
		Last Modified: Tue, 02 Jun 2026 08:19:04 GMT  
		Size: 2.3 MB (2311745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25ae3771136afb25ff27f8f451c6b2ba3295aaa02db431cd3a00f0da4b5f61a0`  
		Last Modified: Tue, 02 Jun 2026 08:19:04 GMT  
		Size: 17.9 KB (17949 bytes)  
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
$ docker pull influxdb@sha256:c27c9b2ca2625b5b6966f0b09baa448102310e63a471fd60dff22646a2522e29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:core` - linux; amd64

```console
$ docker pull influxdb@sha256:c7fd6ab41537a64efa0c1086fa319537013bbe95207c3481a72288556d89ace5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148828426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d3505bfb53281388e25180b07f9eb7cd1c1d688af4b6736a93bc6aca1aff2da`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:17:58 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 02 Jun 2026 08:17:58 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 02 Jun 2026 08:18:03 GMT
ENV INFLUXDB_VERSION=3.9.3
# Tue, 02 Jun 2026 08:18:03 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 02 Jun 2026 08:18:03 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:18:03 GMT
USER influxdb3
# Tue, 02 Jun 2026 08:18:03 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 02 Jun 2026 08:18:03 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 02 Jun 2026 08:18:03 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 02 Jun 2026 08:18:03 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Tue, 02 Jun 2026 08:18:03 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 02 Jun 2026 08:18:03 GMT
ENV LOG_FILTER=info
# Tue, 02 Jun 2026 08:18:03 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 02 Jun 2026 08:18:03 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 02 Jun 2026 08:18:03 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade8c505837de120705feefca71ae19ba5a4999cf9621298e5babc7c06c76e89`  
		Last Modified: Tue, 02 Jun 2026 08:18:21 GMT  
		Size: 6.7 MB (6672925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6c98dbf06904987967684c82fc531600afe85f092a228192c720e6b140d47a`  
		Last Modified: Tue, 02 Jun 2026 08:18:21 GMT  
		Size: 3.6 KB (3649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3fc616b313f8b79b71693d92a507ddbc4448bea1d78cb9a6938793b3d2615d`  
		Last Modified: Tue, 02 Jun 2026 08:18:23 GMT  
		Size: 112.4 MB (112418377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969790be85663fe104269a6e942fabb2b199bedc896cfc3b99de25a052a7fb86`  
		Last Modified: Tue, 02 Jun 2026 08:18:21 GMT  
		Size: 521.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4daa696f40c046e331c8dc0dbcc5de500eda957934079b505ef9ce7e1ac8ea49`  
		Last Modified: Tue, 02 Jun 2026 08:18:22 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:f5bc0ba8d4ed3a0e3af46246e855ce46f5a77c65c2fd14bf97da768eee1c3034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cf5a9948dac3dda6a8b08111978a67d65ce896f265d45d4d3dbdca21915018b`

```dockerfile
```

-	Layers:
	-	`sha256:cb25b6eed079349b38a9d32f651ca9ce6ddeac149983f4f3a395ad3c0181af3e`  
		Last Modified: Tue, 02 Jun 2026 08:18:21 GMT  
		Size: 2.3 MB (2310615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcbf97d4871dcbcb20923a6a4329b867ac8ea561b42e32210f0d3f463390ac35`  
		Last Modified: Tue, 02 Jun 2026 08:18:21 GMT  
		Size: 17.6 KB (17620 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:30a0a93fa38fb80a32386999fc04d3da2b257b941fdafb9e70c9061c79bc09c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.0 MB (140020883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:524a258898e9483f652c29166efb0db1c1546aba05ddf13584458b316d4615f1`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:18:31 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 02 Jun 2026 08:18:31 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 02 Jun 2026 08:18:36 GMT
ENV INFLUXDB_VERSION=3.9.3
# Tue, 02 Jun 2026 08:18:36 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 02 Jun 2026 08:18:36 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:18:36 GMT
USER influxdb3
# Tue, 02 Jun 2026 08:18:36 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 02 Jun 2026 08:18:36 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 02 Jun 2026 08:18:36 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 02 Jun 2026 08:18:36 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Tue, 02 Jun 2026 08:18:36 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 02 Jun 2026 08:18:36 GMT
ENV LOG_FILTER=info
# Tue, 02 Jun 2026 08:18:36 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 02 Jun 2026 08:18:36 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 02 Jun 2026 08:18:36 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8192048613ede57b06877b77b5b15c760702a460e00a9765562011f8400eb0bb`  
		Last Modified: Tue, 02 Jun 2026 08:18:53 GMT  
		Size: 6.7 MB (6682530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27ed7b1a518af169037891be86d878895b7227f145c781aebd36f74ad9fcd7d`  
		Last Modified: Tue, 02 Jun 2026 08:18:52 GMT  
		Size: 3.6 KB (3650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb2d6904a22f4fb7087f1f2c30a6e23bd2073a9ee2dab956d0cd30f5947abcd`  
		Last Modified: Tue, 02 Jun 2026 08:18:55 GMT  
		Size: 104.5 MB (104457628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:074caea2353dc9a4845bb7c86ee19e2a8f73f84e90977346ee563b1151cdd090`  
		Last Modified: Tue, 02 Jun 2026 08:18:52 GMT  
		Size: 520.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b39f4df680d32c2cc4a8b4972bc5bb7ccf34344fd92f563674f3edf84db5b4`  
		Last Modified: Tue, 02 Jun 2026 08:18:54 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:2f816d70eced4289a87ff05c535f2b9bfec2ced85b2963e8151aaf7257ee86a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:109d1990ca3ddb26414e25474d80bd5aa0bec2eb53ac24685b91cc44e0de471b`

```dockerfile
```

-	Layers:
	-	`sha256:5750b7d30243168512f6683ab5cdbd26406e419466579cf5426987b9205d6688`  
		Last Modified: Tue, 02 Jun 2026 08:18:53 GMT  
		Size: 2.3 MB (2311697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f98e29d0a3a997b74ea7619ee1a8a6b09b6d11903643126afce417921633da11`  
		Last Modified: Tue, 02 Jun 2026 08:18:52 GMT  
		Size: 17.8 KB (17769 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:data`

```console
$ docker pull influxdb@sha256:9319bb876d60b6611d7314e40ced0a9093badec94380fd788d26fd2ae2258e7f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:data` - linux; amd64

```console
$ docker pull influxdb@sha256:579ca334f033a171c682d34b1c340d2fe8880c3dea2edb1b861f32cbd8a4ab9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115730454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c666f3a65cbb37594d2787f9802d5d13604d24770dd4ac72f6ff5254ed4f02`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:29:41 GMT
ENV INFLUXDB_VERSION=1.12.4-c1.12.4
# Wed, 20 May 2026 00:29:41 GMT
ENV INFLUXDB_PR=
# Wed, 20 May 2026 00:29:41 GMT
ENV INFLUXDB_PV=1.12.4-c1.12.4
# Wed, 20 May 2026 00:29:41 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"          -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"         "influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     rm -r "influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"           "influxdb-data_${INFLUXDB_PV}_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:29:41 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 20 May 2026 00:29:41 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 20 May 2026 00:29:41 GMT
VOLUME [/var/lib/influxdb]
# Wed, 20 May 2026 00:29:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:29:41 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 20 May 2026 00:29:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:29:41 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e51c50554dce9c9549d76c40bfea45780a8342aea81ba8b270ba1bf46a2aec5`  
		Last Modified: Tue, 19 May 2026 23:23:20 GMT  
		Size: 24.0 MB (24043374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122828ed9828493a392d3bbd9540521410cf9cf21e14801d4368427ab3cd94b3`  
		Last Modified: Wed, 20 May 2026 00:29:55 GMT  
		Size: 43.2 MB (43189878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de91331488774fe9e2d09549cd5a5d1e4d157b3accfc4f111eb66f7e8a78ec4`  
		Last Modified: Wed, 20 May 2026 00:29:54 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c650389a0929f427ce6e58d1ef4b9e97645e7409a49c8eae0691bb95ccf3d10`  
		Last Modified: Wed, 20 May 2026 00:29:54 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f5de10629d35972965ab74df4e979631016090bf6e698d40b7bfb3c9399125`  
		Last Modified: Wed, 20 May 2026 00:29:54 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:data` - unknown; unknown

```console
$ docker pull influxdb@sha256:c0e349314838ec27086c03fedc8033ce30c3a691cfe1c4bb0d22ee06c43435d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4707295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb1fc2a0bec89acfd2cad38c8f018acc50a6fd978d2be2f8502e23fecf642dab`

```dockerfile
```

-	Layers:
	-	`sha256:5493b0b0c59fe03e660e43bf5164927cb17f7eaa8fb42fa6778eb7409226336c`  
		Last Modified: Wed, 20 May 2026 00:29:54 GMT  
		Size: 4.7 MB (4693141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3c95869539703cb6ec78b80a3a4fe4b11f4db2ccdf8b38cb792807c5a67dbe2`  
		Last Modified: Wed, 20 May 2026 00:29:54 GMT  
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
$ docker pull influxdb@sha256:835229f278ea2dd7e139450d90ffa5af00dc731cb3dd9379ba42faa250b8a697
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:72a786b354966a3f05b6906464d2f76beb84db58cecc24cb0e54912b7f182215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.5 MB (159473195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58ab121ae6a1686d392793a96e1403a5dc1d919c930c266ed405e801f89f8da2`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:18:35 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 02 Jun 2026 08:18:35 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 02 Jun 2026 08:18:40 GMT
ENV INFLUXDB_VERSION=3.9.3
# Tue, 02 Jun 2026 08:18:40 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 02 Jun 2026 08:18:40 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:18:40 GMT
USER influxdb3
# Tue, 02 Jun 2026 08:18:40 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 02 Jun 2026 08:18:40 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 02 Jun 2026 08:18:40 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 02 Jun 2026 08:18:40 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Tue, 02 Jun 2026 08:18:40 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 02 Jun 2026 08:18:40 GMT
ENV LOG_FILTER=info
# Tue, 02 Jun 2026 08:18:40 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 02 Jun 2026 08:18:40 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 02 Jun 2026 08:18:40 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a93cc4ed173c2d653d9d05b7d7a395ba4b81eb1928e9519e27de5e7c5c512a`  
		Last Modified: Tue, 02 Jun 2026 08:19:00 GMT  
		Size: 6.7 MB (6672941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ec311104fc1c8b0457287201d08b27f8e0e0d998ec499ec0176c11dbb80711`  
		Last Modified: Tue, 02 Jun 2026 08:19:00 GMT  
		Size: 3.7 KB (3651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4f55416553b1818707f5256d494948439a6e118f1f89be90daacda21fe165e`  
		Last Modified: Tue, 02 Jun 2026 08:19:03 GMT  
		Size: 123.1 MB (123063129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312b7602e21e8e22bfd0fe497ee8ddaa5ed6d2be3da38c63da9e77bd19ef3941`  
		Last Modified: Tue, 02 Jun 2026 08:19:00 GMT  
		Size: 521.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:321a561e097c78a830035cdb9bdae97ee44fa5c1100fef65c7c014696b18eab4`  
		Last Modified: Tue, 02 Jun 2026 08:19:01 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:6277afcfb1fcf8ff0d4292c2117da607eeb263195e596f1ddb7b4f6afdb34c6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc4029b765694577339e6cb3c73e3603c3b2f86e7d2c01ffbc263750e971aec7`

```dockerfile
```

-	Layers:
	-	`sha256:8680a032214d875ea9856434d5e294e96f11a911ce1817715039896a28c90baa`  
		Last Modified: Tue, 02 Jun 2026 08:19:00 GMT  
		Size: 2.3 MB (2310663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44b1302e98b859d594b9f6da2289a1b4bf0847f933025e6af94e37bd87a94b1c`  
		Last Modified: Tue, 02 Jun 2026 08:19:00 GMT  
		Size: 17.8 KB (17800 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:a75ee42f999ea6d313c79f36782a188c508560f27a7d53ece147ddcb2f0b41fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.5 MB (150491979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6208cf7be57cdc24eef049f2a862a47216bbea93f0c6836da844dbc85e2fbed9`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:18:42 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 02 Jun 2026 08:18:42 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 02 Jun 2026 08:18:47 GMT
ENV INFLUXDB_VERSION=3.9.3
# Tue, 02 Jun 2026 08:18:47 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 02 Jun 2026 08:18:47 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:18:47 GMT
USER influxdb3
# Tue, 02 Jun 2026 08:18:47 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 02 Jun 2026 08:18:47 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 02 Jun 2026 08:18:47 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 02 Jun 2026 08:18:47 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Tue, 02 Jun 2026 08:18:47 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 02 Jun 2026 08:18:47 GMT
ENV LOG_FILTER=info
# Tue, 02 Jun 2026 08:18:47 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 02 Jun 2026 08:18:47 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 02 Jun 2026 08:18:47 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233d54f9dc825b34a82ea91bcc0754b7d4c154fc7517c9c2962fd01782faeb5d`  
		Last Modified: Tue, 02 Jun 2026 08:19:05 GMT  
		Size: 6.7 MB (6682535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a2cc1e1d488c31fdbbe6a21443745ac798b9b704fbd24811571310ee5430bb`  
		Last Modified: Tue, 02 Jun 2026 08:19:04 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f77332c2036a26b34d8ca49077225fae7607d919bed80b94976639bb3761f5`  
		Last Modified: Tue, 02 Jun 2026 08:19:07 GMT  
		Size: 114.9 MB (114928715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b25c39ebd758c2acb6e101baba666437493a8e1fc5099e4f87c5bf7d94ac02d`  
		Last Modified: Tue, 02 Jun 2026 08:19:04 GMT  
		Size: 520.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d711546eec3630af6fef47c499afbd8c137014757a448713939d2d9d296ae430`  
		Last Modified: Tue, 02 Jun 2026 08:19:06 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:f908b92dfeb8950758d8b9792d421afeeb07f8a58bc34eed302c2944074893c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b51ea865b515f3357856e492f9177f9d6ce02f5d2b9d79d78d1163fda0ba9d7`

```dockerfile
```

-	Layers:
	-	`sha256:ad48a8a10e7cf0a4a543c2ae930eb4d5c84f93d51d7466b7f4251e0bd4710071`  
		Last Modified: Tue, 02 Jun 2026 08:19:04 GMT  
		Size: 2.3 MB (2311745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25ae3771136afb25ff27f8f451c6b2ba3295aaa02db431cd3a00f0da4b5f61a0`  
		Last Modified: Tue, 02 Jun 2026 08:19:04 GMT  
		Size: 17.9 KB (17949 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:latest`

```console
$ docker pull influxdb@sha256:c9acb506f536915c97ff71c971970ad9c2a38b2b8a0d54200ef0ef430f7a37f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:a6f9bf39c55260644b8d92fda430cdb035553e240e9457fcb7e688714ddd58a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.8 MB (110799736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06abeab9b64ea2bcd9a872dbcfbae45956540fd9e5dda9126d43dd9df66536d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:24:55 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg       util-linux &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:24:55 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Tue, 19 May 2026 23:24:56 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 19 May 2026 23:24:58 GMT
ENV INFLUXDB_VERSION=2.9.1
# Tue, 19 May 2026 23:24:58 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 19 May 2026 23:24:58 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Tue, 19 May 2026 23:25:00 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 19 May 2026 23:25:00 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 19 May 2026 23:25:00 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 19 May 2026 23:25:00 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 19 May 2026 23:25:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 May 2026 23:25:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 May 2026 23:25:00 GMT
CMD ["influxd"]
# Tue, 19 May 2026 23:25:00 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 19 May 2026 23:25:00 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 19 May 2026 23:25:00 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 19 May 2026 23:25:00 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 19 May 2026 23:25:00 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c71a21b19bd6c649ea1e324c4d701c55fb5dad2603879df10dc7afaa323d50`  
		Last Modified: Tue, 19 May 2026 23:25:13 GMT  
		Size: 9.8 MB (9800832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717bcf11cb3cc23b0cff75de4a1c15cc7d26323472f95ba3479c845395c59fb1`  
		Last Modified: Tue, 19 May 2026 23:25:12 GMT  
		Size: 3.8 MB (3822787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0d6975a8cc10b47a2b313757955d26198aef78ac28389bf2f456e96f320ca6`  
		Last Modified: Tue, 19 May 2026 23:25:12 GMT  
		Size: 3.2 KB (3235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41371aff054c12f24015975eb32925ecdbe6cd9dabd561244871778f50a16d2b`  
		Last Modified: Tue, 19 May 2026 23:25:14 GMT  
		Size: 56.5 MB (56510574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90cd044c089a7210079f32826689d04869dbaff450297593e1f61877e9d1847`  
		Last Modified: Tue, 19 May 2026 23:25:14 GMT  
		Size: 12.4 MB (12421825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46d8268bc61e87ea71b79fade2d60c9d8f0884a4858f1f24593ca1f188c133b`  
		Last Modified: Tue, 19 May 2026 23:25:14 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9374c3e54ff0378b9306cccc8b9ca7b75fed4a52791bca44370842bc8aa395`  
		Last Modified: Tue, 19 May 2026 23:25:14 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15861eb3c0e7ac9aa7eebb79d91dc4503d36d432b5391d5c79e420b2d8059a64`  
		Last Modified: Tue, 19 May 2026 23:25:15 GMT  
		Size: 6.5 KB (6497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:4cd7dd0ab43920355f0ee88d7fb4896b9243fd07caa0842158c88d9c4af127f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2988043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b77346806c1383c545a78b619c7d6eb2d4d5b513519152c2a4c83484e338a456`

```dockerfile
```

-	Layers:
	-	`sha256:b3126195e2521ecbed67a65602733863692c0969bcfdbd618638132dbebfaead`  
		Last Modified: Tue, 19 May 2026 23:25:12 GMT  
		Size: 3.0 MB (2959429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b288657180483275616cb5620206f8d0a09327d49de6dc37fab5eaeb3b38c28b`  
		Last Modified: Tue, 19 May 2026 23:25:12 GMT  
		Size: 28.6 KB (28614 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:d6fc942f1fae5ff590d663642865f594b48a0756071c498be8eb38b0d6770574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106330815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea2fc64efaf734880bc89ce2fed2ad2396ea48636bcd90f7b135f7e85fefd70f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:28:14 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg       util-linux &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:28:15 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Tue, 19 May 2026 23:28:15 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 19 May 2026 23:28:18 GMT
ENV INFLUXDB_VERSION=2.9.1
# Tue, 19 May 2026 23:28:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 19 May 2026 23:28:18 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Tue, 19 May 2026 23:28:19 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 19 May 2026 23:28:20 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 19 May 2026 23:28:20 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 19 May 2026 23:28:20 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 19 May 2026 23:28:20 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 May 2026 23:28:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 May 2026 23:28:20 GMT
CMD ["influxd"]
# Tue, 19 May 2026 23:28:20 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 19 May 2026 23:28:20 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 19 May 2026 23:28:20 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 19 May 2026 23:28:20 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 19 May 2026 23:28:20 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a3e4fdf0759b602cc83eee55bb98191a184bf47394c125416bad56fd14cf2e`  
		Last Modified: Tue, 19 May 2026 23:28:31 GMT  
		Size: 9.6 MB (9629316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69d1631bd9b1dc8d27a448997e0d90af077c96a2041f16eb89751cd7a188383`  
		Last Modified: Tue, 19 May 2026 23:28:31 GMT  
		Size: 3.5 MB (3459173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3843f9e7c58fc79d623603a0448fe5eb8b646c9acb86278e08024e28e90e6e1a`  
		Last Modified: Tue, 19 May 2026 23:28:31 GMT  
		Size: 3.2 KB (3227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b748a12a94328f10d7c957a9ef02934ab7b468161e7f3274c68923d716de920d`  
		Last Modified: Tue, 19 May 2026 23:28:33 GMT  
		Size: 53.6 MB (53636820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40bad5774d9135c6e7eabc80742652a79641e86bd6a0f05b13a385c47764bc20`  
		Last Modified: Tue, 19 May 2026 23:28:32 GMT  
		Size: 11.5 MB (11480296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e4221fc8c1ab93c69cafbc88cb0214ea6877c204266846e6add1891ea58a891`  
		Last Modified: Tue, 19 May 2026 23:28:32 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129703821150bfc0ff6995ffa921aaca455ba27668ec104ae6ff73b58cfbba8c`  
		Last Modified: Tue, 19 May 2026 23:28:32 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7424fffba09e6f72ae806428342ccfd9cf858d0dfa3e1acbf6111cf5603a85fe`  
		Last Modified: Tue, 19 May 2026 23:28:33 GMT  
		Size: 6.5 KB (6499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:ba793f9c250c21d96c0eccc2bf682b93706548fcc7def232da980c3ce77bd9b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca7a7141b9565f983497bde826dc595445dbd26abef6d664c30cd7d78280717f`

```dockerfile
```

-	Layers:
	-	`sha256:b176ade03bf084e3c8722d038d297af9345b5ff626542e7bb237a7adc6b1b5aa`  
		Last Modified: Tue, 19 May 2026 23:28:31 GMT  
		Size: 3.0 MB (2958907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a53002c50db871c40a28faf2f74b6de4d013e714ecc96cbbfcbc68704f320026`  
		Last Modified: Tue, 19 May 2026 23:28:31 GMT  
		Size: 28.8 KB (28793 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:meta`

```console
$ docker pull influxdb@sha256:eb1275d9a00d3d902dd398f2eff0c8255039191767cea04c0007f41b22500756
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:meta` - linux; amd64

```console
$ docker pull influxdb@sha256:57a044b67fbcc59869345506b2c3e911a8f5f0917bbef96777c10469d6f82d1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91924518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b463ccdbb88aeddac659fe2cb6f4bf528d2fa31712966603f303ce742a8c90e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:29:46 GMT
ENV INFLUXDB_VERSION=1.12.4-c1.12.4
# Wed, 20 May 2026 00:29:46 GMT
ENV INFLUXDB_PR=
# Wed, 20 May 2026 00:29:46 GMT
ENV INFLUXDB_PV=1.12.4-c1.12.4
# Wed, 20 May 2026 00:29:46 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"          -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"         "influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     rm -r "influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"           "influxdb-meta_${INFLUXDB_PV}_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:29:46 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Wed, 20 May 2026 00:29:46 GMT
EXPOSE map[8091/tcp:{}]
# Wed, 20 May 2026 00:29:46 GMT
VOLUME [/var/lib/influxdb]
# Wed, 20 May 2026 00:29:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 20 May 2026 00:29:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 May 2026 00:29:46 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e51c50554dce9c9549d76c40bfea45780a8342aea81ba8b270ba1bf46a2aec5`  
		Last Modified: Tue, 19 May 2026 23:23:20 GMT  
		Size: 24.0 MB (24043374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231a6a12e39a684b8ef400973532085455b3543f371d1bb90f45442900340a6b`  
		Last Modified: Wed, 20 May 2026 00:29:56 GMT  
		Size: 19.4 MB (19385146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c88a42d2f3e78083f3422ab9fee7830022e74612847d646975dc0e445f467b`  
		Last Modified: Wed, 20 May 2026 00:29:55 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f6fcdeed90a4e263d4d42f8469c6a2f871ea40910010f73940c93664a9bd45`  
		Last Modified: Wed, 20 May 2026 00:29:55 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:6262a32495c2a4fff37a1137f8904b95d7aa4f6d6c66a4190ae73ae7052d82ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4605873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:517704ae2ac63a1323353df03f5108b0356a0a9eb2898e249df613a4d7cf2031`

```dockerfile
```

-	Layers:
	-	`sha256:0a7f7f23c71460ad60a701c4198a800a0f496f8dd4e1b4cc08f25b1ba5cfea80`  
		Last Modified: Wed, 20 May 2026 00:29:56 GMT  
		Size: 4.6 MB (4593209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:534a176d731bc426208fe21876a10f5f82a0dacb9772e2443aaeaaa1ecc6ed18`  
		Last Modified: Wed, 20 May 2026 00:29:56 GMT  
		Size: 12.7 KB (12664 bytes)  
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
