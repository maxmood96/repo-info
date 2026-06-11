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
$ docker pull influxdb@sha256:a8497f6c8bcf742eae6373198ebc888a25570c32ed5428274117ddb7b056a18b
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
$ docker pull influxdb@sha256:6a30e62d548a3cba20706e0c50ef7c60f10c17521b4058973566be906c3b20d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113133593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:908425b2c16ef824517be27dc008ab6492c341a438a78293e4d28c4c2843c597`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:43:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:29:08 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Thu, 11 Jun 2026 02:29:15 GMT
ARG INFLUXDB_VERSION=1.11.8
# Thu, 11 Jun 2026 02:29:15 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:29:15 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 11 Jun 2026 02:29:15 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jun 2026 02:29:15 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jun 2026 02:29:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 02:29:15 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 11 Jun 2026 02:29:15 GMT
USER influxdb
# Thu, 11 Jun 2026 02:29:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 02:29:15 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f511b4c80a6e453785fbcd573c1bf1cb986c4e8d43ed4500ad1ac9a4719762b`  
		Last Modified: Thu, 11 Jun 2026 00:43:56 GMT  
		Size: 23.6 MB (23613296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85e233edb1b0a266b0d7b25eb92a6ad2acc84d018a3e0057b2873e5b67b860a`  
		Last Modified: Thu, 11 Jun 2026 02:29:27 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09e1cf605baef7f4f1f973e129de4121cea2d14c55a8a07192f0ff7bc2dd495`  
		Last Modified: Thu, 11 Jun 2026 02:29:29 GMT  
		Size: 41.1 MB (41128373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52413e9e0444c2d33fb2b5aa603f7004546b23c44661779f8072793c73d85608`  
		Last Modified: Thu, 11 Jun 2026 02:29:27 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4489947f36bef3f7b7993d6afb5ef01655bb07e2d36235d2ec7d5d98c167f0`  
		Last Modified: Thu, 11 Jun 2026 02:29:27 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a036cc9da235e2d2d3722bc0ed24e09c921e74002072eea764ccbc317a886be`  
		Last Modified: Thu, 11 Jun 2026 02:29:28 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11` - unknown; unknown

```console
$ docker pull influxdb@sha256:45d71af16d2db52a780fadced67ad01b3fe2f5dbde7c2ee5593084fd5ff58d83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd1e90a12797c1b125726213ad5f3fea425d29e708a74ab73717723de5b5bc91`

```dockerfile
```

-	Layers:
	-	`sha256:86880c24aa87f73875984c67c8465816113c622222df423a145fa29acfcb667c`  
		Last Modified: Thu, 11 Jun 2026 02:29:28 GMT  
		Size: 5.1 MB (5078772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52494d69c6b41d868d1583a0305be3e9a233e58d22eef4f7336d174bc064d055`  
		Last Modified: Thu, 11 Jun 2026 02:29:27 GMT  
		Size: 15.6 KB (15578 bytes)  
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
$ docker pull influxdb@sha256:a8497f6c8bcf742eae6373198ebc888a25570c32ed5428274117ddb7b056a18b
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
$ docker pull influxdb@sha256:6a30e62d548a3cba20706e0c50ef7c60f10c17521b4058973566be906c3b20d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113133593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:908425b2c16ef824517be27dc008ab6492c341a438a78293e4d28c4c2843c597`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:43:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:29:08 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Thu, 11 Jun 2026 02:29:15 GMT
ARG INFLUXDB_VERSION=1.11.8
# Thu, 11 Jun 2026 02:29:15 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:29:15 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 11 Jun 2026 02:29:15 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jun 2026 02:29:15 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jun 2026 02:29:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 02:29:15 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 11 Jun 2026 02:29:15 GMT
USER influxdb
# Thu, 11 Jun 2026 02:29:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 02:29:15 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f511b4c80a6e453785fbcd573c1bf1cb986c4e8d43ed4500ad1ac9a4719762b`  
		Last Modified: Thu, 11 Jun 2026 00:43:56 GMT  
		Size: 23.6 MB (23613296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85e233edb1b0a266b0d7b25eb92a6ad2acc84d018a3e0057b2873e5b67b860a`  
		Last Modified: Thu, 11 Jun 2026 02:29:27 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09e1cf605baef7f4f1f973e129de4121cea2d14c55a8a07192f0ff7bc2dd495`  
		Last Modified: Thu, 11 Jun 2026 02:29:29 GMT  
		Size: 41.1 MB (41128373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52413e9e0444c2d33fb2b5aa603f7004546b23c44661779f8072793c73d85608`  
		Last Modified: Thu, 11 Jun 2026 02:29:27 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4489947f36bef3f7b7993d6afb5ef01655bb07e2d36235d2ec7d5d98c167f0`  
		Last Modified: Thu, 11 Jun 2026 02:29:27 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a036cc9da235e2d2d3722bc0ed24e09c921e74002072eea764ccbc317a886be`  
		Last Modified: Thu, 11 Jun 2026 02:29:28 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:45d71af16d2db52a780fadced67ad01b3fe2f5dbde7c2ee5593084fd5ff58d83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd1e90a12797c1b125726213ad5f3fea425d29e708a74ab73717723de5b5bc91`

```dockerfile
```

-	Layers:
	-	`sha256:86880c24aa87f73875984c67c8465816113c622222df423a145fa29acfcb667c`  
		Last Modified: Thu, 11 Jun 2026 02:29:28 GMT  
		Size: 5.1 MB (5078772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52494d69c6b41d868d1583a0305be3e9a233e58d22eef4f7336d174bc064d055`  
		Last Modified: Thu, 11 Jun 2026 02:29:27 GMT  
		Size: 15.6 KB (15578 bytes)  
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
$ docker pull influxdb@sha256:2b794658c336f952df0923fe362d7c19fa4fec1ce944eafbbcef37c1a32fec02
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
$ docker pull influxdb@sha256:716b4e7df5355ff3ca0c6236c6af907f615477b7a7d1b82c43924e58bcc6c81f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.8 MB (110759555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd2b76c53755671c6ac4e0b00ad0d3110e941ea9a9d90b23bfae3f565e8ab7f3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:43:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:29:06 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Thu, 11 Jun 2026 02:29:12 GMT
ENV INFLUXDB_VERSION=1.12.4
# Thu, 11 Jun 2026 02:29:12 GMT
ENV INFLUXDB_PR=-1
# Thu, 11 Jun 2026 02:29:12 GMT
ENV INFLUXDB_PV=1.12.4-1
# Thu, 11 Jun 2026 02:29:12 GMT
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_PV}_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:29:12 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 11 Jun 2026 02:29:12 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jun 2026 02:29:12 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jun 2026 02:29:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 02:29:12 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 11 Jun 2026 02:29:12 GMT
USER influxdb
# Thu, 11 Jun 2026 02:29:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 02:29:12 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f511b4c80a6e453785fbcd573c1bf1cb986c4e8d43ed4500ad1ac9a4719762b`  
		Last Modified: Thu, 11 Jun 2026 00:43:56 GMT  
		Size: 23.6 MB (23613296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7fea6389e774308469e6f7f2df24b7205ff321660b48fc7d67394f828275195`  
		Last Modified: Thu, 11 Jun 2026 02:29:24 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf31ccf1ac9abeb5f55aea56ec844c63595a20be7256b35f400879ef78bf7380`  
		Last Modified: Thu, 11 Jun 2026 02:29:25 GMT  
		Size: 38.8 MB (38754333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53b58bd0518200f01fb87f71e57f4445ed14fa2e194781c979eff89f6de46ff`  
		Last Modified: Thu, 11 Jun 2026 02:29:24 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984aaa1e8a8ae2c7808680b68a0e13c112dd5085b91b0b8a4f4b2319f259fdb2`  
		Last Modified: Thu, 11 Jun 2026 02:29:24 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54dbb22c51be188177bdb6401e1658790b89248bb185c52be35908e984c2c0d0`  
		Last Modified: Thu, 11 Jun 2026 02:29:25 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:90dce491ca27ada405206c71df775fce99ca1dfc928072de20efbc52177bcc71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc046a26d15b49d9dca919463e7db9325ca0e69ce580fa9bce0fddd53e9dd245`

```dockerfile
```

-	Layers:
	-	`sha256:339955ab37bd76b282501c1497194a6b114606f06b97edfc7e94af7b0faadfd8`  
		Last Modified: Thu, 11 Jun 2026 02:29:24 GMT  
		Size: 4.7 MB (4677625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33e9c72cec73317f76be8b313c21366e41c74f1ca08da940433a6147755dbd34`  
		Last Modified: Thu, 11 Jun 2026 02:29:23 GMT  
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
$ docker pull influxdb@sha256:2b794658c336f952df0923fe362d7c19fa4fec1ce944eafbbcef37c1a32fec02
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
$ docker pull influxdb@sha256:716b4e7df5355ff3ca0c6236c6af907f615477b7a7d1b82c43924e58bcc6c81f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.8 MB (110759555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd2b76c53755671c6ac4e0b00ad0d3110e941ea9a9d90b23bfae3f565e8ab7f3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:43:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:29:06 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Thu, 11 Jun 2026 02:29:12 GMT
ENV INFLUXDB_VERSION=1.12.4
# Thu, 11 Jun 2026 02:29:12 GMT
ENV INFLUXDB_PR=-1
# Thu, 11 Jun 2026 02:29:12 GMT
ENV INFLUXDB_PV=1.12.4-1
# Thu, 11 Jun 2026 02:29:12 GMT
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_PV}_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:29:12 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Thu, 11 Jun 2026 02:29:12 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jun 2026 02:29:12 GMT
VOLUME [/var/lib/influxdb]
# Thu, 11 Jun 2026 02:29:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 02:29:12 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Thu, 11 Jun 2026 02:29:12 GMT
USER influxdb
# Thu, 11 Jun 2026 02:29:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 02:29:12 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f511b4c80a6e453785fbcd573c1bf1cb986c4e8d43ed4500ad1ac9a4719762b`  
		Last Modified: Thu, 11 Jun 2026 00:43:56 GMT  
		Size: 23.6 MB (23613296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7fea6389e774308469e6f7f2df24b7205ff321660b48fc7d67394f828275195`  
		Last Modified: Thu, 11 Jun 2026 02:29:24 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf31ccf1ac9abeb5f55aea56ec844c63595a20be7256b35f400879ef78bf7380`  
		Last Modified: Thu, 11 Jun 2026 02:29:25 GMT  
		Size: 38.8 MB (38754333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53b58bd0518200f01fb87f71e57f4445ed14fa2e194781c979eff89f6de46ff`  
		Last Modified: Thu, 11 Jun 2026 02:29:24 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984aaa1e8a8ae2c7808680b68a0e13c112dd5085b91b0b8a4f4b2319f259fdb2`  
		Last Modified: Thu, 11 Jun 2026 02:29:24 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54dbb22c51be188177bdb6401e1658790b89248bb185c52be35908e984c2c0d0`  
		Last Modified: Thu, 11 Jun 2026 02:29:25 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.4` - unknown; unknown

```console
$ docker pull influxdb@sha256:90dce491ca27ada405206c71df775fce99ca1dfc928072de20efbc52177bcc71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc046a26d15b49d9dca919463e7db9325ca0e69ce580fa9bce0fddd53e9dd245`

```dockerfile
```

-	Layers:
	-	`sha256:339955ab37bd76b282501c1497194a6b114606f06b97edfc7e94af7b0faadfd8`  
		Last Modified: Thu, 11 Jun 2026 02:29:24 GMT  
		Size: 4.7 MB (4677625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33e9c72cec73317f76be8b313c21366e41c74f1ca08da940433a6147755dbd34`  
		Last Modified: Thu, 11 Jun 2026 02:29:23 GMT  
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
$ docker pull influxdb@sha256:003e028b675205f6148e5f30369fd3e854993b385f1e5e4d2d85bc9f8701bf28
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2` - linux; amd64

```console
$ docker pull influxdb@sha256:b3b6db425bd08e5173b3a8168de701c22526dbbc4eb4ca10ca25e00db57114f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.8 MB (110803771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:216fc6047d5548b9cedd5f8900ccc269534f2e7c6d51cb8015384a9d8687e300`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:44:09 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg       util-linux &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:44:10 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Thu, 11 Jun 2026 00:44:10 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 11 Jun 2026 00:44:13 GMT
ENV INFLUXDB_VERSION=2.9.1
# Thu, 11 Jun 2026 00:44:13 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 11 Jun 2026 00:44:13 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Thu, 11 Jun 2026 00:44:15 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 11 Jun 2026 00:44:15 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 11 Jun 2026 00:44:15 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Jun 2026 00:44:15 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 11 Jun 2026 00:44:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 00:44:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 00:44:15 GMT
CMD ["influxd"]
# Thu, 11 Jun 2026 00:44:15 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jun 2026 00:44:15 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Jun 2026 00:44:15 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Jun 2026 00:44:15 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Jun 2026 00:44:15 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca13784c2e80ea84bbe25bdc33fa82008ff90ee6404be9419dbbe50f82081f91`  
		Last Modified: Thu, 11 Jun 2026 00:44:27 GMT  
		Size: 9.8 MB (9800747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886d8448c571631facc9fe146e26ac66d1b7eb4e0d26934112fdb91a9ca5d9fe`  
		Last Modified: Thu, 11 Jun 2026 00:44:27 GMT  
		Size: 3.8 MB (3822785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d091ef401709b2e0d66f2524bfa92dc53a7628b79460615e607ea51b1761b604`  
		Last Modified: Thu, 11 Jun 2026 00:44:27 GMT  
		Size: 3.2 KB (3229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473282447769ed378f1718d94cfa4240c087e9c693569b46450cbc60a65b7bf8`  
		Last Modified: Thu, 11 Jun 2026 00:44:29 GMT  
		Size: 56.5 MB (56510619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4d2daebcc5a61d6df052588fbb02d58c6f6fba47533d6a032f1a5606c200a3`  
		Last Modified: Thu, 11 Jun 2026 00:44:28 GMT  
		Size: 12.4 MB (12421826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599b7e6339adf53f34ef2b25bd501d42f3eaa40a0a4525d2d009a12ebc026f92`  
		Last Modified: Thu, 11 Jun 2026 00:44:28 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b16bfd3cd1b9b650256b1e2089f7eff3b975d13e250b9fe01d1581f720d345`  
		Last Modified: Thu, 11 Jun 2026 00:44:29 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d442aae476f79aefc39fab6b4b3145f8f5fc7b00798769204f7624a443b611c`  
		Last Modified: Thu, 11 Jun 2026 00:44:30 GMT  
		Size: 6.5 KB (6499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:4b9b3dcd93e61c6911d100560807fd99efe5e5489aa3178b393b687d07009353
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2988061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c96ffda826f90beec04d953f68df55a73052203726258734c11b450f0cfbec7`

```dockerfile
```

-	Layers:
	-	`sha256:f3b378e41b794fbbfecb4f8ff82b963f1281dacea9cddc8e2c7f985ad71ac812`  
		Last Modified: Thu, 11 Jun 2026 00:44:27 GMT  
		Size: 3.0 MB (2959447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b465a9d35a369365b1479b9d69fd50db2fcbe039aa0f5520d4ad44c8198cd6f2`  
		Last Modified: Thu, 11 Jun 2026 00:44:26 GMT  
		Size: 28.6 KB (28614 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:e5d7d3f2475b666d5dd9e9602b118ac5c30c400bc2a9265ee329a06a0b08ebba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106337789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ba9fe5b6043ebcffd255286e160ba78347f7df11b5cd2b9ef11832f517c49ba`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:45:48 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg       util-linux &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:49 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Thu, 11 Jun 2026 00:45:49 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 11 Jun 2026 00:45:53 GMT
ENV INFLUXDB_VERSION=2.9.1
# Thu, 11 Jun 2026 00:45:53 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 11 Jun 2026 00:45:53 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Thu, 11 Jun 2026 00:45:55 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 11 Jun 2026 00:45:55 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 11 Jun 2026 00:45:55 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Jun 2026 00:45:55 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 11 Jun 2026 00:45:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 00:45:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 00:45:55 GMT
CMD ["influxd"]
# Thu, 11 Jun 2026 00:45:55 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jun 2026 00:45:55 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Jun 2026 00:45:55 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Jun 2026 00:45:55 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Jun 2026 00:45:55 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57bb39aa14de947a30f716a21ccc5488e944ce97b3711471a0e593001c28540`  
		Last Modified: Thu, 11 Jun 2026 00:46:07 GMT  
		Size: 9.6 MB (9629019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723baea35ef3ea8149bffeb1c30de73f358f632d869398b34a1c1d98b04e32bb`  
		Last Modified: Thu, 11 Jun 2026 00:46:07 GMT  
		Size: 3.5 MB (3459177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33414b33f32babd71285978fd56dae58d2931354f14783dab98a03f7880c688b`  
		Last Modified: Thu, 11 Jun 2026 00:46:06 GMT  
		Size: 3.2 KB (3228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c509bc7d25f3f9c5fb74fe5296dfb524eacb802433fb61b91ca8282f1cf5f0b`  
		Last Modified: Thu, 11 Jun 2026 00:46:08 GMT  
		Size: 53.6 MB (53636817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14f7108738c858ce74317b9a4029306bdcfd76cb4a6ca31c5c6b71c7e444e5b`  
		Last Modified: Thu, 11 Jun 2026 00:46:08 GMT  
		Size: 11.5 MB (11480300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2193a6345188a1f23214372c687a7ec0c537b748e6228ccf1d8aeeb5ef1ce381`  
		Last Modified: Thu, 11 Jun 2026 00:46:08 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7d973f0e880b165170182660e4a002f2354b3aeef79911af0f9a1a6326fd47`  
		Last Modified: Thu, 11 Jun 2026 00:46:09 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dedd3e27ede6904e2b5729b403f87645b4d7206f51292f5c8145da8d30fc050`  
		Last Modified: Thu, 11 Jun 2026 00:46:09 GMT  
		Size: 6.5 KB (6499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:e26bf54687a5af9cbdd36b95e8da5236a05237654a3eec88fb48af5bf64c00aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d014559c4fac67f921a2db2b95dbf0994a755b966118dc68ee0f57212f33ce9c`

```dockerfile
```

-	Layers:
	-	`sha256:819cf5530c1f61f319767f0599b728ecae98dcb92129fdb8b1add1c5b716e751`  
		Last Modified: Thu, 11 Jun 2026 00:46:07 GMT  
		Size: 3.0 MB (2958925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aab4dee5b6a157c159c496a92e6fcd3792cbcf34116e14d2bbecdbdaf214ebc0`  
		Last Modified: Thu, 11 Jun 2026 00:46:07 GMT  
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
$ docker pull influxdb@sha256:7513c5061ec51f2c53852926b989a14803f285ae4c332f635560394d821defc5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.8` - linux; amd64

```console
$ docker pull influxdb@sha256:2703824926e22674b7d53ea61faa7a8d9dbe911f17284754a1bdf79de642aabb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107244497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be95b306d8fa48c455e6f8daf621be7b2d4cceebb29265c634ff22de41bcf394`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:44:11 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:44:12 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 11 Jun 2026 00:44:12 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 11 Jun 2026 00:44:13 GMT
ENV GOSU_VER=1.19
# Thu, 11 Jun 2026 00:44:13 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 11 Jun 2026 00:44:13 GMT
ENV INFLUXDB_VERSION=2.8.0
# Thu, 11 Jun 2026 00:44:13 GMT
ENV INFLUXDB_PR=-2
# Thu, 11 Jun 2026 00:44:13 GMT
ENV INFLUXDB_PV=2.8.0-2
# Thu, 11 Jun 2026 00:44:16 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 11 Jun 2026 00:44:16 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Thu, 11 Jun 2026 00:44:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 11 Jun 2026 00:44:18 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 11 Jun 2026 00:44:18 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Jun 2026 00:44:18 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 11 Jun 2026 00:44:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 00:44:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 00:44:18 GMT
CMD ["influxd"]
# Thu, 11 Jun 2026 00:44:18 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jun 2026 00:44:18 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Jun 2026 00:44:18 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Jun 2026 00:44:18 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Jun 2026 00:44:18 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529345c15664700bf6c772d363067259b293c1c5e412c438c13ec41e39a66ce0`  
		Last Modified: Thu, 11 Jun 2026 00:44:31 GMT  
		Size: 9.8 MB (9800770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6aa63fc2e093338990e254a1e301dbbbd024ba542fadd8ef120e620b9e486a5`  
		Last Modified: Thu, 11 Jun 2026 00:44:31 GMT  
		Size: 6.2 MB (6156982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478be563530c2f440279228cd80be0dbd3d3aa2d0e6c069fdcc2fbf22c33adc1`  
		Last Modified: Thu, 11 Jun 2026 00:44:30 GMT  
		Size: 3.2 KB (3227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352fc288a2629465aac98b474df732fe739291d8a89665d284db2483f54df434`  
		Last Modified: Thu, 11 Jun 2026 00:44:31 GMT  
		Size: 811.5 KB (811474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca93d49127d44a0050c7db779754c13f4951df70fbd8e1723eb076e79fedcfb`  
		Last Modified: Thu, 11 Jun 2026 00:44:33 GMT  
		Size: 50.5 MB (50451820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad91105fe2b28bcdbb8253705f26cd9a6b6e222a8d63786dc248b5ae87796018`  
		Last Modified: Thu, 11 Jun 2026 00:44:33 GMT  
		Size: 11.8 MB (11775874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e23a76a4c9563c7b2b60026ffbaa6ebeb77b51143892ad0836ea28ac9584b4`  
		Last Modified: Thu, 11 Jun 2026 00:44:32 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d4a721824e59808f27d261bd866f17b6f14764bea0d140b3fa8afdbf5fed53`  
		Last Modified: Thu, 11 Jun 2026 00:44:32 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e79b1ea7f27efcd493d0014ea7c7b99497a031e4c10c7a05356cc076886bbc0`  
		Last Modified: Thu, 11 Jun 2026 00:44:34 GMT  
		Size: 6.3 KB (6284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:5d44e5af132d683755495d3fd016cf81286d716be68d54836dde0378ef3b93d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2966706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e738773c65d3e1c8b738eddc76c6407fdc78c78d8fb26483c9bd15b4f1ed19c`

```dockerfile
```

-	Layers:
	-	`sha256:c5074621ea46459df87e4f65801eedd2c5b2657723bcea212acb46f41edab714`  
		Last Modified: Thu, 11 Jun 2026 00:44:30 GMT  
		Size: 2.9 MB (2933679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:980eb274dfa19f6d25cce97abaa0344df4ff51503fa7ede8550a47ebc64aaa40`  
		Last Modified: Thu, 11 Jun 2026 00:44:30 GMT  
		Size: 33.0 KB (33027 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:91c43ca0d35647700a512b6aadbe649cb663c5c352991d2f5e05882ebf1aae78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103648054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba688332d86cf22dbb4f05bd812c4f0b951f68d10f8579e33e7b76b8d1724f25`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:45:42 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:43 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 11 Jun 2026 00:45:43 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 11 Jun 2026 00:45:45 GMT
ENV GOSU_VER=1.19
# Thu, 11 Jun 2026 00:45:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 11 Jun 2026 00:45:45 GMT
ENV INFLUXDB_VERSION=2.8.0
# Thu, 11 Jun 2026 00:45:45 GMT
ENV INFLUXDB_PR=-2
# Thu, 11 Jun 2026 00:45:45 GMT
ENV INFLUXDB_PV=2.8.0-2
# Thu, 11 Jun 2026 00:45:48 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 11 Jun 2026 00:45:48 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Thu, 11 Jun 2026 00:45:49 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 11 Jun 2026 00:45:50 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 11 Jun 2026 00:45:50 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Jun 2026 00:45:50 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 11 Jun 2026 00:45:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 00:45:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 00:45:50 GMT
CMD ["influxd"]
# Thu, 11 Jun 2026 00:45:50 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jun 2026 00:45:50 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Jun 2026 00:45:50 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Jun 2026 00:45:50 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Jun 2026 00:45:50 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bde372557c257cfd6df534f0978470cecf9aa4374c0d3341d436c61cd9beca3`  
		Last Modified: Thu, 11 Jun 2026 00:46:01 GMT  
		Size: 9.6 MB (9629046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a056ca077ceeb56fd322cd484f3962d1013556888c14cfbac9b97b2872c4c099`  
		Last Modified: Thu, 11 Jun 2026 00:46:01 GMT  
		Size: 5.8 MB (5790426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4d7bb97778ae47010fce608019871893df9eaffab0719e8c7984110a0f1cef`  
		Last Modified: Thu, 11 Jun 2026 00:46:00 GMT  
		Size: 3.2 KB (3227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214aa125b3e88476d4b9445ce1ad15d1a4e61288059165698d46a3ac3d35ce07`  
		Last Modified: Thu, 11 Jun 2026 00:46:00 GMT  
		Size: 766.4 KB (766373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafc3eba862413f79580c977b72fa1f4690c95e889c455b8c764a214fda9c851`  
		Last Modified: Thu, 11 Jun 2026 00:46:03 GMT  
		Size: 48.2 MB (48229552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f70f2940f0e1a1c53c4204bb66b7acb5ca5bd67472ca4361af1150d3b331d4`  
		Last Modified: Thu, 11 Jun 2026 00:46:02 GMT  
		Size: 11.1 MB (11100394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646af7e3d3670f4561ba56e36cc7d4a4d23d647d375a95fae0cc8e161cf32dff`  
		Last Modified: Thu, 11 Jun 2026 00:46:02 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11630d81ca7a752a8f5064d73260c9db176fff2939aaa335cb2e12b6ba3bd29b`  
		Last Modified: Thu, 11 Jun 2026 00:46:03 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8ccfd85c51b64d62c78bee99c49d7cd2517bf113610a2c4871b4d3d3d0c6ec`  
		Last Modified: Thu, 11 Jun 2026 00:46:03 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:59cf0c4bb05525e7cb7f29d28dfc6b20afbb54ff67b7aae19125fd22a062cfb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2966332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa7b5b3ac0ed1827b96f50f77472913a14c0e988b658d2788b5336c127667497`

```dockerfile
```

-	Layers:
	-	`sha256:e6b58fd0e2f332d2420279575b59f57470dc437b079a3bfda5d4aca5b564ebca`  
		Last Modified: Thu, 11 Jun 2026 00:46:01 GMT  
		Size: 2.9 MB (2933135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f122c5f8cee6307f0c07ec4199828b1e946002feaeb9cd80db02954b8137ca02`  
		Last Modified: Thu, 11 Jun 2026 00:46:01 GMT  
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
$ docker pull influxdb@sha256:7513c5061ec51f2c53852926b989a14803f285ae4c332f635560394d821defc5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.8.0` - linux; amd64

```console
$ docker pull influxdb@sha256:2703824926e22674b7d53ea61faa7a8d9dbe911f17284754a1bdf79de642aabb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107244497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be95b306d8fa48c455e6f8daf621be7b2d4cceebb29265c634ff22de41bcf394`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:44:11 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:44:12 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 11 Jun 2026 00:44:12 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 11 Jun 2026 00:44:13 GMT
ENV GOSU_VER=1.19
# Thu, 11 Jun 2026 00:44:13 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 11 Jun 2026 00:44:13 GMT
ENV INFLUXDB_VERSION=2.8.0
# Thu, 11 Jun 2026 00:44:13 GMT
ENV INFLUXDB_PR=-2
# Thu, 11 Jun 2026 00:44:13 GMT
ENV INFLUXDB_PV=2.8.0-2
# Thu, 11 Jun 2026 00:44:16 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 11 Jun 2026 00:44:16 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Thu, 11 Jun 2026 00:44:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 11 Jun 2026 00:44:18 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 11 Jun 2026 00:44:18 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Jun 2026 00:44:18 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 11 Jun 2026 00:44:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 00:44:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 00:44:18 GMT
CMD ["influxd"]
# Thu, 11 Jun 2026 00:44:18 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jun 2026 00:44:18 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Jun 2026 00:44:18 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Jun 2026 00:44:18 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Jun 2026 00:44:18 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529345c15664700bf6c772d363067259b293c1c5e412c438c13ec41e39a66ce0`  
		Last Modified: Thu, 11 Jun 2026 00:44:31 GMT  
		Size: 9.8 MB (9800770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6aa63fc2e093338990e254a1e301dbbbd024ba542fadd8ef120e620b9e486a5`  
		Last Modified: Thu, 11 Jun 2026 00:44:31 GMT  
		Size: 6.2 MB (6156982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478be563530c2f440279228cd80be0dbd3d3aa2d0e6c069fdcc2fbf22c33adc1`  
		Last Modified: Thu, 11 Jun 2026 00:44:30 GMT  
		Size: 3.2 KB (3227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352fc288a2629465aac98b474df732fe739291d8a89665d284db2483f54df434`  
		Last Modified: Thu, 11 Jun 2026 00:44:31 GMT  
		Size: 811.5 KB (811474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca93d49127d44a0050c7db779754c13f4951df70fbd8e1723eb076e79fedcfb`  
		Last Modified: Thu, 11 Jun 2026 00:44:33 GMT  
		Size: 50.5 MB (50451820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad91105fe2b28bcdbb8253705f26cd9a6b6e222a8d63786dc248b5ae87796018`  
		Last Modified: Thu, 11 Jun 2026 00:44:33 GMT  
		Size: 11.8 MB (11775874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e23a76a4c9563c7b2b60026ffbaa6ebeb77b51143892ad0836ea28ac9584b4`  
		Last Modified: Thu, 11 Jun 2026 00:44:32 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d4a721824e59808f27d261bd866f17b6f14764bea0d140b3fa8afdbf5fed53`  
		Last Modified: Thu, 11 Jun 2026 00:44:32 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e79b1ea7f27efcd493d0014ea7c7b99497a031e4c10c7a05356cc076886bbc0`  
		Last Modified: Thu, 11 Jun 2026 00:44:34 GMT  
		Size: 6.3 KB (6284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8.0` - unknown; unknown

```console
$ docker pull influxdb@sha256:5d44e5af132d683755495d3fd016cf81286d716be68d54836dde0378ef3b93d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2966706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e738773c65d3e1c8b738eddc76c6407fdc78c78d8fb26483c9bd15b4f1ed19c`

```dockerfile
```

-	Layers:
	-	`sha256:c5074621ea46459df87e4f65801eedd2c5b2657723bcea212acb46f41edab714`  
		Last Modified: Thu, 11 Jun 2026 00:44:30 GMT  
		Size: 2.9 MB (2933679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:980eb274dfa19f6d25cce97abaa0344df4ff51503fa7ede8550a47ebc64aaa40`  
		Last Modified: Thu, 11 Jun 2026 00:44:30 GMT  
		Size: 33.0 KB (33027 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.8.0` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:91c43ca0d35647700a512b6aadbe649cb663c5c352991d2f5e05882ebf1aae78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103648054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba688332d86cf22dbb4f05bd812c4f0b951f68d10f8579e33e7b76b8d1724f25`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:45:42 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:43 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 11 Jun 2026 00:45:43 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 11 Jun 2026 00:45:45 GMT
ENV GOSU_VER=1.19
# Thu, 11 Jun 2026 00:45:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Thu, 11 Jun 2026 00:45:45 GMT
ENV INFLUXDB_VERSION=2.8.0
# Thu, 11 Jun 2026 00:45:45 GMT
ENV INFLUXDB_PR=-2
# Thu, 11 Jun 2026 00:45:45 GMT
ENV INFLUXDB_PV=2.8.0-2
# Thu, 11 Jun 2026 00:45:48 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 11 Jun 2026 00:45:48 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Thu, 11 Jun 2026 00:45:49 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 11 Jun 2026 00:45:50 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 11 Jun 2026 00:45:50 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Jun 2026 00:45:50 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 11 Jun 2026 00:45:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 00:45:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 00:45:50 GMT
CMD ["influxd"]
# Thu, 11 Jun 2026 00:45:50 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jun 2026 00:45:50 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Jun 2026 00:45:50 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Jun 2026 00:45:50 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Jun 2026 00:45:50 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bde372557c257cfd6df534f0978470cecf9aa4374c0d3341d436c61cd9beca3`  
		Last Modified: Thu, 11 Jun 2026 00:46:01 GMT  
		Size: 9.6 MB (9629046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a056ca077ceeb56fd322cd484f3962d1013556888c14cfbac9b97b2872c4c099`  
		Last Modified: Thu, 11 Jun 2026 00:46:01 GMT  
		Size: 5.8 MB (5790426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4d7bb97778ae47010fce608019871893df9eaffab0719e8c7984110a0f1cef`  
		Last Modified: Thu, 11 Jun 2026 00:46:00 GMT  
		Size: 3.2 KB (3227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214aa125b3e88476d4b9445ce1ad15d1a4e61288059165698d46a3ac3d35ce07`  
		Last Modified: Thu, 11 Jun 2026 00:46:00 GMT  
		Size: 766.4 KB (766373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafc3eba862413f79580c977b72fa1f4690c95e889c455b8c764a214fda9c851`  
		Last Modified: Thu, 11 Jun 2026 00:46:03 GMT  
		Size: 48.2 MB (48229552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f70f2940f0e1a1c53c4204bb66b7acb5ca5bd67472ca4361af1150d3b331d4`  
		Last Modified: Thu, 11 Jun 2026 00:46:02 GMT  
		Size: 11.1 MB (11100394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646af7e3d3670f4561ba56e36cc7d4a4d23d647d375a95fae0cc8e161cf32dff`  
		Last Modified: Thu, 11 Jun 2026 00:46:02 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11630d81ca7a752a8f5064d73260c9db176fff2939aaa335cb2e12b6ba3bd29b`  
		Last Modified: Thu, 11 Jun 2026 00:46:03 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8ccfd85c51b64d62c78bee99c49d7cd2517bf113610a2c4871b4d3d3d0c6ec`  
		Last Modified: Thu, 11 Jun 2026 00:46:03 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8.0` - unknown; unknown

```console
$ docker pull influxdb@sha256:59cf0c4bb05525e7cb7f29d28dfc6b20afbb54ff67b7aae19125fd22a062cfb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2966332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa7b5b3ac0ed1827b96f50f77472913a14c0e988b658d2788b5336c127667497`

```dockerfile
```

-	Layers:
	-	`sha256:e6b58fd0e2f332d2420279575b59f57470dc437b079a3bfda5d4aca5b564ebca`  
		Last Modified: Thu, 11 Jun 2026 00:46:01 GMT  
		Size: 2.9 MB (2933135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f122c5f8cee6307f0c07ec4199828b1e946002feaeb9cd80db02954b8137ca02`  
		Last Modified: Thu, 11 Jun 2026 00:46:01 GMT  
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
$ docker pull influxdb@sha256:003e028b675205f6148e5f30369fd3e854993b385f1e5e4d2d85bc9f8701bf28
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.9` - linux; amd64

```console
$ docker pull influxdb@sha256:b3b6db425bd08e5173b3a8168de701c22526dbbc4eb4ca10ca25e00db57114f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.8 MB (110803771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:216fc6047d5548b9cedd5f8900ccc269534f2e7c6d51cb8015384a9d8687e300`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:44:09 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg       util-linux &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:44:10 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Thu, 11 Jun 2026 00:44:10 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 11 Jun 2026 00:44:13 GMT
ENV INFLUXDB_VERSION=2.9.1
# Thu, 11 Jun 2026 00:44:13 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 11 Jun 2026 00:44:13 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Thu, 11 Jun 2026 00:44:15 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 11 Jun 2026 00:44:15 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 11 Jun 2026 00:44:15 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Jun 2026 00:44:15 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 11 Jun 2026 00:44:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 00:44:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 00:44:15 GMT
CMD ["influxd"]
# Thu, 11 Jun 2026 00:44:15 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jun 2026 00:44:15 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Jun 2026 00:44:15 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Jun 2026 00:44:15 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Jun 2026 00:44:15 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca13784c2e80ea84bbe25bdc33fa82008ff90ee6404be9419dbbe50f82081f91`  
		Last Modified: Thu, 11 Jun 2026 00:44:27 GMT  
		Size: 9.8 MB (9800747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886d8448c571631facc9fe146e26ac66d1b7eb4e0d26934112fdb91a9ca5d9fe`  
		Last Modified: Thu, 11 Jun 2026 00:44:27 GMT  
		Size: 3.8 MB (3822785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d091ef401709b2e0d66f2524bfa92dc53a7628b79460615e607ea51b1761b604`  
		Last Modified: Thu, 11 Jun 2026 00:44:27 GMT  
		Size: 3.2 KB (3229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473282447769ed378f1718d94cfa4240c087e9c693569b46450cbc60a65b7bf8`  
		Last Modified: Thu, 11 Jun 2026 00:44:29 GMT  
		Size: 56.5 MB (56510619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4d2daebcc5a61d6df052588fbb02d58c6f6fba47533d6a032f1a5606c200a3`  
		Last Modified: Thu, 11 Jun 2026 00:44:28 GMT  
		Size: 12.4 MB (12421826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599b7e6339adf53f34ef2b25bd501d42f3eaa40a0a4525d2d009a12ebc026f92`  
		Last Modified: Thu, 11 Jun 2026 00:44:28 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b16bfd3cd1b9b650256b1e2089f7eff3b975d13e250b9fe01d1581f720d345`  
		Last Modified: Thu, 11 Jun 2026 00:44:29 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d442aae476f79aefc39fab6b4b3145f8f5fc7b00798769204f7624a443b611c`  
		Last Modified: Thu, 11 Jun 2026 00:44:30 GMT  
		Size: 6.5 KB (6499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.9` - unknown; unknown

```console
$ docker pull influxdb@sha256:4b9b3dcd93e61c6911d100560807fd99efe5e5489aa3178b393b687d07009353
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2988061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c96ffda826f90beec04d953f68df55a73052203726258734c11b450f0cfbec7`

```dockerfile
```

-	Layers:
	-	`sha256:f3b378e41b794fbbfecb4f8ff82b963f1281dacea9cddc8e2c7f985ad71ac812`  
		Last Modified: Thu, 11 Jun 2026 00:44:27 GMT  
		Size: 3.0 MB (2959447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b465a9d35a369365b1479b9d69fd50db2fcbe039aa0f5520d4ad44c8198cd6f2`  
		Last Modified: Thu, 11 Jun 2026 00:44:26 GMT  
		Size: 28.6 KB (28614 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.9` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:e5d7d3f2475b666d5dd9e9602b118ac5c30c400bc2a9265ee329a06a0b08ebba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106337789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ba9fe5b6043ebcffd255286e160ba78347f7df11b5cd2b9ef11832f517c49ba`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:45:48 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg       util-linux &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:49 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Thu, 11 Jun 2026 00:45:49 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 11 Jun 2026 00:45:53 GMT
ENV INFLUXDB_VERSION=2.9.1
# Thu, 11 Jun 2026 00:45:53 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 11 Jun 2026 00:45:53 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Thu, 11 Jun 2026 00:45:55 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 11 Jun 2026 00:45:55 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 11 Jun 2026 00:45:55 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Jun 2026 00:45:55 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 11 Jun 2026 00:45:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 00:45:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 00:45:55 GMT
CMD ["influxd"]
# Thu, 11 Jun 2026 00:45:55 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jun 2026 00:45:55 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Jun 2026 00:45:55 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Jun 2026 00:45:55 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Jun 2026 00:45:55 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57bb39aa14de947a30f716a21ccc5488e944ce97b3711471a0e593001c28540`  
		Last Modified: Thu, 11 Jun 2026 00:46:07 GMT  
		Size: 9.6 MB (9629019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723baea35ef3ea8149bffeb1c30de73f358f632d869398b34a1c1d98b04e32bb`  
		Last Modified: Thu, 11 Jun 2026 00:46:07 GMT  
		Size: 3.5 MB (3459177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33414b33f32babd71285978fd56dae58d2931354f14783dab98a03f7880c688b`  
		Last Modified: Thu, 11 Jun 2026 00:46:06 GMT  
		Size: 3.2 KB (3228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c509bc7d25f3f9c5fb74fe5296dfb524eacb802433fb61b91ca8282f1cf5f0b`  
		Last Modified: Thu, 11 Jun 2026 00:46:08 GMT  
		Size: 53.6 MB (53636817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14f7108738c858ce74317b9a4029306bdcfd76cb4a6ca31c5c6b71c7e444e5b`  
		Last Modified: Thu, 11 Jun 2026 00:46:08 GMT  
		Size: 11.5 MB (11480300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2193a6345188a1f23214372c687a7ec0c537b748e6228ccf1d8aeeb5ef1ce381`  
		Last Modified: Thu, 11 Jun 2026 00:46:08 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7d973f0e880b165170182660e4a002f2354b3aeef79911af0f9a1a6326fd47`  
		Last Modified: Thu, 11 Jun 2026 00:46:09 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dedd3e27ede6904e2b5729b403f87645b4d7206f51292f5c8145da8d30fc050`  
		Last Modified: Thu, 11 Jun 2026 00:46:09 GMT  
		Size: 6.5 KB (6499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.9` - unknown; unknown

```console
$ docker pull influxdb@sha256:e26bf54687a5af9cbdd36b95e8da5236a05237654a3eec88fb48af5bf64c00aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d014559c4fac67f921a2db2b95dbf0994a755b966118dc68ee0f57212f33ce9c`

```dockerfile
```

-	Layers:
	-	`sha256:819cf5530c1f61f319767f0599b728ecae98dcb92129fdb8b1add1c5b716e751`  
		Last Modified: Thu, 11 Jun 2026 00:46:07 GMT  
		Size: 3.0 MB (2958925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aab4dee5b6a157c159c496a92e6fcd3792cbcf34116e14d2bbecdbdaf214ebc0`  
		Last Modified: Thu, 11 Jun 2026 00:46:07 GMT  
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
$ docker pull influxdb@sha256:003e028b675205f6148e5f30369fd3e854993b385f1e5e4d2d85bc9f8701bf28
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.9.1` - linux; amd64

```console
$ docker pull influxdb@sha256:b3b6db425bd08e5173b3a8168de701c22526dbbc4eb4ca10ca25e00db57114f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.8 MB (110803771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:216fc6047d5548b9cedd5f8900ccc269534f2e7c6d51cb8015384a9d8687e300`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:44:09 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg       util-linux &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:44:10 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Thu, 11 Jun 2026 00:44:10 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 11 Jun 2026 00:44:13 GMT
ENV INFLUXDB_VERSION=2.9.1
# Thu, 11 Jun 2026 00:44:13 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 11 Jun 2026 00:44:13 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Thu, 11 Jun 2026 00:44:15 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 11 Jun 2026 00:44:15 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 11 Jun 2026 00:44:15 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Jun 2026 00:44:15 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 11 Jun 2026 00:44:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 00:44:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 00:44:15 GMT
CMD ["influxd"]
# Thu, 11 Jun 2026 00:44:15 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jun 2026 00:44:15 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Jun 2026 00:44:15 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Jun 2026 00:44:15 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Jun 2026 00:44:15 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca13784c2e80ea84bbe25bdc33fa82008ff90ee6404be9419dbbe50f82081f91`  
		Last Modified: Thu, 11 Jun 2026 00:44:27 GMT  
		Size: 9.8 MB (9800747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886d8448c571631facc9fe146e26ac66d1b7eb4e0d26934112fdb91a9ca5d9fe`  
		Last Modified: Thu, 11 Jun 2026 00:44:27 GMT  
		Size: 3.8 MB (3822785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d091ef401709b2e0d66f2524bfa92dc53a7628b79460615e607ea51b1761b604`  
		Last Modified: Thu, 11 Jun 2026 00:44:27 GMT  
		Size: 3.2 KB (3229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473282447769ed378f1718d94cfa4240c087e9c693569b46450cbc60a65b7bf8`  
		Last Modified: Thu, 11 Jun 2026 00:44:29 GMT  
		Size: 56.5 MB (56510619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4d2daebcc5a61d6df052588fbb02d58c6f6fba47533d6a032f1a5606c200a3`  
		Last Modified: Thu, 11 Jun 2026 00:44:28 GMT  
		Size: 12.4 MB (12421826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599b7e6339adf53f34ef2b25bd501d42f3eaa40a0a4525d2d009a12ebc026f92`  
		Last Modified: Thu, 11 Jun 2026 00:44:28 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b16bfd3cd1b9b650256b1e2089f7eff3b975d13e250b9fe01d1581f720d345`  
		Last Modified: Thu, 11 Jun 2026 00:44:29 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d442aae476f79aefc39fab6b4b3145f8f5fc7b00798769204f7624a443b611c`  
		Last Modified: Thu, 11 Jun 2026 00:44:30 GMT  
		Size: 6.5 KB (6499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.9.1` - unknown; unknown

```console
$ docker pull influxdb@sha256:4b9b3dcd93e61c6911d100560807fd99efe5e5489aa3178b393b687d07009353
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2988061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c96ffda826f90beec04d953f68df55a73052203726258734c11b450f0cfbec7`

```dockerfile
```

-	Layers:
	-	`sha256:f3b378e41b794fbbfecb4f8ff82b963f1281dacea9cddc8e2c7f985ad71ac812`  
		Last Modified: Thu, 11 Jun 2026 00:44:27 GMT  
		Size: 3.0 MB (2959447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b465a9d35a369365b1479b9d69fd50db2fcbe039aa0f5520d4ad44c8198cd6f2`  
		Last Modified: Thu, 11 Jun 2026 00:44:26 GMT  
		Size: 28.6 KB (28614 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.9.1` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:e5d7d3f2475b666d5dd9e9602b118ac5c30c400bc2a9265ee329a06a0b08ebba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106337789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ba9fe5b6043ebcffd255286e160ba78347f7df11b5cd2b9ef11832f517c49ba`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:45:48 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg       util-linux &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:49 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Thu, 11 Jun 2026 00:45:49 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 11 Jun 2026 00:45:53 GMT
ENV INFLUXDB_VERSION=2.9.1
# Thu, 11 Jun 2026 00:45:53 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 11 Jun 2026 00:45:53 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Thu, 11 Jun 2026 00:45:55 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 11 Jun 2026 00:45:55 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 11 Jun 2026 00:45:55 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Jun 2026 00:45:55 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 11 Jun 2026 00:45:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 00:45:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 00:45:55 GMT
CMD ["influxd"]
# Thu, 11 Jun 2026 00:45:55 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jun 2026 00:45:55 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Jun 2026 00:45:55 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Jun 2026 00:45:55 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Jun 2026 00:45:55 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57bb39aa14de947a30f716a21ccc5488e944ce97b3711471a0e593001c28540`  
		Last Modified: Thu, 11 Jun 2026 00:46:07 GMT  
		Size: 9.6 MB (9629019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723baea35ef3ea8149bffeb1c30de73f358f632d869398b34a1c1d98b04e32bb`  
		Last Modified: Thu, 11 Jun 2026 00:46:07 GMT  
		Size: 3.5 MB (3459177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33414b33f32babd71285978fd56dae58d2931354f14783dab98a03f7880c688b`  
		Last Modified: Thu, 11 Jun 2026 00:46:06 GMT  
		Size: 3.2 KB (3228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c509bc7d25f3f9c5fb74fe5296dfb524eacb802433fb61b91ca8282f1cf5f0b`  
		Last Modified: Thu, 11 Jun 2026 00:46:08 GMT  
		Size: 53.6 MB (53636817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14f7108738c858ce74317b9a4029306bdcfd76cb4a6ca31c5c6b71c7e444e5b`  
		Last Modified: Thu, 11 Jun 2026 00:46:08 GMT  
		Size: 11.5 MB (11480300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2193a6345188a1f23214372c687a7ec0c537b748e6228ccf1d8aeeb5ef1ce381`  
		Last Modified: Thu, 11 Jun 2026 00:46:08 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7d973f0e880b165170182660e4a002f2354b3aeef79911af0f9a1a6326fd47`  
		Last Modified: Thu, 11 Jun 2026 00:46:09 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dedd3e27ede6904e2b5729b403f87645b4d7206f51292f5c8145da8d30fc050`  
		Last Modified: Thu, 11 Jun 2026 00:46:09 GMT  
		Size: 6.5 KB (6499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.9.1` - unknown; unknown

```console
$ docker pull influxdb@sha256:e26bf54687a5af9cbdd36b95e8da5236a05237654a3eec88fb48af5bf64c00aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d014559c4fac67f921a2db2b95dbf0994a755b966118dc68ee0f57212f33ce9c`

```dockerfile
```

-	Layers:
	-	`sha256:819cf5530c1f61f319767f0599b728ecae98dcb92129fdb8b1add1c5b716e751`  
		Last Modified: Thu, 11 Jun 2026 00:46:07 GMT  
		Size: 3.0 MB (2958925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aab4dee5b6a157c159c496a92e6fcd3792cbcf34116e14d2bbecdbdaf214ebc0`  
		Last Modified: Thu, 11 Jun 2026 00:46:07 GMT  
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
$ docker pull influxdb@sha256:003e028b675205f6148e5f30369fd3e854993b385f1e5e4d2d85bc9f8701bf28
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:b3b6db425bd08e5173b3a8168de701c22526dbbc4eb4ca10ca25e00db57114f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.8 MB (110803771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:216fc6047d5548b9cedd5f8900ccc269534f2e7c6d51cb8015384a9d8687e300`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:44:09 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg       util-linux &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:44:10 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Thu, 11 Jun 2026 00:44:10 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 11 Jun 2026 00:44:13 GMT
ENV INFLUXDB_VERSION=2.9.1
# Thu, 11 Jun 2026 00:44:13 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 11 Jun 2026 00:44:13 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Thu, 11 Jun 2026 00:44:15 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 11 Jun 2026 00:44:15 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 11 Jun 2026 00:44:15 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Jun 2026 00:44:15 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 11 Jun 2026 00:44:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 00:44:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 00:44:15 GMT
CMD ["influxd"]
# Thu, 11 Jun 2026 00:44:15 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jun 2026 00:44:15 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Jun 2026 00:44:15 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Jun 2026 00:44:15 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Jun 2026 00:44:15 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca13784c2e80ea84bbe25bdc33fa82008ff90ee6404be9419dbbe50f82081f91`  
		Last Modified: Thu, 11 Jun 2026 00:44:27 GMT  
		Size: 9.8 MB (9800747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886d8448c571631facc9fe146e26ac66d1b7eb4e0d26934112fdb91a9ca5d9fe`  
		Last Modified: Thu, 11 Jun 2026 00:44:27 GMT  
		Size: 3.8 MB (3822785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d091ef401709b2e0d66f2524bfa92dc53a7628b79460615e607ea51b1761b604`  
		Last Modified: Thu, 11 Jun 2026 00:44:27 GMT  
		Size: 3.2 KB (3229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473282447769ed378f1718d94cfa4240c087e9c693569b46450cbc60a65b7bf8`  
		Last Modified: Thu, 11 Jun 2026 00:44:29 GMT  
		Size: 56.5 MB (56510619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4d2daebcc5a61d6df052588fbb02d58c6f6fba47533d6a032f1a5606c200a3`  
		Last Modified: Thu, 11 Jun 2026 00:44:28 GMT  
		Size: 12.4 MB (12421826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599b7e6339adf53f34ef2b25bd501d42f3eaa40a0a4525d2d009a12ebc026f92`  
		Last Modified: Thu, 11 Jun 2026 00:44:28 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b16bfd3cd1b9b650256b1e2089f7eff3b975d13e250b9fe01d1581f720d345`  
		Last Modified: Thu, 11 Jun 2026 00:44:29 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d442aae476f79aefc39fab6b4b3145f8f5fc7b00798769204f7624a443b611c`  
		Last Modified: Thu, 11 Jun 2026 00:44:30 GMT  
		Size: 6.5 KB (6499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:4b9b3dcd93e61c6911d100560807fd99efe5e5489aa3178b393b687d07009353
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2988061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c96ffda826f90beec04d953f68df55a73052203726258734c11b450f0cfbec7`

```dockerfile
```

-	Layers:
	-	`sha256:f3b378e41b794fbbfecb4f8ff82b963f1281dacea9cddc8e2c7f985ad71ac812`  
		Last Modified: Thu, 11 Jun 2026 00:44:27 GMT  
		Size: 3.0 MB (2959447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b465a9d35a369365b1479b9d69fd50db2fcbe039aa0f5520d4ad44c8198cd6f2`  
		Last Modified: Thu, 11 Jun 2026 00:44:26 GMT  
		Size: 28.6 KB (28614 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:e5d7d3f2475b666d5dd9e9602b118ac5c30c400bc2a9265ee329a06a0b08ebba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106337789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ba9fe5b6043ebcffd255286e160ba78347f7df11b5cd2b9ef11832f517c49ba`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:45:48 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg       util-linux &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:49 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Thu, 11 Jun 2026 00:45:49 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Thu, 11 Jun 2026 00:45:53 GMT
ENV INFLUXDB_VERSION=2.9.1
# Thu, 11 Jun 2026 00:45:53 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 11 Jun 2026 00:45:53 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Thu, 11 Jun 2026 00:45:55 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 11 Jun 2026 00:45:55 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 11 Jun 2026 00:45:55 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Jun 2026 00:45:55 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 11 Jun 2026 00:45:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 00:45:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 00:45:55 GMT
CMD ["influxd"]
# Thu, 11 Jun 2026 00:45:55 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Jun 2026 00:45:55 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Jun 2026 00:45:55 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Jun 2026 00:45:55 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Jun 2026 00:45:55 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57bb39aa14de947a30f716a21ccc5488e944ce97b3711471a0e593001c28540`  
		Last Modified: Thu, 11 Jun 2026 00:46:07 GMT  
		Size: 9.6 MB (9629019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723baea35ef3ea8149bffeb1c30de73f358f632d869398b34a1c1d98b04e32bb`  
		Last Modified: Thu, 11 Jun 2026 00:46:07 GMT  
		Size: 3.5 MB (3459177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33414b33f32babd71285978fd56dae58d2931354f14783dab98a03f7880c688b`  
		Last Modified: Thu, 11 Jun 2026 00:46:06 GMT  
		Size: 3.2 KB (3228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c509bc7d25f3f9c5fb74fe5296dfb524eacb802433fb61b91ca8282f1cf5f0b`  
		Last Modified: Thu, 11 Jun 2026 00:46:08 GMT  
		Size: 53.6 MB (53636817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14f7108738c858ce74317b9a4029306bdcfd76cb4a6ca31c5c6b71c7e444e5b`  
		Last Modified: Thu, 11 Jun 2026 00:46:08 GMT  
		Size: 11.5 MB (11480300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2193a6345188a1f23214372c687a7ec0c537b748e6228ccf1d8aeeb5ef1ce381`  
		Last Modified: Thu, 11 Jun 2026 00:46:08 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7d973f0e880b165170182660e4a002f2354b3aeef79911af0f9a1a6326fd47`  
		Last Modified: Thu, 11 Jun 2026 00:46:09 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dedd3e27ede6904e2b5729b403f87645b4d7206f51292f5c8145da8d30fc050`  
		Last Modified: Thu, 11 Jun 2026 00:46:09 GMT  
		Size: 6.5 KB (6499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:e26bf54687a5af9cbdd36b95e8da5236a05237654a3eec88fb48af5bf64c00aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d014559c4fac67f921a2db2b95dbf0994a755b966118dc68ee0f57212f33ce9c`

```dockerfile
```

-	Layers:
	-	`sha256:819cf5530c1f61f319767f0599b728ecae98dcb92129fdb8b1add1c5b716e751`  
		Last Modified: Thu, 11 Jun 2026 00:46:07 GMT  
		Size: 3.0 MB (2958925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aab4dee5b6a157c159c496a92e6fcd3792cbcf34116e14d2bbecdbdaf214ebc0`  
		Last Modified: Thu, 11 Jun 2026 00:46:07 GMT  
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
