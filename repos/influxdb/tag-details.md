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
-	[`influxdb:2.7`](#influxdb27)
-	[`influxdb:2.7-alpine`](#influxdb27-alpine)
-	[`influxdb:2.7.12`](#influxdb2712)
-	[`influxdb:2.7.12-alpine`](#influxdb2712-alpine)
-	[`influxdb:2.8`](#influxdb28)
-	[`influxdb:2.8-alpine`](#influxdb28-alpine)
-	[`influxdb:2.8.0`](#influxdb280)
-	[`influxdb:2.8.0-alpine`](#influxdb280-alpine)
-	[`influxdb:3-core`](#influxdb3-core)
-	[`influxdb:3-enterprise`](#influxdb3-enterprise)
-	[`influxdb:3.9-core`](#influxdb39-core)
-	[`influxdb:3.9-enterprise`](#influxdb39-enterprise)
-	[`influxdb:3.9.1-core`](#influxdb391-core)
-	[`influxdb:3.9.1-enterprise`](#influxdb391-enterprise)
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
$ docker pull influxdb@sha256:3b39bc0a11eeaa2c7af953e4499e10123b6de1de1bffe5c37464422995362205
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11` - linux; amd64

```console
$ docker pull influxdb@sha256:6a7bcd300ff88c1491b6f07da3c307af44f996b929f2b79541ba11d4657b16a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116186005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1b23ccbb334045d71985a1f343302bf58a4b64dfff71dfe369aa267ae8b73aa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:50:15 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 07 Apr 2026 02:50:23 GMT
ARG INFLUXDB_VERSION=1.11.8
# Tue, 07 Apr 2026 02:50:23 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:50:23 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 07 Apr 2026 02:50:23 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 07 Apr 2026 02:50:23 GMT
VOLUME [/var/lib/influxdb]
# Tue, 07 Apr 2026 02:50:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 02:50:23 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 07 Apr 2026 02:50:23 GMT
USER influxdb
# Tue, 07 Apr 2026 02:50:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 02:50:23 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c3414b1d6b49c54c305584faac46aad75c67644cf4f8495e8145206d28e416`  
		Last Modified: Tue, 07 Apr 2026 01:47:02 GMT  
		Size: 24.0 MB (24038269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e703d495b3f2846aaa942b0a03538d2dce7ac1ee61781400b8e626463d8e262`  
		Last Modified: Tue, 07 Apr 2026 02:50:36 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e604974fcaa15f2a49445b8e70fa7a3c2e277e8bf29de6de8e7b6337ac3dea8`  
		Last Modified: Tue, 07 Apr 2026 02:50:37 GMT  
		Size: 43.7 MB (43656004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3d2d21b1350355a145badb097b7dc23f1ccf4643746ecba7d0e4a9a26ebfb1`  
		Last Modified: Tue, 07 Apr 2026 02:50:36 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a9b021e817fd3671abef3e66ada790328a0f577e8d115d3bc624048c595537`  
		Last Modified: Tue, 07 Apr 2026 02:50:36 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2472fef3a3444177ff45f4cd1870ed60c8ab4b1dce8c6842da82ac7d5b6d5ec5`  
		Last Modified: Tue, 07 Apr 2026 02:50:37 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11` - unknown; unknown

```console
$ docker pull influxdb@sha256:261cfec11ac4e1ed64275f5c0101008f530a8a0230c890d023053c7dbb5ec23c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb16f25d656fdb95a08fe15b42e8935197ae25dababf5e2aaded402667ae2db`

```dockerfile
```

-	Layers:
	-	`sha256:bc50a00b512940ae6b774f3b7f2583f1096d96f14d836c7b48f3a14bb8bc9859`  
		Last Modified: Tue, 07 Apr 2026 02:50:36 GMT  
		Size: 5.1 MB (5079263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c63a23bb130c35023268a2a1fd9f5db199051deaba464584f0484b3d89e490c`  
		Last Modified: Tue, 07 Apr 2026 02:50:36 GMT  
		Size: 15.5 KB (15485 bytes)  
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
$ docker pull influxdb@sha256:d7df937902af541a5881c6b74630c1fb88f4720b8af3f99cb18ed6e11de07187
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data` - linux; amd64

```console
$ docker pull influxdb@sha256:758d0d3f69f0096323f3175c2d6a29717b3b11eecfb749b7837840c5b370309d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114699664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a92f82cfbc8b66652cc67161480d67645161346e4d145da8350ef7226c6afb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:50:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 02:50:18 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Tue, 07 Apr 2026 02:50:18 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 07 Apr 2026 02:50:18 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 07 Apr 2026 02:50:18 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 07 Apr 2026 02:50:18 GMT
VOLUME [/var/lib/influxdb]
# Tue, 07 Apr 2026 02:50:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 02:50:18 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 07 Apr 2026 02:50:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 02:50:18 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c3414b1d6b49c54c305584faac46aad75c67644cf4f8495e8145206d28e416`  
		Last Modified: Tue, 07 Apr 2026 01:47:02 GMT  
		Size: 24.0 MB (24038269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ebbbcf7f8576796fe43fe91ecaedbb7c2ff572d281e353a5ba13c38202d7e1f`  
		Last Modified: Tue, 07 Apr 2026 02:50:31 GMT  
		Size: 5.1 KB (5057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:424e398f3e75be9c20e2b8dcddbfc3266a5b798b8a550984cde845a106840e52`  
		Last Modified: Tue, 07 Apr 2026 02:50:33 GMT  
		Size: 42.2 MB (42165739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82df79d5cd0fbe3cc9053c4a97b2313b149133b18c96a6db934b2bdb1c113f8e`  
		Last Modified: Tue, 07 Apr 2026 02:50:32 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084ee29046b00f5ad50972d806af952df7f2dea8c92e784252e73c9ed43cade3`  
		Last Modified: Tue, 07 Apr 2026 02:50:32 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130f74006fc5ced1c11ab0c86465e703b013619d6713f7aba00c74a68965a362`  
		Last Modified: Tue, 07 Apr 2026 02:50:33 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:f7d815fe957668e6371df3cc8f53f90c1bf534d2ef0e58446809dd4b8fdec2c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4699071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eadb685b3aaa058aed6ae472b21b59c011da8cdcc41a5697d46e7b8485550d5b`

```dockerfile
```

-	Layers:
	-	`sha256:8e23c95197d9494cefba92875437b5160307e653b4bd0a58acd12801db12484f`  
		Last Modified: Tue, 07 Apr 2026 02:50:32 GMT  
		Size: 4.7 MB (4684406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:728f093bdf28247dc942eeb4a43147522b5d4d8f7aa0a583c5d3f23e720753f5`  
		Last Modified: Tue, 07 Apr 2026 02:50:32 GMT  
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
$ docker pull influxdb@sha256:3a0f316517b3c0b4051ab3a1b8e49ef241cd3958e94e4144ed04a90aa5ae77cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:a4c26ed1af08f08f1071cab53e807523588825de65280dd13bb631d23f6b074e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91128868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1248686d155dcd341a7862fc4a96bbb43c1598fe658047def8accb0e677b545a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:50:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 02:50:19 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Tue, 07 Apr 2026 02:50:19 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 07 Apr 2026 02:50:19 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 07 Apr 2026 02:50:19 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 07 Apr 2026 02:50:19 GMT
VOLUME [/var/lib/influxdb]
# Tue, 07 Apr 2026 02:50:19 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 02:50:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 02:50:19 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c3414b1d6b49c54c305584faac46aad75c67644cf4f8495e8145206d28e416`  
		Last Modified: Tue, 07 Apr 2026 01:47:02 GMT  
		Size: 24.0 MB (24038269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e85d34b701e66a799219dca5f591900454b8e8ba8b22e55dc6b2ff72124a9fe4`  
		Last Modified: Tue, 07 Apr 2026 02:50:31 GMT  
		Size: 5.1 KB (5071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e33307c25adc72d55b15ee1debb5179d4154f9a0b3c4430e902a21394d8b5f7`  
		Last Modified: Tue, 07 Apr 2026 02:50:31 GMT  
		Size: 18.6 MB (18596139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:703f775027d49b8bff40a5278a1df661d41ebfd562885bf55a2b3919082f29cc`  
		Last Modified: Tue, 07 Apr 2026 02:50:31 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2080c1f895e8c8785613562d82f5edb9e3ead41bca78f8f22228e2b24dd13af7`  
		Last Modified: Tue, 07 Apr 2026 02:50:31 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:3acfd3de8a2c8451e9414addb9db11b1617789456ec69e17d5f19cd7e2b5211c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4604273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:429f91d1d49b7431140b4df1d691dff38de64dc659a7f48755de7cbc935b011a`

```dockerfile
```

-	Layers:
	-	`sha256:49090b25955b577649c6ee63361a1bfb807b078d627ea50a7b14a2ea80c23ddf`  
		Last Modified: Tue, 07 Apr 2026 02:50:31 GMT  
		Size: 4.6 MB (4591249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff4d53a0d9f67b039998b011ad6088631d516c2b0f749c332ee906439cd1e1d9`  
		Last Modified: Tue, 07 Apr 2026 02:50:31 GMT  
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
$ docker pull influxdb@sha256:3b39bc0a11eeaa2c7af953e4499e10123b6de1de1bffe5c37464422995362205
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11.8` - linux; amd64

```console
$ docker pull influxdb@sha256:6a7bcd300ff88c1491b6f07da3c307af44f996b929f2b79541ba11d4657b16a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116186005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1b23ccbb334045d71985a1f343302bf58a4b64dfff71dfe369aa267ae8b73aa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:50:15 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 07 Apr 2026 02:50:23 GMT
ARG INFLUXDB_VERSION=1.11.8
# Tue, 07 Apr 2026 02:50:23 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:50:23 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 07 Apr 2026 02:50:23 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 07 Apr 2026 02:50:23 GMT
VOLUME [/var/lib/influxdb]
# Tue, 07 Apr 2026 02:50:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 02:50:23 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 07 Apr 2026 02:50:23 GMT
USER influxdb
# Tue, 07 Apr 2026 02:50:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 02:50:23 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c3414b1d6b49c54c305584faac46aad75c67644cf4f8495e8145206d28e416`  
		Last Modified: Tue, 07 Apr 2026 01:47:02 GMT  
		Size: 24.0 MB (24038269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e703d495b3f2846aaa942b0a03538d2dce7ac1ee61781400b8e626463d8e262`  
		Last Modified: Tue, 07 Apr 2026 02:50:36 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e604974fcaa15f2a49445b8e70fa7a3c2e277e8bf29de6de8e7b6337ac3dea8`  
		Last Modified: Tue, 07 Apr 2026 02:50:37 GMT  
		Size: 43.7 MB (43656004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3d2d21b1350355a145badb097b7dc23f1ccf4643746ecba7d0e4a9a26ebfb1`  
		Last Modified: Tue, 07 Apr 2026 02:50:36 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a9b021e817fd3671abef3e66ada790328a0f577e8d115d3bc624048c595537`  
		Last Modified: Tue, 07 Apr 2026 02:50:36 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2472fef3a3444177ff45f4cd1870ed60c8ab4b1dce8c6842da82ac7d5b6d5ec5`  
		Last Modified: Tue, 07 Apr 2026 02:50:37 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:261cfec11ac4e1ed64275f5c0101008f530a8a0230c890d023053c7dbb5ec23c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb16f25d656fdb95a08fe15b42e8935197ae25dababf5e2aaded402667ae2db`

```dockerfile
```

-	Layers:
	-	`sha256:bc50a00b512940ae6b774f3b7f2583f1096d96f14d836c7b48f3a14bb8bc9859`  
		Last Modified: Tue, 07 Apr 2026 02:50:36 GMT  
		Size: 5.1 MB (5079263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c63a23bb130c35023268a2a1fd9f5db199051deaba464584f0484b3d89e490c`  
		Last Modified: Tue, 07 Apr 2026 02:50:36 GMT  
		Size: 15.5 KB (15485 bytes)  
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
$ docker pull influxdb@sha256:d7df937902af541a5881c6b74630c1fb88f4720b8af3f99cb18ed6e11de07187
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.9-data` - linux; amd64

```console
$ docker pull influxdb@sha256:758d0d3f69f0096323f3175c2d6a29717b3b11eecfb749b7837840c5b370309d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114699664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a92f82cfbc8b66652cc67161480d67645161346e4d145da8350ef7226c6afb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:50:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 02:50:18 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Tue, 07 Apr 2026 02:50:18 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 07 Apr 2026 02:50:18 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 07 Apr 2026 02:50:18 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 07 Apr 2026 02:50:18 GMT
VOLUME [/var/lib/influxdb]
# Tue, 07 Apr 2026 02:50:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 02:50:18 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 07 Apr 2026 02:50:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 02:50:18 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c3414b1d6b49c54c305584faac46aad75c67644cf4f8495e8145206d28e416`  
		Last Modified: Tue, 07 Apr 2026 01:47:02 GMT  
		Size: 24.0 MB (24038269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ebbbcf7f8576796fe43fe91ecaedbb7c2ff572d281e353a5ba13c38202d7e1f`  
		Last Modified: Tue, 07 Apr 2026 02:50:31 GMT  
		Size: 5.1 KB (5057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:424e398f3e75be9c20e2b8dcddbfc3266a5b798b8a550984cde845a106840e52`  
		Last Modified: Tue, 07 Apr 2026 02:50:33 GMT  
		Size: 42.2 MB (42165739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82df79d5cd0fbe3cc9053c4a97b2313b149133b18c96a6db934b2bdb1c113f8e`  
		Last Modified: Tue, 07 Apr 2026 02:50:32 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084ee29046b00f5ad50972d806af952df7f2dea8c92e784252e73c9ed43cade3`  
		Last Modified: Tue, 07 Apr 2026 02:50:32 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130f74006fc5ced1c11ab0c86465e703b013619d6713f7aba00c74a68965a362`  
		Last Modified: Tue, 07 Apr 2026 02:50:33 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.9-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:f7d815fe957668e6371df3cc8f53f90c1bf534d2ef0e58446809dd4b8fdec2c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4699071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eadb685b3aaa058aed6ae472b21b59c011da8cdcc41a5697d46e7b8485550d5b`

```dockerfile
```

-	Layers:
	-	`sha256:8e23c95197d9494cefba92875437b5160307e653b4bd0a58acd12801db12484f`  
		Last Modified: Tue, 07 Apr 2026 02:50:32 GMT  
		Size: 4.7 MB (4684406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:728f093bdf28247dc942eeb4a43147522b5d4d8f7aa0a583c5d3f23e720753f5`  
		Last Modified: Tue, 07 Apr 2026 02:50:32 GMT  
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
$ docker pull influxdb@sha256:3a0f316517b3c0b4051ab3a1b8e49ef241cd3958e94e4144ed04a90aa5ae77cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.9-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:a4c26ed1af08f08f1071cab53e807523588825de65280dd13bb631d23f6b074e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91128868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1248686d155dcd341a7862fc4a96bbb43c1598fe658047def8accb0e677b545a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:50:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 02:50:19 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Tue, 07 Apr 2026 02:50:19 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 07 Apr 2026 02:50:19 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 07 Apr 2026 02:50:19 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 07 Apr 2026 02:50:19 GMT
VOLUME [/var/lib/influxdb]
# Tue, 07 Apr 2026 02:50:19 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 02:50:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 02:50:19 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c3414b1d6b49c54c305584faac46aad75c67644cf4f8495e8145206d28e416`  
		Last Modified: Tue, 07 Apr 2026 01:47:02 GMT  
		Size: 24.0 MB (24038269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e85d34b701e66a799219dca5f591900454b8e8ba8b22e55dc6b2ff72124a9fe4`  
		Last Modified: Tue, 07 Apr 2026 02:50:31 GMT  
		Size: 5.1 KB (5071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e33307c25adc72d55b15ee1debb5179d4154f9a0b3c4430e902a21394d8b5f7`  
		Last Modified: Tue, 07 Apr 2026 02:50:31 GMT  
		Size: 18.6 MB (18596139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:703f775027d49b8bff40a5278a1df661d41ebfd562885bf55a2b3919082f29cc`  
		Last Modified: Tue, 07 Apr 2026 02:50:31 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2080c1f895e8c8785613562d82f5edb9e3ead41bca78f8f22228e2b24dd13af7`  
		Last Modified: Tue, 07 Apr 2026 02:50:31 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.9-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:3acfd3de8a2c8451e9414addb9db11b1617789456ec69e17d5f19cd7e2b5211c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4604273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:429f91d1d49b7431140b4df1d691dff38de64dc659a7f48755de7cbc935b011a`

```dockerfile
```

-	Layers:
	-	`sha256:49090b25955b577649c6ee63361a1bfb807b078d627ea50a7b14a2ea80c23ddf`  
		Last Modified: Tue, 07 Apr 2026 02:50:31 GMT  
		Size: 4.6 MB (4591249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff4d53a0d9f67b039998b011ad6088631d516c2b0f749c332ee906439cd1e1d9`  
		Last Modified: Tue, 07 Apr 2026 02:50:31 GMT  
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
$ docker pull influxdb@sha256:1e968289bd1ee04f09c5cff1727409fc6b34fd445beca12b8d1a6a77409ec887
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.12` - linux; amd64

```console
$ docker pull influxdb@sha256:7b0f78db5f336d31d1784e7fa83f39e74a5b7310009f0f1ff192a144b807e80f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114656286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba2e328a1d77262fa16789b4fc11dcede04299c7fd6446765263071e2617fd1a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Apr 2026 22:49:48 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Mon, 13 Apr 2026 22:49:53 GMT
ENV INFLUXDB_VERSION=1.12.4
# Mon, 13 Apr 2026 22:49:53 GMT
ENV INFLUXDB_PR=-1
# Mon, 13 Apr 2026 22:49:53 GMT
ENV INFLUXDB_PV=1.12.4-1
# Mon, 13 Apr 2026 22:49:53 GMT
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_PV}_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Mon, 13 Apr 2026 22:49:54 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Mon, 13 Apr 2026 22:49:54 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 13 Apr 2026 22:49:54 GMT
VOLUME [/var/lib/influxdb]
# Mon, 13 Apr 2026 22:49:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 13 Apr 2026 22:49:54 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Mon, 13 Apr 2026 22:49:54 GMT
USER influxdb
# Mon, 13 Apr 2026 22:49:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 13 Apr 2026 22:49:54 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c3414b1d6b49c54c305584faac46aad75c67644cf4f8495e8145206d28e416`  
		Last Modified: Tue, 07 Apr 2026 01:47:02 GMT  
		Size: 24.0 MB (24038269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a93a89bf3044d164ae24533228fe848723b3c44177dee5040f3144731cb59e9`  
		Last Modified: Mon, 13 Apr 2026 22:50:06 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557385350afb26f1049961b9f7e9aec3f8deb7df94af64a5d6af5b465792dc37`  
		Last Modified: Mon, 13 Apr 2026 22:50:07 GMT  
		Size: 42.1 MB (42126280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4041f87ce345508b5d7f2e171e489548b53792515ff7dd7e8c9d18a639fdd32`  
		Last Modified: Mon, 13 Apr 2026 22:50:06 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd8b6379d6fd7c0628c3152fcd949fa105a079846acc27e9c6f37cc360abd16`  
		Last Modified: Mon, 13 Apr 2026 22:50:06 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e59160616b15271c85a9beb6895b1c9d53d1a72951f1cc20ab214b124e7dc81`  
		Last Modified: Mon, 13 Apr 2026 22:50:07 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:88db63322b20e72626e7ee17612b59d57ec587742188571b795c6f92da63beb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a63a143c99881ae860c04838a58a0ed53ee3e3495d5fe14b7b11c498c0d692f`

```dockerfile
```

-	Layers:
	-	`sha256:b3937dfc5dba0287a011f3441876fd4094f7b5916c46c6f89a19b950be6adc5a`  
		Last Modified: Mon, 13 Apr 2026 22:50:06 GMT  
		Size: 4.7 MB (4678133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d6f5abe40f4c21e7a4ffb306c809bbedfc76f19cad17462b5766543b7ae0b83`  
		Last Modified: Mon, 13 Apr 2026 22:50:06 GMT  
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
$ docker pull influxdb@sha256:1bb7cb1e53d43d8ee77aadca2d18ec99e34a58376d6a02075c1dc53cadb9272c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12-data` - linux; amd64

```console
$ docker pull influxdb@sha256:dc1f450e108a9944f9d8b1289468c4404ae4070f9078af1ead3a3329f7549d9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115718778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94ab92d581bcd3f0c7e589690b39705a679ed85920980fed9670da1668cfc89b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Apr 2026 22:49:58 GMT
ENV INFLUXDB_VERSION=1.12.4-c1.12.4
# Mon, 13 Apr 2026 22:49:58 GMT
ENV INFLUXDB_PR=
# Mon, 13 Apr 2026 22:49:58 GMT
ENV INFLUXDB_PV=1.12.4-c1.12.4
# Mon, 13 Apr 2026 22:49:58 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"          -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"         "influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     rm -r "influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"           "influxdb-data_${INFLUXDB_PV}_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Mon, 13 Apr 2026 22:49:58 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Mon, 13 Apr 2026 22:49:58 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 13 Apr 2026 22:49:58 GMT
VOLUME [/var/lib/influxdb]
# Mon, 13 Apr 2026 22:49:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 13 Apr 2026 22:49:58 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Mon, 13 Apr 2026 22:49:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 13 Apr 2026 22:49:58 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c3414b1d6b49c54c305584faac46aad75c67644cf4f8495e8145206d28e416`  
		Last Modified: Tue, 07 Apr 2026 01:47:02 GMT  
		Size: 24.0 MB (24038269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3ad30cc0f9885db6f3f3b9af8834a49c6770603219f0899c8d2b121cf6cd75`  
		Last Modified: Mon, 13 Apr 2026 22:50:12 GMT  
		Size: 43.2 MB (43189910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b51b01a2ef33a85cd8edbca066d9077822df136af91cb6971a800ff131c1d3`  
		Last Modified: Mon, 13 Apr 2026 22:50:10 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b386d41662c8a1289ff94f784995f6bc7d20e2659612891b88325f6e0ce041`  
		Last Modified: Mon, 13 Apr 2026 22:50:10 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6862c17b4bebcee9f221229f33be2b8ac982dc5d0fd5948d8ef92064fca5f9f`  
		Last Modified: Mon, 13 Apr 2026 22:50:10 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:a323cb246451e75e29967f9d1defcaa49773f6a25b58859e305cb3c3e23eac8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4707277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae13ff8cded04988bd0ab05649dbbf083dd16bb2f83d6ebf9a53eaca28b85ac2`

```dockerfile
```

-	Layers:
	-	`sha256:9c371c2fe64f56971440a22d98001dec89849263c3fb9dc70f789d0b05416005`  
		Last Modified: Mon, 13 Apr 2026 22:50:11 GMT  
		Size: 4.7 MB (4693123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cc70504e235817a2900902046909c763540085aaf1d0029847445180cd92d57`  
		Last Modified: Mon, 13 Apr 2026 22:50:10 GMT  
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
$ docker pull influxdb@sha256:f342f786f4676fd37b672f9e5ed587a67d2743bf5b261418d7bf2f5528b7fdad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:69850756eb4fa42a326833d36958ee6fe52bc688caa6a905eaa348e4948b7bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91912837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b46ed6e9d38d9dd2ed2dbd7d545899f7b54641fbc4954ee4b97e9ffd380ae51a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Apr 2026 22:50:11 GMT
ENV INFLUXDB_VERSION=1.12.4-c1.12.4
# Mon, 13 Apr 2026 22:50:11 GMT
ENV INFLUXDB_PR=
# Mon, 13 Apr 2026 22:50:11 GMT
ENV INFLUXDB_PV=1.12.4-c1.12.4
# Mon, 13 Apr 2026 22:50:11 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"          -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"         "influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     rm -r "influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"           "influxdb-meta_${INFLUXDB_PV}_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Mon, 13 Apr 2026 22:50:11 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Mon, 13 Apr 2026 22:50:11 GMT
EXPOSE map[8091/tcp:{}]
# Mon, 13 Apr 2026 22:50:11 GMT
VOLUME [/var/lib/influxdb]
# Mon, 13 Apr 2026 22:50:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 13 Apr 2026 22:50:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 13 Apr 2026 22:50:11 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c3414b1d6b49c54c305584faac46aad75c67644cf4f8495e8145206d28e416`  
		Last Modified: Tue, 07 Apr 2026 01:47:02 GMT  
		Size: 24.0 MB (24038269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e0f7ee8b658eb6c5de752b1bd460cda5d8872f4ea0a2df909f45efd8e90456`  
		Last Modified: Mon, 13 Apr 2026 22:50:20 GMT  
		Size: 19.4 MB (19385177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3254a32e0e98355d9f943f389fe638e71c63cbd4508958193df0c491d009c2bb`  
		Last Modified: Mon, 13 Apr 2026 22:50:19 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5468d99e6cd4392f3f013ce29f74b2ada303391e9986578bd2f0c1aead188e56`  
		Last Modified: Mon, 13 Apr 2026 22:50:20 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:6b9f9dccb6d0521215ede40cab59ce3c7c223552881b94551ffdcf7c98f6be2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4605855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3661736a8ccd815549acaeaf7c0e080ab67f781d78da19fd935aa8dfcc9cf08`

```dockerfile
```

-	Layers:
	-	`sha256:e0979c1b4e7584dc7714f4cf6efd676c9bfecb7cf0b8d78005cf161d1f8245d3`  
		Last Modified: Mon, 13 Apr 2026 22:50:20 GMT  
		Size: 4.6 MB (4593191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70e1dcac49afc270d8058e7d8ea06e41fa0dd32457c9e2fc4c0c9cbfcd00ea55`  
		Last Modified: Mon, 13 Apr 2026 22:50:20 GMT  
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
$ docker pull influxdb@sha256:1e968289bd1ee04f09c5cff1727409fc6b34fd445beca12b8d1a6a77409ec887
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.12.4` - linux; amd64

```console
$ docker pull influxdb@sha256:7b0f78db5f336d31d1784e7fa83f39e74a5b7310009f0f1ff192a144b807e80f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114656286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba2e328a1d77262fa16789b4fc11dcede04299c7fd6446765263071e2617fd1a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Apr 2026 22:49:48 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Mon, 13 Apr 2026 22:49:53 GMT
ENV INFLUXDB_VERSION=1.12.4
# Mon, 13 Apr 2026 22:49:53 GMT
ENV INFLUXDB_PR=-1
# Mon, 13 Apr 2026 22:49:53 GMT
ENV INFLUXDB_PV=1.12.4-1
# Mon, 13 Apr 2026 22:49:53 GMT
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_PV}_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Mon, 13 Apr 2026 22:49:54 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Mon, 13 Apr 2026 22:49:54 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 13 Apr 2026 22:49:54 GMT
VOLUME [/var/lib/influxdb]
# Mon, 13 Apr 2026 22:49:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 13 Apr 2026 22:49:54 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Mon, 13 Apr 2026 22:49:54 GMT
USER influxdb
# Mon, 13 Apr 2026 22:49:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 13 Apr 2026 22:49:54 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c3414b1d6b49c54c305584faac46aad75c67644cf4f8495e8145206d28e416`  
		Last Modified: Tue, 07 Apr 2026 01:47:02 GMT  
		Size: 24.0 MB (24038269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a93a89bf3044d164ae24533228fe848723b3c44177dee5040f3144731cb59e9`  
		Last Modified: Mon, 13 Apr 2026 22:50:06 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557385350afb26f1049961b9f7e9aec3f8deb7df94af64a5d6af5b465792dc37`  
		Last Modified: Mon, 13 Apr 2026 22:50:07 GMT  
		Size: 42.1 MB (42126280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4041f87ce345508b5d7f2e171e489548b53792515ff7dd7e8c9d18a639fdd32`  
		Last Modified: Mon, 13 Apr 2026 22:50:06 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd8b6379d6fd7c0628c3152fcd949fa105a079846acc27e9c6f37cc360abd16`  
		Last Modified: Mon, 13 Apr 2026 22:50:06 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e59160616b15271c85a9beb6895b1c9d53d1a72951f1cc20ab214b124e7dc81`  
		Last Modified: Mon, 13 Apr 2026 22:50:07 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.4` - unknown; unknown

```console
$ docker pull influxdb@sha256:88db63322b20e72626e7ee17612b59d57ec587742188571b795c6f92da63beb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a63a143c99881ae860c04838a58a0ed53ee3e3495d5fe14b7b11c498c0d692f`

```dockerfile
```

-	Layers:
	-	`sha256:b3937dfc5dba0287a011f3441876fd4094f7b5916c46c6f89a19b950be6adc5a`  
		Last Modified: Mon, 13 Apr 2026 22:50:06 GMT  
		Size: 4.7 MB (4678133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d6f5abe40f4c21e7a4ffb306c809bbedfc76f19cad17462b5766543b7ae0b83`  
		Last Modified: Mon, 13 Apr 2026 22:50:06 GMT  
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
$ docker pull influxdb@sha256:1bb7cb1e53d43d8ee77aadca2d18ec99e34a58376d6a02075c1dc53cadb9272c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12.4-data` - linux; amd64

```console
$ docker pull influxdb@sha256:dc1f450e108a9944f9d8b1289468c4404ae4070f9078af1ead3a3329f7549d9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115718778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94ab92d581bcd3f0c7e589690b39705a679ed85920980fed9670da1668cfc89b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Apr 2026 22:49:58 GMT
ENV INFLUXDB_VERSION=1.12.4-c1.12.4
# Mon, 13 Apr 2026 22:49:58 GMT
ENV INFLUXDB_PR=
# Mon, 13 Apr 2026 22:49:58 GMT
ENV INFLUXDB_PV=1.12.4-c1.12.4
# Mon, 13 Apr 2026 22:49:58 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"          -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"         "influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     rm -r "influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"           "influxdb-data_${INFLUXDB_PV}_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Mon, 13 Apr 2026 22:49:58 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Mon, 13 Apr 2026 22:49:58 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 13 Apr 2026 22:49:58 GMT
VOLUME [/var/lib/influxdb]
# Mon, 13 Apr 2026 22:49:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 13 Apr 2026 22:49:58 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Mon, 13 Apr 2026 22:49:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 13 Apr 2026 22:49:58 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c3414b1d6b49c54c305584faac46aad75c67644cf4f8495e8145206d28e416`  
		Last Modified: Tue, 07 Apr 2026 01:47:02 GMT  
		Size: 24.0 MB (24038269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3ad30cc0f9885db6f3f3b9af8834a49c6770603219f0899c8d2b121cf6cd75`  
		Last Modified: Mon, 13 Apr 2026 22:50:12 GMT  
		Size: 43.2 MB (43189910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b51b01a2ef33a85cd8edbca066d9077822df136af91cb6971a800ff131c1d3`  
		Last Modified: Mon, 13 Apr 2026 22:50:10 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b386d41662c8a1289ff94f784995f6bc7d20e2659612891b88325f6e0ce041`  
		Last Modified: Mon, 13 Apr 2026 22:50:10 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6862c17b4bebcee9f221229f33be2b8ac982dc5d0fd5948d8ef92064fca5f9f`  
		Last Modified: Mon, 13 Apr 2026 22:50:10 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.4-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:a323cb246451e75e29967f9d1defcaa49773f6a25b58859e305cb3c3e23eac8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4707277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae13ff8cded04988bd0ab05649dbbf083dd16bb2f83d6ebf9a53eaca28b85ac2`

```dockerfile
```

-	Layers:
	-	`sha256:9c371c2fe64f56971440a22d98001dec89849263c3fb9dc70f789d0b05416005`  
		Last Modified: Mon, 13 Apr 2026 22:50:11 GMT  
		Size: 4.7 MB (4693123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cc70504e235817a2900902046909c763540085aaf1d0029847445180cd92d57`  
		Last Modified: Mon, 13 Apr 2026 22:50:10 GMT  
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
$ docker pull influxdb@sha256:f342f786f4676fd37b672f9e5ed587a67d2743bf5b261418d7bf2f5528b7fdad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12.4-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:69850756eb4fa42a326833d36958ee6fe52bc688caa6a905eaa348e4948b7bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91912837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b46ed6e9d38d9dd2ed2dbd7d545899f7b54641fbc4954ee4b97e9ffd380ae51a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Apr 2026 22:50:11 GMT
ENV INFLUXDB_VERSION=1.12.4-c1.12.4
# Mon, 13 Apr 2026 22:50:11 GMT
ENV INFLUXDB_PR=
# Mon, 13 Apr 2026 22:50:11 GMT
ENV INFLUXDB_PV=1.12.4-c1.12.4
# Mon, 13 Apr 2026 22:50:11 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"          -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"         "influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     rm -r "influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"           "influxdb-meta_${INFLUXDB_PV}_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Mon, 13 Apr 2026 22:50:11 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Mon, 13 Apr 2026 22:50:11 GMT
EXPOSE map[8091/tcp:{}]
# Mon, 13 Apr 2026 22:50:11 GMT
VOLUME [/var/lib/influxdb]
# Mon, 13 Apr 2026 22:50:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 13 Apr 2026 22:50:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 13 Apr 2026 22:50:11 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c3414b1d6b49c54c305584faac46aad75c67644cf4f8495e8145206d28e416`  
		Last Modified: Tue, 07 Apr 2026 01:47:02 GMT  
		Size: 24.0 MB (24038269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e0f7ee8b658eb6c5de752b1bd460cda5d8872f4ea0a2df909f45efd8e90456`  
		Last Modified: Mon, 13 Apr 2026 22:50:20 GMT  
		Size: 19.4 MB (19385177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3254a32e0e98355d9f943f389fe638e71c63cbd4508958193df0c491d009c2bb`  
		Last Modified: Mon, 13 Apr 2026 22:50:19 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5468d99e6cd4392f3f013ce29f74b2ada303391e9986578bd2f0c1aead188e56`  
		Last Modified: Mon, 13 Apr 2026 22:50:20 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.4-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:6b9f9dccb6d0521215ede40cab59ce3c7c223552881b94551ffdcf7c98f6be2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4605855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3661736a8ccd815549acaeaf7c0e080ab67f781d78da19fd935aa8dfcc9cf08`

```dockerfile
```

-	Layers:
	-	`sha256:e0979c1b4e7584dc7714f4cf6efd676c9bfecb7cf0b8d78005cf161d1f8245d3`  
		Last Modified: Mon, 13 Apr 2026 22:50:20 GMT  
		Size: 4.6 MB (4593191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70e1dcac49afc270d8058e7d8ea06e41fa0dd32457c9e2fc4c0c9cbfcd00ea55`  
		Last Modified: Mon, 13 Apr 2026 22:50:20 GMT  
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
$ docker pull influxdb@sha256:71f2bce68b47a3e26c1ed38f7480a9372b008ba9b7c8a35cb2c913d3102d377f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2` - linux; amd64

```console
$ docker pull influxdb@sha256:e532279db2ffef29e7eab17961841291927e228f2703bafd9255023d5480d056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107241320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:759ec9162770032bdcd5f75d588d4bdd548f5ea87abdbd151e3711dfc50cf4f4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:41:32 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:41:33 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 22 Apr 2026 01:41:33 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 22 Apr 2026 01:41:35 GMT
ENV GOSU_VER=1.19
# Wed, 22 Apr 2026 01:41:35 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Wed, 22 Apr 2026 01:41:35 GMT
ENV INFLUXDB_VERSION=2.8.0
# Wed, 22 Apr 2026 01:41:35 GMT
ENV INFLUXDB_PR=-2
# Wed, 22 Apr 2026 01:41:35 GMT
ENV INFLUXDB_PV=2.8.0-2
# Wed, 22 Apr 2026 01:41:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 22 Apr 2026 01:41:37 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 22 Apr 2026 01:41:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 22 Apr 2026 01:41:38 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 22 Apr 2026 01:41:38 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 22 Apr 2026 01:41:39 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 22 Apr 2026 01:41:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 01:41:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 01:41:39 GMT
CMD ["influxd"]
# Wed, 22 Apr 2026 01:41:39 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 22 Apr 2026 01:41:39 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 22 Apr 2026 01:41:39 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 22 Apr 2026 01:41:39 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 22 Apr 2026 01:41:39 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c791747626e2412d3502fd05d4fac3fffd42cdd349ef47e7884ae03da2dbef`  
		Last Modified: Wed, 22 Apr 2026 01:41:50 GMT  
		Size: 9.8 MB (9798990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2ee315242c36b9238a9f0e643e4281f93755787bc77c2b111e887c7653da6d`  
		Last Modified: Wed, 22 Apr 2026 01:41:50 GMT  
		Size: 6.2 MB (6156971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844de845c21c0436926d498f8ebd39d4698a948c5fb968d09c52f49a33e30c54`  
		Last Modified: Wed, 22 Apr 2026 01:41:50 GMT  
		Size: 3.2 KB (3229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41868ae9fbbede4b0f6bdbd0af43852ad245ea7c610f402e2220bd8847c6b729`  
		Last Modified: Wed, 22 Apr 2026 01:41:50 GMT  
		Size: 811.5 KB (811478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4da638bcf081222b7033e64890358a3f551ee2a1060e73d60775bb4cce4888a`  
		Last Modified: Wed, 22 Apr 2026 01:41:52 GMT  
		Size: 50.5 MB (50451802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4fea9ea328927d53fc80fd2b38cd6f7a8dffe1745ef87a3a3159347389e9f2e`  
		Last Modified: Wed, 22 Apr 2026 01:41:52 GMT  
		Size: 11.8 MB (11775870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ddc1c71a8a7f9d5167a61bdc437327b756110396f40992677ef72157e08775`  
		Last Modified: Wed, 22 Apr 2026 01:41:51 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e55f58da73fd395ac05c086627b0e088853dbeb76527b853bdcd5d76adddca`  
		Last Modified: Wed, 22 Apr 2026 01:41:52 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70d15b5d427c0540fea4882696f4da3a2a6787732964d6542233dc71e311537`  
		Last Modified: Wed, 22 Apr 2026 01:41:53 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:8938d3511aaa20b791700f8a2e5817323627e5360965a4f98d6140dc066ff3ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b027564a5f64ce815d5a5005299ddd5ea69b030647832e23bbc5a547bd4809b1`

```dockerfile
```

-	Layers:
	-	`sha256:ec06b068a4d9e7482bd3578659a536954e9c49b80b862002a0c69866d0d7e1f6`  
		Last Modified: Wed, 22 Apr 2026 01:41:50 GMT  
		Size: 2.9 MB (2934237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a481924326704569284e4ea29a85d10c6460d99223990fd6292868077c45765`  
		Last Modified: Wed, 22 Apr 2026 01:41:50 GMT  
		Size: 33.6 KB (33621 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:4749be1eb7cb5803e7fe7c7abfb0e4a868c3017bc903299d3526cbfc5ff85379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103640890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a3d056402f328a5ae7b1e564dedf01aa4df264f034fedd872385e3bb96accdd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:44:39 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:40 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 22 Apr 2026 01:44:40 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 22 Apr 2026 01:44:42 GMT
ENV GOSU_VER=1.19
# Wed, 22 Apr 2026 01:44:42 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Wed, 22 Apr 2026 01:44:42 GMT
ENV INFLUXDB_VERSION=2.8.0
# Wed, 22 Apr 2026 01:44:42 GMT
ENV INFLUXDB_PR=-2
# Wed, 22 Apr 2026 01:44:42 GMT
ENV INFLUXDB_PV=2.8.0-2
# Wed, 22 Apr 2026 01:44:46 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 22 Apr 2026 01:44:46 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 22 Apr 2026 01:44:47 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 22 Apr 2026 01:44:47 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 22 Apr 2026 01:44:47 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 22 Apr 2026 01:44:47 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 22 Apr 2026 01:44:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 01:44:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 01:44:47 GMT
CMD ["influxd"]
# Wed, 22 Apr 2026 01:44:47 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 22 Apr 2026 01:44:47 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 22 Apr 2026 01:44:47 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 22 Apr 2026 01:44:47 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 22 Apr 2026 01:44:47 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ddf21f4abba315d4e405b0b7ca7380c3b03e816eea5fd8219965fed687ac4f`  
		Last Modified: Wed, 22 Apr 2026 01:44:58 GMT  
		Size: 9.6 MB (9628094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c560fbc3a39b1a11f3127f89d636cc2517753a085eaf3afbf4f928d215e86c8b`  
		Last Modified: Wed, 22 Apr 2026 01:44:58 GMT  
		Size: 5.8 MB (5790421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f267c0a54c465bfc52d652cfab1ac62dfafe3e42649811dab584056706e1db51`  
		Last Modified: Wed, 22 Apr 2026 01:44:57 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01fd1f2188e7bc5e9738f5ddde7c01d895d6f100721c3eca47f0448d1c4921c`  
		Last Modified: Wed, 22 Apr 2026 01:44:57 GMT  
		Size: 766.4 KB (766364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9245aa8cd37661f6b67a498039d6cc9574d07919bf07b31b7ce44f594b552802`  
		Last Modified: Wed, 22 Apr 2026 01:45:00 GMT  
		Size: 48.2 MB (48229530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17a6763a2749ecf5870e80619513e273d0e1a10c00743d701c94e21be334b3f`  
		Last Modified: Wed, 22 Apr 2026 01:44:59 GMT  
		Size: 11.1 MB (11100415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69e2b2742458b735c0dc03bd705017e3e0d65e05db242e409d99a66ce5e26a6`  
		Last Modified: Wed, 22 Apr 2026 01:44:59 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95186bc453fe3657a6cd1bbd5b28c20dcd8355d9ba05951c3ec5b6c00a573e4`  
		Last Modified: Wed, 22 Apr 2026 01:44:59 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f382dd5f3b374f7003cd1b28910bd54c378e293152f8e5a1d9870d5e406147a`  
		Last Modified: Wed, 22 Apr 2026 01:45:00 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:439f6863a26e4a35763bda86f99511c908da7c6f97b9d593c7c3a1094666c347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9196348dc3b5c505a243f0014bdc51b8210eb9a0d606b67eef4fbb93c121620`

```dockerfile
```

-	Layers:
	-	`sha256:219a4fdfdfad1438a2554524a5be2b3f344b6802c2cc229aba88bf6973f82621`  
		Last Modified: Wed, 22 Apr 2026 01:44:57 GMT  
		Size: 2.9 MB (2933717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79c489575215cf3dd7f3007ba6ae0f8970239be059d7c86d56c59b83c70b12b4`  
		Last Modified: Wed, 22 Apr 2026 01:44:57 GMT  
		Size: 33.8 KB (33815 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2-alpine`

```console
$ docker pull influxdb@sha256:4f90d40c00193d91889ad872c39a586a011db4ac4d1a766e248d9cbbcc6cec3e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:ef8bad9a5c5f604e1a139b7b99c452bc9cb62affdcb9f11afad1b2e5c20c45a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81923288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70540d47f741606ec70538d2489a54d267d7fd74f4b276a176e53ad8c2efacf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:29:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 00:29:56 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:29:56 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 17 Apr 2026 00:29:56 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Fri, 17 Apr 2026 00:30:00 GMT
ENV INFLUXDB_VERSION=2.8.0
# Fri, 17 Apr 2026 00:30:00 GMT
ENV INFLUXDB_PR=-2
# Fri, 17 Apr 2026 00:30:00 GMT
ENV INFLUXDB_PV=2.8.0-2
# Fri, 17 Apr 2026 00:30:00 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Fri, 17 Apr 2026 00:30:00 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Fri, 17 Apr 2026 00:30:01 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 17 Apr 2026 00:30:02 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 17 Apr 2026 00:30:02 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 17 Apr 2026 00:30:02 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 17 Apr 2026 00:30:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:30:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:30:02 GMT
CMD ["influxd"]
# Fri, 17 Apr 2026 00:30:02 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 17 Apr 2026 00:30:02 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 17 Apr 2026 00:30:02 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 17 Apr 2026 00:30:02 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 17 Apr 2026 00:30:02 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef79b6f3d2e846d055a2620421abd1ea83d1a2a5c141a54104accb233ed0ce59`  
		Last Modified: Fri, 17 Apr 2026 00:30:12 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd92961fcb2124af0c103187cef2632786c556874b686090cae17de4638ed98`  
		Last Modified: Fri, 17 Apr 2026 00:30:12 GMT  
		Size: 9.9 MB (9883791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21ab53b0f55c96701571d89ea72fe10e15495a5399811272d01416b505d8848`  
		Last Modified: Fri, 17 Apr 2026 00:30:12 GMT  
		Size: 6.2 MB (6156985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788c81c58d331aa59131e00c438630fb5aefff8373c89b0adc66d24f393ae7cb`  
		Last Modified: Fri, 17 Apr 2026 00:30:12 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1fff6940a3878ed3aee43c506ecf21d4bce29f9e7388a17ce375c9b9c0a44cf`  
		Last Modified: Fri, 17 Apr 2026 00:30:15 GMT  
		Size: 50.5 MB (50451820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6c03c0be2850f9c82b37631d6cba13fdd3f1e632d3643edc54d2cdc6edf2c9`  
		Last Modified: Fri, 17 Apr 2026 00:30:13 GMT  
		Size: 11.8 MB (11775863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aea5f86be29cb56a759d7142f5a9b62bfd6ed99d100b921dd3a33e4ce9314a5`  
		Last Modified: Fri, 17 Apr 2026 00:30:13 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ef07b04bbe77eb925cb81d0e6082ce24328e0d2c296d61c460e11aa33b6b3a`  
		Last Modified: Fri, 17 Apr 2026 00:30:14 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ddd87b55db792237d8b7cd099de585015d86816d1215b2f57c4dd5011ba91e`  
		Last Modified: Fri, 17 Apr 2026 00:30:15 GMT  
		Size: 6.3 KB (6283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:40fca214b400941be68a739f6f59448a6e931f730682c1d89026fee13fe21c34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **946.1 KB (946058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7f880a5909c565d62181a36572e16dac17e9bb0131551dfa514d962d26c4a97`

```dockerfile
```

-	Layers:
	-	`sha256:33f778c6f613bedfa5d2ec41b08b10f6bf6ce196ef899601b0ec66f7637095f3`  
		Last Modified: Fri, 17 Apr 2026 00:30:12 GMT  
		Size: 915.2 KB (915211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:629ffea1f9f8527114e2ed5a812a800fe7b6e1a1947e4b14a6b8302f319cb11d`  
		Last Modified: Fri, 17 Apr 2026 00:30:12 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:1d6e285b1a5e3fa23695d08c8586d0d17c004443a83a93e22a40d9f7c449227c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.0 MB (78965173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ba6389eb739af52c14de9f6ed96efacfbe53dccc3e41f42ab1f51fef176da67`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:13 GMT
ADD alpine-minirootfs-3.21.7-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:13 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:31:02 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 00:31:03 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:31:03 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 17 Apr 2026 00:31:04 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Fri, 17 Apr 2026 00:31:07 GMT
ENV INFLUXDB_VERSION=2.8.0
# Fri, 17 Apr 2026 00:31:07 GMT
ENV INFLUXDB_PR=-2
# Fri, 17 Apr 2026 00:31:07 GMT
ENV INFLUXDB_PV=2.8.0-2
# Fri, 17 Apr 2026 00:31:07 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Fri, 17 Apr 2026 00:31:07 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Fri, 17 Apr 2026 00:31:07 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 17 Apr 2026 00:31:08 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 17 Apr 2026 00:31:08 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 17 Apr 2026 00:31:08 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 17 Apr 2026 00:31:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:31:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:31:08 GMT
CMD ["influxd"]
# Fri, 17 Apr 2026 00:31:08 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 17 Apr 2026 00:31:08 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 17 Apr 2026 00:31:08 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 17 Apr 2026 00:31:08 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 17 Apr 2026 00:31:08 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:2dd7199cff98a7400e801cbfad6de906972a4e3dd0a749d4c1b80f5a1e3e4108`  
		Last Modified: Thu, 16 Apr 2026 05:32:50 GMT  
		Size: 4.0 MB (3994465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f652e0c01e29334dc1fe16c1d56127042156c3a64857b4a0ead43d3986f7986`  
		Last Modified: Fri, 17 Apr 2026 00:31:17 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5ddaea2126344e5b11cf5e6c97cd44d5b59a15fabcb438bb0a343fd2c1b7162`  
		Last Modified: Fri, 17 Apr 2026 00:31:18 GMT  
		Size: 9.8 MB (9842397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9394ce182bd0c5ee862a0d2428947e1a0d0fc3da081624b53bb5b05e37972f48`  
		Last Modified: Fri, 17 Apr 2026 00:31:17 GMT  
		Size: 5.8 MB (5790430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98541319cbb33b6799c13cddcd9cd7e00fe5295fea9954da3eaa7af2a1be8ca9`  
		Last Modified: Fri, 17 Apr 2026 00:31:17 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872f29647bbd3f39d47cc2a6b1b76f958b61aeb29480eec96b42c03288cd1472`  
		Last Modified: Fri, 17 Apr 2026 00:31:20 GMT  
		Size: 48.2 MB (48229511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff3598b437a8492690885c52bd82ed6d9ba85af743856cdcdc03e23cff14b84b`  
		Last Modified: Fri, 17 Apr 2026 00:31:19 GMT  
		Size: 11.1 MB (11100414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca69b2befa8351ec86c62df1caca82193562d274be054f00c148c6b5f5ba67b`  
		Last Modified: Fri, 17 Apr 2026 00:31:18 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba50550e7b2ebf586c1c93af205b4fb509ff55bfeda64342a548be9f7eb0b4d`  
		Last Modified: Fri, 17 Apr 2026 00:31:19 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8195a95763ebcb79e75c6db51ef9341b1678f6bd5070f114326209a91fff3bb8`  
		Last Modified: Fri, 17 Apr 2026 00:31:20 GMT  
		Size: 6.3 KB (6284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:866fdba0f42c46c21ba2c8d62ea1a6c90a46ca6d38e54989b009617072a3b43c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **945.5 KB (945503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48090246a2f4e0d9530f4b14c374ee2497817d1ef5d6807100cc1f963980061`

```dockerfile
```

-	Layers:
	-	`sha256:7f3a296bce432225eae41d3f9ad0d93e77867c28796a18dbaf6693ac05624f1b`  
		Last Modified: Fri, 17 Apr 2026 00:31:17 GMT  
		Size: 914.5 KB (914462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0eb74c7252a3cb8f2dd15f0ae328f0107f804876760828392c2573c155759432`  
		Last Modified: Fri, 17 Apr 2026 00:31:17 GMT  
		Size: 31.0 KB (31041 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7`

```console
$ docker pull influxdb@sha256:587b7878881812cf6e5481f8889f53f210180fd6790e6c3ddaa0b456dcffd5ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7` - linux; amd64

```console
$ docker pull influxdb@sha256:3b4f54f583cd5d6d31f4642cad69a69e3d50b79531dd972801a1dc524754d2fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157236305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb98f8cbec6871d05f08b60625b7b174b3d2b26ac6f1ab0ab98f3a34c3a833a5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:41:20 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:41:21 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 22 Apr 2026 01:41:21 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 22 Apr 2026 01:41:23 GMT
ENV GOSU_VER=1.16
# Wed, 22 Apr 2026 01:41:23 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Wed, 22 Apr 2026 01:41:23 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 22 Apr 2026 01:41:26 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Wed, 22 Apr 2026 01:41:26 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 22 Apr 2026 01:41:27 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 22 Apr 2026 01:41:27 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 22 Apr 2026 01:41:27 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 22 Apr 2026 01:41:27 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 22 Apr 2026 01:41:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 01:41:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 01:41:27 GMT
CMD ["influxd"]
# Wed, 22 Apr 2026 01:41:27 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 22 Apr 2026 01:41:27 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 22 Apr 2026 01:41:27 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 22 Apr 2026 01:41:27 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 22 Apr 2026 01:41:27 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29f07cc9ba59ef00f61011edce588e98164ffd1b6e7ac7af9be3a24113d75d6`  
		Last Modified: Wed, 22 Apr 2026 01:41:43 GMT  
		Size: 9.8 MB (9799042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe897ac537e2db135be8699f8cf64f46db637043a940e8c738a8d53ffaacb3c`  
		Last Modified: Wed, 22 Apr 2026 01:41:43 GMT  
		Size: 6.2 MB (6156974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd711476a81735c2f5896d28216c672eb9d67057747bf0ed8dec36d20c415d0`  
		Last Modified: Wed, 22 Apr 2026 01:41:42 GMT  
		Size: 3.2 KB (3228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364f823b105ccbba816839ddba9dbbb2c325e426881b8ed79bbcc960eb9bcf77`  
		Last Modified: Wed, 22 Apr 2026 01:41:42 GMT  
		Size: 1.0 MB (1012039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d5b7cd45e9439ced8ca3a6818858c500e2d5e8a96bde07ad7925ce4b58dd29`  
		Last Modified: Wed, 22 Apr 2026 01:41:46 GMT  
		Size: 100.2 MB (100246163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab0e7ce3787869b9101a59584e44a71d0b17d86c274c5b64ffe8ae829d9ee86`  
		Last Modified: Wed, 22 Apr 2026 01:41:45 GMT  
		Size: 11.8 MB (11775880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cdf38892ce537a1ae82212d0f408af180c67c5814db50b32ed9d10898b75355`  
		Last Modified: Wed, 22 Apr 2026 01:41:44 GMT  
		Size: 207.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118346765087f08818eb0b37709db078a185e7240d28ef9d5920fa0c9f9c6949`  
		Last Modified: Wed, 22 Apr 2026 01:41:44 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a679d3bb179326735cf604f6f11914653be7426528d2ec498ea5010ca50e4d53`  
		Last Modified: Wed, 22 Apr 2026 01:41:45 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:ffb9fc1043235069d2dfe2f762c0ce3ef34e43a52d6466f9f74f575668f2f6b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3014384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d682d84083d3451c9d12fee9172da41d90e9ba979913f86376ef4ca4c6c225`

```dockerfile
```

-	Layers:
	-	`sha256:6a680b1575c8d06b1e037fbb4e14b707e21703dfaf8443cd6a244f54a36935d7`  
		Last Modified: Wed, 22 Apr 2026 01:41:42 GMT  
		Size: 3.0 MB (2981484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bff474574493b8406c4984e87e8d3457858e1a2d646c812acee044494fcdcce0`  
		Last Modified: Wed, 22 Apr 2026 01:41:42 GMT  
		Size: 32.9 KB (32900 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:f180153db00fb65bc9447d1f1ea36588a846de7e36863b34b24d752fc428189d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151625536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d437663aa45683e3aea1381347d0e377293f50afde2073da22aaa569ba39b33`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:44:36 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 22 Apr 2026 01:44:37 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 22 Apr 2026 01:44:39 GMT
ENV GOSU_VER=1.16
# Wed, 22 Apr 2026 01:44:39 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Wed, 22 Apr 2026 01:44:39 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 22 Apr 2026 01:44:44 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Wed, 22 Apr 2026 01:44:44 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 22 Apr 2026 01:44:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 22 Apr 2026 01:44:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 22 Apr 2026 01:44:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 22 Apr 2026 01:44:45 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 22 Apr 2026 01:44:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 01:44:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 01:44:45 GMT
CMD ["influxd"]
# Wed, 22 Apr 2026 01:44:45 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 22 Apr 2026 01:44:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 22 Apr 2026 01:44:45 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 22 Apr 2026 01:44:45 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 22 Apr 2026 01:44:45 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387a1587236ec51fe27e6a475764b3582ca81353283861373f191110999fb121`  
		Last Modified: Wed, 22 Apr 2026 01:44:59 GMT  
		Size: 9.6 MB (9628061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c15338b943524f08bd8534fe024b05145b98eb00da062b780858e7c8cc6a7c`  
		Last Modified: Wed, 22 Apr 2026 01:44:59 GMT  
		Size: 5.8 MB (5790416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f237dc5b10389a57e18783d12d9511d7a73d0747921e369690b1f992522a9f2`  
		Last Modified: Wed, 22 Apr 2026 01:44:59 GMT  
		Size: 3.2 KB (3228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b254d000bb8f070b191a46d14398fb24e28b1d81bf0780fe6148b7d43bde0ef6`  
		Last Modified: Wed, 22 Apr 2026 01:44:59 GMT  
		Size: 938.9 KB (938883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef001e56afeb60a74634dfc64abd229fb5fe1abfc104b537a2df21af52905b61`  
		Last Modified: Wed, 22 Apr 2026 01:45:03 GMT  
		Size: 96.0 MB (96041716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158d254574795ce20ded8a85d81993007ccab1eed2046cdc69e3ea4731b76c9a`  
		Last Modified: Wed, 22 Apr 2026 01:45:01 GMT  
		Size: 11.1 MB (11100388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf5b36ec252a2d1d18588347441c364f7d7da469d19c615ee44e03824bd0617`  
		Last Modified: Wed, 22 Apr 2026 01:45:01 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35afbdc6acb5fe6669f56074f523754d15668082dbe1ac6ca233c820491cca77`  
		Last Modified: Wed, 22 Apr 2026 01:45:01 GMT  
		Size: 235.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feca5e9a9c1c85f1293916d86f1f12632f018bffa159156b4cb7b8f645000abc`  
		Last Modified: Wed, 22 Apr 2026 01:45:02 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:e4d8202ac8a034aeb13d26f67181f8574e36990f929fa5522cd8de2c4c5c8a78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3013747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62a0d37667b3073fa90dba998ed16d02df4e10be2dc8f481a50c5f8a4081acb5`

```dockerfile
```

-	Layers:
	-	`sha256:7f5810e2f1bc0468bab32e6ff2fef771b7fba0d5bfab2c376cc7c81aa49cb81a`  
		Last Modified: Wed, 22 Apr 2026 01:44:59 GMT  
		Size: 3.0 MB (2980688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24e27dab536ca69ef5cb533f615eafe6c7aea731b8856f24961a24ddc8acece1`  
		Last Modified: Wed, 22 Apr 2026 01:44:59 GMT  
		Size: 33.1 KB (33059 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7-alpine`

```console
$ docker pull influxdb@sha256:cf6476ce69eb017522fce67a5e69670d79ce05322b9271accfb9a9ca39c97b07
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:a63f1abb587b40e272a34684502f813b11534f2796a6e180a390591ff19d5bf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81592338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d07629cd20c54eca2bf9fa79ae7ab852a8920fadf113b7dd4a87622f5ea84a0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:29:52 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 00:29:53 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:29:54 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 17 Apr 2026 00:29:54 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Fri, 17 Apr 2026 00:29:59 GMT
ENV INFLUXDB_VERSION=2.7.12
# Fri, 17 Apr 2026 00:29:59 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Fri, 17 Apr 2026 00:29:59 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Fri, 17 Apr 2026 00:30:00 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 17 Apr 2026 00:30:00 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 17 Apr 2026 00:30:00 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 17 Apr 2026 00:30:00 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 17 Apr 2026 00:30:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:30:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:30:00 GMT
CMD ["influxd"]
# Fri, 17 Apr 2026 00:30:00 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 17 Apr 2026 00:30:00 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 17 Apr 2026 00:30:00 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 17 Apr 2026 00:30:00 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 17 Apr 2026 00:30:00 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34dc1d883690517ae685fc63bb161f7fc336f5db7ff9d689cf1e477cad7cb500`  
		Last Modified: Fri, 17 Apr 2026 00:30:09 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13158ef7e36a22d4b2839dab788ab8ddf34a3f6cfec26bb5c6fc4b3b60dfb21e`  
		Last Modified: Fri, 17 Apr 2026 00:30:09 GMT  
		Size: 9.9 MB (9883755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df9537cbf7bfca6bee23b1c14225fe362085e540573b07ba4f1a7f700166b86`  
		Last Modified: Fri, 17 Apr 2026 00:30:10 GMT  
		Size: 6.2 MB (6156988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2013535d8a94129c0282272aaa2c4861a3862fc01718c76e032035cb4746f63`  
		Last Modified: Fri, 17 Apr 2026 00:30:09 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1fa7e1dbe81f98aff0660c3a49ee340954ac7a38973f6bb82f6db28bbb51b10`  
		Last Modified: Fri, 17 Apr 2026 00:30:13 GMT  
		Size: 50.1 MB (50120912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9021c9b07af74a6a8772e32cfafb5d2ff49896afcd379266db4aebcd96cd59`  
		Last Modified: Fri, 17 Apr 2026 00:30:11 GMT  
		Size: 11.8 MB (11775857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39cc9439814248798aac7751d0e21ad7a96316c74d9d8b6e986de66c3b45fdfe`  
		Last Modified: Fri, 17 Apr 2026 00:30:11 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03f2a9ba47145fa22947d6e34317a627e7f66858410abff70ced177356ec2d2`  
		Last Modified: Fri, 17 Apr 2026 00:30:11 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa31db6e1c0d624aba57f25e567f938463f524d8b942613cbc7896ca2bf55b1`  
		Last Modified: Fri, 17 Apr 2026 00:30:12 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:0569cbc8f53a2a3ba7e48ae8070b09a7c99bc295a6665357a3bc50743fc3ac78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **942.6 KB (942650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccbd0f62f74b358602d757e6e03fe4bdb0b116ec3cd697e6d89aff02e9d74422`

```dockerfile
```

-	Layers:
	-	`sha256:71eb6856c6df8fd538099f8bea992c8c3d8ce9489ff5585eb6a4568bed243cf2`  
		Last Modified: Fri, 17 Apr 2026 00:30:09 GMT  
		Size: 912.5 KB (912532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fa1cf8a4f6c231f9a062e312a9949dfd0c46fb4910ee687fe22d6e95d25358d`  
		Last Modified: Fri, 17 Apr 2026 00:30:09 GMT  
		Size: 30.1 KB (30118 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:d8bba543dd7957bf4ff6c86c6988eefca2aae94f8544a807186df490de242304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.8 MB (78753601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:009e9f2403a04f2b67a85665b4135e4e7d98af11b3d4e80c10b2c3032c759e43`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:13 GMT
ADD alpine-minirootfs-3.21.7-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:13 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:30:50 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 00:30:51 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:30:52 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 17 Apr 2026 00:30:52 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Fri, 17 Apr 2026 00:30:55 GMT
ENV INFLUXDB_VERSION=2.7.12
# Fri, 17 Apr 2026 00:30:55 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Fri, 17 Apr 2026 00:30:55 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Fri, 17 Apr 2026 00:30:56 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 17 Apr 2026 00:30:56 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 17 Apr 2026 00:30:56 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 17 Apr 2026 00:30:56 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 17 Apr 2026 00:30:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:30:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:30:56 GMT
CMD ["influxd"]
# Fri, 17 Apr 2026 00:30:56 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 17 Apr 2026 00:30:56 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 17 Apr 2026 00:30:56 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 17 Apr 2026 00:30:56 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 17 Apr 2026 00:30:56 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:2dd7199cff98a7400e801cbfad6de906972a4e3dd0a749d4c1b80f5a1e3e4108`  
		Last Modified: Thu, 16 Apr 2026 05:32:50 GMT  
		Size: 4.0 MB (3994465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57919f2da9ccf3cbf004ab0822b1e771ac4b7c28edb6497b307e30831b04768c`  
		Last Modified: Fri, 17 Apr 2026 00:31:05 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b178d5851d796e606bc17110cbd657c3395903f0118362582c16cb57c494f9f`  
		Last Modified: Fri, 17 Apr 2026 00:31:06 GMT  
		Size: 9.8 MB (9842333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e834fed4dd780327fc357b35f87770f109a9a1c81ad82abbdd87108844e51c`  
		Last Modified: Fri, 17 Apr 2026 00:31:06 GMT  
		Size: 5.8 MB (5790434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44528ba6f34db31dd37cc62145eba18797869d7ca36df8ce00bdc0e8d2cfb6e3`  
		Last Modified: Fri, 17 Apr 2026 00:31:06 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6a08fb364b2f11c679d5d9c8647a9eeaddc7ca78b5df94117800079fbae87e`  
		Last Modified: Fri, 17 Apr 2026 00:31:08 GMT  
		Size: 48.0 MB (48017991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca94b59173a7d6d223a54a28f4882b40388572eb1fccf06c78fe5e260329a6f`  
		Last Modified: Fri, 17 Apr 2026 00:31:07 GMT  
		Size: 11.1 MB (11100426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3b6694d90a266bc5a8b986e5f06883fcc4856d4542db76bf66b50a0e472bce`  
		Last Modified: Fri, 17 Apr 2026 00:31:07 GMT  
		Size: 207.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dea6a566ae936b53f2e600d7d4d84587698bd04426f014a6511a0389f765075`  
		Last Modified: Fri, 17 Apr 2026 00:31:08 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d83c9443b9a4f4870ebf96ff3bb5b19eae81290aa2653dc734fad8e9560ca6`  
		Last Modified: Fri, 17 Apr 2026 00:31:09 GMT  
		Size: 6.3 KB (6283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:803cbdb4c6c722827e367c5f89c95e4b3ff10f5f92dc8c5336519faea8faf271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **942.0 KB (942047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7915998211cbf9e7364c78145865c78ddf310b78b4ffb49b153f4d83025131c4`

```dockerfile
```

-	Layers:
	-	`sha256:41f3b87caa14bc13134e7be18181eae6f5a37b9b691f9fdd3aede31d5f6875c3`  
		Last Modified: Fri, 17 Apr 2026 00:31:05 GMT  
		Size: 911.8 KB (911759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79a7f14dca24064909205a6c1ff80a1bd203dac968ad72d931498682ac10df52`  
		Last Modified: Fri, 17 Apr 2026 00:31:05 GMT  
		Size: 30.3 KB (30288 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7.12`

```console
$ docker pull influxdb@sha256:587b7878881812cf6e5481f8889f53f210180fd6790e6c3ddaa0b456dcffd5ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.12` - linux; amd64

```console
$ docker pull influxdb@sha256:3b4f54f583cd5d6d31f4642cad69a69e3d50b79531dd972801a1dc524754d2fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157236305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb98f8cbec6871d05f08b60625b7b174b3d2b26ac6f1ab0ab98f3a34c3a833a5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:41:20 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:41:21 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 22 Apr 2026 01:41:21 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 22 Apr 2026 01:41:23 GMT
ENV GOSU_VER=1.16
# Wed, 22 Apr 2026 01:41:23 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Wed, 22 Apr 2026 01:41:23 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 22 Apr 2026 01:41:26 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Wed, 22 Apr 2026 01:41:26 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 22 Apr 2026 01:41:27 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 22 Apr 2026 01:41:27 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 22 Apr 2026 01:41:27 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 22 Apr 2026 01:41:27 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 22 Apr 2026 01:41:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 01:41:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 01:41:27 GMT
CMD ["influxd"]
# Wed, 22 Apr 2026 01:41:27 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 22 Apr 2026 01:41:27 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 22 Apr 2026 01:41:27 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 22 Apr 2026 01:41:27 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 22 Apr 2026 01:41:27 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29f07cc9ba59ef00f61011edce588e98164ffd1b6e7ac7af9be3a24113d75d6`  
		Last Modified: Wed, 22 Apr 2026 01:41:43 GMT  
		Size: 9.8 MB (9799042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe897ac537e2db135be8699f8cf64f46db637043a940e8c738a8d53ffaacb3c`  
		Last Modified: Wed, 22 Apr 2026 01:41:43 GMT  
		Size: 6.2 MB (6156974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd711476a81735c2f5896d28216c672eb9d67057747bf0ed8dec36d20c415d0`  
		Last Modified: Wed, 22 Apr 2026 01:41:42 GMT  
		Size: 3.2 KB (3228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364f823b105ccbba816839ddba9dbbb2c325e426881b8ed79bbcc960eb9bcf77`  
		Last Modified: Wed, 22 Apr 2026 01:41:42 GMT  
		Size: 1.0 MB (1012039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d5b7cd45e9439ced8ca3a6818858c500e2d5e8a96bde07ad7925ce4b58dd29`  
		Last Modified: Wed, 22 Apr 2026 01:41:46 GMT  
		Size: 100.2 MB (100246163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab0e7ce3787869b9101a59584e44a71d0b17d86c274c5b64ffe8ae829d9ee86`  
		Last Modified: Wed, 22 Apr 2026 01:41:45 GMT  
		Size: 11.8 MB (11775880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cdf38892ce537a1ae82212d0f408af180c67c5814db50b32ed9d10898b75355`  
		Last Modified: Wed, 22 Apr 2026 01:41:44 GMT  
		Size: 207.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118346765087f08818eb0b37709db078a185e7240d28ef9d5920fa0c9f9c6949`  
		Last Modified: Wed, 22 Apr 2026 01:41:44 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a679d3bb179326735cf604f6f11914653be7426528d2ec498ea5010ca50e4d53`  
		Last Modified: Wed, 22 Apr 2026 01:41:45 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:ffb9fc1043235069d2dfe2f762c0ce3ef34e43a52d6466f9f74f575668f2f6b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3014384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d682d84083d3451c9d12fee9172da41d90e9ba979913f86376ef4ca4c6c225`

```dockerfile
```

-	Layers:
	-	`sha256:6a680b1575c8d06b1e037fbb4e14b707e21703dfaf8443cd6a244f54a36935d7`  
		Last Modified: Wed, 22 Apr 2026 01:41:42 GMT  
		Size: 3.0 MB (2981484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bff474574493b8406c4984e87e8d3457858e1a2d646c812acee044494fcdcce0`  
		Last Modified: Wed, 22 Apr 2026 01:41:42 GMT  
		Size: 32.9 KB (32900 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7.12` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:f180153db00fb65bc9447d1f1ea36588a846de7e36863b34b24d752fc428189d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151625536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d437663aa45683e3aea1381347d0e377293f50afde2073da22aaa569ba39b33`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:44:36 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 22 Apr 2026 01:44:37 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 22 Apr 2026 01:44:39 GMT
ENV GOSU_VER=1.16
# Wed, 22 Apr 2026 01:44:39 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Wed, 22 Apr 2026 01:44:39 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 22 Apr 2026 01:44:44 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Wed, 22 Apr 2026 01:44:44 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 22 Apr 2026 01:44:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 22 Apr 2026 01:44:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 22 Apr 2026 01:44:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 22 Apr 2026 01:44:45 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 22 Apr 2026 01:44:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 01:44:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 01:44:45 GMT
CMD ["influxd"]
# Wed, 22 Apr 2026 01:44:45 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 22 Apr 2026 01:44:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 22 Apr 2026 01:44:45 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 22 Apr 2026 01:44:45 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 22 Apr 2026 01:44:45 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387a1587236ec51fe27e6a475764b3582ca81353283861373f191110999fb121`  
		Last Modified: Wed, 22 Apr 2026 01:44:59 GMT  
		Size: 9.6 MB (9628061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c15338b943524f08bd8534fe024b05145b98eb00da062b780858e7c8cc6a7c`  
		Last Modified: Wed, 22 Apr 2026 01:44:59 GMT  
		Size: 5.8 MB (5790416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f237dc5b10389a57e18783d12d9511d7a73d0747921e369690b1f992522a9f2`  
		Last Modified: Wed, 22 Apr 2026 01:44:59 GMT  
		Size: 3.2 KB (3228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b254d000bb8f070b191a46d14398fb24e28b1d81bf0780fe6148b7d43bde0ef6`  
		Last Modified: Wed, 22 Apr 2026 01:44:59 GMT  
		Size: 938.9 KB (938883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef001e56afeb60a74634dfc64abd229fb5fe1abfc104b537a2df21af52905b61`  
		Last Modified: Wed, 22 Apr 2026 01:45:03 GMT  
		Size: 96.0 MB (96041716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158d254574795ce20ded8a85d81993007ccab1eed2046cdc69e3ea4731b76c9a`  
		Last Modified: Wed, 22 Apr 2026 01:45:01 GMT  
		Size: 11.1 MB (11100388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf5b36ec252a2d1d18588347441c364f7d7da469d19c615ee44e03824bd0617`  
		Last Modified: Wed, 22 Apr 2026 01:45:01 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35afbdc6acb5fe6669f56074f523754d15668082dbe1ac6ca233c820491cca77`  
		Last Modified: Wed, 22 Apr 2026 01:45:01 GMT  
		Size: 235.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feca5e9a9c1c85f1293916d86f1f12632f018bffa159156b4cb7b8f645000abc`  
		Last Modified: Wed, 22 Apr 2026 01:45:02 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:e4d8202ac8a034aeb13d26f67181f8574e36990f929fa5522cd8de2c4c5c8a78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3013747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62a0d37667b3073fa90dba998ed16d02df4e10be2dc8f481a50c5f8a4081acb5`

```dockerfile
```

-	Layers:
	-	`sha256:7f5810e2f1bc0468bab32e6ff2fef771b7fba0d5bfab2c376cc7c81aa49cb81a`  
		Last Modified: Wed, 22 Apr 2026 01:44:59 GMT  
		Size: 3.0 MB (2980688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24e27dab536ca69ef5cb533f615eafe6c7aea731b8856f24961a24ddc8acece1`  
		Last Modified: Wed, 22 Apr 2026 01:44:59 GMT  
		Size: 33.1 KB (33059 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7.12-alpine`

```console
$ docker pull influxdb@sha256:cf6476ce69eb017522fce67a5e69670d79ce05322b9271accfb9a9ca39c97b07
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.12-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:a63f1abb587b40e272a34684502f813b11534f2796a6e180a390591ff19d5bf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81592338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d07629cd20c54eca2bf9fa79ae7ab852a8920fadf113b7dd4a87622f5ea84a0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:29:52 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 00:29:53 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:29:54 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 17 Apr 2026 00:29:54 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Fri, 17 Apr 2026 00:29:59 GMT
ENV INFLUXDB_VERSION=2.7.12
# Fri, 17 Apr 2026 00:29:59 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Fri, 17 Apr 2026 00:29:59 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Fri, 17 Apr 2026 00:30:00 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 17 Apr 2026 00:30:00 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 17 Apr 2026 00:30:00 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 17 Apr 2026 00:30:00 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 17 Apr 2026 00:30:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:30:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:30:00 GMT
CMD ["influxd"]
# Fri, 17 Apr 2026 00:30:00 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 17 Apr 2026 00:30:00 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 17 Apr 2026 00:30:00 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 17 Apr 2026 00:30:00 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 17 Apr 2026 00:30:00 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34dc1d883690517ae685fc63bb161f7fc336f5db7ff9d689cf1e477cad7cb500`  
		Last Modified: Fri, 17 Apr 2026 00:30:09 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13158ef7e36a22d4b2839dab788ab8ddf34a3f6cfec26bb5c6fc4b3b60dfb21e`  
		Last Modified: Fri, 17 Apr 2026 00:30:09 GMT  
		Size: 9.9 MB (9883755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df9537cbf7bfca6bee23b1c14225fe362085e540573b07ba4f1a7f700166b86`  
		Last Modified: Fri, 17 Apr 2026 00:30:10 GMT  
		Size: 6.2 MB (6156988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2013535d8a94129c0282272aaa2c4861a3862fc01718c76e032035cb4746f63`  
		Last Modified: Fri, 17 Apr 2026 00:30:09 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1fa7e1dbe81f98aff0660c3a49ee340954ac7a38973f6bb82f6db28bbb51b10`  
		Last Modified: Fri, 17 Apr 2026 00:30:13 GMT  
		Size: 50.1 MB (50120912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9021c9b07af74a6a8772e32cfafb5d2ff49896afcd379266db4aebcd96cd59`  
		Last Modified: Fri, 17 Apr 2026 00:30:11 GMT  
		Size: 11.8 MB (11775857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39cc9439814248798aac7751d0e21ad7a96316c74d9d8b6e986de66c3b45fdfe`  
		Last Modified: Fri, 17 Apr 2026 00:30:11 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03f2a9ba47145fa22947d6e34317a627e7f66858410abff70ced177356ec2d2`  
		Last Modified: Fri, 17 Apr 2026 00:30:11 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa31db6e1c0d624aba57f25e567f938463f524d8b942613cbc7896ca2bf55b1`  
		Last Modified: Fri, 17 Apr 2026 00:30:12 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:0569cbc8f53a2a3ba7e48ae8070b09a7c99bc295a6665357a3bc50743fc3ac78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **942.6 KB (942650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccbd0f62f74b358602d757e6e03fe4bdb0b116ec3cd697e6d89aff02e9d74422`

```dockerfile
```

-	Layers:
	-	`sha256:71eb6856c6df8fd538099f8bea992c8c3d8ce9489ff5585eb6a4568bed243cf2`  
		Last Modified: Fri, 17 Apr 2026 00:30:09 GMT  
		Size: 912.5 KB (912532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fa1cf8a4f6c231f9a062e312a9949dfd0c46fb4910ee687fe22d6e95d25358d`  
		Last Modified: Fri, 17 Apr 2026 00:30:09 GMT  
		Size: 30.1 KB (30118 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7.12-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:d8bba543dd7957bf4ff6c86c6988eefca2aae94f8544a807186df490de242304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.8 MB (78753601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:009e9f2403a04f2b67a85665b4135e4e7d98af11b3d4e80c10b2c3032c759e43`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:13 GMT
ADD alpine-minirootfs-3.21.7-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:13 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:30:50 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 00:30:51 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:30:52 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 17 Apr 2026 00:30:52 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Fri, 17 Apr 2026 00:30:55 GMT
ENV INFLUXDB_VERSION=2.7.12
# Fri, 17 Apr 2026 00:30:55 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Fri, 17 Apr 2026 00:30:55 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Fri, 17 Apr 2026 00:30:56 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 17 Apr 2026 00:30:56 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 17 Apr 2026 00:30:56 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 17 Apr 2026 00:30:56 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 17 Apr 2026 00:30:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:30:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:30:56 GMT
CMD ["influxd"]
# Fri, 17 Apr 2026 00:30:56 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 17 Apr 2026 00:30:56 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 17 Apr 2026 00:30:56 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 17 Apr 2026 00:30:56 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 17 Apr 2026 00:30:56 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:2dd7199cff98a7400e801cbfad6de906972a4e3dd0a749d4c1b80f5a1e3e4108`  
		Last Modified: Thu, 16 Apr 2026 05:32:50 GMT  
		Size: 4.0 MB (3994465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57919f2da9ccf3cbf004ab0822b1e771ac4b7c28edb6497b307e30831b04768c`  
		Last Modified: Fri, 17 Apr 2026 00:31:05 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b178d5851d796e606bc17110cbd657c3395903f0118362582c16cb57c494f9f`  
		Last Modified: Fri, 17 Apr 2026 00:31:06 GMT  
		Size: 9.8 MB (9842333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e834fed4dd780327fc357b35f87770f109a9a1c81ad82abbdd87108844e51c`  
		Last Modified: Fri, 17 Apr 2026 00:31:06 GMT  
		Size: 5.8 MB (5790434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44528ba6f34db31dd37cc62145eba18797869d7ca36df8ce00bdc0e8d2cfb6e3`  
		Last Modified: Fri, 17 Apr 2026 00:31:06 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6a08fb364b2f11c679d5d9c8647a9eeaddc7ca78b5df94117800079fbae87e`  
		Last Modified: Fri, 17 Apr 2026 00:31:08 GMT  
		Size: 48.0 MB (48017991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca94b59173a7d6d223a54a28f4882b40388572eb1fccf06c78fe5e260329a6f`  
		Last Modified: Fri, 17 Apr 2026 00:31:07 GMT  
		Size: 11.1 MB (11100426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3b6694d90a266bc5a8b986e5f06883fcc4856d4542db76bf66b50a0e472bce`  
		Last Modified: Fri, 17 Apr 2026 00:31:07 GMT  
		Size: 207.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dea6a566ae936b53f2e600d7d4d84587698bd04426f014a6511a0389f765075`  
		Last Modified: Fri, 17 Apr 2026 00:31:08 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d83c9443b9a4f4870ebf96ff3bb5b19eae81290aa2653dc734fad8e9560ca6`  
		Last Modified: Fri, 17 Apr 2026 00:31:09 GMT  
		Size: 6.3 KB (6283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:803cbdb4c6c722827e367c5f89c95e4b3ff10f5f92dc8c5336519faea8faf271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **942.0 KB (942047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7915998211cbf9e7364c78145865c78ddf310b78b4ffb49b153f4d83025131c4`

```dockerfile
```

-	Layers:
	-	`sha256:41f3b87caa14bc13134e7be18181eae6f5a37b9b691f9fdd3aede31d5f6875c3`  
		Last Modified: Fri, 17 Apr 2026 00:31:05 GMT  
		Size: 911.8 KB (911759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79a7f14dca24064909205a6c1ff80a1bd203dac968ad72d931498682ac10df52`  
		Last Modified: Fri, 17 Apr 2026 00:31:05 GMT  
		Size: 30.3 KB (30288 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.8`

```console
$ docker pull influxdb@sha256:71f2bce68b47a3e26c1ed38f7480a9372b008ba9b7c8a35cb2c913d3102d377f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.8` - linux; amd64

```console
$ docker pull influxdb@sha256:e532279db2ffef29e7eab17961841291927e228f2703bafd9255023d5480d056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107241320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:759ec9162770032bdcd5f75d588d4bdd548f5ea87abdbd151e3711dfc50cf4f4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:41:32 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:41:33 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 22 Apr 2026 01:41:33 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 22 Apr 2026 01:41:35 GMT
ENV GOSU_VER=1.19
# Wed, 22 Apr 2026 01:41:35 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Wed, 22 Apr 2026 01:41:35 GMT
ENV INFLUXDB_VERSION=2.8.0
# Wed, 22 Apr 2026 01:41:35 GMT
ENV INFLUXDB_PR=-2
# Wed, 22 Apr 2026 01:41:35 GMT
ENV INFLUXDB_PV=2.8.0-2
# Wed, 22 Apr 2026 01:41:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 22 Apr 2026 01:41:37 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 22 Apr 2026 01:41:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 22 Apr 2026 01:41:38 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 22 Apr 2026 01:41:38 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 22 Apr 2026 01:41:39 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 22 Apr 2026 01:41:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 01:41:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 01:41:39 GMT
CMD ["influxd"]
# Wed, 22 Apr 2026 01:41:39 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 22 Apr 2026 01:41:39 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 22 Apr 2026 01:41:39 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 22 Apr 2026 01:41:39 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 22 Apr 2026 01:41:39 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c791747626e2412d3502fd05d4fac3fffd42cdd349ef47e7884ae03da2dbef`  
		Last Modified: Wed, 22 Apr 2026 01:41:50 GMT  
		Size: 9.8 MB (9798990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2ee315242c36b9238a9f0e643e4281f93755787bc77c2b111e887c7653da6d`  
		Last Modified: Wed, 22 Apr 2026 01:41:50 GMT  
		Size: 6.2 MB (6156971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844de845c21c0436926d498f8ebd39d4698a948c5fb968d09c52f49a33e30c54`  
		Last Modified: Wed, 22 Apr 2026 01:41:50 GMT  
		Size: 3.2 KB (3229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41868ae9fbbede4b0f6bdbd0af43852ad245ea7c610f402e2220bd8847c6b729`  
		Last Modified: Wed, 22 Apr 2026 01:41:50 GMT  
		Size: 811.5 KB (811478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4da638bcf081222b7033e64890358a3f551ee2a1060e73d60775bb4cce4888a`  
		Last Modified: Wed, 22 Apr 2026 01:41:52 GMT  
		Size: 50.5 MB (50451802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4fea9ea328927d53fc80fd2b38cd6f7a8dffe1745ef87a3a3159347389e9f2e`  
		Last Modified: Wed, 22 Apr 2026 01:41:52 GMT  
		Size: 11.8 MB (11775870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ddc1c71a8a7f9d5167a61bdc437327b756110396f40992677ef72157e08775`  
		Last Modified: Wed, 22 Apr 2026 01:41:51 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e55f58da73fd395ac05c086627b0e088853dbeb76527b853bdcd5d76adddca`  
		Last Modified: Wed, 22 Apr 2026 01:41:52 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70d15b5d427c0540fea4882696f4da3a2a6787732964d6542233dc71e311537`  
		Last Modified: Wed, 22 Apr 2026 01:41:53 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:8938d3511aaa20b791700f8a2e5817323627e5360965a4f98d6140dc066ff3ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b027564a5f64ce815d5a5005299ddd5ea69b030647832e23bbc5a547bd4809b1`

```dockerfile
```

-	Layers:
	-	`sha256:ec06b068a4d9e7482bd3578659a536954e9c49b80b862002a0c69866d0d7e1f6`  
		Last Modified: Wed, 22 Apr 2026 01:41:50 GMT  
		Size: 2.9 MB (2934237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a481924326704569284e4ea29a85d10c6460d99223990fd6292868077c45765`  
		Last Modified: Wed, 22 Apr 2026 01:41:50 GMT  
		Size: 33.6 KB (33621 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:4749be1eb7cb5803e7fe7c7abfb0e4a868c3017bc903299d3526cbfc5ff85379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103640890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a3d056402f328a5ae7b1e564dedf01aa4df264f034fedd872385e3bb96accdd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:44:39 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:40 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 22 Apr 2026 01:44:40 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 22 Apr 2026 01:44:42 GMT
ENV GOSU_VER=1.19
# Wed, 22 Apr 2026 01:44:42 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Wed, 22 Apr 2026 01:44:42 GMT
ENV INFLUXDB_VERSION=2.8.0
# Wed, 22 Apr 2026 01:44:42 GMT
ENV INFLUXDB_PR=-2
# Wed, 22 Apr 2026 01:44:42 GMT
ENV INFLUXDB_PV=2.8.0-2
# Wed, 22 Apr 2026 01:44:46 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 22 Apr 2026 01:44:46 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 22 Apr 2026 01:44:47 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 22 Apr 2026 01:44:47 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 22 Apr 2026 01:44:47 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 22 Apr 2026 01:44:47 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 22 Apr 2026 01:44:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 01:44:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 01:44:47 GMT
CMD ["influxd"]
# Wed, 22 Apr 2026 01:44:47 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 22 Apr 2026 01:44:47 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 22 Apr 2026 01:44:47 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 22 Apr 2026 01:44:47 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 22 Apr 2026 01:44:47 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ddf21f4abba315d4e405b0b7ca7380c3b03e816eea5fd8219965fed687ac4f`  
		Last Modified: Wed, 22 Apr 2026 01:44:58 GMT  
		Size: 9.6 MB (9628094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c560fbc3a39b1a11f3127f89d636cc2517753a085eaf3afbf4f928d215e86c8b`  
		Last Modified: Wed, 22 Apr 2026 01:44:58 GMT  
		Size: 5.8 MB (5790421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f267c0a54c465bfc52d652cfab1ac62dfafe3e42649811dab584056706e1db51`  
		Last Modified: Wed, 22 Apr 2026 01:44:57 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01fd1f2188e7bc5e9738f5ddde7c01d895d6f100721c3eca47f0448d1c4921c`  
		Last Modified: Wed, 22 Apr 2026 01:44:57 GMT  
		Size: 766.4 KB (766364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9245aa8cd37661f6b67a498039d6cc9574d07919bf07b31b7ce44f594b552802`  
		Last Modified: Wed, 22 Apr 2026 01:45:00 GMT  
		Size: 48.2 MB (48229530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17a6763a2749ecf5870e80619513e273d0e1a10c00743d701c94e21be334b3f`  
		Last Modified: Wed, 22 Apr 2026 01:44:59 GMT  
		Size: 11.1 MB (11100415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69e2b2742458b735c0dc03bd705017e3e0d65e05db242e409d99a66ce5e26a6`  
		Last Modified: Wed, 22 Apr 2026 01:44:59 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95186bc453fe3657a6cd1bbd5b28c20dcd8355d9ba05951c3ec5b6c00a573e4`  
		Last Modified: Wed, 22 Apr 2026 01:44:59 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f382dd5f3b374f7003cd1b28910bd54c378e293152f8e5a1d9870d5e406147a`  
		Last Modified: Wed, 22 Apr 2026 01:45:00 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:439f6863a26e4a35763bda86f99511c908da7c6f97b9d593c7c3a1094666c347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9196348dc3b5c505a243f0014bdc51b8210eb9a0d606b67eef4fbb93c121620`

```dockerfile
```

-	Layers:
	-	`sha256:219a4fdfdfad1438a2554524a5be2b3f344b6802c2cc229aba88bf6973f82621`  
		Last Modified: Wed, 22 Apr 2026 01:44:57 GMT  
		Size: 2.9 MB (2933717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79c489575215cf3dd7f3007ba6ae0f8970239be059d7c86d56c59b83c70b12b4`  
		Last Modified: Wed, 22 Apr 2026 01:44:57 GMT  
		Size: 33.8 KB (33815 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.8-alpine`

```console
$ docker pull influxdb@sha256:4f90d40c00193d91889ad872c39a586a011db4ac4d1a766e248d9cbbcc6cec3e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.8-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:ef8bad9a5c5f604e1a139b7b99c452bc9cb62affdcb9f11afad1b2e5c20c45a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81923288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70540d47f741606ec70538d2489a54d267d7fd74f4b276a176e53ad8c2efacf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:29:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 00:29:56 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:29:56 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 17 Apr 2026 00:29:56 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Fri, 17 Apr 2026 00:30:00 GMT
ENV INFLUXDB_VERSION=2.8.0
# Fri, 17 Apr 2026 00:30:00 GMT
ENV INFLUXDB_PR=-2
# Fri, 17 Apr 2026 00:30:00 GMT
ENV INFLUXDB_PV=2.8.0-2
# Fri, 17 Apr 2026 00:30:00 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Fri, 17 Apr 2026 00:30:00 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Fri, 17 Apr 2026 00:30:01 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 17 Apr 2026 00:30:02 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 17 Apr 2026 00:30:02 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 17 Apr 2026 00:30:02 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 17 Apr 2026 00:30:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:30:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:30:02 GMT
CMD ["influxd"]
# Fri, 17 Apr 2026 00:30:02 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 17 Apr 2026 00:30:02 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 17 Apr 2026 00:30:02 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 17 Apr 2026 00:30:02 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 17 Apr 2026 00:30:02 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef79b6f3d2e846d055a2620421abd1ea83d1a2a5c141a54104accb233ed0ce59`  
		Last Modified: Fri, 17 Apr 2026 00:30:12 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd92961fcb2124af0c103187cef2632786c556874b686090cae17de4638ed98`  
		Last Modified: Fri, 17 Apr 2026 00:30:12 GMT  
		Size: 9.9 MB (9883791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21ab53b0f55c96701571d89ea72fe10e15495a5399811272d01416b505d8848`  
		Last Modified: Fri, 17 Apr 2026 00:30:12 GMT  
		Size: 6.2 MB (6156985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788c81c58d331aa59131e00c438630fb5aefff8373c89b0adc66d24f393ae7cb`  
		Last Modified: Fri, 17 Apr 2026 00:30:12 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1fff6940a3878ed3aee43c506ecf21d4bce29f9e7388a17ce375c9b9c0a44cf`  
		Last Modified: Fri, 17 Apr 2026 00:30:15 GMT  
		Size: 50.5 MB (50451820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6c03c0be2850f9c82b37631d6cba13fdd3f1e632d3643edc54d2cdc6edf2c9`  
		Last Modified: Fri, 17 Apr 2026 00:30:13 GMT  
		Size: 11.8 MB (11775863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aea5f86be29cb56a759d7142f5a9b62bfd6ed99d100b921dd3a33e4ce9314a5`  
		Last Modified: Fri, 17 Apr 2026 00:30:13 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ef07b04bbe77eb925cb81d0e6082ce24328e0d2c296d61c460e11aa33b6b3a`  
		Last Modified: Fri, 17 Apr 2026 00:30:14 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ddd87b55db792237d8b7cd099de585015d86816d1215b2f57c4dd5011ba91e`  
		Last Modified: Fri, 17 Apr 2026 00:30:15 GMT  
		Size: 6.3 KB (6283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:40fca214b400941be68a739f6f59448a6e931f730682c1d89026fee13fe21c34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **946.1 KB (946058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7f880a5909c565d62181a36572e16dac17e9bb0131551dfa514d962d26c4a97`

```dockerfile
```

-	Layers:
	-	`sha256:33f778c6f613bedfa5d2ec41b08b10f6bf6ce196ef899601b0ec66f7637095f3`  
		Last Modified: Fri, 17 Apr 2026 00:30:12 GMT  
		Size: 915.2 KB (915211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:629ffea1f9f8527114e2ed5a812a800fe7b6e1a1947e4b14a6b8302f319cb11d`  
		Last Modified: Fri, 17 Apr 2026 00:30:12 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.8-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:1d6e285b1a5e3fa23695d08c8586d0d17c004443a83a93e22a40d9f7c449227c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.0 MB (78965173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ba6389eb739af52c14de9f6ed96efacfbe53dccc3e41f42ab1f51fef176da67`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:13 GMT
ADD alpine-minirootfs-3.21.7-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:13 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:31:02 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 00:31:03 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:31:03 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 17 Apr 2026 00:31:04 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Fri, 17 Apr 2026 00:31:07 GMT
ENV INFLUXDB_VERSION=2.8.0
# Fri, 17 Apr 2026 00:31:07 GMT
ENV INFLUXDB_PR=-2
# Fri, 17 Apr 2026 00:31:07 GMT
ENV INFLUXDB_PV=2.8.0-2
# Fri, 17 Apr 2026 00:31:07 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Fri, 17 Apr 2026 00:31:07 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Fri, 17 Apr 2026 00:31:07 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 17 Apr 2026 00:31:08 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 17 Apr 2026 00:31:08 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 17 Apr 2026 00:31:08 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 17 Apr 2026 00:31:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:31:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:31:08 GMT
CMD ["influxd"]
# Fri, 17 Apr 2026 00:31:08 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 17 Apr 2026 00:31:08 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 17 Apr 2026 00:31:08 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 17 Apr 2026 00:31:08 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 17 Apr 2026 00:31:08 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:2dd7199cff98a7400e801cbfad6de906972a4e3dd0a749d4c1b80f5a1e3e4108`  
		Last Modified: Thu, 16 Apr 2026 05:32:50 GMT  
		Size: 4.0 MB (3994465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f652e0c01e29334dc1fe16c1d56127042156c3a64857b4a0ead43d3986f7986`  
		Last Modified: Fri, 17 Apr 2026 00:31:17 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5ddaea2126344e5b11cf5e6c97cd44d5b59a15fabcb438bb0a343fd2c1b7162`  
		Last Modified: Fri, 17 Apr 2026 00:31:18 GMT  
		Size: 9.8 MB (9842397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9394ce182bd0c5ee862a0d2428947e1a0d0fc3da081624b53bb5b05e37972f48`  
		Last Modified: Fri, 17 Apr 2026 00:31:17 GMT  
		Size: 5.8 MB (5790430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98541319cbb33b6799c13cddcd9cd7e00fe5295fea9954da3eaa7af2a1be8ca9`  
		Last Modified: Fri, 17 Apr 2026 00:31:17 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872f29647bbd3f39d47cc2a6b1b76f958b61aeb29480eec96b42c03288cd1472`  
		Last Modified: Fri, 17 Apr 2026 00:31:20 GMT  
		Size: 48.2 MB (48229511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff3598b437a8492690885c52bd82ed6d9ba85af743856cdcdc03e23cff14b84b`  
		Last Modified: Fri, 17 Apr 2026 00:31:19 GMT  
		Size: 11.1 MB (11100414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca69b2befa8351ec86c62df1caca82193562d274be054f00c148c6b5f5ba67b`  
		Last Modified: Fri, 17 Apr 2026 00:31:18 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba50550e7b2ebf586c1c93af205b4fb509ff55bfeda64342a548be9f7eb0b4d`  
		Last Modified: Fri, 17 Apr 2026 00:31:19 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8195a95763ebcb79e75c6db51ef9341b1678f6bd5070f114326209a91fff3bb8`  
		Last Modified: Fri, 17 Apr 2026 00:31:20 GMT  
		Size: 6.3 KB (6284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:866fdba0f42c46c21ba2c8d62ea1a6c90a46ca6d38e54989b009617072a3b43c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **945.5 KB (945503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48090246a2f4e0d9530f4b14c374ee2497817d1ef5d6807100cc1f963980061`

```dockerfile
```

-	Layers:
	-	`sha256:7f3a296bce432225eae41d3f9ad0d93e77867c28796a18dbaf6693ac05624f1b`  
		Last Modified: Fri, 17 Apr 2026 00:31:17 GMT  
		Size: 914.5 KB (914462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0eb74c7252a3cb8f2dd15f0ae328f0107f804876760828392c2573c155759432`  
		Last Modified: Fri, 17 Apr 2026 00:31:17 GMT  
		Size: 31.0 KB (31041 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.8.0`

```console
$ docker pull influxdb@sha256:71f2bce68b47a3e26c1ed38f7480a9372b008ba9b7c8a35cb2c913d3102d377f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.8.0` - linux; amd64

```console
$ docker pull influxdb@sha256:e532279db2ffef29e7eab17961841291927e228f2703bafd9255023d5480d056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107241320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:759ec9162770032bdcd5f75d588d4bdd548f5ea87abdbd151e3711dfc50cf4f4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:41:32 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:41:33 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 22 Apr 2026 01:41:33 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 22 Apr 2026 01:41:35 GMT
ENV GOSU_VER=1.19
# Wed, 22 Apr 2026 01:41:35 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Wed, 22 Apr 2026 01:41:35 GMT
ENV INFLUXDB_VERSION=2.8.0
# Wed, 22 Apr 2026 01:41:35 GMT
ENV INFLUXDB_PR=-2
# Wed, 22 Apr 2026 01:41:35 GMT
ENV INFLUXDB_PV=2.8.0-2
# Wed, 22 Apr 2026 01:41:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 22 Apr 2026 01:41:37 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 22 Apr 2026 01:41:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 22 Apr 2026 01:41:38 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 22 Apr 2026 01:41:38 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 22 Apr 2026 01:41:39 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 22 Apr 2026 01:41:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 01:41:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 01:41:39 GMT
CMD ["influxd"]
# Wed, 22 Apr 2026 01:41:39 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 22 Apr 2026 01:41:39 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 22 Apr 2026 01:41:39 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 22 Apr 2026 01:41:39 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 22 Apr 2026 01:41:39 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c791747626e2412d3502fd05d4fac3fffd42cdd349ef47e7884ae03da2dbef`  
		Last Modified: Wed, 22 Apr 2026 01:41:50 GMT  
		Size: 9.8 MB (9798990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2ee315242c36b9238a9f0e643e4281f93755787bc77c2b111e887c7653da6d`  
		Last Modified: Wed, 22 Apr 2026 01:41:50 GMT  
		Size: 6.2 MB (6156971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844de845c21c0436926d498f8ebd39d4698a948c5fb968d09c52f49a33e30c54`  
		Last Modified: Wed, 22 Apr 2026 01:41:50 GMT  
		Size: 3.2 KB (3229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41868ae9fbbede4b0f6bdbd0af43852ad245ea7c610f402e2220bd8847c6b729`  
		Last Modified: Wed, 22 Apr 2026 01:41:50 GMT  
		Size: 811.5 KB (811478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4da638bcf081222b7033e64890358a3f551ee2a1060e73d60775bb4cce4888a`  
		Last Modified: Wed, 22 Apr 2026 01:41:52 GMT  
		Size: 50.5 MB (50451802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4fea9ea328927d53fc80fd2b38cd6f7a8dffe1745ef87a3a3159347389e9f2e`  
		Last Modified: Wed, 22 Apr 2026 01:41:52 GMT  
		Size: 11.8 MB (11775870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ddc1c71a8a7f9d5167a61bdc437327b756110396f40992677ef72157e08775`  
		Last Modified: Wed, 22 Apr 2026 01:41:51 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e55f58da73fd395ac05c086627b0e088853dbeb76527b853bdcd5d76adddca`  
		Last Modified: Wed, 22 Apr 2026 01:41:52 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70d15b5d427c0540fea4882696f4da3a2a6787732964d6542233dc71e311537`  
		Last Modified: Wed, 22 Apr 2026 01:41:53 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8.0` - unknown; unknown

```console
$ docker pull influxdb@sha256:8938d3511aaa20b791700f8a2e5817323627e5360965a4f98d6140dc066ff3ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b027564a5f64ce815d5a5005299ddd5ea69b030647832e23bbc5a547bd4809b1`

```dockerfile
```

-	Layers:
	-	`sha256:ec06b068a4d9e7482bd3578659a536954e9c49b80b862002a0c69866d0d7e1f6`  
		Last Modified: Wed, 22 Apr 2026 01:41:50 GMT  
		Size: 2.9 MB (2934237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a481924326704569284e4ea29a85d10c6460d99223990fd6292868077c45765`  
		Last Modified: Wed, 22 Apr 2026 01:41:50 GMT  
		Size: 33.6 KB (33621 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.8.0` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:4749be1eb7cb5803e7fe7c7abfb0e4a868c3017bc903299d3526cbfc5ff85379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103640890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a3d056402f328a5ae7b1e564dedf01aa4df264f034fedd872385e3bb96accdd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:44:39 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:40 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 22 Apr 2026 01:44:40 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 22 Apr 2026 01:44:42 GMT
ENV GOSU_VER=1.19
# Wed, 22 Apr 2026 01:44:42 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Wed, 22 Apr 2026 01:44:42 GMT
ENV INFLUXDB_VERSION=2.8.0
# Wed, 22 Apr 2026 01:44:42 GMT
ENV INFLUXDB_PR=-2
# Wed, 22 Apr 2026 01:44:42 GMT
ENV INFLUXDB_PV=2.8.0-2
# Wed, 22 Apr 2026 01:44:46 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 22 Apr 2026 01:44:46 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 22 Apr 2026 01:44:47 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 22 Apr 2026 01:44:47 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 22 Apr 2026 01:44:47 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 22 Apr 2026 01:44:47 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 22 Apr 2026 01:44:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 01:44:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 01:44:47 GMT
CMD ["influxd"]
# Wed, 22 Apr 2026 01:44:47 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 22 Apr 2026 01:44:47 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 22 Apr 2026 01:44:47 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 22 Apr 2026 01:44:47 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 22 Apr 2026 01:44:47 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ddf21f4abba315d4e405b0b7ca7380c3b03e816eea5fd8219965fed687ac4f`  
		Last Modified: Wed, 22 Apr 2026 01:44:58 GMT  
		Size: 9.6 MB (9628094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c560fbc3a39b1a11f3127f89d636cc2517753a085eaf3afbf4f928d215e86c8b`  
		Last Modified: Wed, 22 Apr 2026 01:44:58 GMT  
		Size: 5.8 MB (5790421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f267c0a54c465bfc52d652cfab1ac62dfafe3e42649811dab584056706e1db51`  
		Last Modified: Wed, 22 Apr 2026 01:44:57 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01fd1f2188e7bc5e9738f5ddde7c01d895d6f100721c3eca47f0448d1c4921c`  
		Last Modified: Wed, 22 Apr 2026 01:44:57 GMT  
		Size: 766.4 KB (766364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9245aa8cd37661f6b67a498039d6cc9574d07919bf07b31b7ce44f594b552802`  
		Last Modified: Wed, 22 Apr 2026 01:45:00 GMT  
		Size: 48.2 MB (48229530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17a6763a2749ecf5870e80619513e273d0e1a10c00743d701c94e21be334b3f`  
		Last Modified: Wed, 22 Apr 2026 01:44:59 GMT  
		Size: 11.1 MB (11100415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69e2b2742458b735c0dc03bd705017e3e0d65e05db242e409d99a66ce5e26a6`  
		Last Modified: Wed, 22 Apr 2026 01:44:59 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95186bc453fe3657a6cd1bbd5b28c20dcd8355d9ba05951c3ec5b6c00a573e4`  
		Last Modified: Wed, 22 Apr 2026 01:44:59 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f382dd5f3b374f7003cd1b28910bd54c378e293152f8e5a1d9870d5e406147a`  
		Last Modified: Wed, 22 Apr 2026 01:45:00 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8.0` - unknown; unknown

```console
$ docker pull influxdb@sha256:439f6863a26e4a35763bda86f99511c908da7c6f97b9d593c7c3a1094666c347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9196348dc3b5c505a243f0014bdc51b8210eb9a0d606b67eef4fbb93c121620`

```dockerfile
```

-	Layers:
	-	`sha256:219a4fdfdfad1438a2554524a5be2b3f344b6802c2cc229aba88bf6973f82621`  
		Last Modified: Wed, 22 Apr 2026 01:44:57 GMT  
		Size: 2.9 MB (2933717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79c489575215cf3dd7f3007ba6ae0f8970239be059d7c86d56c59b83c70b12b4`  
		Last Modified: Wed, 22 Apr 2026 01:44:57 GMT  
		Size: 33.8 KB (33815 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.8.0-alpine`

```console
$ docker pull influxdb@sha256:4f90d40c00193d91889ad872c39a586a011db4ac4d1a766e248d9cbbcc6cec3e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.8.0-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:ef8bad9a5c5f604e1a139b7b99c452bc9cb62affdcb9f11afad1b2e5c20c45a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81923288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70540d47f741606ec70538d2489a54d267d7fd74f4b276a176e53ad8c2efacf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:29:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 00:29:56 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:29:56 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 17 Apr 2026 00:29:56 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Fri, 17 Apr 2026 00:30:00 GMT
ENV INFLUXDB_VERSION=2.8.0
# Fri, 17 Apr 2026 00:30:00 GMT
ENV INFLUXDB_PR=-2
# Fri, 17 Apr 2026 00:30:00 GMT
ENV INFLUXDB_PV=2.8.0-2
# Fri, 17 Apr 2026 00:30:00 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Fri, 17 Apr 2026 00:30:00 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Fri, 17 Apr 2026 00:30:01 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 17 Apr 2026 00:30:02 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 17 Apr 2026 00:30:02 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 17 Apr 2026 00:30:02 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 17 Apr 2026 00:30:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:30:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:30:02 GMT
CMD ["influxd"]
# Fri, 17 Apr 2026 00:30:02 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 17 Apr 2026 00:30:02 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 17 Apr 2026 00:30:02 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 17 Apr 2026 00:30:02 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 17 Apr 2026 00:30:02 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef79b6f3d2e846d055a2620421abd1ea83d1a2a5c141a54104accb233ed0ce59`  
		Last Modified: Fri, 17 Apr 2026 00:30:12 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd92961fcb2124af0c103187cef2632786c556874b686090cae17de4638ed98`  
		Last Modified: Fri, 17 Apr 2026 00:30:12 GMT  
		Size: 9.9 MB (9883791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21ab53b0f55c96701571d89ea72fe10e15495a5399811272d01416b505d8848`  
		Last Modified: Fri, 17 Apr 2026 00:30:12 GMT  
		Size: 6.2 MB (6156985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788c81c58d331aa59131e00c438630fb5aefff8373c89b0adc66d24f393ae7cb`  
		Last Modified: Fri, 17 Apr 2026 00:30:12 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1fff6940a3878ed3aee43c506ecf21d4bce29f9e7388a17ce375c9b9c0a44cf`  
		Last Modified: Fri, 17 Apr 2026 00:30:15 GMT  
		Size: 50.5 MB (50451820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6c03c0be2850f9c82b37631d6cba13fdd3f1e632d3643edc54d2cdc6edf2c9`  
		Last Modified: Fri, 17 Apr 2026 00:30:13 GMT  
		Size: 11.8 MB (11775863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aea5f86be29cb56a759d7142f5a9b62bfd6ed99d100b921dd3a33e4ce9314a5`  
		Last Modified: Fri, 17 Apr 2026 00:30:13 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ef07b04bbe77eb925cb81d0e6082ce24328e0d2c296d61c460e11aa33b6b3a`  
		Last Modified: Fri, 17 Apr 2026 00:30:14 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ddd87b55db792237d8b7cd099de585015d86816d1215b2f57c4dd5011ba91e`  
		Last Modified: Fri, 17 Apr 2026 00:30:15 GMT  
		Size: 6.3 KB (6283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8.0-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:40fca214b400941be68a739f6f59448a6e931f730682c1d89026fee13fe21c34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **946.1 KB (946058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7f880a5909c565d62181a36572e16dac17e9bb0131551dfa514d962d26c4a97`

```dockerfile
```

-	Layers:
	-	`sha256:33f778c6f613bedfa5d2ec41b08b10f6bf6ce196ef899601b0ec66f7637095f3`  
		Last Modified: Fri, 17 Apr 2026 00:30:12 GMT  
		Size: 915.2 KB (915211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:629ffea1f9f8527114e2ed5a812a800fe7b6e1a1947e4b14a6b8302f319cb11d`  
		Last Modified: Fri, 17 Apr 2026 00:30:12 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.8.0-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:1d6e285b1a5e3fa23695d08c8586d0d17c004443a83a93e22a40d9f7c449227c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.0 MB (78965173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ba6389eb739af52c14de9f6ed96efacfbe53dccc3e41f42ab1f51fef176da67`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:13 GMT
ADD alpine-minirootfs-3.21.7-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:13 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:31:02 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 00:31:03 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:31:03 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 17 Apr 2026 00:31:04 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Fri, 17 Apr 2026 00:31:07 GMT
ENV INFLUXDB_VERSION=2.8.0
# Fri, 17 Apr 2026 00:31:07 GMT
ENV INFLUXDB_PR=-2
# Fri, 17 Apr 2026 00:31:07 GMT
ENV INFLUXDB_PV=2.8.0-2
# Fri, 17 Apr 2026 00:31:07 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Fri, 17 Apr 2026 00:31:07 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Fri, 17 Apr 2026 00:31:07 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 17 Apr 2026 00:31:08 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 17 Apr 2026 00:31:08 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 17 Apr 2026 00:31:08 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 17 Apr 2026 00:31:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:31:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:31:08 GMT
CMD ["influxd"]
# Fri, 17 Apr 2026 00:31:08 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 17 Apr 2026 00:31:08 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 17 Apr 2026 00:31:08 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 17 Apr 2026 00:31:08 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 17 Apr 2026 00:31:08 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:2dd7199cff98a7400e801cbfad6de906972a4e3dd0a749d4c1b80f5a1e3e4108`  
		Last Modified: Thu, 16 Apr 2026 05:32:50 GMT  
		Size: 4.0 MB (3994465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f652e0c01e29334dc1fe16c1d56127042156c3a64857b4a0ead43d3986f7986`  
		Last Modified: Fri, 17 Apr 2026 00:31:17 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5ddaea2126344e5b11cf5e6c97cd44d5b59a15fabcb438bb0a343fd2c1b7162`  
		Last Modified: Fri, 17 Apr 2026 00:31:18 GMT  
		Size: 9.8 MB (9842397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9394ce182bd0c5ee862a0d2428947e1a0d0fc3da081624b53bb5b05e37972f48`  
		Last Modified: Fri, 17 Apr 2026 00:31:17 GMT  
		Size: 5.8 MB (5790430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98541319cbb33b6799c13cddcd9cd7e00fe5295fea9954da3eaa7af2a1be8ca9`  
		Last Modified: Fri, 17 Apr 2026 00:31:17 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872f29647bbd3f39d47cc2a6b1b76f958b61aeb29480eec96b42c03288cd1472`  
		Last Modified: Fri, 17 Apr 2026 00:31:20 GMT  
		Size: 48.2 MB (48229511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff3598b437a8492690885c52bd82ed6d9ba85af743856cdcdc03e23cff14b84b`  
		Last Modified: Fri, 17 Apr 2026 00:31:19 GMT  
		Size: 11.1 MB (11100414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca69b2befa8351ec86c62df1caca82193562d274be054f00c148c6b5f5ba67b`  
		Last Modified: Fri, 17 Apr 2026 00:31:18 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba50550e7b2ebf586c1c93af205b4fb509ff55bfeda64342a548be9f7eb0b4d`  
		Last Modified: Fri, 17 Apr 2026 00:31:19 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8195a95763ebcb79e75c6db51ef9341b1678f6bd5070f114326209a91fff3bb8`  
		Last Modified: Fri, 17 Apr 2026 00:31:20 GMT  
		Size: 6.3 KB (6284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8.0-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:866fdba0f42c46c21ba2c8d62ea1a6c90a46ca6d38e54989b009617072a3b43c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **945.5 KB (945503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48090246a2f4e0d9530f4b14c374ee2497817d1ef5d6807100cc1f963980061`

```dockerfile
```

-	Layers:
	-	`sha256:7f3a296bce432225eae41d3f9ad0d93e77867c28796a18dbaf6693ac05624f1b`  
		Last Modified: Fri, 17 Apr 2026 00:31:17 GMT  
		Size: 914.5 KB (914462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0eb74c7252a3cb8f2dd15f0ae328f0107f804876760828392c2573c155759432`  
		Last Modified: Fri, 17 Apr 2026 00:31:17 GMT  
		Size: 31.0 KB (31041 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3-core`

```console
$ docker pull influxdb@sha256:1d58c8b9ac90153ae3a020ede2810c8284933dda50ac71e7573389ab6f012128
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-core` - linux; amd64

```console
$ docker pull influxdb@sha256:fe11b1e876597df9299d3f35411960587f2b5f2815dcef6a9f1f5a6ac8cd3ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149120890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c93d5f48b898003bdfb0e9ac56040cf4ff0645836b8f0439e8f0d0c00a3442fd`
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
# Wed, 15 Apr 2026 20:43:28 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 15 Apr 2026 20:43:28 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 15 Apr 2026 20:43:33 GMT
ENV INFLUXDB_VERSION=3.9.1
# Wed, 15 Apr 2026 20:43:33 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 15 Apr 2026 20:43:33 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:43:33 GMT
USER influxdb3
# Wed, 15 Apr 2026 20:43:33 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 15 Apr 2026 20:43:33 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 15 Apr 2026 20:43:33 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 15 Apr 2026 20:43:33 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 15 Apr 2026 20:43:33 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 15 Apr 2026 20:43:33 GMT
ENV LOG_FILTER=info
# Wed, 15 Apr 2026 20:43:33 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 15 Apr 2026 20:43:33 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 15 Apr 2026 20:43:33 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb85a1612071842cc709708034e092cd219f01edf4a9b9762c0f183a3441ecf`  
		Last Modified: Wed, 15 Apr 2026 20:43:51 GMT  
		Size: 6.7 MB (6671641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b32837ce4e56248bf07e7ff916abed714dbe90eb6395eebac86b090f5cac87`  
		Last Modified: Wed, 15 Apr 2026 20:43:51 GMT  
		Size: 3.6 KB (3644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b097d884f34508800b955f7367bf2eb4bcbc6da1428ee8e6f065581cf2e22f25`  
		Last Modified: Wed, 15 Apr 2026 20:43:53 GMT  
		Size: 112.7 MB (112711959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ded072d71b9df4d79d6fcb4f2d1886ffc352ee501284d55301d15e27f8c638`  
		Last Modified: Wed, 15 Apr 2026 20:43:51 GMT  
		Size: 518.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ea4f908e157134e7630698fc0d7d5382c889cf502f09fd3bb603cd23691d1a`  
		Last Modified: Wed, 15 Apr 2026 20:43:52 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:652471149c89e684e9191468501e341d603a736695f0b144375211385cc6094b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b9dd6e9add57346769772585ff6d04d3fe25307ef017476731d4eefa017ce2`

```dockerfile
```

-	Layers:
	-	`sha256:4551c43b7943abba7b3ded791c92a4c94a59e338ea16063ac500d5045ef18be4`  
		Last Modified: Wed, 15 Apr 2026 20:43:51 GMT  
		Size: 2.3 MB (2310597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63aafdd4a6f1432a8324260dc22045c383a922f0e4a4a5d0369ceec7db4c9532`  
		Last Modified: Wed, 15 Apr 2026 20:43:50 GMT  
		Size: 17.6 KB (17619 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:81681dee889cc3a3e5ed75687baedd16c5879379204d30b378c01da5623af612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140062904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c9c1af5bc3c9718fdc8ba857d3dfc6bc07b8c3be495603f5dbc76b9f52b4be5`
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
# Wed, 15 Apr 2026 20:43:36 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 15 Apr 2026 20:43:37 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 15 Apr 2026 20:43:42 GMT
ENV INFLUXDB_VERSION=3.9.1
# Wed, 15 Apr 2026 20:43:42 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 15 Apr 2026 20:43:42 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:43:42 GMT
USER influxdb3
# Wed, 15 Apr 2026 20:43:42 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 15 Apr 2026 20:43:42 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 15 Apr 2026 20:43:42 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 15 Apr 2026 20:43:42 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 15 Apr 2026 20:43:42 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 15 Apr 2026 20:43:42 GMT
ENV LOG_FILTER=info
# Wed, 15 Apr 2026 20:43:42 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 15 Apr 2026 20:43:42 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 15 Apr 2026 20:43:42 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f08ac250787db9f963390f932e1c5da35f7e8c89ca9da7b9042fd0957365d86`  
		Last Modified: Wed, 15 Apr 2026 20:43:58 GMT  
		Size: 6.7 MB (6681852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1206008ad447c4fd90bb7cc623cdb10e613f182f166550529e8ccd4f6df65f3`  
		Last Modified: Wed, 15 Apr 2026 20:43:58 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4de3b0cf867358d35a07dda31a27e09112537c510d666c5e85dc48f38b9948`  
		Last Modified: Wed, 15 Apr 2026 20:44:00 GMT  
		Size: 104.5 MB (104500945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab531844cdf13d434c23663168a76540de29e691f5f74aa4d00859fa9b56adc`  
		Last Modified: Wed, 15 Apr 2026 20:43:58 GMT  
		Size: 520.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd3a466131393335a59d93e8a5df450632faed8b450e18e03fa9445df50d544`  
		Last Modified: Wed, 15 Apr 2026 20:43:59 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:9b378c72d59a92a91ad9ebd029c180e55cab7308cf5d5f99decc684ad8065254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6945d6a683f4c1a88ffe161de85441ad6200e506e8267681c57c8e0fe6a81807`

```dockerfile
```

-	Layers:
	-	`sha256:4289a8ee02ce5554b7f057d2bcda399af9b640aac1bfcd448d13090d65f9728c`  
		Last Modified: Wed, 15 Apr 2026 20:43:58 GMT  
		Size: 2.3 MB (2311679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7ec699b6edea9a3daa2eed69aca2520bae97c228253d9d921690eaf16410244`  
		Last Modified: Wed, 15 Apr 2026 20:43:58 GMT  
		Size: 17.8 KB (17769 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3-enterprise`

```console
$ docker pull influxdb@sha256:4113f82acd887c5d0228865dbe6b3591794d78b6057458d655eef7f7b937a6aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:7781d9f311036bbb44141f6983369f29b467a1fc82c3d9c3c3993f07adb9edaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.9 MB (159923454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14c982870ed0f2165579cc75426eb003f3ec1cf0501b950e53146052e68a7b34`
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
# Wed, 15 Apr 2026 20:43:33 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 15 Apr 2026 20:43:33 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 15 Apr 2026 20:43:39 GMT
ENV INFLUXDB_VERSION=3.9.1
# Wed, 15 Apr 2026 20:43:39 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 15 Apr 2026 20:43:39 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:43:39 GMT
USER influxdb3
# Wed, 15 Apr 2026 20:43:39 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 15 Apr 2026 20:43:39 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 15 Apr 2026 20:43:39 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 15 Apr 2026 20:43:39 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 15 Apr 2026 20:43:39 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 15 Apr 2026 20:43:39 GMT
ENV LOG_FILTER=info
# Wed, 15 Apr 2026 20:43:39 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 15 Apr 2026 20:43:39 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 15 Apr 2026 20:43:39 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e0999e8f1462fbb09cb39ef08c282eda58df5d1e8c389005f194ea00cccecf`  
		Last Modified: Wed, 15 Apr 2026 20:43:59 GMT  
		Size: 6.7 MB (6671623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f38afebbd5132d82f9901425991a82a49bf410374f60e1b0ba57e420f0d33a6e`  
		Last Modified: Wed, 15 Apr 2026 20:43:59 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08080051254204def33427dfac5ec1b091a9b5849d1552a1ca4e632b7441b59`  
		Last Modified: Wed, 15 Apr 2026 20:44:02 GMT  
		Size: 123.5 MB (123514533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d79ef371b5b265f128726acb79e36bd502e0227916d0f86fbf724d348d58da6`  
		Last Modified: Wed, 15 Apr 2026 20:43:59 GMT  
		Size: 518.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42215201c4d468436362f05d42e64e4431e5fc007db05220d0f0b4d3e72419ca`  
		Last Modified: Wed, 15 Apr 2026 20:44:00 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:f3f71dc42bfbbfd2a66fc92826a16ba17524e254845208f94ac1b9e601993189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52b6fa96bed968f1e3db363fbbbb9c073c019f438e75ca05b5cc05d1db2012a8`

```dockerfile
```

-	Layers:
	-	`sha256:7044d2ea7b43afb998f551a78cc6cca87a848c19440a08858760886060d29034`  
		Last Modified: Wed, 15 Apr 2026 20:43:59 GMT  
		Size: 2.3 MB (2310645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0dc250eea8be207f77782a07b795db475744e9fb46ff0cbf67acc02fd41ce4a`  
		Last Modified: Wed, 15 Apr 2026 20:43:59 GMT  
		Size: 17.8 KB (17800 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:50dfce3b801a3bb452684d5744f928286d8d70682cab1d39d80e53580a094a96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.8 MB (150758023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bf7cc1716fb81f0809d6de6a2da460353e027e871816f1904a91dbf4c8ed482`
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
# Wed, 15 Apr 2026 20:43:40 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 15 Apr 2026 20:43:40 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 15 Apr 2026 20:43:45 GMT
ENV INFLUXDB_VERSION=3.9.1
# Wed, 15 Apr 2026 20:43:45 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 15 Apr 2026 20:43:45 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:43:45 GMT
USER influxdb3
# Wed, 15 Apr 2026 20:43:46 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 15 Apr 2026 20:43:46 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 15 Apr 2026 20:43:46 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 15 Apr 2026 20:43:46 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 15 Apr 2026 20:43:46 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 15 Apr 2026 20:43:46 GMT
ENV LOG_FILTER=info
# Wed, 15 Apr 2026 20:43:46 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 15 Apr 2026 20:43:46 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 15 Apr 2026 20:43:46 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e62244524400b4e44e3ad020813e0a0618188bb064c5732855c664af09a06f`  
		Last Modified: Wed, 15 Apr 2026 20:44:03 GMT  
		Size: 6.7 MB (6681811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16cf1620991e32dbed4397cdb8eb7293d57ee810171bf8c1a886dddd30185cb9`  
		Last Modified: Wed, 15 Apr 2026 20:44:03 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa7bb728ae5e717ec96034e40136c46b01ea54f9d2b9142f000fbca57e405353`  
		Last Modified: Wed, 15 Apr 2026 20:44:06 GMT  
		Size: 115.2 MB (115196105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69fd7d303d393e57b9f180646bdde3ef3cbf21f9612aac91a2a17c4430410f93`  
		Last Modified: Wed, 15 Apr 2026 20:44:03 GMT  
		Size: 519.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e591569b32d278adfe2b3b261c7775fbaade74d1da69cbfda55f85e1be4d613`  
		Last Modified: Wed, 15 Apr 2026 20:44:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:745f936b54711018736135ccfc600a044e5ae237c330e17c303f3856250ae77b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe0ed19d8d0b7ccbf973e3ca952ebe95b6391b09e5363c6bc98b16359316256f`

```dockerfile
```

-	Layers:
	-	`sha256:5beb6f6b3a5737648090b5d78aadc2bc4d7e778c10f15d2da4c1621082b926bf`  
		Last Modified: Wed, 15 Apr 2026 20:44:03 GMT  
		Size: 2.3 MB (2311727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46b2310865e366114310e7a1d79734538d6ff848e247c157eeaac77405db85e5`  
		Last Modified: Wed, 15 Apr 2026 20:44:02 GMT  
		Size: 17.9 KB (17949 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.9-core`

```console
$ docker pull influxdb@sha256:1d58c8b9ac90153ae3a020ede2810c8284933dda50ac71e7573389ab6f012128
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.9-core` - linux; amd64

```console
$ docker pull influxdb@sha256:fe11b1e876597df9299d3f35411960587f2b5f2815dcef6a9f1f5a6ac8cd3ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149120890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c93d5f48b898003bdfb0e9ac56040cf4ff0645836b8f0439e8f0d0c00a3442fd`
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
# Wed, 15 Apr 2026 20:43:28 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 15 Apr 2026 20:43:28 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 15 Apr 2026 20:43:33 GMT
ENV INFLUXDB_VERSION=3.9.1
# Wed, 15 Apr 2026 20:43:33 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 15 Apr 2026 20:43:33 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:43:33 GMT
USER influxdb3
# Wed, 15 Apr 2026 20:43:33 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 15 Apr 2026 20:43:33 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 15 Apr 2026 20:43:33 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 15 Apr 2026 20:43:33 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 15 Apr 2026 20:43:33 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 15 Apr 2026 20:43:33 GMT
ENV LOG_FILTER=info
# Wed, 15 Apr 2026 20:43:33 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 15 Apr 2026 20:43:33 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 15 Apr 2026 20:43:33 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb85a1612071842cc709708034e092cd219f01edf4a9b9762c0f183a3441ecf`  
		Last Modified: Wed, 15 Apr 2026 20:43:51 GMT  
		Size: 6.7 MB (6671641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b32837ce4e56248bf07e7ff916abed714dbe90eb6395eebac86b090f5cac87`  
		Last Modified: Wed, 15 Apr 2026 20:43:51 GMT  
		Size: 3.6 KB (3644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b097d884f34508800b955f7367bf2eb4bcbc6da1428ee8e6f065581cf2e22f25`  
		Last Modified: Wed, 15 Apr 2026 20:43:53 GMT  
		Size: 112.7 MB (112711959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ded072d71b9df4d79d6fcb4f2d1886ffc352ee501284d55301d15e27f8c638`  
		Last Modified: Wed, 15 Apr 2026 20:43:51 GMT  
		Size: 518.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ea4f908e157134e7630698fc0d7d5382c889cf502f09fd3bb603cd23691d1a`  
		Last Modified: Wed, 15 Apr 2026 20:43:52 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.9-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:652471149c89e684e9191468501e341d603a736695f0b144375211385cc6094b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b9dd6e9add57346769772585ff6d04d3fe25307ef017476731d4eefa017ce2`

```dockerfile
```

-	Layers:
	-	`sha256:4551c43b7943abba7b3ded791c92a4c94a59e338ea16063ac500d5045ef18be4`  
		Last Modified: Wed, 15 Apr 2026 20:43:51 GMT  
		Size: 2.3 MB (2310597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63aafdd4a6f1432a8324260dc22045c383a922f0e4a4a5d0369ceec7db4c9532`  
		Last Modified: Wed, 15 Apr 2026 20:43:50 GMT  
		Size: 17.6 KB (17619 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.9-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:81681dee889cc3a3e5ed75687baedd16c5879379204d30b378c01da5623af612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140062904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c9c1af5bc3c9718fdc8ba857d3dfc6bc07b8c3be495603f5dbc76b9f52b4be5`
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
# Wed, 15 Apr 2026 20:43:36 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 15 Apr 2026 20:43:37 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 15 Apr 2026 20:43:42 GMT
ENV INFLUXDB_VERSION=3.9.1
# Wed, 15 Apr 2026 20:43:42 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 15 Apr 2026 20:43:42 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:43:42 GMT
USER influxdb3
# Wed, 15 Apr 2026 20:43:42 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 15 Apr 2026 20:43:42 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 15 Apr 2026 20:43:42 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 15 Apr 2026 20:43:42 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 15 Apr 2026 20:43:42 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 15 Apr 2026 20:43:42 GMT
ENV LOG_FILTER=info
# Wed, 15 Apr 2026 20:43:42 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 15 Apr 2026 20:43:42 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 15 Apr 2026 20:43:42 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f08ac250787db9f963390f932e1c5da35f7e8c89ca9da7b9042fd0957365d86`  
		Last Modified: Wed, 15 Apr 2026 20:43:58 GMT  
		Size: 6.7 MB (6681852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1206008ad447c4fd90bb7cc623cdb10e613f182f166550529e8ccd4f6df65f3`  
		Last Modified: Wed, 15 Apr 2026 20:43:58 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4de3b0cf867358d35a07dda31a27e09112537c510d666c5e85dc48f38b9948`  
		Last Modified: Wed, 15 Apr 2026 20:44:00 GMT  
		Size: 104.5 MB (104500945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab531844cdf13d434c23663168a76540de29e691f5f74aa4d00859fa9b56adc`  
		Last Modified: Wed, 15 Apr 2026 20:43:58 GMT  
		Size: 520.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd3a466131393335a59d93e8a5df450632faed8b450e18e03fa9445df50d544`  
		Last Modified: Wed, 15 Apr 2026 20:43:59 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.9-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:9b378c72d59a92a91ad9ebd029c180e55cab7308cf5d5f99decc684ad8065254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6945d6a683f4c1a88ffe161de85441ad6200e506e8267681c57c8e0fe6a81807`

```dockerfile
```

-	Layers:
	-	`sha256:4289a8ee02ce5554b7f057d2bcda399af9b640aac1bfcd448d13090d65f9728c`  
		Last Modified: Wed, 15 Apr 2026 20:43:58 GMT  
		Size: 2.3 MB (2311679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7ec699b6edea9a3daa2eed69aca2520bae97c228253d9d921690eaf16410244`  
		Last Modified: Wed, 15 Apr 2026 20:43:58 GMT  
		Size: 17.8 KB (17769 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.9-enterprise`

```console
$ docker pull influxdb@sha256:4113f82acd887c5d0228865dbe6b3591794d78b6057458d655eef7f7b937a6aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.9-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:7781d9f311036bbb44141f6983369f29b467a1fc82c3d9c3c3993f07adb9edaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.9 MB (159923454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14c982870ed0f2165579cc75426eb003f3ec1cf0501b950e53146052e68a7b34`
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
# Wed, 15 Apr 2026 20:43:33 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 15 Apr 2026 20:43:33 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 15 Apr 2026 20:43:39 GMT
ENV INFLUXDB_VERSION=3.9.1
# Wed, 15 Apr 2026 20:43:39 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 15 Apr 2026 20:43:39 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:43:39 GMT
USER influxdb3
# Wed, 15 Apr 2026 20:43:39 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 15 Apr 2026 20:43:39 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 15 Apr 2026 20:43:39 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 15 Apr 2026 20:43:39 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 15 Apr 2026 20:43:39 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 15 Apr 2026 20:43:39 GMT
ENV LOG_FILTER=info
# Wed, 15 Apr 2026 20:43:39 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 15 Apr 2026 20:43:39 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 15 Apr 2026 20:43:39 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e0999e8f1462fbb09cb39ef08c282eda58df5d1e8c389005f194ea00cccecf`  
		Last Modified: Wed, 15 Apr 2026 20:43:59 GMT  
		Size: 6.7 MB (6671623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f38afebbd5132d82f9901425991a82a49bf410374f60e1b0ba57e420f0d33a6e`  
		Last Modified: Wed, 15 Apr 2026 20:43:59 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08080051254204def33427dfac5ec1b091a9b5849d1552a1ca4e632b7441b59`  
		Last Modified: Wed, 15 Apr 2026 20:44:02 GMT  
		Size: 123.5 MB (123514533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d79ef371b5b265f128726acb79e36bd502e0227916d0f86fbf724d348d58da6`  
		Last Modified: Wed, 15 Apr 2026 20:43:59 GMT  
		Size: 518.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42215201c4d468436362f05d42e64e4431e5fc007db05220d0f0b4d3e72419ca`  
		Last Modified: Wed, 15 Apr 2026 20:44:00 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.9-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:f3f71dc42bfbbfd2a66fc92826a16ba17524e254845208f94ac1b9e601993189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52b6fa96bed968f1e3db363fbbbb9c073c019f438e75ca05b5cc05d1db2012a8`

```dockerfile
```

-	Layers:
	-	`sha256:7044d2ea7b43afb998f551a78cc6cca87a848c19440a08858760886060d29034`  
		Last Modified: Wed, 15 Apr 2026 20:43:59 GMT  
		Size: 2.3 MB (2310645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0dc250eea8be207f77782a07b795db475744e9fb46ff0cbf67acc02fd41ce4a`  
		Last Modified: Wed, 15 Apr 2026 20:43:59 GMT  
		Size: 17.8 KB (17800 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.9-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:50dfce3b801a3bb452684d5744f928286d8d70682cab1d39d80e53580a094a96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.8 MB (150758023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bf7cc1716fb81f0809d6de6a2da460353e027e871816f1904a91dbf4c8ed482`
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
# Wed, 15 Apr 2026 20:43:40 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 15 Apr 2026 20:43:40 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 15 Apr 2026 20:43:45 GMT
ENV INFLUXDB_VERSION=3.9.1
# Wed, 15 Apr 2026 20:43:45 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 15 Apr 2026 20:43:45 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:43:45 GMT
USER influxdb3
# Wed, 15 Apr 2026 20:43:46 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 15 Apr 2026 20:43:46 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 15 Apr 2026 20:43:46 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 15 Apr 2026 20:43:46 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 15 Apr 2026 20:43:46 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 15 Apr 2026 20:43:46 GMT
ENV LOG_FILTER=info
# Wed, 15 Apr 2026 20:43:46 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 15 Apr 2026 20:43:46 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 15 Apr 2026 20:43:46 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e62244524400b4e44e3ad020813e0a0618188bb064c5732855c664af09a06f`  
		Last Modified: Wed, 15 Apr 2026 20:44:03 GMT  
		Size: 6.7 MB (6681811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16cf1620991e32dbed4397cdb8eb7293d57ee810171bf8c1a886dddd30185cb9`  
		Last Modified: Wed, 15 Apr 2026 20:44:03 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa7bb728ae5e717ec96034e40136c46b01ea54f9d2b9142f000fbca57e405353`  
		Last Modified: Wed, 15 Apr 2026 20:44:06 GMT  
		Size: 115.2 MB (115196105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69fd7d303d393e57b9f180646bdde3ef3cbf21f9612aac91a2a17c4430410f93`  
		Last Modified: Wed, 15 Apr 2026 20:44:03 GMT  
		Size: 519.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e591569b32d278adfe2b3b261c7775fbaade74d1da69cbfda55f85e1be4d613`  
		Last Modified: Wed, 15 Apr 2026 20:44:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.9-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:745f936b54711018736135ccfc600a044e5ae237c330e17c303f3856250ae77b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe0ed19d8d0b7ccbf973e3ca952ebe95b6391b09e5363c6bc98b16359316256f`

```dockerfile
```

-	Layers:
	-	`sha256:5beb6f6b3a5737648090b5d78aadc2bc4d7e778c10f15d2da4c1621082b926bf`  
		Last Modified: Wed, 15 Apr 2026 20:44:03 GMT  
		Size: 2.3 MB (2311727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46b2310865e366114310e7a1d79734538d6ff848e247c157eeaac77405db85e5`  
		Last Modified: Wed, 15 Apr 2026 20:44:02 GMT  
		Size: 17.9 KB (17949 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.9.1-core`

```console
$ docker pull influxdb@sha256:1d58c8b9ac90153ae3a020ede2810c8284933dda50ac71e7573389ab6f012128
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.9.1-core` - linux; amd64

```console
$ docker pull influxdb@sha256:fe11b1e876597df9299d3f35411960587f2b5f2815dcef6a9f1f5a6ac8cd3ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149120890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c93d5f48b898003bdfb0e9ac56040cf4ff0645836b8f0439e8f0d0c00a3442fd`
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
# Wed, 15 Apr 2026 20:43:28 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 15 Apr 2026 20:43:28 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 15 Apr 2026 20:43:33 GMT
ENV INFLUXDB_VERSION=3.9.1
# Wed, 15 Apr 2026 20:43:33 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 15 Apr 2026 20:43:33 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:43:33 GMT
USER influxdb3
# Wed, 15 Apr 2026 20:43:33 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 15 Apr 2026 20:43:33 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 15 Apr 2026 20:43:33 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 15 Apr 2026 20:43:33 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 15 Apr 2026 20:43:33 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 15 Apr 2026 20:43:33 GMT
ENV LOG_FILTER=info
# Wed, 15 Apr 2026 20:43:33 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 15 Apr 2026 20:43:33 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 15 Apr 2026 20:43:33 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb85a1612071842cc709708034e092cd219f01edf4a9b9762c0f183a3441ecf`  
		Last Modified: Wed, 15 Apr 2026 20:43:51 GMT  
		Size: 6.7 MB (6671641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b32837ce4e56248bf07e7ff916abed714dbe90eb6395eebac86b090f5cac87`  
		Last Modified: Wed, 15 Apr 2026 20:43:51 GMT  
		Size: 3.6 KB (3644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b097d884f34508800b955f7367bf2eb4bcbc6da1428ee8e6f065581cf2e22f25`  
		Last Modified: Wed, 15 Apr 2026 20:43:53 GMT  
		Size: 112.7 MB (112711959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ded072d71b9df4d79d6fcb4f2d1886ffc352ee501284d55301d15e27f8c638`  
		Last Modified: Wed, 15 Apr 2026 20:43:51 GMT  
		Size: 518.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ea4f908e157134e7630698fc0d7d5382c889cf502f09fd3bb603cd23691d1a`  
		Last Modified: Wed, 15 Apr 2026 20:43:52 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.9.1-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:652471149c89e684e9191468501e341d603a736695f0b144375211385cc6094b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b9dd6e9add57346769772585ff6d04d3fe25307ef017476731d4eefa017ce2`

```dockerfile
```

-	Layers:
	-	`sha256:4551c43b7943abba7b3ded791c92a4c94a59e338ea16063ac500d5045ef18be4`  
		Last Modified: Wed, 15 Apr 2026 20:43:51 GMT  
		Size: 2.3 MB (2310597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63aafdd4a6f1432a8324260dc22045c383a922f0e4a4a5d0369ceec7db4c9532`  
		Last Modified: Wed, 15 Apr 2026 20:43:50 GMT  
		Size: 17.6 KB (17619 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.9.1-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:81681dee889cc3a3e5ed75687baedd16c5879379204d30b378c01da5623af612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140062904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c9c1af5bc3c9718fdc8ba857d3dfc6bc07b8c3be495603f5dbc76b9f52b4be5`
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
# Wed, 15 Apr 2026 20:43:36 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 15 Apr 2026 20:43:37 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 15 Apr 2026 20:43:42 GMT
ENV INFLUXDB_VERSION=3.9.1
# Wed, 15 Apr 2026 20:43:42 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 15 Apr 2026 20:43:42 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:43:42 GMT
USER influxdb3
# Wed, 15 Apr 2026 20:43:42 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 15 Apr 2026 20:43:42 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 15 Apr 2026 20:43:42 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 15 Apr 2026 20:43:42 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 15 Apr 2026 20:43:42 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 15 Apr 2026 20:43:42 GMT
ENV LOG_FILTER=info
# Wed, 15 Apr 2026 20:43:42 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 15 Apr 2026 20:43:42 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 15 Apr 2026 20:43:42 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f08ac250787db9f963390f932e1c5da35f7e8c89ca9da7b9042fd0957365d86`  
		Last Modified: Wed, 15 Apr 2026 20:43:58 GMT  
		Size: 6.7 MB (6681852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1206008ad447c4fd90bb7cc623cdb10e613f182f166550529e8ccd4f6df65f3`  
		Last Modified: Wed, 15 Apr 2026 20:43:58 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4de3b0cf867358d35a07dda31a27e09112537c510d666c5e85dc48f38b9948`  
		Last Modified: Wed, 15 Apr 2026 20:44:00 GMT  
		Size: 104.5 MB (104500945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab531844cdf13d434c23663168a76540de29e691f5f74aa4d00859fa9b56adc`  
		Last Modified: Wed, 15 Apr 2026 20:43:58 GMT  
		Size: 520.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd3a466131393335a59d93e8a5df450632faed8b450e18e03fa9445df50d544`  
		Last Modified: Wed, 15 Apr 2026 20:43:59 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.9.1-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:9b378c72d59a92a91ad9ebd029c180e55cab7308cf5d5f99decc684ad8065254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6945d6a683f4c1a88ffe161de85441ad6200e506e8267681c57c8e0fe6a81807`

```dockerfile
```

-	Layers:
	-	`sha256:4289a8ee02ce5554b7f057d2bcda399af9b640aac1bfcd448d13090d65f9728c`  
		Last Modified: Wed, 15 Apr 2026 20:43:58 GMT  
		Size: 2.3 MB (2311679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7ec699b6edea9a3daa2eed69aca2520bae97c228253d9d921690eaf16410244`  
		Last Modified: Wed, 15 Apr 2026 20:43:58 GMT  
		Size: 17.8 KB (17769 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.9.1-enterprise`

```console
$ docker pull influxdb@sha256:4113f82acd887c5d0228865dbe6b3591794d78b6057458d655eef7f7b937a6aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.9.1-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:7781d9f311036bbb44141f6983369f29b467a1fc82c3d9c3c3993f07adb9edaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.9 MB (159923454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14c982870ed0f2165579cc75426eb003f3ec1cf0501b950e53146052e68a7b34`
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
# Wed, 15 Apr 2026 20:43:33 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 15 Apr 2026 20:43:33 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 15 Apr 2026 20:43:39 GMT
ENV INFLUXDB_VERSION=3.9.1
# Wed, 15 Apr 2026 20:43:39 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 15 Apr 2026 20:43:39 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:43:39 GMT
USER influxdb3
# Wed, 15 Apr 2026 20:43:39 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 15 Apr 2026 20:43:39 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 15 Apr 2026 20:43:39 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 15 Apr 2026 20:43:39 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 15 Apr 2026 20:43:39 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 15 Apr 2026 20:43:39 GMT
ENV LOG_FILTER=info
# Wed, 15 Apr 2026 20:43:39 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 15 Apr 2026 20:43:39 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 15 Apr 2026 20:43:39 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e0999e8f1462fbb09cb39ef08c282eda58df5d1e8c389005f194ea00cccecf`  
		Last Modified: Wed, 15 Apr 2026 20:43:59 GMT  
		Size: 6.7 MB (6671623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f38afebbd5132d82f9901425991a82a49bf410374f60e1b0ba57e420f0d33a6e`  
		Last Modified: Wed, 15 Apr 2026 20:43:59 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08080051254204def33427dfac5ec1b091a9b5849d1552a1ca4e632b7441b59`  
		Last Modified: Wed, 15 Apr 2026 20:44:02 GMT  
		Size: 123.5 MB (123514533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d79ef371b5b265f128726acb79e36bd502e0227916d0f86fbf724d348d58da6`  
		Last Modified: Wed, 15 Apr 2026 20:43:59 GMT  
		Size: 518.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42215201c4d468436362f05d42e64e4431e5fc007db05220d0f0b4d3e72419ca`  
		Last Modified: Wed, 15 Apr 2026 20:44:00 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.9.1-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:f3f71dc42bfbbfd2a66fc92826a16ba17524e254845208f94ac1b9e601993189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52b6fa96bed968f1e3db363fbbbb9c073c019f438e75ca05b5cc05d1db2012a8`

```dockerfile
```

-	Layers:
	-	`sha256:7044d2ea7b43afb998f551a78cc6cca87a848c19440a08858760886060d29034`  
		Last Modified: Wed, 15 Apr 2026 20:43:59 GMT  
		Size: 2.3 MB (2310645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0dc250eea8be207f77782a07b795db475744e9fb46ff0cbf67acc02fd41ce4a`  
		Last Modified: Wed, 15 Apr 2026 20:43:59 GMT  
		Size: 17.8 KB (17800 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.9.1-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:50dfce3b801a3bb452684d5744f928286d8d70682cab1d39d80e53580a094a96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.8 MB (150758023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bf7cc1716fb81f0809d6de6a2da460353e027e871816f1904a91dbf4c8ed482`
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
# Wed, 15 Apr 2026 20:43:40 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 15 Apr 2026 20:43:40 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 15 Apr 2026 20:43:45 GMT
ENV INFLUXDB_VERSION=3.9.1
# Wed, 15 Apr 2026 20:43:45 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 15 Apr 2026 20:43:45 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:43:45 GMT
USER influxdb3
# Wed, 15 Apr 2026 20:43:46 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 15 Apr 2026 20:43:46 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 15 Apr 2026 20:43:46 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 15 Apr 2026 20:43:46 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 15 Apr 2026 20:43:46 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 15 Apr 2026 20:43:46 GMT
ENV LOG_FILTER=info
# Wed, 15 Apr 2026 20:43:46 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 15 Apr 2026 20:43:46 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 15 Apr 2026 20:43:46 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e62244524400b4e44e3ad020813e0a0618188bb064c5732855c664af09a06f`  
		Last Modified: Wed, 15 Apr 2026 20:44:03 GMT  
		Size: 6.7 MB (6681811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16cf1620991e32dbed4397cdb8eb7293d57ee810171bf8c1a886dddd30185cb9`  
		Last Modified: Wed, 15 Apr 2026 20:44:03 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa7bb728ae5e717ec96034e40136c46b01ea54f9d2b9142f000fbca57e405353`  
		Last Modified: Wed, 15 Apr 2026 20:44:06 GMT  
		Size: 115.2 MB (115196105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69fd7d303d393e57b9f180646bdde3ef3cbf21f9612aac91a2a17c4430410f93`  
		Last Modified: Wed, 15 Apr 2026 20:44:03 GMT  
		Size: 519.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e591569b32d278adfe2b3b261c7775fbaade74d1da69cbfda55f85e1be4d613`  
		Last Modified: Wed, 15 Apr 2026 20:44:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.9.1-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:745f936b54711018736135ccfc600a044e5ae237c330e17c303f3856250ae77b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe0ed19d8d0b7ccbf973e3ca952ebe95b6391b09e5363c6bc98b16359316256f`

```dockerfile
```

-	Layers:
	-	`sha256:5beb6f6b3a5737648090b5d78aadc2bc4d7e778c10f15d2da4c1621082b926bf`  
		Last Modified: Wed, 15 Apr 2026 20:44:03 GMT  
		Size: 2.3 MB (2311727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46b2310865e366114310e7a1d79734538d6ff848e247c157eeaac77405db85e5`  
		Last Modified: Wed, 15 Apr 2026 20:44:02 GMT  
		Size: 17.9 KB (17949 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:4f90d40c00193d91889ad872c39a586a011db4ac4d1a766e248d9cbbcc6cec3e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:ef8bad9a5c5f604e1a139b7b99c452bc9cb62affdcb9f11afad1b2e5c20c45a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81923288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70540d47f741606ec70538d2489a54d267d7fd74f4b276a176e53ad8c2efacf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:29:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 00:29:56 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:29:56 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 17 Apr 2026 00:29:56 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Fri, 17 Apr 2026 00:30:00 GMT
ENV INFLUXDB_VERSION=2.8.0
# Fri, 17 Apr 2026 00:30:00 GMT
ENV INFLUXDB_PR=-2
# Fri, 17 Apr 2026 00:30:00 GMT
ENV INFLUXDB_PV=2.8.0-2
# Fri, 17 Apr 2026 00:30:00 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Fri, 17 Apr 2026 00:30:00 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Fri, 17 Apr 2026 00:30:01 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 17 Apr 2026 00:30:02 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 17 Apr 2026 00:30:02 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 17 Apr 2026 00:30:02 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 17 Apr 2026 00:30:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:30:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:30:02 GMT
CMD ["influxd"]
# Fri, 17 Apr 2026 00:30:02 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 17 Apr 2026 00:30:02 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 17 Apr 2026 00:30:02 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 17 Apr 2026 00:30:02 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 17 Apr 2026 00:30:02 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef79b6f3d2e846d055a2620421abd1ea83d1a2a5c141a54104accb233ed0ce59`  
		Last Modified: Fri, 17 Apr 2026 00:30:12 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd92961fcb2124af0c103187cef2632786c556874b686090cae17de4638ed98`  
		Last Modified: Fri, 17 Apr 2026 00:30:12 GMT  
		Size: 9.9 MB (9883791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21ab53b0f55c96701571d89ea72fe10e15495a5399811272d01416b505d8848`  
		Last Modified: Fri, 17 Apr 2026 00:30:12 GMT  
		Size: 6.2 MB (6156985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788c81c58d331aa59131e00c438630fb5aefff8373c89b0adc66d24f393ae7cb`  
		Last Modified: Fri, 17 Apr 2026 00:30:12 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1fff6940a3878ed3aee43c506ecf21d4bce29f9e7388a17ce375c9b9c0a44cf`  
		Last Modified: Fri, 17 Apr 2026 00:30:15 GMT  
		Size: 50.5 MB (50451820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6c03c0be2850f9c82b37631d6cba13fdd3f1e632d3643edc54d2cdc6edf2c9`  
		Last Modified: Fri, 17 Apr 2026 00:30:13 GMT  
		Size: 11.8 MB (11775863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aea5f86be29cb56a759d7142f5a9b62bfd6ed99d100b921dd3a33e4ce9314a5`  
		Last Modified: Fri, 17 Apr 2026 00:30:13 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ef07b04bbe77eb925cb81d0e6082ce24328e0d2c296d61c460e11aa33b6b3a`  
		Last Modified: Fri, 17 Apr 2026 00:30:14 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ddd87b55db792237d8b7cd099de585015d86816d1215b2f57c4dd5011ba91e`  
		Last Modified: Fri, 17 Apr 2026 00:30:15 GMT  
		Size: 6.3 KB (6283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:40fca214b400941be68a739f6f59448a6e931f730682c1d89026fee13fe21c34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **946.1 KB (946058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7f880a5909c565d62181a36572e16dac17e9bb0131551dfa514d962d26c4a97`

```dockerfile
```

-	Layers:
	-	`sha256:33f778c6f613bedfa5d2ec41b08b10f6bf6ce196ef899601b0ec66f7637095f3`  
		Last Modified: Fri, 17 Apr 2026 00:30:12 GMT  
		Size: 915.2 KB (915211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:629ffea1f9f8527114e2ed5a812a800fe7b6e1a1947e4b14a6b8302f319cb11d`  
		Last Modified: Fri, 17 Apr 2026 00:30:12 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:1d6e285b1a5e3fa23695d08c8586d0d17c004443a83a93e22a40d9f7c449227c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.0 MB (78965173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ba6389eb739af52c14de9f6ed96efacfbe53dccc3e41f42ab1f51fef176da67`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:13 GMT
ADD alpine-minirootfs-3.21.7-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:13 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:31:02 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 00:31:03 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:31:03 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Fri, 17 Apr 2026 00:31:04 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Fri, 17 Apr 2026 00:31:07 GMT
ENV INFLUXDB_VERSION=2.8.0
# Fri, 17 Apr 2026 00:31:07 GMT
ENV INFLUXDB_PR=-2
# Fri, 17 Apr 2026 00:31:07 GMT
ENV INFLUXDB_PV=2.8.0-2
# Fri, 17 Apr 2026 00:31:07 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Fri, 17 Apr 2026 00:31:07 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Fri, 17 Apr 2026 00:31:07 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Fri, 17 Apr 2026 00:31:08 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Fri, 17 Apr 2026 00:31:08 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 17 Apr 2026 00:31:08 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Fri, 17 Apr 2026 00:31:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:31:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:31:08 GMT
CMD ["influxd"]
# Fri, 17 Apr 2026 00:31:08 GMT
EXPOSE map[8086/tcp:{}]
# Fri, 17 Apr 2026 00:31:08 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Fri, 17 Apr 2026 00:31:08 GMT
ENV INFLUXD_INIT_PORT=9999
# Fri, 17 Apr 2026 00:31:08 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Fri, 17 Apr 2026 00:31:08 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:2dd7199cff98a7400e801cbfad6de906972a4e3dd0a749d4c1b80f5a1e3e4108`  
		Last Modified: Thu, 16 Apr 2026 05:32:50 GMT  
		Size: 4.0 MB (3994465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f652e0c01e29334dc1fe16c1d56127042156c3a64857b4a0ead43d3986f7986`  
		Last Modified: Fri, 17 Apr 2026 00:31:17 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5ddaea2126344e5b11cf5e6c97cd44d5b59a15fabcb438bb0a343fd2c1b7162`  
		Last Modified: Fri, 17 Apr 2026 00:31:18 GMT  
		Size: 9.8 MB (9842397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9394ce182bd0c5ee862a0d2428947e1a0d0fc3da081624b53bb5b05e37972f48`  
		Last Modified: Fri, 17 Apr 2026 00:31:17 GMT  
		Size: 5.8 MB (5790430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98541319cbb33b6799c13cddcd9cd7e00fe5295fea9954da3eaa7af2a1be8ca9`  
		Last Modified: Fri, 17 Apr 2026 00:31:17 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872f29647bbd3f39d47cc2a6b1b76f958b61aeb29480eec96b42c03288cd1472`  
		Last Modified: Fri, 17 Apr 2026 00:31:20 GMT  
		Size: 48.2 MB (48229511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff3598b437a8492690885c52bd82ed6d9ba85af743856cdcdc03e23cff14b84b`  
		Last Modified: Fri, 17 Apr 2026 00:31:19 GMT  
		Size: 11.1 MB (11100414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca69b2befa8351ec86c62df1caca82193562d274be054f00c148c6b5f5ba67b`  
		Last Modified: Fri, 17 Apr 2026 00:31:18 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba50550e7b2ebf586c1c93af205b4fb509ff55bfeda64342a548be9f7eb0b4d`  
		Last Modified: Fri, 17 Apr 2026 00:31:19 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8195a95763ebcb79e75c6db51ef9341b1678f6bd5070f114326209a91fff3bb8`  
		Last Modified: Fri, 17 Apr 2026 00:31:20 GMT  
		Size: 6.3 KB (6284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:866fdba0f42c46c21ba2c8d62ea1a6c90a46ca6d38e54989b009617072a3b43c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **945.5 KB (945503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48090246a2f4e0d9530f4b14c374ee2497817d1ef5d6807100cc1f963980061`

```dockerfile
```

-	Layers:
	-	`sha256:7f3a296bce432225eae41d3f9ad0d93e77867c28796a18dbaf6693ac05624f1b`  
		Last Modified: Fri, 17 Apr 2026 00:31:17 GMT  
		Size: 914.5 KB (914462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0eb74c7252a3cb8f2dd15f0ae328f0107f804876760828392c2573c155759432`  
		Last Modified: Fri, 17 Apr 2026 00:31:17 GMT  
		Size: 31.0 KB (31041 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:core`

```console
$ docker pull influxdb@sha256:1d58c8b9ac90153ae3a020ede2810c8284933dda50ac71e7573389ab6f012128
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:core` - linux; amd64

```console
$ docker pull influxdb@sha256:fe11b1e876597df9299d3f35411960587f2b5f2815dcef6a9f1f5a6ac8cd3ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149120890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c93d5f48b898003bdfb0e9ac56040cf4ff0645836b8f0439e8f0d0c00a3442fd`
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
# Wed, 15 Apr 2026 20:43:28 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 15 Apr 2026 20:43:28 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 15 Apr 2026 20:43:33 GMT
ENV INFLUXDB_VERSION=3.9.1
# Wed, 15 Apr 2026 20:43:33 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 15 Apr 2026 20:43:33 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:43:33 GMT
USER influxdb3
# Wed, 15 Apr 2026 20:43:33 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 15 Apr 2026 20:43:33 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 15 Apr 2026 20:43:33 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 15 Apr 2026 20:43:33 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 15 Apr 2026 20:43:33 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 15 Apr 2026 20:43:33 GMT
ENV LOG_FILTER=info
# Wed, 15 Apr 2026 20:43:33 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 15 Apr 2026 20:43:33 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 15 Apr 2026 20:43:33 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb85a1612071842cc709708034e092cd219f01edf4a9b9762c0f183a3441ecf`  
		Last Modified: Wed, 15 Apr 2026 20:43:51 GMT  
		Size: 6.7 MB (6671641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b32837ce4e56248bf07e7ff916abed714dbe90eb6395eebac86b090f5cac87`  
		Last Modified: Wed, 15 Apr 2026 20:43:51 GMT  
		Size: 3.6 KB (3644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b097d884f34508800b955f7367bf2eb4bcbc6da1428ee8e6f065581cf2e22f25`  
		Last Modified: Wed, 15 Apr 2026 20:43:53 GMT  
		Size: 112.7 MB (112711959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ded072d71b9df4d79d6fcb4f2d1886ffc352ee501284d55301d15e27f8c638`  
		Last Modified: Wed, 15 Apr 2026 20:43:51 GMT  
		Size: 518.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ea4f908e157134e7630698fc0d7d5382c889cf502f09fd3bb603cd23691d1a`  
		Last Modified: Wed, 15 Apr 2026 20:43:52 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:652471149c89e684e9191468501e341d603a736695f0b144375211385cc6094b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b9dd6e9add57346769772585ff6d04d3fe25307ef017476731d4eefa017ce2`

```dockerfile
```

-	Layers:
	-	`sha256:4551c43b7943abba7b3ded791c92a4c94a59e338ea16063ac500d5045ef18be4`  
		Last Modified: Wed, 15 Apr 2026 20:43:51 GMT  
		Size: 2.3 MB (2310597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63aafdd4a6f1432a8324260dc22045c383a922f0e4a4a5d0369ceec7db4c9532`  
		Last Modified: Wed, 15 Apr 2026 20:43:50 GMT  
		Size: 17.6 KB (17619 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:81681dee889cc3a3e5ed75687baedd16c5879379204d30b378c01da5623af612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140062904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c9c1af5bc3c9718fdc8ba857d3dfc6bc07b8c3be495603f5dbc76b9f52b4be5`
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
# Wed, 15 Apr 2026 20:43:36 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 15 Apr 2026 20:43:37 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 15 Apr 2026 20:43:42 GMT
ENV INFLUXDB_VERSION=3.9.1
# Wed, 15 Apr 2026 20:43:42 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 15 Apr 2026 20:43:42 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:43:42 GMT
USER influxdb3
# Wed, 15 Apr 2026 20:43:42 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 15 Apr 2026 20:43:42 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 15 Apr 2026 20:43:42 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 15 Apr 2026 20:43:42 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 15 Apr 2026 20:43:42 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 15 Apr 2026 20:43:42 GMT
ENV LOG_FILTER=info
# Wed, 15 Apr 2026 20:43:42 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 15 Apr 2026 20:43:42 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 15 Apr 2026 20:43:42 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f08ac250787db9f963390f932e1c5da35f7e8c89ca9da7b9042fd0957365d86`  
		Last Modified: Wed, 15 Apr 2026 20:43:58 GMT  
		Size: 6.7 MB (6681852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1206008ad447c4fd90bb7cc623cdb10e613f182f166550529e8ccd4f6df65f3`  
		Last Modified: Wed, 15 Apr 2026 20:43:58 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4de3b0cf867358d35a07dda31a27e09112537c510d666c5e85dc48f38b9948`  
		Last Modified: Wed, 15 Apr 2026 20:44:00 GMT  
		Size: 104.5 MB (104500945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab531844cdf13d434c23663168a76540de29e691f5f74aa4d00859fa9b56adc`  
		Last Modified: Wed, 15 Apr 2026 20:43:58 GMT  
		Size: 520.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd3a466131393335a59d93e8a5df450632faed8b450e18e03fa9445df50d544`  
		Last Modified: Wed, 15 Apr 2026 20:43:59 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:9b378c72d59a92a91ad9ebd029c180e55cab7308cf5d5f99decc684ad8065254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6945d6a683f4c1a88ffe161de85441ad6200e506e8267681c57c8e0fe6a81807`

```dockerfile
```

-	Layers:
	-	`sha256:4289a8ee02ce5554b7f057d2bcda399af9b640aac1bfcd448d13090d65f9728c`  
		Last Modified: Wed, 15 Apr 2026 20:43:58 GMT  
		Size: 2.3 MB (2311679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7ec699b6edea9a3daa2eed69aca2520bae97c228253d9d921690eaf16410244`  
		Last Modified: Wed, 15 Apr 2026 20:43:58 GMT  
		Size: 17.8 KB (17769 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:data`

```console
$ docker pull influxdb@sha256:1bb7cb1e53d43d8ee77aadca2d18ec99e34a58376d6a02075c1dc53cadb9272c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:data` - linux; amd64

```console
$ docker pull influxdb@sha256:dc1f450e108a9944f9d8b1289468c4404ae4070f9078af1ead3a3329f7549d9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115718778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94ab92d581bcd3f0c7e589690b39705a679ed85920980fed9670da1668cfc89b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Apr 2026 22:49:58 GMT
ENV INFLUXDB_VERSION=1.12.4-c1.12.4
# Mon, 13 Apr 2026 22:49:58 GMT
ENV INFLUXDB_PR=
# Mon, 13 Apr 2026 22:49:58 GMT
ENV INFLUXDB_PV=1.12.4-c1.12.4
# Mon, 13 Apr 2026 22:49:58 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"          -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"         "influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     rm -r "influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"           "influxdb-data_${INFLUXDB_PV}_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Mon, 13 Apr 2026 22:49:58 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Mon, 13 Apr 2026 22:49:58 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 13 Apr 2026 22:49:58 GMT
VOLUME [/var/lib/influxdb]
# Mon, 13 Apr 2026 22:49:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 13 Apr 2026 22:49:58 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Mon, 13 Apr 2026 22:49:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 13 Apr 2026 22:49:58 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c3414b1d6b49c54c305584faac46aad75c67644cf4f8495e8145206d28e416`  
		Last Modified: Tue, 07 Apr 2026 01:47:02 GMT  
		Size: 24.0 MB (24038269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3ad30cc0f9885db6f3f3b9af8834a49c6770603219f0899c8d2b121cf6cd75`  
		Last Modified: Mon, 13 Apr 2026 22:50:12 GMT  
		Size: 43.2 MB (43189910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b51b01a2ef33a85cd8edbca066d9077822df136af91cb6971a800ff131c1d3`  
		Last Modified: Mon, 13 Apr 2026 22:50:10 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b386d41662c8a1289ff94f784995f6bc7d20e2659612891b88325f6e0ce041`  
		Last Modified: Mon, 13 Apr 2026 22:50:10 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6862c17b4bebcee9f221229f33be2b8ac982dc5d0fd5948d8ef92064fca5f9f`  
		Last Modified: Mon, 13 Apr 2026 22:50:10 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:data` - unknown; unknown

```console
$ docker pull influxdb@sha256:a323cb246451e75e29967f9d1defcaa49773f6a25b58859e305cb3c3e23eac8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4707277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae13ff8cded04988bd0ab05649dbbf083dd16bb2f83d6ebf9a53eaca28b85ac2`

```dockerfile
```

-	Layers:
	-	`sha256:9c371c2fe64f56971440a22d98001dec89849263c3fb9dc70f789d0b05416005`  
		Last Modified: Mon, 13 Apr 2026 22:50:11 GMT  
		Size: 4.7 MB (4693123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cc70504e235817a2900902046909c763540085aaf1d0029847445180cd92d57`  
		Last Modified: Mon, 13 Apr 2026 22:50:10 GMT  
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
$ docker pull influxdb@sha256:4113f82acd887c5d0228865dbe6b3591794d78b6057458d655eef7f7b937a6aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:7781d9f311036bbb44141f6983369f29b467a1fc82c3d9c3c3993f07adb9edaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.9 MB (159923454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14c982870ed0f2165579cc75426eb003f3ec1cf0501b950e53146052e68a7b34`
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
# Wed, 15 Apr 2026 20:43:33 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 15 Apr 2026 20:43:33 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 15 Apr 2026 20:43:39 GMT
ENV INFLUXDB_VERSION=3.9.1
# Wed, 15 Apr 2026 20:43:39 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 15 Apr 2026 20:43:39 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:43:39 GMT
USER influxdb3
# Wed, 15 Apr 2026 20:43:39 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 15 Apr 2026 20:43:39 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 15 Apr 2026 20:43:39 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 15 Apr 2026 20:43:39 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 15 Apr 2026 20:43:39 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 15 Apr 2026 20:43:39 GMT
ENV LOG_FILTER=info
# Wed, 15 Apr 2026 20:43:39 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 15 Apr 2026 20:43:39 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 15 Apr 2026 20:43:39 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e0999e8f1462fbb09cb39ef08c282eda58df5d1e8c389005f194ea00cccecf`  
		Last Modified: Wed, 15 Apr 2026 20:43:59 GMT  
		Size: 6.7 MB (6671623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f38afebbd5132d82f9901425991a82a49bf410374f60e1b0ba57e420f0d33a6e`  
		Last Modified: Wed, 15 Apr 2026 20:43:59 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08080051254204def33427dfac5ec1b091a9b5849d1552a1ca4e632b7441b59`  
		Last Modified: Wed, 15 Apr 2026 20:44:02 GMT  
		Size: 123.5 MB (123514533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d79ef371b5b265f128726acb79e36bd502e0227916d0f86fbf724d348d58da6`  
		Last Modified: Wed, 15 Apr 2026 20:43:59 GMT  
		Size: 518.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42215201c4d468436362f05d42e64e4431e5fc007db05220d0f0b4d3e72419ca`  
		Last Modified: Wed, 15 Apr 2026 20:44:00 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:f3f71dc42bfbbfd2a66fc92826a16ba17524e254845208f94ac1b9e601993189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52b6fa96bed968f1e3db363fbbbb9c073c019f438e75ca05b5cc05d1db2012a8`

```dockerfile
```

-	Layers:
	-	`sha256:7044d2ea7b43afb998f551a78cc6cca87a848c19440a08858760886060d29034`  
		Last Modified: Wed, 15 Apr 2026 20:43:59 GMT  
		Size: 2.3 MB (2310645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0dc250eea8be207f77782a07b795db475744e9fb46ff0cbf67acc02fd41ce4a`  
		Last Modified: Wed, 15 Apr 2026 20:43:59 GMT  
		Size: 17.8 KB (17800 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:50dfce3b801a3bb452684d5744f928286d8d70682cab1d39d80e53580a094a96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.8 MB (150758023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bf7cc1716fb81f0809d6de6a2da460353e027e871816f1904a91dbf4c8ed482`
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
# Wed, 15 Apr 2026 20:43:40 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 15 Apr 2026 20:43:40 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 15 Apr 2026 20:43:45 GMT
ENV INFLUXDB_VERSION=3.9.1
# Wed, 15 Apr 2026 20:43:45 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 15 Apr 2026 20:43:45 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:43:45 GMT
USER influxdb3
# Wed, 15 Apr 2026 20:43:46 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 15 Apr 2026 20:43:46 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 15 Apr 2026 20:43:46 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 15 Apr 2026 20:43:46 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 15 Apr 2026 20:43:46 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 15 Apr 2026 20:43:46 GMT
ENV LOG_FILTER=info
# Wed, 15 Apr 2026 20:43:46 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 15 Apr 2026 20:43:46 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 15 Apr 2026 20:43:46 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e62244524400b4e44e3ad020813e0a0618188bb064c5732855c664af09a06f`  
		Last Modified: Wed, 15 Apr 2026 20:44:03 GMT  
		Size: 6.7 MB (6681811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16cf1620991e32dbed4397cdb8eb7293d57ee810171bf8c1a886dddd30185cb9`  
		Last Modified: Wed, 15 Apr 2026 20:44:03 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa7bb728ae5e717ec96034e40136c46b01ea54f9d2b9142f000fbca57e405353`  
		Last Modified: Wed, 15 Apr 2026 20:44:06 GMT  
		Size: 115.2 MB (115196105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69fd7d303d393e57b9f180646bdde3ef3cbf21f9612aac91a2a17c4430410f93`  
		Last Modified: Wed, 15 Apr 2026 20:44:03 GMT  
		Size: 519.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e591569b32d278adfe2b3b261c7775fbaade74d1da69cbfda55f85e1be4d613`  
		Last Modified: Wed, 15 Apr 2026 20:44:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:745f936b54711018736135ccfc600a044e5ae237c330e17c303f3856250ae77b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe0ed19d8d0b7ccbf973e3ca952ebe95b6391b09e5363c6bc98b16359316256f`

```dockerfile
```

-	Layers:
	-	`sha256:5beb6f6b3a5737648090b5d78aadc2bc4d7e778c10f15d2da4c1621082b926bf`  
		Last Modified: Wed, 15 Apr 2026 20:44:03 GMT  
		Size: 2.3 MB (2311727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46b2310865e366114310e7a1d79734538d6ff848e247c157eeaac77405db85e5`  
		Last Modified: Wed, 15 Apr 2026 20:44:02 GMT  
		Size: 17.9 KB (17949 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:latest`

```console
$ docker pull influxdb@sha256:71f2bce68b47a3e26c1ed38f7480a9372b008ba9b7c8a35cb2c913d3102d377f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:e532279db2ffef29e7eab17961841291927e228f2703bafd9255023d5480d056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107241320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:759ec9162770032bdcd5f75d588d4bdd548f5ea87abdbd151e3711dfc50cf4f4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:41:32 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:41:33 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 22 Apr 2026 01:41:33 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 22 Apr 2026 01:41:35 GMT
ENV GOSU_VER=1.19
# Wed, 22 Apr 2026 01:41:35 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Wed, 22 Apr 2026 01:41:35 GMT
ENV INFLUXDB_VERSION=2.8.0
# Wed, 22 Apr 2026 01:41:35 GMT
ENV INFLUXDB_PR=-2
# Wed, 22 Apr 2026 01:41:35 GMT
ENV INFLUXDB_PV=2.8.0-2
# Wed, 22 Apr 2026 01:41:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 22 Apr 2026 01:41:37 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 22 Apr 2026 01:41:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 22 Apr 2026 01:41:38 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 22 Apr 2026 01:41:38 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 22 Apr 2026 01:41:39 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 22 Apr 2026 01:41:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 01:41:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 01:41:39 GMT
CMD ["influxd"]
# Wed, 22 Apr 2026 01:41:39 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 22 Apr 2026 01:41:39 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 22 Apr 2026 01:41:39 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 22 Apr 2026 01:41:39 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 22 Apr 2026 01:41:39 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c791747626e2412d3502fd05d4fac3fffd42cdd349ef47e7884ae03da2dbef`  
		Last Modified: Wed, 22 Apr 2026 01:41:50 GMT  
		Size: 9.8 MB (9798990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2ee315242c36b9238a9f0e643e4281f93755787bc77c2b111e887c7653da6d`  
		Last Modified: Wed, 22 Apr 2026 01:41:50 GMT  
		Size: 6.2 MB (6156971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844de845c21c0436926d498f8ebd39d4698a948c5fb968d09c52f49a33e30c54`  
		Last Modified: Wed, 22 Apr 2026 01:41:50 GMT  
		Size: 3.2 KB (3229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41868ae9fbbede4b0f6bdbd0af43852ad245ea7c610f402e2220bd8847c6b729`  
		Last Modified: Wed, 22 Apr 2026 01:41:50 GMT  
		Size: 811.5 KB (811478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4da638bcf081222b7033e64890358a3f551ee2a1060e73d60775bb4cce4888a`  
		Last Modified: Wed, 22 Apr 2026 01:41:52 GMT  
		Size: 50.5 MB (50451802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4fea9ea328927d53fc80fd2b38cd6f7a8dffe1745ef87a3a3159347389e9f2e`  
		Last Modified: Wed, 22 Apr 2026 01:41:52 GMT  
		Size: 11.8 MB (11775870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ddc1c71a8a7f9d5167a61bdc437327b756110396f40992677ef72157e08775`  
		Last Modified: Wed, 22 Apr 2026 01:41:51 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e55f58da73fd395ac05c086627b0e088853dbeb76527b853bdcd5d76adddca`  
		Last Modified: Wed, 22 Apr 2026 01:41:52 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70d15b5d427c0540fea4882696f4da3a2a6787732964d6542233dc71e311537`  
		Last Modified: Wed, 22 Apr 2026 01:41:53 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:8938d3511aaa20b791700f8a2e5817323627e5360965a4f98d6140dc066ff3ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b027564a5f64ce815d5a5005299ddd5ea69b030647832e23bbc5a547bd4809b1`

```dockerfile
```

-	Layers:
	-	`sha256:ec06b068a4d9e7482bd3578659a536954e9c49b80b862002a0c69866d0d7e1f6`  
		Last Modified: Wed, 22 Apr 2026 01:41:50 GMT  
		Size: 2.9 MB (2934237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a481924326704569284e4ea29a85d10c6460d99223990fd6292868077c45765`  
		Last Modified: Wed, 22 Apr 2026 01:41:50 GMT  
		Size: 33.6 KB (33621 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:4749be1eb7cb5803e7fe7c7abfb0e4a868c3017bc903299d3526cbfc5ff85379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103640890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a3d056402f328a5ae7b1e564dedf01aa4df264f034fedd872385e3bb96accdd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:44:39 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:40 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 22 Apr 2026 01:44:40 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Wed, 22 Apr 2026 01:44:42 GMT
ENV GOSU_VER=1.19
# Wed, 22 Apr 2026 01:44:42 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Wed, 22 Apr 2026 01:44:42 GMT
ENV INFLUXDB_VERSION=2.8.0
# Wed, 22 Apr 2026 01:44:42 GMT
ENV INFLUXDB_PR=-2
# Wed, 22 Apr 2026 01:44:42 GMT
ENV INFLUXDB_PV=2.8.0-2
# Wed, 22 Apr 2026 01:44:46 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 22 Apr 2026 01:44:46 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 22 Apr 2026 01:44:47 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 22 Apr 2026 01:44:47 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 22 Apr 2026 01:44:47 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 22 Apr 2026 01:44:47 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 22 Apr 2026 01:44:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 01:44:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 01:44:47 GMT
CMD ["influxd"]
# Wed, 22 Apr 2026 01:44:47 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 22 Apr 2026 01:44:47 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 22 Apr 2026 01:44:47 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 22 Apr 2026 01:44:47 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 22 Apr 2026 01:44:47 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ddf21f4abba315d4e405b0b7ca7380c3b03e816eea5fd8219965fed687ac4f`  
		Last Modified: Wed, 22 Apr 2026 01:44:58 GMT  
		Size: 9.6 MB (9628094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c560fbc3a39b1a11f3127f89d636cc2517753a085eaf3afbf4f928d215e86c8b`  
		Last Modified: Wed, 22 Apr 2026 01:44:58 GMT  
		Size: 5.8 MB (5790421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f267c0a54c465bfc52d652cfab1ac62dfafe3e42649811dab584056706e1db51`  
		Last Modified: Wed, 22 Apr 2026 01:44:57 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01fd1f2188e7bc5e9738f5ddde7c01d895d6f100721c3eca47f0448d1c4921c`  
		Last Modified: Wed, 22 Apr 2026 01:44:57 GMT  
		Size: 766.4 KB (766364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9245aa8cd37661f6b67a498039d6cc9574d07919bf07b31b7ce44f594b552802`  
		Last Modified: Wed, 22 Apr 2026 01:45:00 GMT  
		Size: 48.2 MB (48229530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17a6763a2749ecf5870e80619513e273d0e1a10c00743d701c94e21be334b3f`  
		Last Modified: Wed, 22 Apr 2026 01:44:59 GMT  
		Size: 11.1 MB (11100415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69e2b2742458b735c0dc03bd705017e3e0d65e05db242e409d99a66ce5e26a6`  
		Last Modified: Wed, 22 Apr 2026 01:44:59 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95186bc453fe3657a6cd1bbd5b28c20dcd8355d9ba05951c3ec5b6c00a573e4`  
		Last Modified: Wed, 22 Apr 2026 01:44:59 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f382dd5f3b374f7003cd1b28910bd54c378e293152f8e5a1d9870d5e406147a`  
		Last Modified: Wed, 22 Apr 2026 01:45:00 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:439f6863a26e4a35763bda86f99511c908da7c6f97b9d593c7c3a1094666c347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9196348dc3b5c505a243f0014bdc51b8210eb9a0d606b67eef4fbb93c121620`

```dockerfile
```

-	Layers:
	-	`sha256:219a4fdfdfad1438a2554524a5be2b3f344b6802c2cc229aba88bf6973f82621`  
		Last Modified: Wed, 22 Apr 2026 01:44:57 GMT  
		Size: 2.9 MB (2933717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79c489575215cf3dd7f3007ba6ae0f8970239be059d7c86d56c59b83c70b12b4`  
		Last Modified: Wed, 22 Apr 2026 01:44:57 GMT  
		Size: 33.8 KB (33815 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:meta`

```console
$ docker pull influxdb@sha256:f342f786f4676fd37b672f9e5ed587a67d2743bf5b261418d7bf2f5528b7fdad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:meta` - linux; amd64

```console
$ docker pull influxdb@sha256:69850756eb4fa42a326833d36958ee6fe52bc688caa6a905eaa348e4948b7bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91912837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b46ed6e9d38d9dd2ed2dbd7d545899f7b54641fbc4954ee4b97e9ffd380ae51a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Apr 2026 22:50:11 GMT
ENV INFLUXDB_VERSION=1.12.4-c1.12.4
# Mon, 13 Apr 2026 22:50:11 GMT
ENV INFLUXDB_PR=
# Mon, 13 Apr 2026 22:50:11 GMT
ENV INFLUXDB_PV=1.12.4-c1.12.4
# Mon, 13 Apr 2026 22:50:11 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"          -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"         "influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     rm -r "influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"           "influxdb-meta_${INFLUXDB_PV}_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Mon, 13 Apr 2026 22:50:11 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Mon, 13 Apr 2026 22:50:11 GMT
EXPOSE map[8091/tcp:{}]
# Mon, 13 Apr 2026 22:50:11 GMT
VOLUME [/var/lib/influxdb]
# Mon, 13 Apr 2026 22:50:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 13 Apr 2026 22:50:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 13 Apr 2026 22:50:11 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c3414b1d6b49c54c305584faac46aad75c67644cf4f8495e8145206d28e416`  
		Last Modified: Tue, 07 Apr 2026 01:47:02 GMT  
		Size: 24.0 MB (24038269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e0f7ee8b658eb6c5de752b1bd460cda5d8872f4ea0a2df909f45efd8e90456`  
		Last Modified: Mon, 13 Apr 2026 22:50:20 GMT  
		Size: 19.4 MB (19385177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3254a32e0e98355d9f943f389fe638e71c63cbd4508958193df0c491d009c2bb`  
		Last Modified: Mon, 13 Apr 2026 22:50:19 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5468d99e6cd4392f3f013ce29f74b2ada303391e9986578bd2f0c1aead188e56`  
		Last Modified: Mon, 13 Apr 2026 22:50:20 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:6b9f9dccb6d0521215ede40cab59ce3c7c223552881b94551ffdcf7c98f6be2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4605855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3661736a8ccd815549acaeaf7c0e080ab67f781d78da19fd935aa8dfcc9cf08`

```dockerfile
```

-	Layers:
	-	`sha256:e0979c1b4e7584dc7714f4cf6efd676c9bfecb7cf0b8d78005cf161d1f8245d3`  
		Last Modified: Mon, 13 Apr 2026 22:50:20 GMT  
		Size: 4.6 MB (4593191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70e1dcac49afc270d8058e7d8ea06e41fa0dd32457c9e2fc4c0c9cbfcd00ea55`  
		Last Modified: Mon, 13 Apr 2026 22:50:20 GMT  
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
