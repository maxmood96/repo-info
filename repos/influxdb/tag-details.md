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
-	[`influxdb:2.9.0`](#influxdb290)
-	[`influxdb:2.9.0-alpine`](#influxdb290-alpine)
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
$ docker pull influxdb@sha256:b86a02dd44303b64866dc265fec59b0b8bcb7c5cd94d21a950722c014984ec03
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11` - linux; amd64

```console
$ docker pull influxdb@sha256:9ea209df0b6c00c7740a2734a425a5d66dcbf3640f00dacb4b806abf36ca6020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116189778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d420a9fcf21f327a29b17c460562d2f3b6c3520280b06e9ad321676e16f31640`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 05:00:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:14:48 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Wed, 22 Apr 2026 05:14:56 GMT
ARG INFLUXDB_VERSION=1.11.8
# Wed, 22 Apr 2026 05:14:56 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:14:56 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 22 Apr 2026 05:14:56 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 22 Apr 2026 05:14:56 GMT
VOLUME [/var/lib/influxdb]
# Wed, 22 Apr 2026 05:14:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 05:14:56 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 22 Apr 2026 05:14:56 GMT
USER influxdb
# Wed, 22 Apr 2026 05:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 05:14:56 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5203b2bfeff92b72e816dc6cbb1f16856f0cd592e521e3c0cfa195a78fe180e`  
		Last Modified: Wed, 22 Apr 2026 05:01:15 GMT  
		Size: 24.0 MB (24042234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f6b05ddf5a915781fd295bb8a1e5de1a3f3470bf2982da61d89dfa6ffd618a`  
		Last Modified: Wed, 22 Apr 2026 05:15:07 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ec5f30dc117086ce588e26f78610d58f993ac6b4e5a6f2b86ccb4aa8203236`  
		Last Modified: Wed, 22 Apr 2026 05:15:09 GMT  
		Size: 43.7 MB (43656009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c998bf645dd53e52f2b9d7dc306148602674ed656d9da2f30dea0be5e6dae0c0`  
		Last Modified: Wed, 22 Apr 2026 05:15:07 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bac48e961f2cd6eda52c1789465600c43cd40556544855fe5c3146c0edfa37f`  
		Last Modified: Wed, 22 Apr 2026 05:15:07 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536da4c668238479fa0985eee283c187dc6c5c9ee505e81a73e5fbb780e9f115`  
		Last Modified: Wed, 22 Apr 2026 05:15:08 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11` - unknown; unknown

```console
$ docker pull influxdb@sha256:6a2602613ef658f847b52b031bca5f1d8c2ba16bb205e7aaee9d807fc02f375e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bd99ab60767ded6d6851ecfaff3cf4b81ed8e880f66f363b382b287dc0ecbc0`

```dockerfile
```

-	Layers:
	-	`sha256:1ea538cc3116d98624c28e3615be6e6bba2cedeb168459abc006d53407d65e2f`  
		Last Modified: Wed, 22 Apr 2026 05:15:07 GMT  
		Size: 5.1 MB (5079263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c506ecc0131e7fe8ffa771a78c515bb5aeee8a443d72c0793a149a142645f8fc`  
		Last Modified: Wed, 22 Apr 2026 05:15:07 GMT  
		Size: 15.5 KB (15483 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:5516334ecfa5d9a2ab29083cd8378e129db57e38f507b29efbb859f5bd6f5861
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113108117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:455f29802e4e36d50444b7831cb331dba80151a5c1d9ce5b95ccb7767e80c218`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:42:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:36:15 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Wed, 22 Apr 2026 02:36:24 GMT
ARG INFLUXDB_VERSION=1.11.8
# Wed, 22 Apr 2026 02:36:24 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:36:24 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 22 Apr 2026 02:36:24 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 22 Apr 2026 02:36:24 GMT
VOLUME [/var/lib/influxdb]
# Wed, 22 Apr 2026 02:36:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 02:36:24 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 22 Apr 2026 02:36:24 GMT
USER influxdb
# Wed, 22 Apr 2026 02:36:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 02:36:24 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb7bd28fbdfe678a7f45878b7b1c07dbbc0fa7753b0312aa8fd049667a9e137`  
		Last Modified: Wed, 22 Apr 2026 01:43:06 GMT  
		Size: 23.6 MB (23609423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114143dc6296d2f3b3586925261a4bdc17029219b9fbeae0f4ed780d8c55961c`  
		Last Modified: Wed, 22 Apr 2026 02:36:38 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7eef8081eab7a4240b94b0f1b4442dcc28c6709cbdbaebee542722022979637`  
		Last Modified: Wed, 22 Apr 2026 02:36:39 GMT  
		Size: 41.1 MB (41122717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090efa0fb498a34ca6c27fc451fd709e2c6e14769ca63fd26683252643f0202f`  
		Last Modified: Wed, 22 Apr 2026 02:36:38 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f80a345fc351814a454c4ffa56acc30dc274fd36efe526e5125060500f2937`  
		Last Modified: Wed, 22 Apr 2026 02:36:38 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9baf91c16b5b8bfdf8c01efe771bf9ca8e3a9efcf45edf5120e69c76c15ccac9`  
		Last Modified: Wed, 22 Apr 2026 02:36:39 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11` - unknown; unknown

```console
$ docker pull influxdb@sha256:a1793b135670f06d2d48887f5d54fe720f8f691668543c9efd84194ca3391c47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99e59eb96ad3ffc55620c9b0c844ae6ec092b7efa58c7479c81fe1d02a0de192`

```dockerfile
```

-	Layers:
	-	`sha256:e824aa3e3c062526a1e00bfa536a39b5fa90eb7970f9f4221c1c1f30556a46c3`  
		Last Modified: Wed, 22 Apr 2026 02:36:38 GMT  
		Size: 5.1 MB (5078728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:228cfbc0147448fe1a08b1b6ef8895f5e07d38f3f00f28654c1065c1a201c271`  
		Last Modified: Wed, 22 Apr 2026 02:36:38 GMT  
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
$ docker pull influxdb@sha256:8775a9fe738c10b62eda9f70323ce09dc76c8e93c3efaa8c1a369d985a5ff4fb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data` - linux; amd64

```console
$ docker pull influxdb@sha256:ff66cac71bb302360fb395ec37f290a31a6f55246985504827754880c011fd84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114703436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f721c9f5b9f8133357e9310da4c7f91c2583d50aaf293fb1aa30a22382053bbd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 05:00:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:14:51 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 05:14:54 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Wed, 22 Apr 2026 05:14:54 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Wed, 22 Apr 2026 05:14:54 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 22 Apr 2026 05:14:54 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 22 Apr 2026 05:14:54 GMT
VOLUME [/var/lib/influxdb]
# Wed, 22 Apr 2026 05:14:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 05:14:54 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 22 Apr 2026 05:14:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 05:14:54 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5203b2bfeff92b72e816dc6cbb1f16856f0cd592e521e3c0cfa195a78fe180e`  
		Last Modified: Wed, 22 Apr 2026 05:01:15 GMT  
		Size: 24.0 MB (24042234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f155390245d5286ab062bac74ed4ba57587adbe288991bb0b4874107172d2a`  
		Last Modified: Wed, 22 Apr 2026 05:15:05 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1917c023636a70529c2744e84d6591b4a7ef2c338ac0604ab07640fcdad805a5`  
		Last Modified: Wed, 22 Apr 2026 05:15:07 GMT  
		Size: 42.2 MB (42165729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b2a9a62e89e4d34216a2937587767254c254f24ebe7ecd205ffe215a31713a`  
		Last Modified: Wed, 22 Apr 2026 05:15:06 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c3052e2838a906278a5a62b0b41bdcda7d79f1e9ad56a729e207353d709e8f`  
		Last Modified: Wed, 22 Apr 2026 05:15:06 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15db9ed7f815fe02c82827e19e011c20566aadb010b0976fe91cd1bc29aae76a`  
		Last Modified: Wed, 22 Apr 2026 05:15:07 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:50a2abbc0a59411a53c50a9927f84c9ebccb4f4efc82a1e2b1bb5ac7144a67ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4699071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0914528b4d1a6439bd74fe515666be9dea46d655cbf5dce24e2cdc27b39d03de`

```dockerfile
```

-	Layers:
	-	`sha256:ea527fe6eb23eaebd69fc5a90930228589de5eef29c4e1fccc18761c8d314c99`  
		Last Modified: Wed, 22 Apr 2026 05:15:06 GMT  
		Size: 4.7 MB (4684406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67508d6f36e0af41c02c79f03f70645259bfb22c0976302e346ad4c0b73e0f4a`  
		Last Modified: Wed, 22 Apr 2026 05:15:06 GMT  
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
$ docker pull influxdb@sha256:11f90b3d8577c9264734c794e3e53378e609e3ceb1aaa1f2bd55038d752ee542
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:8698497de01a3ff8d806d6daf1013f9f6620e9661bc2d25dbbc4f56e0bae1ac1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91132621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f4fefd3011c345c7500a3cb40d86d30cff24ffe45957ac2ade4e09699ad91f4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 05:00:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:14:57 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 05:14:59 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Wed, 22 Apr 2026 05:14:59 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Wed, 22 Apr 2026 05:14:59 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Wed, 22 Apr 2026 05:14:59 GMT
EXPOSE map[8091/tcp:{}]
# Wed, 22 Apr 2026 05:14:59 GMT
VOLUME [/var/lib/influxdb]
# Wed, 22 Apr 2026 05:14:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 05:14:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 05:14:59 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5203b2bfeff92b72e816dc6cbb1f16856f0cd592e521e3c0cfa195a78fe180e`  
		Last Modified: Wed, 22 Apr 2026 05:01:15 GMT  
		Size: 24.0 MB (24042234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c65a81f6831e749e3129747b4d4af574bb09c5d2c927e21e11b50458c79b70`  
		Last Modified: Wed, 22 Apr 2026 05:15:08 GMT  
		Size: 5.1 KB (5056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c0a94894ebba1bba595d504c7ef0ae1a7e979aad6bfd5425d950bb6263098d`  
		Last Modified: Wed, 22 Apr 2026 05:15:09 GMT  
		Size: 18.6 MB (18596140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5892d118679be9ea2a44134469e9c97c8bfe0664b80128bb3c33081d6bf58334`  
		Last Modified: Wed, 22 Apr 2026 05:15:08 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544fa5874482c61fd48e87fe0ff350eb61d67faff84d0cda6e88a067b7a800a7`  
		Last Modified: Wed, 22 Apr 2026 05:15:08 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:c096d57b1c8c09b3a17fa483fcfd5b3f64b570cf7da4d8ed67c0b6c17bc1af9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4604273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e420f2fda8d40b518419cf6569e112fa9a5d28a40a23822aa4a457759a50d9df`

```dockerfile
```

-	Layers:
	-	`sha256:98181d9a340539cff37eb3138747b00bfe8e3df67fb69fd494a5a3af82c65bf7`  
		Last Modified: Wed, 22 Apr 2026 05:15:08 GMT  
		Size: 4.6 MB (4591249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbb0768ef3dc6de245ef9f648904da6544ce48cf2600645b7e608cb274d8788a`  
		Last Modified: Wed, 22 Apr 2026 05:15:08 GMT  
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
$ docker pull influxdb@sha256:b86a02dd44303b64866dc265fec59b0b8bcb7c5cd94d21a950722c014984ec03
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11.8` - linux; amd64

```console
$ docker pull influxdb@sha256:9ea209df0b6c00c7740a2734a425a5d66dcbf3640f00dacb4b806abf36ca6020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116189778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d420a9fcf21f327a29b17c460562d2f3b6c3520280b06e9ad321676e16f31640`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 05:00:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:14:48 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Wed, 22 Apr 2026 05:14:56 GMT
ARG INFLUXDB_VERSION=1.11.8
# Wed, 22 Apr 2026 05:14:56 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:14:56 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 22 Apr 2026 05:14:56 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 22 Apr 2026 05:14:56 GMT
VOLUME [/var/lib/influxdb]
# Wed, 22 Apr 2026 05:14:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 05:14:56 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 22 Apr 2026 05:14:56 GMT
USER influxdb
# Wed, 22 Apr 2026 05:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 05:14:56 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5203b2bfeff92b72e816dc6cbb1f16856f0cd592e521e3c0cfa195a78fe180e`  
		Last Modified: Wed, 22 Apr 2026 05:01:15 GMT  
		Size: 24.0 MB (24042234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f6b05ddf5a915781fd295bb8a1e5de1a3f3470bf2982da61d89dfa6ffd618a`  
		Last Modified: Wed, 22 Apr 2026 05:15:07 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ec5f30dc117086ce588e26f78610d58f993ac6b4e5a6f2b86ccb4aa8203236`  
		Last Modified: Wed, 22 Apr 2026 05:15:09 GMT  
		Size: 43.7 MB (43656009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c998bf645dd53e52f2b9d7dc306148602674ed656d9da2f30dea0be5e6dae0c0`  
		Last Modified: Wed, 22 Apr 2026 05:15:07 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bac48e961f2cd6eda52c1789465600c43cd40556544855fe5c3146c0edfa37f`  
		Last Modified: Wed, 22 Apr 2026 05:15:07 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536da4c668238479fa0985eee283c187dc6c5c9ee505e81a73e5fbb780e9f115`  
		Last Modified: Wed, 22 Apr 2026 05:15:08 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:6a2602613ef658f847b52b031bca5f1d8c2ba16bb205e7aaee9d807fc02f375e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bd99ab60767ded6d6851ecfaff3cf4b81ed8e880f66f363b382b287dc0ecbc0`

```dockerfile
```

-	Layers:
	-	`sha256:1ea538cc3116d98624c28e3615be6e6bba2cedeb168459abc006d53407d65e2f`  
		Last Modified: Wed, 22 Apr 2026 05:15:07 GMT  
		Size: 5.1 MB (5079263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c506ecc0131e7fe8ffa771a78c515bb5aeee8a443d72c0793a149a142645f8fc`  
		Last Modified: Wed, 22 Apr 2026 05:15:07 GMT  
		Size: 15.5 KB (15483 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:5516334ecfa5d9a2ab29083cd8378e129db57e38f507b29efbb859f5bd6f5861
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113108117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:455f29802e4e36d50444b7831cb331dba80151a5c1d9ce5b95ccb7767e80c218`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:42:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:36:15 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Wed, 22 Apr 2026 02:36:24 GMT
ARG INFLUXDB_VERSION=1.11.8
# Wed, 22 Apr 2026 02:36:24 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:36:24 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 22 Apr 2026 02:36:24 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 22 Apr 2026 02:36:24 GMT
VOLUME [/var/lib/influxdb]
# Wed, 22 Apr 2026 02:36:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 02:36:24 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 22 Apr 2026 02:36:24 GMT
USER influxdb
# Wed, 22 Apr 2026 02:36:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 02:36:24 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb7bd28fbdfe678a7f45878b7b1c07dbbc0fa7753b0312aa8fd049667a9e137`  
		Last Modified: Wed, 22 Apr 2026 01:43:06 GMT  
		Size: 23.6 MB (23609423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114143dc6296d2f3b3586925261a4bdc17029219b9fbeae0f4ed780d8c55961c`  
		Last Modified: Wed, 22 Apr 2026 02:36:38 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7eef8081eab7a4240b94b0f1b4442dcc28c6709cbdbaebee542722022979637`  
		Last Modified: Wed, 22 Apr 2026 02:36:39 GMT  
		Size: 41.1 MB (41122717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090efa0fb498a34ca6c27fc451fd709e2c6e14769ca63fd26683252643f0202f`  
		Last Modified: Wed, 22 Apr 2026 02:36:38 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f80a345fc351814a454c4ffa56acc30dc274fd36efe526e5125060500f2937`  
		Last Modified: Wed, 22 Apr 2026 02:36:38 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9baf91c16b5b8bfdf8c01efe771bf9ca8e3a9efcf45edf5120e69c76c15ccac9`  
		Last Modified: Wed, 22 Apr 2026 02:36:39 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:a1793b135670f06d2d48887f5d54fe720f8f691668543c9efd84194ca3391c47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99e59eb96ad3ffc55620c9b0c844ae6ec092b7efa58c7479c81fe1d02a0de192`

```dockerfile
```

-	Layers:
	-	`sha256:e824aa3e3c062526a1e00bfa536a39b5fa90eb7970f9f4221c1c1f30556a46c3`  
		Last Modified: Wed, 22 Apr 2026 02:36:38 GMT  
		Size: 5.1 MB (5078728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:228cfbc0147448fe1a08b1b6ef8895f5e07d38f3f00f28654c1065c1a201c271`  
		Last Modified: Wed, 22 Apr 2026 02:36:38 GMT  
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
$ docker pull influxdb@sha256:8775a9fe738c10b62eda9f70323ce09dc76c8e93c3efaa8c1a369d985a5ff4fb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.9-data` - linux; amd64

```console
$ docker pull influxdb@sha256:ff66cac71bb302360fb395ec37f290a31a6f55246985504827754880c011fd84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114703436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f721c9f5b9f8133357e9310da4c7f91c2583d50aaf293fb1aa30a22382053bbd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 05:00:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:14:51 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 05:14:54 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Wed, 22 Apr 2026 05:14:54 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Wed, 22 Apr 2026 05:14:54 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 22 Apr 2026 05:14:54 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 22 Apr 2026 05:14:54 GMT
VOLUME [/var/lib/influxdb]
# Wed, 22 Apr 2026 05:14:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 05:14:54 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 22 Apr 2026 05:14:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 05:14:54 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5203b2bfeff92b72e816dc6cbb1f16856f0cd592e521e3c0cfa195a78fe180e`  
		Last Modified: Wed, 22 Apr 2026 05:01:15 GMT  
		Size: 24.0 MB (24042234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f155390245d5286ab062bac74ed4ba57587adbe288991bb0b4874107172d2a`  
		Last Modified: Wed, 22 Apr 2026 05:15:05 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1917c023636a70529c2744e84d6591b4a7ef2c338ac0604ab07640fcdad805a5`  
		Last Modified: Wed, 22 Apr 2026 05:15:07 GMT  
		Size: 42.2 MB (42165729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b2a9a62e89e4d34216a2937587767254c254f24ebe7ecd205ffe215a31713a`  
		Last Modified: Wed, 22 Apr 2026 05:15:06 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c3052e2838a906278a5a62b0b41bdcda7d79f1e9ad56a729e207353d709e8f`  
		Last Modified: Wed, 22 Apr 2026 05:15:06 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15db9ed7f815fe02c82827e19e011c20566aadb010b0976fe91cd1bc29aae76a`  
		Last Modified: Wed, 22 Apr 2026 05:15:07 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.9-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:50a2abbc0a59411a53c50a9927f84c9ebccb4f4efc82a1e2b1bb5ac7144a67ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4699071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0914528b4d1a6439bd74fe515666be9dea46d655cbf5dce24e2cdc27b39d03de`

```dockerfile
```

-	Layers:
	-	`sha256:ea527fe6eb23eaebd69fc5a90930228589de5eef29c4e1fccc18761c8d314c99`  
		Last Modified: Wed, 22 Apr 2026 05:15:06 GMT  
		Size: 4.7 MB (4684406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67508d6f36e0af41c02c79f03f70645259bfb22c0976302e346ad4c0b73e0f4a`  
		Last Modified: Wed, 22 Apr 2026 05:15:06 GMT  
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
$ docker pull influxdb@sha256:11f90b3d8577c9264734c794e3e53378e609e3ceb1aaa1f2bd55038d752ee542
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.9-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:8698497de01a3ff8d806d6daf1013f9f6620e9661bc2d25dbbc4f56e0bae1ac1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91132621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f4fefd3011c345c7500a3cb40d86d30cff24ffe45957ac2ade4e09699ad91f4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 05:00:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:14:57 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 05:14:59 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Wed, 22 Apr 2026 05:14:59 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Wed, 22 Apr 2026 05:14:59 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Wed, 22 Apr 2026 05:14:59 GMT
EXPOSE map[8091/tcp:{}]
# Wed, 22 Apr 2026 05:14:59 GMT
VOLUME [/var/lib/influxdb]
# Wed, 22 Apr 2026 05:14:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 05:14:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 05:14:59 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5203b2bfeff92b72e816dc6cbb1f16856f0cd592e521e3c0cfa195a78fe180e`  
		Last Modified: Wed, 22 Apr 2026 05:01:15 GMT  
		Size: 24.0 MB (24042234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c65a81f6831e749e3129747b4d4af574bb09c5d2c927e21e11b50458c79b70`  
		Last Modified: Wed, 22 Apr 2026 05:15:08 GMT  
		Size: 5.1 KB (5056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c0a94894ebba1bba595d504c7ef0ae1a7e979aad6bfd5425d950bb6263098d`  
		Last Modified: Wed, 22 Apr 2026 05:15:09 GMT  
		Size: 18.6 MB (18596140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5892d118679be9ea2a44134469e9c97c8bfe0664b80128bb3c33081d6bf58334`  
		Last Modified: Wed, 22 Apr 2026 05:15:08 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544fa5874482c61fd48e87fe0ff350eb61d67faff84d0cda6e88a067b7a800a7`  
		Last Modified: Wed, 22 Apr 2026 05:15:08 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.9-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:c096d57b1c8c09b3a17fa483fcfd5b3f64b570cf7da4d8ed67c0b6c17bc1af9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4604273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e420f2fda8d40b518419cf6569e112fa9a5d28a40a23822aa4a457759a50d9df`

```dockerfile
```

-	Layers:
	-	`sha256:98181d9a340539cff37eb3138747b00bfe8e3df67fb69fd494a5a3af82c65bf7`  
		Last Modified: Wed, 22 Apr 2026 05:15:08 GMT  
		Size: 4.6 MB (4591249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbb0768ef3dc6de245ef9f648904da6544ce48cf2600645b7e608cb274d8788a`  
		Last Modified: Wed, 22 Apr 2026 05:15:08 GMT  
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
$ docker pull influxdb@sha256:494656d3c3f9c9a56024004c5202df2055c54ec50c0a54a6bc3f91e761ab9b23
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.12` - linux; amd64

```console
$ docker pull influxdb@sha256:77f90966dc2d078c280ee5df32fd3439973493b0ed9736b9cda9930df0e1f90d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114660046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2776331ede600879ecef058da396676de24f94fc61bf7aa412339a272eab6149`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 05:00:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:14:15 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Wed, 22 Apr 2026 05:14:19 GMT
ENV INFLUXDB_VERSION=1.12.4
# Wed, 22 Apr 2026 05:14:19 GMT
ENV INFLUXDB_PR=-1
# Wed, 22 Apr 2026 05:14:19 GMT
ENV INFLUXDB_PV=1.12.4-1
# Wed, 22 Apr 2026 05:14:19 GMT
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_PV}_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:14:19 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 22 Apr 2026 05:14:19 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 22 Apr 2026 05:14:19 GMT
VOLUME [/var/lib/influxdb]
# Wed, 22 Apr 2026 05:14:19 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 05:14:19 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 22 Apr 2026 05:14:19 GMT
USER influxdb
# Wed, 22 Apr 2026 05:14:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 05:14:19 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5203b2bfeff92b72e816dc6cbb1f16856f0cd592e521e3c0cfa195a78fe180e`  
		Last Modified: Wed, 22 Apr 2026 05:01:15 GMT  
		Size: 24.0 MB (24042234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97753bb98f25fb39d0fc3902b1a342f01b25899ef32a2d5e9147f44430ae27a`  
		Last Modified: Wed, 22 Apr 2026 05:14:30 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540aabe82221c10413f8df2fe043bf4c4e55efa7b2e7e778aa365f0297243ca4`  
		Last Modified: Wed, 22 Apr 2026 05:14:32 GMT  
		Size: 42.1 MB (42126275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca545e60d14e79d6e0eabf0aec9832998c46202c67f7e43ddf9ab0eaf5a3ab13`  
		Last Modified: Wed, 22 Apr 2026 05:14:31 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e739d539619585e43cb3e7c1063e4ed3e415f60244fe5d315d2c010bc87876b6`  
		Last Modified: Wed, 22 Apr 2026 05:14:31 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:020bbbdaa38fd3f6f91973d4a2a4e3f613a81f6954f04252c6caca553a998a17`  
		Last Modified: Wed, 22 Apr 2026 05:14:32 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:5a5a9567c49b2bfdb2ab01f4b64eff23e65226b711e4d2bdd4f10dc47408eee0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a2b33b25e77a5d064c85a90014f04f10e7cd161dc69494ecf4f20bd67371c80`

```dockerfile
```

-	Layers:
	-	`sha256:faee33fb723fa47856e80aa191d2079a83100175d63b44041a4cd7eef9e342a6`  
		Last Modified: Wed, 22 Apr 2026 05:14:31 GMT  
		Size: 4.7 MB (4678133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:190eeee02ae11c8643393333ce5a86cdae8814409095b94aa8adf9fa96d95dbc`  
		Last Modified: Wed, 22 Apr 2026 05:14:30 GMT  
		Size: 16.5 KB (16529 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.12` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:c840967ca255da9d6b726caf2290fea4fd653586600862d3ea17c25c2fec1d36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110739822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb567ee58f57e433f8c57fdd190372fb37ea8e0e1a9173a6a616d09d37db249e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:42:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:36:10 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Wed, 22 Apr 2026 02:36:17 GMT
ENV INFLUXDB_VERSION=1.12.4
# Wed, 22 Apr 2026 02:36:17 GMT
ENV INFLUXDB_PR=-1
# Wed, 22 Apr 2026 02:36:17 GMT
ENV INFLUXDB_PV=1.12.4-1
# Wed, 22 Apr 2026 02:36:17 GMT
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_PV}_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:36:17 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 22 Apr 2026 02:36:17 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 22 Apr 2026 02:36:17 GMT
VOLUME [/var/lib/influxdb]
# Wed, 22 Apr 2026 02:36:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 02:36:17 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 22 Apr 2026 02:36:17 GMT
USER influxdb
# Wed, 22 Apr 2026 02:36:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 02:36:17 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb7bd28fbdfe678a7f45878b7b1c07dbbc0fa7753b0312aa8fd049667a9e137`  
		Last Modified: Wed, 22 Apr 2026 01:43:06 GMT  
		Size: 23.6 MB (23609423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a102ee9f27c401399728a9550447527ac0d22c34eaa0add3829ad3282c7f2479`  
		Last Modified: Wed, 22 Apr 2026 02:36:29 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba80590d32df17e9bfa14b230e6e243ca3a56ae1e41ef435aa83449375fba193`  
		Last Modified: Wed, 22 Apr 2026 02:36:30 GMT  
		Size: 38.8 MB (38754420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def07bde14a364eae108f08cf52277eb573190c95b9ba96977e899a14896dbbb`  
		Last Modified: Wed, 22 Apr 2026 02:36:29 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3889fe66469f4e5ed771e76f337e829d2858af5d1ff4a455e0980c48c30556`  
		Last Modified: Wed, 22 Apr 2026 02:36:29 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db92aca40a7f0e5c83fa2e032f010ceb6add3f40c87d373ec14564c26607a7f6`  
		Last Modified: Wed, 22 Apr 2026 02:36:30 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:243b0f933109c88e4a377f04e8cdad1737d735c7a9b7980b184f3e3f31faac31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c188d653a9852e7a7b5805fe5ce6075295aac1960e716588dec836a773d730f5`

```dockerfile
```

-	Layers:
	-	`sha256:f9d87e41b0d880da4823115f8967263e30daf36d507b25ff4219b6b4bb07bf2c`  
		Last Modified: Wed, 22 Apr 2026 02:36:29 GMT  
		Size: 4.7 MB (4677589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36d21e9b95a405be21a4cb40a980722b10a8c455cef59071d88e39533b1560a5`  
		Last Modified: Wed, 22 Apr 2026 02:36:29 GMT  
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
$ docker pull influxdb@sha256:aaab103695b866158a897c55c154dfaa6f8a2f4ac585476a0366a2629073dc37
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12-data` - linux; amd64

```console
$ docker pull influxdb@sha256:c163e1c74230ad947f16635ff9725dbcbba5843a028681017d0ef70d645b3c09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115722575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4883d307573f9e797a50418b1a17a12876dc37164cfb213c304d7cc3ed09fef6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 05:00:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:14:29 GMT
ENV INFLUXDB_VERSION=1.12.4-c1.12.4
# Wed, 22 Apr 2026 05:14:29 GMT
ENV INFLUXDB_PR=
# Wed, 22 Apr 2026 05:14:29 GMT
ENV INFLUXDB_PV=1.12.4-c1.12.4
# Wed, 22 Apr 2026 05:14:29 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"          -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"         "influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     rm -r "influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"           "influxdb-data_${INFLUXDB_PV}_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:14:29 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 22 Apr 2026 05:14:29 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 22 Apr 2026 05:14:29 GMT
VOLUME [/var/lib/influxdb]
# Wed, 22 Apr 2026 05:14:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 05:14:29 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 22 Apr 2026 05:14:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 05:14:29 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5203b2bfeff92b72e816dc6cbb1f16856f0cd592e521e3c0cfa195a78fe180e`  
		Last Modified: Wed, 22 Apr 2026 05:01:15 GMT  
		Size: 24.0 MB (24042234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d1b05c94f056b0fef25f7d3701eb4af5525bf42505e9b3f0df5dd9a1211b10`  
		Last Modified: Wed, 22 Apr 2026 05:14:42 GMT  
		Size: 43.2 MB (43189938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbdb9d678b77131f240e0218ae056660148f3ac566622f82d333b3ceb03fc98`  
		Last Modified: Wed, 22 Apr 2026 05:14:40 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5e81ad4dc7b1e62945535319a65fcb67e9d77314995d8fc1a8d08b1ffba585`  
		Last Modified: Wed, 22 Apr 2026 05:14:40 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d02b2b35e363d3943df28cdb271eabde79211e8048802fd5232dbd35d9d72f1`  
		Last Modified: Wed, 22 Apr 2026 05:14:40 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:910d30926eb1e6af41ee5ba90fd70b3431ae7e62e35aabb92899efa6aa4112cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4707275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ccaa32dd87ba5f1543fe3da309ec4a169538093f8088556b3c6486610ccc3d`

```dockerfile
```

-	Layers:
	-	`sha256:47a6e53cea8423ba56cae5c47e6b86ca66e764621c331101aa3bca02996e92f2`  
		Last Modified: Wed, 22 Apr 2026 05:14:41 GMT  
		Size: 4.7 MB (4693123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad84735b3a53e9c955883456219b0c38e9c06aa370261f17be39874f7755f732`  
		Last Modified: Wed, 22 Apr 2026 05:14:40 GMT  
		Size: 14.2 KB (14152 bytes)  
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
$ docker pull influxdb@sha256:50920e6bc1e5cc790337bd2ddfa0536fa0d83934c6de205eaaba7a44460e8b56
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:7295a2784b0151002df34fd70bfbba0f22e2ac1b88fd5cf86a3d6f3a8027c74c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91916606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c8ae624edc2715109986b7ceaa9738b05593b259093fce0caa98c18b1a4085`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 05:00:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:14:42 GMT
ENV INFLUXDB_VERSION=1.12.4-c1.12.4
# Wed, 22 Apr 2026 05:14:42 GMT
ENV INFLUXDB_PR=
# Wed, 22 Apr 2026 05:14:42 GMT
ENV INFLUXDB_PV=1.12.4-c1.12.4
# Wed, 22 Apr 2026 05:14:42 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"          -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"         "influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     rm -r "influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"           "influxdb-meta_${INFLUXDB_PV}_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:14:42 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Wed, 22 Apr 2026 05:14:42 GMT
EXPOSE map[8091/tcp:{}]
# Wed, 22 Apr 2026 05:14:42 GMT
VOLUME [/var/lib/influxdb]
# Wed, 22 Apr 2026 05:14:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 05:14:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 05:14:42 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5203b2bfeff92b72e816dc6cbb1f16856f0cd592e521e3c0cfa195a78fe180e`  
		Last Modified: Wed, 22 Apr 2026 05:01:15 GMT  
		Size: 24.0 MB (24042234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ba82e5c4dcd2ffca6424b1feec7f5f20c3a85084d439de2b4ee2f08891315e`  
		Last Modified: Wed, 22 Apr 2026 05:14:51 GMT  
		Size: 19.4 MB (19385177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:910a461f97b55c63b3bf72d7cad4cca02b14e2ad5d9cc52841600918632c64f2`  
		Last Modified: Wed, 22 Apr 2026 05:14:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fceae9ecbcce3b449a8ef4056200d3b2f6b5e26989049aebe1f736392e4b1d5e`  
		Last Modified: Wed, 22 Apr 2026 05:14:51 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:d025602733440f7510197429672effd4078d264103b8fc4d3429b07ee749350f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4605855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75ea009d0d1f2932cc697f45dedebc3fb4b19cf437bad3d2c681e2fdb95fc892`

```dockerfile
```

-	Layers:
	-	`sha256:4c314086460a2da89802ac24ffdb500a7532a3af20766d99ebd9dc00ce2eec2a`  
		Last Modified: Wed, 22 Apr 2026 05:14:51 GMT  
		Size: 4.6 MB (4593191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7aaae0b352fbcf87a40be275e27cf62c73fdfd11ddec8256a3d71429b01a9c30`  
		Last Modified: Wed, 22 Apr 2026 05:14:51 GMT  
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
$ docker pull influxdb@sha256:494656d3c3f9c9a56024004c5202df2055c54ec50c0a54a6bc3f91e761ab9b23
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.12.4` - linux; amd64

```console
$ docker pull influxdb@sha256:77f90966dc2d078c280ee5df32fd3439973493b0ed9736b9cda9930df0e1f90d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114660046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2776331ede600879ecef058da396676de24f94fc61bf7aa412339a272eab6149`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 05:00:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:14:15 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Wed, 22 Apr 2026 05:14:19 GMT
ENV INFLUXDB_VERSION=1.12.4
# Wed, 22 Apr 2026 05:14:19 GMT
ENV INFLUXDB_PR=-1
# Wed, 22 Apr 2026 05:14:19 GMT
ENV INFLUXDB_PV=1.12.4-1
# Wed, 22 Apr 2026 05:14:19 GMT
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_PV}_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:14:19 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 22 Apr 2026 05:14:19 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 22 Apr 2026 05:14:19 GMT
VOLUME [/var/lib/influxdb]
# Wed, 22 Apr 2026 05:14:19 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 05:14:19 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 22 Apr 2026 05:14:19 GMT
USER influxdb
# Wed, 22 Apr 2026 05:14:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 05:14:19 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5203b2bfeff92b72e816dc6cbb1f16856f0cd592e521e3c0cfa195a78fe180e`  
		Last Modified: Wed, 22 Apr 2026 05:01:15 GMT  
		Size: 24.0 MB (24042234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97753bb98f25fb39d0fc3902b1a342f01b25899ef32a2d5e9147f44430ae27a`  
		Last Modified: Wed, 22 Apr 2026 05:14:30 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540aabe82221c10413f8df2fe043bf4c4e55efa7b2e7e778aa365f0297243ca4`  
		Last Modified: Wed, 22 Apr 2026 05:14:32 GMT  
		Size: 42.1 MB (42126275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca545e60d14e79d6e0eabf0aec9832998c46202c67f7e43ddf9ab0eaf5a3ab13`  
		Last Modified: Wed, 22 Apr 2026 05:14:31 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e739d539619585e43cb3e7c1063e4ed3e415f60244fe5d315d2c010bc87876b6`  
		Last Modified: Wed, 22 Apr 2026 05:14:31 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:020bbbdaa38fd3f6f91973d4a2a4e3f613a81f6954f04252c6caca553a998a17`  
		Last Modified: Wed, 22 Apr 2026 05:14:32 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.4` - unknown; unknown

```console
$ docker pull influxdb@sha256:5a5a9567c49b2bfdb2ab01f4b64eff23e65226b711e4d2bdd4f10dc47408eee0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a2b33b25e77a5d064c85a90014f04f10e7cd161dc69494ecf4f20bd67371c80`

```dockerfile
```

-	Layers:
	-	`sha256:faee33fb723fa47856e80aa191d2079a83100175d63b44041a4cd7eef9e342a6`  
		Last Modified: Wed, 22 Apr 2026 05:14:31 GMT  
		Size: 4.7 MB (4678133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:190eeee02ae11c8643393333ce5a86cdae8814409095b94aa8adf9fa96d95dbc`  
		Last Modified: Wed, 22 Apr 2026 05:14:30 GMT  
		Size: 16.5 KB (16529 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.12.4` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:c840967ca255da9d6b726caf2290fea4fd653586600862d3ea17c25c2fec1d36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110739822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb567ee58f57e433f8c57fdd190372fb37ea8e0e1a9173a6a616d09d37db249e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:42:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:36:10 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Wed, 22 Apr 2026 02:36:17 GMT
ENV INFLUXDB_VERSION=1.12.4
# Wed, 22 Apr 2026 02:36:17 GMT
ENV INFLUXDB_PR=-1
# Wed, 22 Apr 2026 02:36:17 GMT
ENV INFLUXDB_PV=1.12.4-1
# Wed, 22 Apr 2026 02:36:17 GMT
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_PV}_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:36:17 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 22 Apr 2026 02:36:17 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 22 Apr 2026 02:36:17 GMT
VOLUME [/var/lib/influxdb]
# Wed, 22 Apr 2026 02:36:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 02:36:17 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 22 Apr 2026 02:36:17 GMT
USER influxdb
# Wed, 22 Apr 2026 02:36:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 02:36:17 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb7bd28fbdfe678a7f45878b7b1c07dbbc0fa7753b0312aa8fd049667a9e137`  
		Last Modified: Wed, 22 Apr 2026 01:43:06 GMT  
		Size: 23.6 MB (23609423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a102ee9f27c401399728a9550447527ac0d22c34eaa0add3829ad3282c7f2479`  
		Last Modified: Wed, 22 Apr 2026 02:36:29 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba80590d32df17e9bfa14b230e6e243ca3a56ae1e41ef435aa83449375fba193`  
		Last Modified: Wed, 22 Apr 2026 02:36:30 GMT  
		Size: 38.8 MB (38754420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def07bde14a364eae108f08cf52277eb573190c95b9ba96977e899a14896dbbb`  
		Last Modified: Wed, 22 Apr 2026 02:36:29 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3889fe66469f4e5ed771e76f337e829d2858af5d1ff4a455e0980c48c30556`  
		Last Modified: Wed, 22 Apr 2026 02:36:29 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db92aca40a7f0e5c83fa2e032f010ceb6add3f40c87d373ec14564c26607a7f6`  
		Last Modified: Wed, 22 Apr 2026 02:36:30 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.4` - unknown; unknown

```console
$ docker pull influxdb@sha256:243b0f933109c88e4a377f04e8cdad1737d735c7a9b7980b184f3e3f31faac31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c188d653a9852e7a7b5805fe5ce6075295aac1960e716588dec836a773d730f5`

```dockerfile
```

-	Layers:
	-	`sha256:f9d87e41b0d880da4823115f8967263e30daf36d507b25ff4219b6b4bb07bf2c`  
		Last Modified: Wed, 22 Apr 2026 02:36:29 GMT  
		Size: 4.7 MB (4677589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36d21e9b95a405be21a4cb40a980722b10a8c455cef59071d88e39533b1560a5`  
		Last Modified: Wed, 22 Apr 2026 02:36:29 GMT  
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
$ docker pull influxdb@sha256:aaab103695b866158a897c55c154dfaa6f8a2f4ac585476a0366a2629073dc37
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12.4-data` - linux; amd64

```console
$ docker pull influxdb@sha256:c163e1c74230ad947f16635ff9725dbcbba5843a028681017d0ef70d645b3c09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115722575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4883d307573f9e797a50418b1a17a12876dc37164cfb213c304d7cc3ed09fef6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 05:00:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:14:29 GMT
ENV INFLUXDB_VERSION=1.12.4-c1.12.4
# Wed, 22 Apr 2026 05:14:29 GMT
ENV INFLUXDB_PR=
# Wed, 22 Apr 2026 05:14:29 GMT
ENV INFLUXDB_PV=1.12.4-c1.12.4
# Wed, 22 Apr 2026 05:14:29 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"          -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"         "influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     rm -r "influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"           "influxdb-data_${INFLUXDB_PV}_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:14:29 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 22 Apr 2026 05:14:29 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 22 Apr 2026 05:14:29 GMT
VOLUME [/var/lib/influxdb]
# Wed, 22 Apr 2026 05:14:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 05:14:29 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 22 Apr 2026 05:14:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 05:14:29 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5203b2bfeff92b72e816dc6cbb1f16856f0cd592e521e3c0cfa195a78fe180e`  
		Last Modified: Wed, 22 Apr 2026 05:01:15 GMT  
		Size: 24.0 MB (24042234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d1b05c94f056b0fef25f7d3701eb4af5525bf42505e9b3f0df5dd9a1211b10`  
		Last Modified: Wed, 22 Apr 2026 05:14:42 GMT  
		Size: 43.2 MB (43189938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbdb9d678b77131f240e0218ae056660148f3ac566622f82d333b3ceb03fc98`  
		Last Modified: Wed, 22 Apr 2026 05:14:40 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5e81ad4dc7b1e62945535319a65fcb67e9d77314995d8fc1a8d08b1ffba585`  
		Last Modified: Wed, 22 Apr 2026 05:14:40 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d02b2b35e363d3943df28cdb271eabde79211e8048802fd5232dbd35d9d72f1`  
		Last Modified: Wed, 22 Apr 2026 05:14:40 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.4-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:910d30926eb1e6af41ee5ba90fd70b3431ae7e62e35aabb92899efa6aa4112cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4707275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ccaa32dd87ba5f1543fe3da309ec4a169538093f8088556b3c6486610ccc3d`

```dockerfile
```

-	Layers:
	-	`sha256:47a6e53cea8423ba56cae5c47e6b86ca66e764621c331101aa3bca02996e92f2`  
		Last Modified: Wed, 22 Apr 2026 05:14:41 GMT  
		Size: 4.7 MB (4693123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad84735b3a53e9c955883456219b0c38e9c06aa370261f17be39874f7755f732`  
		Last Modified: Wed, 22 Apr 2026 05:14:40 GMT  
		Size: 14.2 KB (14152 bytes)  
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
$ docker pull influxdb@sha256:50920e6bc1e5cc790337bd2ddfa0536fa0d83934c6de205eaaba7a44460e8b56
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12.4-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:7295a2784b0151002df34fd70bfbba0f22e2ac1b88fd5cf86a3d6f3a8027c74c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91916606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c8ae624edc2715109986b7ceaa9738b05593b259093fce0caa98c18b1a4085`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 05:00:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:14:42 GMT
ENV INFLUXDB_VERSION=1.12.4-c1.12.4
# Wed, 22 Apr 2026 05:14:42 GMT
ENV INFLUXDB_PR=
# Wed, 22 Apr 2026 05:14:42 GMT
ENV INFLUXDB_PV=1.12.4-c1.12.4
# Wed, 22 Apr 2026 05:14:42 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"          -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"         "influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     rm -r "influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"           "influxdb-meta_${INFLUXDB_PV}_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:14:42 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Wed, 22 Apr 2026 05:14:42 GMT
EXPOSE map[8091/tcp:{}]
# Wed, 22 Apr 2026 05:14:42 GMT
VOLUME [/var/lib/influxdb]
# Wed, 22 Apr 2026 05:14:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 05:14:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 05:14:42 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5203b2bfeff92b72e816dc6cbb1f16856f0cd592e521e3c0cfa195a78fe180e`  
		Last Modified: Wed, 22 Apr 2026 05:01:15 GMT  
		Size: 24.0 MB (24042234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ba82e5c4dcd2ffca6424b1feec7f5f20c3a85084d439de2b4ee2f08891315e`  
		Last Modified: Wed, 22 Apr 2026 05:14:51 GMT  
		Size: 19.4 MB (19385177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:910a461f97b55c63b3bf72d7cad4cca02b14e2ad5d9cc52841600918632c64f2`  
		Last Modified: Wed, 22 Apr 2026 05:14:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fceae9ecbcce3b449a8ef4056200d3b2f6b5e26989049aebe1f736392e4b1d5e`  
		Last Modified: Wed, 22 Apr 2026 05:14:51 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.4-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:d025602733440f7510197429672effd4078d264103b8fc4d3429b07ee749350f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4605855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75ea009d0d1f2932cc697f45dedebc3fb4b19cf437bad3d2c681e2fdb95fc892`

```dockerfile
```

-	Layers:
	-	`sha256:4c314086460a2da89802ac24ffdb500a7532a3af20766d99ebd9dc00ce2eec2a`  
		Last Modified: Wed, 22 Apr 2026 05:14:51 GMT  
		Size: 4.6 MB (4593191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7aaae0b352fbcf87a40be275e27cf62c73fdfd11ddec8256a3d71429b01a9c30`  
		Last Modified: Wed, 22 Apr 2026 05:14:51 GMT  
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
$ docker pull influxdb@sha256:a27b4d07c0561ab6d1069fcb8bb66331c1e1b32cf813549181e05bd5eea1506d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2` - linux; amd64

```console
$ docker pull influxdb@sha256:30ab5491312ddae344739c5443aa5300ea53c8c2666c3ed555a69a14a001065b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.8 MB (110771067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ec736138b87d4d4bc7aa6f097e89db933c64d902e0228d08c25b32a37ab11f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 06 May 2026 21:39:35 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg       util-linux &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 21:39:36 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Wed, 06 May 2026 21:39:36 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 06 May 2026 21:39:39 GMT
ENV INFLUXDB_VERSION=2.9.0
# Wed, 06 May 2026 21:39:39 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 06 May 2026 21:39:39 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Wed, 06 May 2026 21:39:40 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 06 May 2026 21:39:40 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 06 May 2026 21:39:40 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 06 May 2026 21:39:40 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 06 May 2026 21:39:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 06 May 2026 21:39:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 06 May 2026 21:39:40 GMT
CMD ["influxd"]
# Wed, 06 May 2026 21:39:40 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 06 May 2026 21:39:40 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 06 May 2026 21:39:40 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 06 May 2026 21:39:40 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 06 May 2026 21:39:40 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7819382621221a6e3200e2ad1ee8e7d819fde411b1f225fa6195986047882e`  
		Last Modified: Wed, 06 May 2026 21:39:51 GMT  
		Size: 9.8 MB (9798988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d5ff83386de8f2ec8ad12c0b892b1783d29993d3476d7491905d8306ad1f00`  
		Last Modified: Wed, 06 May 2026 21:39:51 GMT  
		Size: 3.8 MB (3822788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7150eb574c955f65092dea0ad2851563777af70669df0bb6f92bed6d642438e9`  
		Last Modified: Wed, 06 May 2026 21:39:51 GMT  
		Size: 3.2 KB (3231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4eadcf808dcebfe7efa997a11dad09672418214a9b29e38b95ba9f82571ec5`  
		Last Modified: Wed, 06 May 2026 21:39:53 GMT  
		Size: 56.5 MB (56481033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aeb66f0a5010dbf6a32c7b1cf2691a5090e5f6ba6c9d179e3da1e8bce4a548e`  
		Last Modified: Wed, 06 May 2026 21:39:52 GMT  
		Size: 12.4 MB (12421824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d8c6eb1872fb0549eaa58c97bd1d3b2be36ac77a87ab737970c86455d6628f`  
		Last Modified: Wed, 06 May 2026 21:39:52 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36e89de3c4b23ec450927e1b246e25293312ce9dd31c0ac77f1ba5c02045c3d`  
		Last Modified: Wed, 06 May 2026 21:39:53 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb9dfb0bada6fd7ea5f35efd276800e04b8ede9a23260925b8b37626466454d`  
		Last Modified: Wed, 06 May 2026 21:39:53 GMT  
		Size: 6.5 KB (6509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:a3c61bba8dfd3483f17bb9d05b6c20046d8ef770edce53de87274b01bdc35a43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8837c5cfbf9dd7c9bbf4672f453ccd9f1e4c3b54079d8adc2f6fd9b233672b97`

```dockerfile
```

-	Layers:
	-	`sha256:b1f0ea3eaa70cc4157d432bea7dc995ea0d6a1252ae6bf4c59a90eaf6ec7855f`  
		Last Modified: Wed, 06 May 2026 21:39:51 GMT  
		Size: 3.0 MB (2958900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:082cae7e33b89dd240005735955df9f2153ddd9ba599672999da04b9c5c2f1ba`  
		Last Modified: Wed, 06 May 2026 21:39:51 GMT  
		Size: 28.6 KB (28614 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:5d6b9d436af21a0fd9323d9981a8baf8db893ac82c51f0d57202cf6fcd1ceb1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106319198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e358abf872fc17013847c829a2fc4cf77e21020628769e463a4dc2d819f4794e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 06 May 2026 21:39:27 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg       util-linux &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 21:39:27 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Wed, 06 May 2026 21:39:28 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 06 May 2026 21:39:30 GMT
ENV INFLUXDB_VERSION=2.9.0
# Wed, 06 May 2026 21:39:30 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 06 May 2026 21:39:30 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Wed, 06 May 2026 21:39:32 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 06 May 2026 21:39:32 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 06 May 2026 21:39:32 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 06 May 2026 21:39:32 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 06 May 2026 21:39:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 06 May 2026 21:39:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 06 May 2026 21:39:32 GMT
CMD ["influxd"]
# Wed, 06 May 2026 21:39:32 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 06 May 2026 21:39:32 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 06 May 2026 21:39:32 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 06 May 2026 21:39:32 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 06 May 2026 21:39:32 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f5ea306b91844e1a73d4db5778718f1d5bdaae9fd6ef67940e8c4f1ab041ff`  
		Last Modified: Wed, 06 May 2026 21:39:44 GMT  
		Size: 9.6 MB (9628158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72c4f2a7d6dbd419a4e8b815ce5f7f5519071b4f1b417a38095054e58b07a11`  
		Last Modified: Wed, 06 May 2026 21:39:43 GMT  
		Size: 3.5 MB (3459168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232a250e1c380943ea0f01867c8ee064b9938109854d2ed39f89cdf68ca90f84`  
		Last Modified: Wed, 06 May 2026 21:39:43 GMT  
		Size: 3.2 KB (3231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fda2c1d0c8ba4f7c2c1272393809e00516a6ca3534723aaa3e35592931f9516`  
		Last Modified: Wed, 06 May 2026 21:39:45 GMT  
		Size: 53.6 MB (53625275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df02bb909f1341b6a5733261853a843f1a28422a119cb6f3a903f9bd22734f9b`  
		Last Modified: Wed, 06 May 2026 21:39:45 GMT  
		Size: 11.5 MB (11480299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c906da5ae1b664f1c3067f5af5658bbd134ebe0a8456e623efe51ef7fb6e5a22`  
		Last Modified: Wed, 06 May 2026 21:39:45 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22dbf3a5b996208fcba6df4259f74e371e40ab1f3dff83ef88bdde3996ece0c7`  
		Last Modified: Wed, 06 May 2026 21:39:45 GMT  
		Size: 235.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303468d3c26e3929b00a331d7a79d02fa1cc76d2bd516c98da23adfdd0444033`  
		Last Modified: Wed, 06 May 2026 21:39:46 GMT  
		Size: 6.5 KB (6509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:29a1242586560841e00b5ea36e63e7dc1f5b363fe263aa39be5ac4039c86e359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac3ecb28bd2eab71417912b935035fe6d81a786ead3c9a1496a4ee5b752a8202`

```dockerfile
```

-	Layers:
	-	`sha256:84ae0b3395a4e40fed8b397d3831a3d20ba3b4f48394d9d60c706fd72e7a5799`  
		Last Modified: Wed, 06 May 2026 21:39:43 GMT  
		Size: 3.0 MB (2958378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:191e0323a5ff726ed3539243b36cf08a9c69d8a2f389e9a4e3b8d153e995470c`  
		Last Modified: Wed, 06 May 2026 21:39:43 GMT  
		Size: 28.8 KB (28793 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2-alpine`

```console
$ docker pull influxdb@sha256:20c190638610b37cf296e4c2751d276862adaeb76909529ebe5f49b44008ac4b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:3ed797d0dc7290277232778d53ac26495f767e519c2be61c95b9a4c4d243338e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86872613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c303fd4fda03370b1c11f52e97e341b8ca80b8179a8a9fccecb91d61c1b96a7c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 06 May 2026 21:40:00 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 06 May 2026 21:40:01 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       setpriv       tzdata &&     update-ca-certificates # buildkit
# Wed, 06 May 2026 21:40:01 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Wed, 06 May 2026 21:40:01 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 06 May 2026 21:40:04 GMT
ENV INFLUXDB_VERSION=2.9.0
# Wed, 06 May 2026 21:40:04 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 06 May 2026 21:40:04 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Wed, 06 May 2026 21:40:05 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 06 May 2026 21:40:05 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 06 May 2026 21:40:05 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 06 May 2026 21:40:05 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 06 May 2026 21:40:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 06 May 2026 21:40:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 06 May 2026 21:40:05 GMT
CMD ["influxd"]
# Wed, 06 May 2026 21:40:05 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 06 May 2026 21:40:05 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 06 May 2026 21:40:05 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 06 May 2026 21:40:05 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 06 May 2026 21:40:05 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb79d1ed18eeb3d6f5c271fdf653577d69d4d0764a1eb563897195bc9d366118`  
		Last Modified: Wed, 06 May 2026 21:40:15 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5a206fee67f78672abeeee77d0f62f99293f32f283ca7c47281828af0c82e3`  
		Last Modified: Wed, 06 May 2026 21:40:15 GMT  
		Size: 10.3 MB (10274614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e467f9b7af2c31f6c4a3c017e9b18bce199a8c2be28449379b953e24200883c8`  
		Last Modified: Wed, 06 May 2026 21:40:15 GMT  
		Size: 3.8 MB (3822791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e55f0dd43ee45c68e1e27b7afcfbf9ba943fdd3277e929821cec6aa52f1f03`  
		Last Modified: Wed, 06 May 2026 21:40:15 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39339bfeececba7e69e364f628bed2a0451df80bfac4b47618fdf6cb81d022c`  
		Last Modified: Wed, 06 May 2026 21:40:17 GMT  
		Size: 56.5 MB (56481027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ceca1e5da0156f481a5165986f351c4fedfd11ecbebe4d8fc67fd1a6e1a3ca7`  
		Last Modified: Wed, 06 May 2026 21:40:16 GMT  
		Size: 12.4 MB (12421824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757b24c82e8981206d95f4ecee0fb6f384a9f026e45cae243abdfaeea38901b6`  
		Last Modified: Wed, 06 May 2026 21:40:16 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4745596672a039b446f3a93b10ce4041aa6bd07ef1dff5e6435e9dd438d591d`  
		Last Modified: Wed, 06 May 2026 21:40:17 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491fd2b5baaf913e486e95bbfb0d5b5e745b127f5e8ea33780c02ff1f37aeeae`  
		Last Modified: Wed, 06 May 2026 21:40:17 GMT  
		Size: 6.5 KB (6495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:8912a719ab53af53d896c03651fee25f20d44df1d9a911422acd00fdd843e770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **982.1 KB (982051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f577946b3d7eee2a2ef0476de59639f7dfcb0f6f3639ee7b87ae51e92e586965`

```dockerfile
```

-	Layers:
	-	`sha256:74f08e765f63a0e2596a16323fbcf79498c8763b45564b9b0888ed3f16b01691`  
		Last Modified: Wed, 06 May 2026 21:40:15 GMT  
		Size: 951.4 KB (951443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:203444d5aa6d3fadf305c98b64e66aa8d7fb5eba3b2467c9957e8860797185b2`  
		Last Modified: Wed, 06 May 2026 21:40:15 GMT  
		Size: 30.6 KB (30608 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:d3282a1741672942eef26b658644a8add9f5e8f8e905721149eea3ee03e7a9f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.0 MB (83017290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b866906e78906c2516cd6cb0e16a480df65db6420a979856a7c36287a38f35a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 06 May 2026 21:39:53 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 06 May 2026 21:39:54 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       setpriv       tzdata &&     update-ca-certificates # buildkit
# Wed, 06 May 2026 21:39:55 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Wed, 06 May 2026 21:39:55 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 06 May 2026 21:39:57 GMT
ENV INFLUXDB_VERSION=2.9.0
# Wed, 06 May 2026 21:39:57 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 06 May 2026 21:39:57 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Wed, 06 May 2026 21:39:58 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 06 May 2026 21:39:58 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 06 May 2026 21:39:58 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 06 May 2026 21:39:58 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 06 May 2026 21:39:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 06 May 2026 21:39:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 06 May 2026 21:39:58 GMT
CMD ["influxd"]
# Wed, 06 May 2026 21:39:58 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 06 May 2026 21:39:58 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 06 May 2026 21:39:58 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 06 May 2026 21:39:58 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 06 May 2026 21:39:58 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52d4e249758288e00010688d3c1bb8b6800bcab7f139bd022f8ef11d583da1c`  
		Last Modified: Wed, 06 May 2026 21:40:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0666fbf5c116272707f31634b1a74d7aed279bd316c8c3f64de12b6ea1916046`  
		Last Modified: Wed, 06 May 2026 21:40:09 GMT  
		Size: 10.2 MB (10244523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ec68e7e3514c27ab7030c2440724f09bf21fe961611efe0c6e640272595242`  
		Last Modified: Wed, 06 May 2026 21:40:08 GMT  
		Size: 3.5 MB (3459167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc20889b7797f3e03b223773138f664e73e89acc69f50ec802276a85c94eaea6`  
		Last Modified: Wed, 06 May 2026 21:40:08 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbaab4f69184be43ad588fc7688bf73a689390dce16a2b9ed39e66623ebce5e8`  
		Last Modified: Wed, 06 May 2026 21:40:11 GMT  
		Size: 53.6 MB (53625275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5832391974b1224c19d0fff4b188d6407ba1c7e8df018d185083dcc08f1ee71d`  
		Last Modified: Wed, 06 May 2026 21:40:10 GMT  
		Size: 11.5 MB (11480287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d3f56a74c0a7f435d42603799b5b7df618ebe0018995494c54ef6db689811e`  
		Last Modified: Wed, 06 May 2026 21:40:10 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b4de779a96566f0e2656bf431c70d2d4e46eafac705ce9088db1a1221cbff5`  
		Last Modified: Wed, 06 May 2026 21:40:10 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652d8a22b531248dad4af51f9e6893646a04ee47fbcbb2f66b1a30e4a931a9cb`  
		Last Modified: Wed, 06 May 2026 21:40:11 GMT  
		Size: 6.5 KB (6495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:83cc3f49881f77ba3f97418fbf404353423de5e99b31238bf7151d1e2b4965bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **980.8 KB (980845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67b7c4f117777ee43cf76a8287ee6ac37a24f1025516d6c019154c6f5968948f`

```dockerfile
```

-	Layers:
	-	`sha256:86c6fcdc0e8f299e8e322b4fa932df7543904410a5e8fe303f8e933aea93c091`  
		Last Modified: Wed, 06 May 2026 21:40:08 GMT  
		Size: 950.0 KB (950042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4a775fa634b84f9740977457ce60b899de0810383bbb43c9b57045cd396460a`  
		Last Modified: Wed, 06 May 2026 21:40:08 GMT  
		Size: 30.8 KB (30803 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.8`

```console
$ docker pull influxdb@sha256:35d7c6c3be561dd602ff091b8ced714f37fbb50677283cae092662fb79e4a20f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.8` - linux; amd64

```console
$ docker pull influxdb@sha256:b975a67c3e17ecbaa18c7c167c58933f29fc6d121acf44a3deb3d9c353a8be80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107241458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f869b98074b6ed4235c827bdf4dcd48130abe75f99e0cfae8ec0da7904d16fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Mon, 04 May 2026 19:25:04 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 May 2026 19:25:04 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 04 May 2026 19:25:05 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Mon, 04 May 2026 19:25:06 GMT
ENV GOSU_VER=1.19
# Mon, 04 May 2026 19:25:06 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Mon, 04 May 2026 19:25:06 GMT
ENV INFLUXDB_VERSION=2.8.0
# Mon, 04 May 2026 19:25:06 GMT
ENV INFLUXDB_PR=-2
# Mon, 04 May 2026 19:25:06 GMT
ENV INFLUXDB_PV=2.8.0-2
# Mon, 04 May 2026 19:25:08 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 04 May 2026 19:25:08 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 04 May 2026 19:25:09 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 04 May 2026 19:25:09 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 04 May 2026 19:25:09 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 04 May 2026 19:25:09 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 04 May 2026 19:25:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 04 May 2026 19:25:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 19:25:09 GMT
CMD ["influxd"]
# Mon, 04 May 2026 19:25:09 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 04 May 2026 19:25:09 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 04 May 2026 19:25:09 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 04 May 2026 19:25:09 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 04 May 2026 19:25:09 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd829162a16f5e99c357f1a9c2c6220b66cd94cc4f09c3b5e14fbc52d0182924`  
		Last Modified: Mon, 04 May 2026 19:25:21 GMT  
		Size: 9.8 MB (9799058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfeba6fab73d425e1e23e969014a3871fb9f8721daa95e130bbe3ec7d2a79686`  
		Last Modified: Mon, 04 May 2026 19:25:21 GMT  
		Size: 6.2 MB (6156969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a970c211c9b12982a367ac61780264e300188e8b513d01238efd43e7092f98`  
		Last Modified: Mon, 04 May 2026 19:25:21 GMT  
		Size: 3.2 KB (3235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a5dfedf6064921d39c2e7d8085824251ae9e674b2561dfc873b0c5515e9c09`  
		Last Modified: Mon, 04 May 2026 19:25:21 GMT  
		Size: 811.5 KB (811474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb0c11cb7c09d91e267f67e744c8a4de030f0fa8fdafc89e025cb88c918ad62d`  
		Last Modified: Mon, 04 May 2026 19:25:24 GMT  
		Size: 50.5 MB (50451869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9caa1f2566afcab19f6ae09927978476ef786eb5f4c2e1981639ad677f975628`  
		Last Modified: Mon, 04 May 2026 19:25:23 GMT  
		Size: 11.8 MB (11775872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41fdfdbf457af6e40fc7d56a11e03ebfaa206d8011297950072454dc5a02751e`  
		Last Modified: Mon, 04 May 2026 19:25:23 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2741a82e22a40d9a558248f33e41772f23c956a2e38c1d7b49a057487bb6aa3c`  
		Last Modified: Mon, 04 May 2026 19:25:23 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75492e04214888e1ad9d952dc02da543cc9c85ce43323fe6a89fb728207e813f`  
		Last Modified: Mon, 04 May 2026 19:25:24 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:1f338a154a230136db8816e5e67c7090592dcdb2476177986547a88a0f45eb3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea7a167b1455141970096b099192eef7204b7b39b25663f300fdd3adda122b0`

```dockerfile
```

-	Layers:
	-	`sha256:bebd8189163f9c215ab87391478fae07f2697964f602106318802b5cd42240fe`  
		Last Modified: Mon, 04 May 2026 19:25:21 GMT  
		Size: 2.9 MB (2934237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3213dcc3cb4b3a01e8825953391318db533f77491437c206827432ec8c1fda81`  
		Last Modified: Mon, 04 May 2026 19:25:21 GMT  
		Size: 33.6 KB (33621 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:5455cfc0fd83cabc2b0aa751c146cd1bcf950148a7b1d99f3e7236edde21981a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103640854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c3ca510845a94d1916b15704cc50751c173afc230cb4ccec12bf79b260bc9a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Mon, 04 May 2026 19:25:04 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 May 2026 19:25:04 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 04 May 2026 19:25:04 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Mon, 04 May 2026 19:25:06 GMT
ENV GOSU_VER=1.19
# Mon, 04 May 2026 19:25:06 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Mon, 04 May 2026 19:25:06 GMT
ENV INFLUXDB_VERSION=2.8.0
# Mon, 04 May 2026 19:25:06 GMT
ENV INFLUXDB_PR=-2
# Mon, 04 May 2026 19:25:06 GMT
ENV INFLUXDB_PV=2.8.0-2
# Mon, 04 May 2026 19:25:09 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 04 May 2026 19:25:09 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 04 May 2026 19:25:10 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 04 May 2026 19:25:10 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 04 May 2026 19:25:10 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 04 May 2026 19:25:10 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 04 May 2026 19:25:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 04 May 2026 19:25:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 19:25:10 GMT
CMD ["influxd"]
# Mon, 04 May 2026 19:25:10 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 04 May 2026 19:25:10 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 04 May 2026 19:25:10 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 04 May 2026 19:25:10 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 04 May 2026 19:25:10 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3254714c1f38f1d5d6fde5ddca1592560618b3b245010a79354dcbb0689ffafc`  
		Last Modified: Mon, 04 May 2026 19:25:22 GMT  
		Size: 9.6 MB (9628055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d19fdf2e62899c44954af0c56715f572efc98fd26c316646d020893dd561e5`  
		Last Modified: Mon, 04 May 2026 19:25:21 GMT  
		Size: 5.8 MB (5790415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea794d9c62a85ae50a2e783e76ec9f6b50bd8505a1ff259e3d29c901beccf748`  
		Last Modified: Mon, 04 May 2026 19:25:21 GMT  
		Size: 3.2 KB (3230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e207dd3f049ce1e333048e52ce962a576106bfc202cd003a81210ad5a616dd27`  
		Last Modified: Mon, 04 May 2026 19:25:21 GMT  
		Size: 766.4 KB (766370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a931311fbc44a7f158c9978f50e5fe5e8921e48522a537668d7d7f6ea1f1c2f8`  
		Last Modified: Mon, 04 May 2026 19:25:24 GMT  
		Size: 48.2 MB (48229546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b557b4b30b49a9bfce2aac5813e34bf701470b1f1f23cb1c20313db4306a1612`  
		Last Modified: Mon, 04 May 2026 19:25:23 GMT  
		Size: 11.1 MB (11100393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486749149ddfca07451076bccab53ef3a890461c044bc8658a9d684bf32ab8c3`  
		Last Modified: Mon, 04 May 2026 19:25:23 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7e69586c955416fef311ea5ca0906695835416b6a93c2a4367cd557c8b9f23`  
		Last Modified: Mon, 04 May 2026 19:25:23 GMT  
		Size: 235.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03a5e4ad96d0cebd218308740321a2ff52e61e23f925f8bb2cecbfb08907661`  
		Last Modified: Mon, 04 May 2026 19:25:25 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:776956b5cc3e09b62d2077452ba847591317b9dd9e4e8aa23ae9dbbb409797a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7ace3530cfe06e8efda3804ea2dcd9cd22a8dabfe42bcec15a79fe650dbfe9a`

```dockerfile
```

-	Layers:
	-	`sha256:fa07ef46a7537e539f2c53f3e4f40cbb915e7af664607d4fd10be92e455304b6`  
		Last Modified: Mon, 04 May 2026 19:25:21 GMT  
		Size: 2.9 MB (2933717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ef3f34ee3248d48fdf7b4d4f2feb53ebf3e60ec6ea27e00a6dcf94fdbd984b9`  
		Last Modified: Mon, 04 May 2026 19:25:21 GMT  
		Size: 33.8 KB (33815 bytes)  
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
$ docker pull influxdb@sha256:35d7c6c3be561dd602ff091b8ced714f37fbb50677283cae092662fb79e4a20f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.8.0` - linux; amd64

```console
$ docker pull influxdb@sha256:b975a67c3e17ecbaa18c7c167c58933f29fc6d121acf44a3deb3d9c353a8be80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107241458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f869b98074b6ed4235c827bdf4dcd48130abe75f99e0cfae8ec0da7904d16fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Mon, 04 May 2026 19:25:04 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 May 2026 19:25:04 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 04 May 2026 19:25:05 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Mon, 04 May 2026 19:25:06 GMT
ENV GOSU_VER=1.19
# Mon, 04 May 2026 19:25:06 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Mon, 04 May 2026 19:25:06 GMT
ENV INFLUXDB_VERSION=2.8.0
# Mon, 04 May 2026 19:25:06 GMT
ENV INFLUXDB_PR=-2
# Mon, 04 May 2026 19:25:06 GMT
ENV INFLUXDB_PV=2.8.0-2
# Mon, 04 May 2026 19:25:08 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 04 May 2026 19:25:08 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 04 May 2026 19:25:09 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 04 May 2026 19:25:09 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 04 May 2026 19:25:09 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 04 May 2026 19:25:09 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 04 May 2026 19:25:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 04 May 2026 19:25:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 19:25:09 GMT
CMD ["influxd"]
# Mon, 04 May 2026 19:25:09 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 04 May 2026 19:25:09 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 04 May 2026 19:25:09 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 04 May 2026 19:25:09 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 04 May 2026 19:25:09 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd829162a16f5e99c357f1a9c2c6220b66cd94cc4f09c3b5e14fbc52d0182924`  
		Last Modified: Mon, 04 May 2026 19:25:21 GMT  
		Size: 9.8 MB (9799058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfeba6fab73d425e1e23e969014a3871fb9f8721daa95e130bbe3ec7d2a79686`  
		Last Modified: Mon, 04 May 2026 19:25:21 GMT  
		Size: 6.2 MB (6156969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a970c211c9b12982a367ac61780264e300188e8b513d01238efd43e7092f98`  
		Last Modified: Mon, 04 May 2026 19:25:21 GMT  
		Size: 3.2 KB (3235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a5dfedf6064921d39c2e7d8085824251ae9e674b2561dfc873b0c5515e9c09`  
		Last Modified: Mon, 04 May 2026 19:25:21 GMT  
		Size: 811.5 KB (811474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb0c11cb7c09d91e267f67e744c8a4de030f0fa8fdafc89e025cb88c918ad62d`  
		Last Modified: Mon, 04 May 2026 19:25:24 GMT  
		Size: 50.5 MB (50451869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9caa1f2566afcab19f6ae09927978476ef786eb5f4c2e1981639ad677f975628`  
		Last Modified: Mon, 04 May 2026 19:25:23 GMT  
		Size: 11.8 MB (11775872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41fdfdbf457af6e40fc7d56a11e03ebfaa206d8011297950072454dc5a02751e`  
		Last Modified: Mon, 04 May 2026 19:25:23 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2741a82e22a40d9a558248f33e41772f23c956a2e38c1d7b49a057487bb6aa3c`  
		Last Modified: Mon, 04 May 2026 19:25:23 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75492e04214888e1ad9d952dc02da543cc9c85ce43323fe6a89fb728207e813f`  
		Last Modified: Mon, 04 May 2026 19:25:24 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8.0` - unknown; unknown

```console
$ docker pull influxdb@sha256:1f338a154a230136db8816e5e67c7090592dcdb2476177986547a88a0f45eb3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea7a167b1455141970096b099192eef7204b7b39b25663f300fdd3adda122b0`

```dockerfile
```

-	Layers:
	-	`sha256:bebd8189163f9c215ab87391478fae07f2697964f602106318802b5cd42240fe`  
		Last Modified: Mon, 04 May 2026 19:25:21 GMT  
		Size: 2.9 MB (2934237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3213dcc3cb4b3a01e8825953391318db533f77491437c206827432ec8c1fda81`  
		Last Modified: Mon, 04 May 2026 19:25:21 GMT  
		Size: 33.6 KB (33621 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.8.0` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:5455cfc0fd83cabc2b0aa751c146cd1bcf950148a7b1d99f3e7236edde21981a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103640854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c3ca510845a94d1916b15704cc50751c173afc230cb4ccec12bf79b260bc9a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Mon, 04 May 2026 19:25:04 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 May 2026 19:25:04 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 04 May 2026 19:25:04 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Mon, 04 May 2026 19:25:06 GMT
ENV GOSU_VER=1.19
# Mon, 04 May 2026 19:25:06 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Mon, 04 May 2026 19:25:06 GMT
ENV INFLUXDB_VERSION=2.8.0
# Mon, 04 May 2026 19:25:06 GMT
ENV INFLUXDB_PR=-2
# Mon, 04 May 2026 19:25:06 GMT
ENV INFLUXDB_PV=2.8.0-2
# Mon, 04 May 2026 19:25:09 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 04 May 2026 19:25:09 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 04 May 2026 19:25:10 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 04 May 2026 19:25:10 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 04 May 2026 19:25:10 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 04 May 2026 19:25:10 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 04 May 2026 19:25:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 04 May 2026 19:25:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 19:25:10 GMT
CMD ["influxd"]
# Mon, 04 May 2026 19:25:10 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 04 May 2026 19:25:10 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 04 May 2026 19:25:10 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 04 May 2026 19:25:10 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 04 May 2026 19:25:10 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3254714c1f38f1d5d6fde5ddca1592560618b3b245010a79354dcbb0689ffafc`  
		Last Modified: Mon, 04 May 2026 19:25:22 GMT  
		Size: 9.6 MB (9628055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d19fdf2e62899c44954af0c56715f572efc98fd26c316646d020893dd561e5`  
		Last Modified: Mon, 04 May 2026 19:25:21 GMT  
		Size: 5.8 MB (5790415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea794d9c62a85ae50a2e783e76ec9f6b50bd8505a1ff259e3d29c901beccf748`  
		Last Modified: Mon, 04 May 2026 19:25:21 GMT  
		Size: 3.2 KB (3230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e207dd3f049ce1e333048e52ce962a576106bfc202cd003a81210ad5a616dd27`  
		Last Modified: Mon, 04 May 2026 19:25:21 GMT  
		Size: 766.4 KB (766370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a931311fbc44a7f158c9978f50e5fe5e8921e48522a537668d7d7f6ea1f1c2f8`  
		Last Modified: Mon, 04 May 2026 19:25:24 GMT  
		Size: 48.2 MB (48229546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b557b4b30b49a9bfce2aac5813e34bf701470b1f1f23cb1c20313db4306a1612`  
		Last Modified: Mon, 04 May 2026 19:25:23 GMT  
		Size: 11.1 MB (11100393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486749149ddfca07451076bccab53ef3a890461c044bc8658a9d684bf32ab8c3`  
		Last Modified: Mon, 04 May 2026 19:25:23 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7e69586c955416fef311ea5ca0906695835416b6a93c2a4367cd557c8b9f23`  
		Last Modified: Mon, 04 May 2026 19:25:23 GMT  
		Size: 235.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03a5e4ad96d0cebd218308740321a2ff52e61e23f925f8bb2cecbfb08907661`  
		Last Modified: Mon, 04 May 2026 19:25:25 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8.0` - unknown; unknown

```console
$ docker pull influxdb@sha256:776956b5cc3e09b62d2077452ba847591317b9dd9e4e8aa23ae9dbbb409797a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7ace3530cfe06e8efda3804ea2dcd9cd22a8dabfe42bcec15a79fe650dbfe9a`

```dockerfile
```

-	Layers:
	-	`sha256:fa07ef46a7537e539f2c53f3e4f40cbb915e7af664607d4fd10be92e455304b6`  
		Last Modified: Mon, 04 May 2026 19:25:21 GMT  
		Size: 2.9 MB (2933717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ef3f34ee3248d48fdf7b4d4f2feb53ebf3e60ec6ea27e00a6dcf94fdbd984b9`  
		Last Modified: Mon, 04 May 2026 19:25:21 GMT  
		Size: 33.8 KB (33815 bytes)  
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
$ docker pull influxdb@sha256:a27b4d07c0561ab6d1069fcb8bb66331c1e1b32cf813549181e05bd5eea1506d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.9` - linux; amd64

```console
$ docker pull influxdb@sha256:30ab5491312ddae344739c5443aa5300ea53c8c2666c3ed555a69a14a001065b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.8 MB (110771067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ec736138b87d4d4bc7aa6f097e89db933c64d902e0228d08c25b32a37ab11f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 06 May 2026 21:39:35 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg       util-linux &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 21:39:36 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Wed, 06 May 2026 21:39:36 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 06 May 2026 21:39:39 GMT
ENV INFLUXDB_VERSION=2.9.0
# Wed, 06 May 2026 21:39:39 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 06 May 2026 21:39:39 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Wed, 06 May 2026 21:39:40 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 06 May 2026 21:39:40 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 06 May 2026 21:39:40 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 06 May 2026 21:39:40 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 06 May 2026 21:39:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 06 May 2026 21:39:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 06 May 2026 21:39:40 GMT
CMD ["influxd"]
# Wed, 06 May 2026 21:39:40 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 06 May 2026 21:39:40 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 06 May 2026 21:39:40 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 06 May 2026 21:39:40 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 06 May 2026 21:39:40 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7819382621221a6e3200e2ad1ee8e7d819fde411b1f225fa6195986047882e`  
		Last Modified: Wed, 06 May 2026 21:39:51 GMT  
		Size: 9.8 MB (9798988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d5ff83386de8f2ec8ad12c0b892b1783d29993d3476d7491905d8306ad1f00`  
		Last Modified: Wed, 06 May 2026 21:39:51 GMT  
		Size: 3.8 MB (3822788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7150eb574c955f65092dea0ad2851563777af70669df0bb6f92bed6d642438e9`  
		Last Modified: Wed, 06 May 2026 21:39:51 GMT  
		Size: 3.2 KB (3231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4eadcf808dcebfe7efa997a11dad09672418214a9b29e38b95ba9f82571ec5`  
		Last Modified: Wed, 06 May 2026 21:39:53 GMT  
		Size: 56.5 MB (56481033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aeb66f0a5010dbf6a32c7b1cf2691a5090e5f6ba6c9d179e3da1e8bce4a548e`  
		Last Modified: Wed, 06 May 2026 21:39:52 GMT  
		Size: 12.4 MB (12421824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d8c6eb1872fb0549eaa58c97bd1d3b2be36ac77a87ab737970c86455d6628f`  
		Last Modified: Wed, 06 May 2026 21:39:52 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36e89de3c4b23ec450927e1b246e25293312ce9dd31c0ac77f1ba5c02045c3d`  
		Last Modified: Wed, 06 May 2026 21:39:53 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb9dfb0bada6fd7ea5f35efd276800e04b8ede9a23260925b8b37626466454d`  
		Last Modified: Wed, 06 May 2026 21:39:53 GMT  
		Size: 6.5 KB (6509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.9` - unknown; unknown

```console
$ docker pull influxdb@sha256:a3c61bba8dfd3483f17bb9d05b6c20046d8ef770edce53de87274b01bdc35a43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8837c5cfbf9dd7c9bbf4672f453ccd9f1e4c3b54079d8adc2f6fd9b233672b97`

```dockerfile
```

-	Layers:
	-	`sha256:b1f0ea3eaa70cc4157d432bea7dc995ea0d6a1252ae6bf4c59a90eaf6ec7855f`  
		Last Modified: Wed, 06 May 2026 21:39:51 GMT  
		Size: 3.0 MB (2958900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:082cae7e33b89dd240005735955df9f2153ddd9ba599672999da04b9c5c2f1ba`  
		Last Modified: Wed, 06 May 2026 21:39:51 GMT  
		Size: 28.6 KB (28614 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.9` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:5d6b9d436af21a0fd9323d9981a8baf8db893ac82c51f0d57202cf6fcd1ceb1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106319198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e358abf872fc17013847c829a2fc4cf77e21020628769e463a4dc2d819f4794e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 06 May 2026 21:39:27 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg       util-linux &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 21:39:27 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Wed, 06 May 2026 21:39:28 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 06 May 2026 21:39:30 GMT
ENV INFLUXDB_VERSION=2.9.0
# Wed, 06 May 2026 21:39:30 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 06 May 2026 21:39:30 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Wed, 06 May 2026 21:39:32 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 06 May 2026 21:39:32 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 06 May 2026 21:39:32 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 06 May 2026 21:39:32 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 06 May 2026 21:39:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 06 May 2026 21:39:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 06 May 2026 21:39:32 GMT
CMD ["influxd"]
# Wed, 06 May 2026 21:39:32 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 06 May 2026 21:39:32 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 06 May 2026 21:39:32 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 06 May 2026 21:39:32 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 06 May 2026 21:39:32 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f5ea306b91844e1a73d4db5778718f1d5bdaae9fd6ef67940e8c4f1ab041ff`  
		Last Modified: Wed, 06 May 2026 21:39:44 GMT  
		Size: 9.6 MB (9628158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72c4f2a7d6dbd419a4e8b815ce5f7f5519071b4f1b417a38095054e58b07a11`  
		Last Modified: Wed, 06 May 2026 21:39:43 GMT  
		Size: 3.5 MB (3459168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232a250e1c380943ea0f01867c8ee064b9938109854d2ed39f89cdf68ca90f84`  
		Last Modified: Wed, 06 May 2026 21:39:43 GMT  
		Size: 3.2 KB (3231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fda2c1d0c8ba4f7c2c1272393809e00516a6ca3534723aaa3e35592931f9516`  
		Last Modified: Wed, 06 May 2026 21:39:45 GMT  
		Size: 53.6 MB (53625275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df02bb909f1341b6a5733261853a843f1a28422a119cb6f3a903f9bd22734f9b`  
		Last Modified: Wed, 06 May 2026 21:39:45 GMT  
		Size: 11.5 MB (11480299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c906da5ae1b664f1c3067f5af5658bbd134ebe0a8456e623efe51ef7fb6e5a22`  
		Last Modified: Wed, 06 May 2026 21:39:45 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22dbf3a5b996208fcba6df4259f74e371e40ab1f3dff83ef88bdde3996ece0c7`  
		Last Modified: Wed, 06 May 2026 21:39:45 GMT  
		Size: 235.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303468d3c26e3929b00a331d7a79d02fa1cc76d2bd516c98da23adfdd0444033`  
		Last Modified: Wed, 06 May 2026 21:39:46 GMT  
		Size: 6.5 KB (6509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.9` - unknown; unknown

```console
$ docker pull influxdb@sha256:29a1242586560841e00b5ea36e63e7dc1f5b363fe263aa39be5ac4039c86e359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac3ecb28bd2eab71417912b935035fe6d81a786ead3c9a1496a4ee5b752a8202`

```dockerfile
```

-	Layers:
	-	`sha256:84ae0b3395a4e40fed8b397d3831a3d20ba3b4f48394d9d60c706fd72e7a5799`  
		Last Modified: Wed, 06 May 2026 21:39:43 GMT  
		Size: 3.0 MB (2958378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:191e0323a5ff726ed3539243b36cf08a9c69d8a2f389e9a4e3b8d153e995470c`  
		Last Modified: Wed, 06 May 2026 21:39:43 GMT  
		Size: 28.8 KB (28793 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.9-alpine`

```console
$ docker pull influxdb@sha256:20c190638610b37cf296e4c2751d276862adaeb76909529ebe5f49b44008ac4b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.9-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:3ed797d0dc7290277232778d53ac26495f767e519c2be61c95b9a4c4d243338e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86872613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c303fd4fda03370b1c11f52e97e341b8ca80b8179a8a9fccecb91d61c1b96a7c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 06 May 2026 21:40:00 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 06 May 2026 21:40:01 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       setpriv       tzdata &&     update-ca-certificates # buildkit
# Wed, 06 May 2026 21:40:01 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Wed, 06 May 2026 21:40:01 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 06 May 2026 21:40:04 GMT
ENV INFLUXDB_VERSION=2.9.0
# Wed, 06 May 2026 21:40:04 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 06 May 2026 21:40:04 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Wed, 06 May 2026 21:40:05 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 06 May 2026 21:40:05 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 06 May 2026 21:40:05 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 06 May 2026 21:40:05 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 06 May 2026 21:40:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 06 May 2026 21:40:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 06 May 2026 21:40:05 GMT
CMD ["influxd"]
# Wed, 06 May 2026 21:40:05 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 06 May 2026 21:40:05 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 06 May 2026 21:40:05 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 06 May 2026 21:40:05 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 06 May 2026 21:40:05 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb79d1ed18eeb3d6f5c271fdf653577d69d4d0764a1eb563897195bc9d366118`  
		Last Modified: Wed, 06 May 2026 21:40:15 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5a206fee67f78672abeeee77d0f62f99293f32f283ca7c47281828af0c82e3`  
		Last Modified: Wed, 06 May 2026 21:40:15 GMT  
		Size: 10.3 MB (10274614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e467f9b7af2c31f6c4a3c017e9b18bce199a8c2be28449379b953e24200883c8`  
		Last Modified: Wed, 06 May 2026 21:40:15 GMT  
		Size: 3.8 MB (3822791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e55f0dd43ee45c68e1e27b7afcfbf9ba943fdd3277e929821cec6aa52f1f03`  
		Last Modified: Wed, 06 May 2026 21:40:15 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39339bfeececba7e69e364f628bed2a0451df80bfac4b47618fdf6cb81d022c`  
		Last Modified: Wed, 06 May 2026 21:40:17 GMT  
		Size: 56.5 MB (56481027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ceca1e5da0156f481a5165986f351c4fedfd11ecbebe4d8fc67fd1a6e1a3ca7`  
		Last Modified: Wed, 06 May 2026 21:40:16 GMT  
		Size: 12.4 MB (12421824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757b24c82e8981206d95f4ecee0fb6f384a9f026e45cae243abdfaeea38901b6`  
		Last Modified: Wed, 06 May 2026 21:40:16 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4745596672a039b446f3a93b10ce4041aa6bd07ef1dff5e6435e9dd438d591d`  
		Last Modified: Wed, 06 May 2026 21:40:17 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491fd2b5baaf913e486e95bbfb0d5b5e745b127f5e8ea33780c02ff1f37aeeae`  
		Last Modified: Wed, 06 May 2026 21:40:17 GMT  
		Size: 6.5 KB (6495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.9-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:8912a719ab53af53d896c03651fee25f20d44df1d9a911422acd00fdd843e770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **982.1 KB (982051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f577946b3d7eee2a2ef0476de59639f7dfcb0f6f3639ee7b87ae51e92e586965`

```dockerfile
```

-	Layers:
	-	`sha256:74f08e765f63a0e2596a16323fbcf79498c8763b45564b9b0888ed3f16b01691`  
		Last Modified: Wed, 06 May 2026 21:40:15 GMT  
		Size: 951.4 KB (951443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:203444d5aa6d3fadf305c98b64e66aa8d7fb5eba3b2467c9957e8860797185b2`  
		Last Modified: Wed, 06 May 2026 21:40:15 GMT  
		Size: 30.6 KB (30608 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.9-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:d3282a1741672942eef26b658644a8add9f5e8f8e905721149eea3ee03e7a9f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.0 MB (83017290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b866906e78906c2516cd6cb0e16a480df65db6420a979856a7c36287a38f35a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 06 May 2026 21:39:53 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 06 May 2026 21:39:54 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       setpriv       tzdata &&     update-ca-certificates # buildkit
# Wed, 06 May 2026 21:39:55 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Wed, 06 May 2026 21:39:55 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 06 May 2026 21:39:57 GMT
ENV INFLUXDB_VERSION=2.9.0
# Wed, 06 May 2026 21:39:57 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 06 May 2026 21:39:57 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Wed, 06 May 2026 21:39:58 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 06 May 2026 21:39:58 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 06 May 2026 21:39:58 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 06 May 2026 21:39:58 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 06 May 2026 21:39:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 06 May 2026 21:39:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 06 May 2026 21:39:58 GMT
CMD ["influxd"]
# Wed, 06 May 2026 21:39:58 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 06 May 2026 21:39:58 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 06 May 2026 21:39:58 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 06 May 2026 21:39:58 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 06 May 2026 21:39:58 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52d4e249758288e00010688d3c1bb8b6800bcab7f139bd022f8ef11d583da1c`  
		Last Modified: Wed, 06 May 2026 21:40:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0666fbf5c116272707f31634b1a74d7aed279bd316c8c3f64de12b6ea1916046`  
		Last Modified: Wed, 06 May 2026 21:40:09 GMT  
		Size: 10.2 MB (10244523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ec68e7e3514c27ab7030c2440724f09bf21fe961611efe0c6e640272595242`  
		Last Modified: Wed, 06 May 2026 21:40:08 GMT  
		Size: 3.5 MB (3459167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc20889b7797f3e03b223773138f664e73e89acc69f50ec802276a85c94eaea6`  
		Last Modified: Wed, 06 May 2026 21:40:08 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbaab4f69184be43ad588fc7688bf73a689390dce16a2b9ed39e66623ebce5e8`  
		Last Modified: Wed, 06 May 2026 21:40:11 GMT  
		Size: 53.6 MB (53625275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5832391974b1224c19d0fff4b188d6407ba1c7e8df018d185083dcc08f1ee71d`  
		Last Modified: Wed, 06 May 2026 21:40:10 GMT  
		Size: 11.5 MB (11480287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d3f56a74c0a7f435d42603799b5b7df618ebe0018995494c54ef6db689811e`  
		Last Modified: Wed, 06 May 2026 21:40:10 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b4de779a96566f0e2656bf431c70d2d4e46eafac705ce9088db1a1221cbff5`  
		Last Modified: Wed, 06 May 2026 21:40:10 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652d8a22b531248dad4af51f9e6893646a04ee47fbcbb2f66b1a30e4a931a9cb`  
		Last Modified: Wed, 06 May 2026 21:40:11 GMT  
		Size: 6.5 KB (6495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.9-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:83cc3f49881f77ba3f97418fbf404353423de5e99b31238bf7151d1e2b4965bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **980.8 KB (980845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67b7c4f117777ee43cf76a8287ee6ac37a24f1025516d6c019154c6f5968948f`

```dockerfile
```

-	Layers:
	-	`sha256:86c6fcdc0e8f299e8e322b4fa932df7543904410a5e8fe303f8e933aea93c091`  
		Last Modified: Wed, 06 May 2026 21:40:08 GMT  
		Size: 950.0 KB (950042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4a775fa634b84f9740977457ce60b899de0810383bbb43c9b57045cd396460a`  
		Last Modified: Wed, 06 May 2026 21:40:08 GMT  
		Size: 30.8 KB (30803 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.9.0`

```console
$ docker pull influxdb@sha256:a27b4d07c0561ab6d1069fcb8bb66331c1e1b32cf813549181e05bd5eea1506d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.9.0` - linux; amd64

```console
$ docker pull influxdb@sha256:30ab5491312ddae344739c5443aa5300ea53c8c2666c3ed555a69a14a001065b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.8 MB (110771067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ec736138b87d4d4bc7aa6f097e89db933c64d902e0228d08c25b32a37ab11f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 06 May 2026 21:39:35 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg       util-linux &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 21:39:36 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Wed, 06 May 2026 21:39:36 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 06 May 2026 21:39:39 GMT
ENV INFLUXDB_VERSION=2.9.0
# Wed, 06 May 2026 21:39:39 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 06 May 2026 21:39:39 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Wed, 06 May 2026 21:39:40 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 06 May 2026 21:39:40 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 06 May 2026 21:39:40 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 06 May 2026 21:39:40 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 06 May 2026 21:39:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 06 May 2026 21:39:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 06 May 2026 21:39:40 GMT
CMD ["influxd"]
# Wed, 06 May 2026 21:39:40 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 06 May 2026 21:39:40 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 06 May 2026 21:39:40 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 06 May 2026 21:39:40 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 06 May 2026 21:39:40 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7819382621221a6e3200e2ad1ee8e7d819fde411b1f225fa6195986047882e`  
		Last Modified: Wed, 06 May 2026 21:39:51 GMT  
		Size: 9.8 MB (9798988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d5ff83386de8f2ec8ad12c0b892b1783d29993d3476d7491905d8306ad1f00`  
		Last Modified: Wed, 06 May 2026 21:39:51 GMT  
		Size: 3.8 MB (3822788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7150eb574c955f65092dea0ad2851563777af70669df0bb6f92bed6d642438e9`  
		Last Modified: Wed, 06 May 2026 21:39:51 GMT  
		Size: 3.2 KB (3231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4eadcf808dcebfe7efa997a11dad09672418214a9b29e38b95ba9f82571ec5`  
		Last Modified: Wed, 06 May 2026 21:39:53 GMT  
		Size: 56.5 MB (56481033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aeb66f0a5010dbf6a32c7b1cf2691a5090e5f6ba6c9d179e3da1e8bce4a548e`  
		Last Modified: Wed, 06 May 2026 21:39:52 GMT  
		Size: 12.4 MB (12421824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d8c6eb1872fb0549eaa58c97bd1d3b2be36ac77a87ab737970c86455d6628f`  
		Last Modified: Wed, 06 May 2026 21:39:52 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36e89de3c4b23ec450927e1b246e25293312ce9dd31c0ac77f1ba5c02045c3d`  
		Last Modified: Wed, 06 May 2026 21:39:53 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb9dfb0bada6fd7ea5f35efd276800e04b8ede9a23260925b8b37626466454d`  
		Last Modified: Wed, 06 May 2026 21:39:53 GMT  
		Size: 6.5 KB (6509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.9.0` - unknown; unknown

```console
$ docker pull influxdb@sha256:a3c61bba8dfd3483f17bb9d05b6c20046d8ef770edce53de87274b01bdc35a43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8837c5cfbf9dd7c9bbf4672f453ccd9f1e4c3b54079d8adc2f6fd9b233672b97`

```dockerfile
```

-	Layers:
	-	`sha256:b1f0ea3eaa70cc4157d432bea7dc995ea0d6a1252ae6bf4c59a90eaf6ec7855f`  
		Last Modified: Wed, 06 May 2026 21:39:51 GMT  
		Size: 3.0 MB (2958900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:082cae7e33b89dd240005735955df9f2153ddd9ba599672999da04b9c5c2f1ba`  
		Last Modified: Wed, 06 May 2026 21:39:51 GMT  
		Size: 28.6 KB (28614 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.9.0` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:5d6b9d436af21a0fd9323d9981a8baf8db893ac82c51f0d57202cf6fcd1ceb1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106319198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e358abf872fc17013847c829a2fc4cf77e21020628769e463a4dc2d819f4794e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 06 May 2026 21:39:27 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg       util-linux &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 21:39:27 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Wed, 06 May 2026 21:39:28 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 06 May 2026 21:39:30 GMT
ENV INFLUXDB_VERSION=2.9.0
# Wed, 06 May 2026 21:39:30 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 06 May 2026 21:39:30 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Wed, 06 May 2026 21:39:32 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 06 May 2026 21:39:32 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 06 May 2026 21:39:32 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 06 May 2026 21:39:32 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 06 May 2026 21:39:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 06 May 2026 21:39:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 06 May 2026 21:39:32 GMT
CMD ["influxd"]
# Wed, 06 May 2026 21:39:32 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 06 May 2026 21:39:32 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 06 May 2026 21:39:32 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 06 May 2026 21:39:32 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 06 May 2026 21:39:32 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f5ea306b91844e1a73d4db5778718f1d5bdaae9fd6ef67940e8c4f1ab041ff`  
		Last Modified: Wed, 06 May 2026 21:39:44 GMT  
		Size: 9.6 MB (9628158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72c4f2a7d6dbd419a4e8b815ce5f7f5519071b4f1b417a38095054e58b07a11`  
		Last Modified: Wed, 06 May 2026 21:39:43 GMT  
		Size: 3.5 MB (3459168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232a250e1c380943ea0f01867c8ee064b9938109854d2ed39f89cdf68ca90f84`  
		Last Modified: Wed, 06 May 2026 21:39:43 GMT  
		Size: 3.2 KB (3231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fda2c1d0c8ba4f7c2c1272393809e00516a6ca3534723aaa3e35592931f9516`  
		Last Modified: Wed, 06 May 2026 21:39:45 GMT  
		Size: 53.6 MB (53625275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df02bb909f1341b6a5733261853a843f1a28422a119cb6f3a903f9bd22734f9b`  
		Last Modified: Wed, 06 May 2026 21:39:45 GMT  
		Size: 11.5 MB (11480299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c906da5ae1b664f1c3067f5af5658bbd134ebe0a8456e623efe51ef7fb6e5a22`  
		Last Modified: Wed, 06 May 2026 21:39:45 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22dbf3a5b996208fcba6df4259f74e371e40ab1f3dff83ef88bdde3996ece0c7`  
		Last Modified: Wed, 06 May 2026 21:39:45 GMT  
		Size: 235.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303468d3c26e3929b00a331d7a79d02fa1cc76d2bd516c98da23adfdd0444033`  
		Last Modified: Wed, 06 May 2026 21:39:46 GMT  
		Size: 6.5 KB (6509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.9.0` - unknown; unknown

```console
$ docker pull influxdb@sha256:29a1242586560841e00b5ea36e63e7dc1f5b363fe263aa39be5ac4039c86e359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac3ecb28bd2eab71417912b935035fe6d81a786ead3c9a1496a4ee5b752a8202`

```dockerfile
```

-	Layers:
	-	`sha256:84ae0b3395a4e40fed8b397d3831a3d20ba3b4f48394d9d60c706fd72e7a5799`  
		Last Modified: Wed, 06 May 2026 21:39:43 GMT  
		Size: 3.0 MB (2958378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:191e0323a5ff726ed3539243b36cf08a9c69d8a2f389e9a4e3b8d153e995470c`  
		Last Modified: Wed, 06 May 2026 21:39:43 GMT  
		Size: 28.8 KB (28793 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.9.0-alpine`

```console
$ docker pull influxdb@sha256:20c190638610b37cf296e4c2751d276862adaeb76909529ebe5f49b44008ac4b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.9.0-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:3ed797d0dc7290277232778d53ac26495f767e519c2be61c95b9a4c4d243338e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86872613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c303fd4fda03370b1c11f52e97e341b8ca80b8179a8a9fccecb91d61c1b96a7c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 06 May 2026 21:40:00 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 06 May 2026 21:40:01 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       setpriv       tzdata &&     update-ca-certificates # buildkit
# Wed, 06 May 2026 21:40:01 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Wed, 06 May 2026 21:40:01 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 06 May 2026 21:40:04 GMT
ENV INFLUXDB_VERSION=2.9.0
# Wed, 06 May 2026 21:40:04 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 06 May 2026 21:40:04 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Wed, 06 May 2026 21:40:05 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 06 May 2026 21:40:05 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 06 May 2026 21:40:05 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 06 May 2026 21:40:05 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 06 May 2026 21:40:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 06 May 2026 21:40:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 06 May 2026 21:40:05 GMT
CMD ["influxd"]
# Wed, 06 May 2026 21:40:05 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 06 May 2026 21:40:05 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 06 May 2026 21:40:05 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 06 May 2026 21:40:05 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 06 May 2026 21:40:05 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb79d1ed18eeb3d6f5c271fdf653577d69d4d0764a1eb563897195bc9d366118`  
		Last Modified: Wed, 06 May 2026 21:40:15 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5a206fee67f78672abeeee77d0f62f99293f32f283ca7c47281828af0c82e3`  
		Last Modified: Wed, 06 May 2026 21:40:15 GMT  
		Size: 10.3 MB (10274614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e467f9b7af2c31f6c4a3c017e9b18bce199a8c2be28449379b953e24200883c8`  
		Last Modified: Wed, 06 May 2026 21:40:15 GMT  
		Size: 3.8 MB (3822791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e55f0dd43ee45c68e1e27b7afcfbf9ba943fdd3277e929821cec6aa52f1f03`  
		Last Modified: Wed, 06 May 2026 21:40:15 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39339bfeececba7e69e364f628bed2a0451df80bfac4b47618fdf6cb81d022c`  
		Last Modified: Wed, 06 May 2026 21:40:17 GMT  
		Size: 56.5 MB (56481027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ceca1e5da0156f481a5165986f351c4fedfd11ecbebe4d8fc67fd1a6e1a3ca7`  
		Last Modified: Wed, 06 May 2026 21:40:16 GMT  
		Size: 12.4 MB (12421824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757b24c82e8981206d95f4ecee0fb6f384a9f026e45cae243abdfaeea38901b6`  
		Last Modified: Wed, 06 May 2026 21:40:16 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4745596672a039b446f3a93b10ce4041aa6bd07ef1dff5e6435e9dd438d591d`  
		Last Modified: Wed, 06 May 2026 21:40:17 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491fd2b5baaf913e486e95bbfb0d5b5e745b127f5e8ea33780c02ff1f37aeeae`  
		Last Modified: Wed, 06 May 2026 21:40:17 GMT  
		Size: 6.5 KB (6495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.9.0-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:8912a719ab53af53d896c03651fee25f20d44df1d9a911422acd00fdd843e770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **982.1 KB (982051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f577946b3d7eee2a2ef0476de59639f7dfcb0f6f3639ee7b87ae51e92e586965`

```dockerfile
```

-	Layers:
	-	`sha256:74f08e765f63a0e2596a16323fbcf79498c8763b45564b9b0888ed3f16b01691`  
		Last Modified: Wed, 06 May 2026 21:40:15 GMT  
		Size: 951.4 KB (951443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:203444d5aa6d3fadf305c98b64e66aa8d7fb5eba3b2467c9957e8860797185b2`  
		Last Modified: Wed, 06 May 2026 21:40:15 GMT  
		Size: 30.6 KB (30608 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.9.0-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:d3282a1741672942eef26b658644a8add9f5e8f8e905721149eea3ee03e7a9f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.0 MB (83017290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b866906e78906c2516cd6cb0e16a480df65db6420a979856a7c36287a38f35a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 06 May 2026 21:39:53 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 06 May 2026 21:39:54 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       setpriv       tzdata &&     update-ca-certificates # buildkit
# Wed, 06 May 2026 21:39:55 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Wed, 06 May 2026 21:39:55 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 06 May 2026 21:39:57 GMT
ENV INFLUXDB_VERSION=2.9.0
# Wed, 06 May 2026 21:39:57 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 06 May 2026 21:39:57 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Wed, 06 May 2026 21:39:58 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 06 May 2026 21:39:58 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 06 May 2026 21:39:58 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 06 May 2026 21:39:58 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 06 May 2026 21:39:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 06 May 2026 21:39:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 06 May 2026 21:39:58 GMT
CMD ["influxd"]
# Wed, 06 May 2026 21:39:58 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 06 May 2026 21:39:58 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 06 May 2026 21:39:58 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 06 May 2026 21:39:58 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 06 May 2026 21:39:58 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52d4e249758288e00010688d3c1bb8b6800bcab7f139bd022f8ef11d583da1c`  
		Last Modified: Wed, 06 May 2026 21:40:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0666fbf5c116272707f31634b1a74d7aed279bd316c8c3f64de12b6ea1916046`  
		Last Modified: Wed, 06 May 2026 21:40:09 GMT  
		Size: 10.2 MB (10244523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ec68e7e3514c27ab7030c2440724f09bf21fe961611efe0c6e640272595242`  
		Last Modified: Wed, 06 May 2026 21:40:08 GMT  
		Size: 3.5 MB (3459167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc20889b7797f3e03b223773138f664e73e89acc69f50ec802276a85c94eaea6`  
		Last Modified: Wed, 06 May 2026 21:40:08 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbaab4f69184be43ad588fc7688bf73a689390dce16a2b9ed39e66623ebce5e8`  
		Last Modified: Wed, 06 May 2026 21:40:11 GMT  
		Size: 53.6 MB (53625275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5832391974b1224c19d0fff4b188d6407ba1c7e8df018d185083dcc08f1ee71d`  
		Last Modified: Wed, 06 May 2026 21:40:10 GMT  
		Size: 11.5 MB (11480287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d3f56a74c0a7f435d42603799b5b7df618ebe0018995494c54ef6db689811e`  
		Last Modified: Wed, 06 May 2026 21:40:10 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b4de779a96566f0e2656bf431c70d2d4e46eafac705ce9088db1a1221cbff5`  
		Last Modified: Wed, 06 May 2026 21:40:10 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652d8a22b531248dad4af51f9e6893646a04ee47fbcbb2f66b1a30e4a931a9cb`  
		Last Modified: Wed, 06 May 2026 21:40:11 GMT  
		Size: 6.5 KB (6495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.9.0-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:83cc3f49881f77ba3f97418fbf404353423de5e99b31238bf7151d1e2b4965bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **980.8 KB (980845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67b7c4f117777ee43cf76a8287ee6ac37a24f1025516d6c019154c6f5968948f`

```dockerfile
```

-	Layers:
	-	`sha256:86c6fcdc0e8f299e8e322b4fa932df7543904410a5e8fe303f8e933aea93c091`  
		Last Modified: Wed, 06 May 2026 21:40:08 GMT  
		Size: 950.0 KB (950042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4a775fa634b84f9740977457ce60b899de0810383bbb43c9b57045cd396460a`  
		Last Modified: Wed, 06 May 2026 21:40:08 GMT  
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
$ docker pull influxdb@sha256:20c190638610b37cf296e4c2751d276862adaeb76909529ebe5f49b44008ac4b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:3ed797d0dc7290277232778d53ac26495f767e519c2be61c95b9a4c4d243338e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86872613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c303fd4fda03370b1c11f52e97e341b8ca80b8179a8a9fccecb91d61c1b96a7c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 06 May 2026 21:40:00 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 06 May 2026 21:40:01 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       setpriv       tzdata &&     update-ca-certificates # buildkit
# Wed, 06 May 2026 21:40:01 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Wed, 06 May 2026 21:40:01 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 06 May 2026 21:40:04 GMT
ENV INFLUXDB_VERSION=2.9.0
# Wed, 06 May 2026 21:40:04 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 06 May 2026 21:40:04 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Wed, 06 May 2026 21:40:05 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 06 May 2026 21:40:05 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 06 May 2026 21:40:05 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 06 May 2026 21:40:05 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 06 May 2026 21:40:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 06 May 2026 21:40:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 06 May 2026 21:40:05 GMT
CMD ["influxd"]
# Wed, 06 May 2026 21:40:05 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 06 May 2026 21:40:05 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 06 May 2026 21:40:05 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 06 May 2026 21:40:05 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 06 May 2026 21:40:05 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb79d1ed18eeb3d6f5c271fdf653577d69d4d0764a1eb563897195bc9d366118`  
		Last Modified: Wed, 06 May 2026 21:40:15 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5a206fee67f78672abeeee77d0f62f99293f32f283ca7c47281828af0c82e3`  
		Last Modified: Wed, 06 May 2026 21:40:15 GMT  
		Size: 10.3 MB (10274614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e467f9b7af2c31f6c4a3c017e9b18bce199a8c2be28449379b953e24200883c8`  
		Last Modified: Wed, 06 May 2026 21:40:15 GMT  
		Size: 3.8 MB (3822791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e55f0dd43ee45c68e1e27b7afcfbf9ba943fdd3277e929821cec6aa52f1f03`  
		Last Modified: Wed, 06 May 2026 21:40:15 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39339bfeececba7e69e364f628bed2a0451df80bfac4b47618fdf6cb81d022c`  
		Last Modified: Wed, 06 May 2026 21:40:17 GMT  
		Size: 56.5 MB (56481027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ceca1e5da0156f481a5165986f351c4fedfd11ecbebe4d8fc67fd1a6e1a3ca7`  
		Last Modified: Wed, 06 May 2026 21:40:16 GMT  
		Size: 12.4 MB (12421824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757b24c82e8981206d95f4ecee0fb6f384a9f026e45cae243abdfaeea38901b6`  
		Last Modified: Wed, 06 May 2026 21:40:16 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4745596672a039b446f3a93b10ce4041aa6bd07ef1dff5e6435e9dd438d591d`  
		Last Modified: Wed, 06 May 2026 21:40:17 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491fd2b5baaf913e486e95bbfb0d5b5e745b127f5e8ea33780c02ff1f37aeeae`  
		Last Modified: Wed, 06 May 2026 21:40:17 GMT  
		Size: 6.5 KB (6495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:8912a719ab53af53d896c03651fee25f20d44df1d9a911422acd00fdd843e770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **982.1 KB (982051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f577946b3d7eee2a2ef0476de59639f7dfcb0f6f3639ee7b87ae51e92e586965`

```dockerfile
```

-	Layers:
	-	`sha256:74f08e765f63a0e2596a16323fbcf79498c8763b45564b9b0888ed3f16b01691`  
		Last Modified: Wed, 06 May 2026 21:40:15 GMT  
		Size: 951.4 KB (951443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:203444d5aa6d3fadf305c98b64e66aa8d7fb5eba3b2467c9957e8860797185b2`  
		Last Modified: Wed, 06 May 2026 21:40:15 GMT  
		Size: 30.6 KB (30608 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:d3282a1741672942eef26b658644a8add9f5e8f8e905721149eea3ee03e7a9f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.0 MB (83017290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b866906e78906c2516cd6cb0e16a480df65db6420a979856a7c36287a38f35a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 06 May 2026 21:39:53 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 06 May 2026 21:39:54 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       setpriv       tzdata &&     update-ca-certificates # buildkit
# Wed, 06 May 2026 21:39:55 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Wed, 06 May 2026 21:39:55 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 06 May 2026 21:39:57 GMT
ENV INFLUXDB_VERSION=2.9.0
# Wed, 06 May 2026 21:39:57 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 06 May 2026 21:39:57 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Wed, 06 May 2026 21:39:58 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 06 May 2026 21:39:58 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 06 May 2026 21:39:58 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 06 May 2026 21:39:58 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 06 May 2026 21:39:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 06 May 2026 21:39:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 06 May 2026 21:39:58 GMT
CMD ["influxd"]
# Wed, 06 May 2026 21:39:58 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 06 May 2026 21:39:58 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 06 May 2026 21:39:58 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 06 May 2026 21:39:58 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 06 May 2026 21:39:58 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52d4e249758288e00010688d3c1bb8b6800bcab7f139bd022f8ef11d583da1c`  
		Last Modified: Wed, 06 May 2026 21:40:08 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0666fbf5c116272707f31634b1a74d7aed279bd316c8c3f64de12b6ea1916046`  
		Last Modified: Wed, 06 May 2026 21:40:09 GMT  
		Size: 10.2 MB (10244523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ec68e7e3514c27ab7030c2440724f09bf21fe961611efe0c6e640272595242`  
		Last Modified: Wed, 06 May 2026 21:40:08 GMT  
		Size: 3.5 MB (3459167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc20889b7797f3e03b223773138f664e73e89acc69f50ec802276a85c94eaea6`  
		Last Modified: Wed, 06 May 2026 21:40:08 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbaab4f69184be43ad588fc7688bf73a689390dce16a2b9ed39e66623ebce5e8`  
		Last Modified: Wed, 06 May 2026 21:40:11 GMT  
		Size: 53.6 MB (53625275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5832391974b1224c19d0fff4b188d6407ba1c7e8df018d185083dcc08f1ee71d`  
		Last Modified: Wed, 06 May 2026 21:40:10 GMT  
		Size: 11.5 MB (11480287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d3f56a74c0a7f435d42603799b5b7df618ebe0018995494c54ef6db689811e`  
		Last Modified: Wed, 06 May 2026 21:40:10 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b4de779a96566f0e2656bf431c70d2d4e46eafac705ce9088db1a1221cbff5`  
		Last Modified: Wed, 06 May 2026 21:40:10 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652d8a22b531248dad4af51f9e6893646a04ee47fbcbb2f66b1a30e4a931a9cb`  
		Last Modified: Wed, 06 May 2026 21:40:11 GMT  
		Size: 6.5 KB (6495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:83cc3f49881f77ba3f97418fbf404353423de5e99b31238bf7151d1e2b4965bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **980.8 KB (980845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67b7c4f117777ee43cf76a8287ee6ac37a24f1025516d6c019154c6f5968948f`

```dockerfile
```

-	Layers:
	-	`sha256:86c6fcdc0e8f299e8e322b4fa932df7543904410a5e8fe303f8e933aea93c091`  
		Last Modified: Wed, 06 May 2026 21:40:08 GMT  
		Size: 950.0 KB (950042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4a775fa634b84f9740977457ce60b899de0810383bbb43c9b57045cd396460a`  
		Last Modified: Wed, 06 May 2026 21:40:08 GMT  
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
$ docker pull influxdb@sha256:aaab103695b866158a897c55c154dfaa6f8a2f4ac585476a0366a2629073dc37
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:data` - linux; amd64

```console
$ docker pull influxdb@sha256:c163e1c74230ad947f16635ff9725dbcbba5843a028681017d0ef70d645b3c09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115722575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4883d307573f9e797a50418b1a17a12876dc37164cfb213c304d7cc3ed09fef6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 05:00:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:14:29 GMT
ENV INFLUXDB_VERSION=1.12.4-c1.12.4
# Wed, 22 Apr 2026 05:14:29 GMT
ENV INFLUXDB_PR=
# Wed, 22 Apr 2026 05:14:29 GMT
ENV INFLUXDB_PV=1.12.4-c1.12.4
# Wed, 22 Apr 2026 05:14:29 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"          -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"         "influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     rm -r "influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"           "influxdb-data_${INFLUXDB_PV}_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:14:29 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 22 Apr 2026 05:14:29 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 22 Apr 2026 05:14:29 GMT
VOLUME [/var/lib/influxdb]
# Wed, 22 Apr 2026 05:14:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 05:14:29 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 22 Apr 2026 05:14:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 05:14:29 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5203b2bfeff92b72e816dc6cbb1f16856f0cd592e521e3c0cfa195a78fe180e`  
		Last Modified: Wed, 22 Apr 2026 05:01:15 GMT  
		Size: 24.0 MB (24042234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d1b05c94f056b0fef25f7d3701eb4af5525bf42505e9b3f0df5dd9a1211b10`  
		Last Modified: Wed, 22 Apr 2026 05:14:42 GMT  
		Size: 43.2 MB (43189938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbdb9d678b77131f240e0218ae056660148f3ac566622f82d333b3ceb03fc98`  
		Last Modified: Wed, 22 Apr 2026 05:14:40 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5e81ad4dc7b1e62945535319a65fcb67e9d77314995d8fc1a8d08b1ffba585`  
		Last Modified: Wed, 22 Apr 2026 05:14:40 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d02b2b35e363d3943df28cdb271eabde79211e8048802fd5232dbd35d9d72f1`  
		Last Modified: Wed, 22 Apr 2026 05:14:40 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:data` - unknown; unknown

```console
$ docker pull influxdb@sha256:910d30926eb1e6af41ee5ba90fd70b3431ae7e62e35aabb92899efa6aa4112cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4707275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ccaa32dd87ba5f1543fe3da309ec4a169538093f8088556b3c6486610ccc3d`

```dockerfile
```

-	Layers:
	-	`sha256:47a6e53cea8423ba56cae5c47e6b86ca66e764621c331101aa3bca02996e92f2`  
		Last Modified: Wed, 22 Apr 2026 05:14:41 GMT  
		Size: 4.7 MB (4693123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad84735b3a53e9c955883456219b0c38e9c06aa370261f17be39874f7755f732`  
		Last Modified: Wed, 22 Apr 2026 05:14:40 GMT  
		Size: 14.2 KB (14152 bytes)  
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
$ docker pull influxdb@sha256:a27b4d07c0561ab6d1069fcb8bb66331c1e1b32cf813549181e05bd5eea1506d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:30ab5491312ddae344739c5443aa5300ea53c8c2666c3ed555a69a14a001065b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.8 MB (110771067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ec736138b87d4d4bc7aa6f097e89db933c64d902e0228d08c25b32a37ab11f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 06 May 2026 21:39:35 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg       util-linux &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 21:39:36 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Wed, 06 May 2026 21:39:36 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 06 May 2026 21:39:39 GMT
ENV INFLUXDB_VERSION=2.9.0
# Wed, 06 May 2026 21:39:39 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 06 May 2026 21:39:39 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Wed, 06 May 2026 21:39:40 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 06 May 2026 21:39:40 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 06 May 2026 21:39:40 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 06 May 2026 21:39:40 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 06 May 2026 21:39:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 06 May 2026 21:39:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 06 May 2026 21:39:40 GMT
CMD ["influxd"]
# Wed, 06 May 2026 21:39:40 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 06 May 2026 21:39:40 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 06 May 2026 21:39:40 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 06 May 2026 21:39:40 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 06 May 2026 21:39:40 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7819382621221a6e3200e2ad1ee8e7d819fde411b1f225fa6195986047882e`  
		Last Modified: Wed, 06 May 2026 21:39:51 GMT  
		Size: 9.8 MB (9798988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d5ff83386de8f2ec8ad12c0b892b1783d29993d3476d7491905d8306ad1f00`  
		Last Modified: Wed, 06 May 2026 21:39:51 GMT  
		Size: 3.8 MB (3822788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7150eb574c955f65092dea0ad2851563777af70669df0bb6f92bed6d642438e9`  
		Last Modified: Wed, 06 May 2026 21:39:51 GMT  
		Size: 3.2 KB (3231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4eadcf808dcebfe7efa997a11dad09672418214a9b29e38b95ba9f82571ec5`  
		Last Modified: Wed, 06 May 2026 21:39:53 GMT  
		Size: 56.5 MB (56481033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aeb66f0a5010dbf6a32c7b1cf2691a5090e5f6ba6c9d179e3da1e8bce4a548e`  
		Last Modified: Wed, 06 May 2026 21:39:52 GMT  
		Size: 12.4 MB (12421824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d8c6eb1872fb0549eaa58c97bd1d3b2be36ac77a87ab737970c86455d6628f`  
		Last Modified: Wed, 06 May 2026 21:39:52 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36e89de3c4b23ec450927e1b246e25293312ce9dd31c0ac77f1ba5c02045c3d`  
		Last Modified: Wed, 06 May 2026 21:39:53 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb9dfb0bada6fd7ea5f35efd276800e04b8ede9a23260925b8b37626466454d`  
		Last Modified: Wed, 06 May 2026 21:39:53 GMT  
		Size: 6.5 KB (6509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:a3c61bba8dfd3483f17bb9d05b6c20046d8ef770edce53de87274b01bdc35a43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8837c5cfbf9dd7c9bbf4672f453ccd9f1e4c3b54079d8adc2f6fd9b233672b97`

```dockerfile
```

-	Layers:
	-	`sha256:b1f0ea3eaa70cc4157d432bea7dc995ea0d6a1252ae6bf4c59a90eaf6ec7855f`  
		Last Modified: Wed, 06 May 2026 21:39:51 GMT  
		Size: 3.0 MB (2958900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:082cae7e33b89dd240005735955df9f2153ddd9ba599672999da04b9c5c2f1ba`  
		Last Modified: Wed, 06 May 2026 21:39:51 GMT  
		Size: 28.6 KB (28614 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:5d6b9d436af21a0fd9323d9981a8baf8db893ac82c51f0d57202cf6fcd1ceb1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106319198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e358abf872fc17013847c829a2fc4cf77e21020628769e463a4dc2d819f4794e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 06 May 2026 21:39:27 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg       util-linux &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 06 May 2026 21:39:27 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v3.4.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '3c947a8dcd88856a32c172081db091c38059394fb57a15fa43871f6d046427e1  /usr/local/bin/dasel' ;;       arm64) echo 'a128c5554c53e6e4af880700adba1d212ce651db208da1592fb1cae0e959cbc6  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel version # buildkit
# Wed, 06 May 2026 21:39:28 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 06 May 2026 21:39:30 GMT
ENV INFLUXDB_VERSION=2.9.0
# Wed, 06 May 2026 21:39:30 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 06 May 2026 21:39:30 GMT
ENV INFLUX_CLI_VERSION=2.8.0
# Wed, 06 May 2026 21:39:32 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 06 May 2026 21:39:32 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 06 May 2026 21:39:32 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 06 May 2026 21:39:32 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 06 May 2026 21:39:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 06 May 2026 21:39:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 06 May 2026 21:39:32 GMT
CMD ["influxd"]
# Wed, 06 May 2026 21:39:32 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 06 May 2026 21:39:32 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 06 May 2026 21:39:32 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 06 May 2026 21:39:32 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 06 May 2026 21:39:32 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f5ea306b91844e1a73d4db5778718f1d5bdaae9fd6ef67940e8c4f1ab041ff`  
		Last Modified: Wed, 06 May 2026 21:39:44 GMT  
		Size: 9.6 MB (9628158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72c4f2a7d6dbd419a4e8b815ce5f7f5519071b4f1b417a38095054e58b07a11`  
		Last Modified: Wed, 06 May 2026 21:39:43 GMT  
		Size: 3.5 MB (3459168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232a250e1c380943ea0f01867c8ee064b9938109854d2ed39f89cdf68ca90f84`  
		Last Modified: Wed, 06 May 2026 21:39:43 GMT  
		Size: 3.2 KB (3231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fda2c1d0c8ba4f7c2c1272393809e00516a6ca3534723aaa3e35592931f9516`  
		Last Modified: Wed, 06 May 2026 21:39:45 GMT  
		Size: 53.6 MB (53625275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df02bb909f1341b6a5733261853a843f1a28422a119cb6f3a903f9bd22734f9b`  
		Last Modified: Wed, 06 May 2026 21:39:45 GMT  
		Size: 11.5 MB (11480299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c906da5ae1b664f1c3067f5af5658bbd134ebe0a8456e623efe51ef7fb6e5a22`  
		Last Modified: Wed, 06 May 2026 21:39:45 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22dbf3a5b996208fcba6df4259f74e371e40ab1f3dff83ef88bdde3996ece0c7`  
		Last Modified: Wed, 06 May 2026 21:39:45 GMT  
		Size: 235.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303468d3c26e3929b00a331d7a79d02fa1cc76d2bd516c98da23adfdd0444033`  
		Last Modified: Wed, 06 May 2026 21:39:46 GMT  
		Size: 6.5 KB (6509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:29a1242586560841e00b5ea36e63e7dc1f5b363fe263aa39be5ac4039c86e359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac3ecb28bd2eab71417912b935035fe6d81a786ead3c9a1496a4ee5b752a8202`

```dockerfile
```

-	Layers:
	-	`sha256:84ae0b3395a4e40fed8b397d3831a3d20ba3b4f48394d9d60c706fd72e7a5799`  
		Last Modified: Wed, 06 May 2026 21:39:43 GMT  
		Size: 3.0 MB (2958378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:191e0323a5ff726ed3539243b36cf08a9c69d8a2f389e9a4e3b8d153e995470c`  
		Last Modified: Wed, 06 May 2026 21:39:43 GMT  
		Size: 28.8 KB (28793 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:meta`

```console
$ docker pull influxdb@sha256:50920e6bc1e5cc790337bd2ddfa0536fa0d83934c6de205eaaba7a44460e8b56
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:meta` - linux; amd64

```console
$ docker pull influxdb@sha256:7295a2784b0151002df34fd70bfbba0f22e2ac1b88fd5cf86a3d6f3a8027c74c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91916606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c8ae624edc2715109986b7ceaa9738b05593b259093fce0caa98c18b1a4085`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 05:00:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:14:42 GMT
ENV INFLUXDB_VERSION=1.12.4-c1.12.4
# Wed, 22 Apr 2026 05:14:42 GMT
ENV INFLUXDB_PR=
# Wed, 22 Apr 2026 05:14:42 GMT
ENV INFLUXDB_PV=1.12.4-c1.12.4
# Wed, 22 Apr 2026 05:14:42 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"          -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"         "influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     rm -r "influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"           "influxdb-meta_${INFLUXDB_PV}_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:14:42 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Wed, 22 Apr 2026 05:14:42 GMT
EXPOSE map[8091/tcp:{}]
# Wed, 22 Apr 2026 05:14:42 GMT
VOLUME [/var/lib/influxdb]
# Wed, 22 Apr 2026 05:14:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 05:14:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 05:14:42 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5203b2bfeff92b72e816dc6cbb1f16856f0cd592e521e3c0cfa195a78fe180e`  
		Last Modified: Wed, 22 Apr 2026 05:01:15 GMT  
		Size: 24.0 MB (24042234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ba82e5c4dcd2ffca6424b1feec7f5f20c3a85084d439de2b4ee2f08891315e`  
		Last Modified: Wed, 22 Apr 2026 05:14:51 GMT  
		Size: 19.4 MB (19385177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:910a461f97b55c63b3bf72d7cad4cca02b14e2ad5d9cc52841600918632c64f2`  
		Last Modified: Wed, 22 Apr 2026 05:14:51 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fceae9ecbcce3b449a8ef4056200d3b2f6b5e26989049aebe1f736392e4b1d5e`  
		Last Modified: Wed, 22 Apr 2026 05:14:51 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:d025602733440f7510197429672effd4078d264103b8fc4d3429b07ee749350f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4605855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75ea009d0d1f2932cc697f45dedebc3fb4b19cf437bad3d2c681e2fdb95fc892`

```dockerfile
```

-	Layers:
	-	`sha256:4c314086460a2da89802ac24ffdb500a7532a3af20766d99ebd9dc00ce2eec2a`  
		Last Modified: Wed, 22 Apr 2026 05:14:51 GMT  
		Size: 4.6 MB (4593191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7aaae0b352fbcf87a40be275e27cf62c73fdfd11ddec8256a3d71429b01a9c30`  
		Last Modified: Wed, 22 Apr 2026 05:14:51 GMT  
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
