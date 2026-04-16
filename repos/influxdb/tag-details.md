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
$ docker pull influxdb@sha256:0844ff5a67f9c6f9a1547074cb7d64ce00556016a98d029b7ab96e1c031b526d
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
$ docker pull influxdb@sha256:add7694223af746863dd0c86fe651780611efe8b87c65c247dab8119d5eaa8de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113103613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775c7ea618b3c090597e4855f8209f7f850ddc0b623a8ad3f162b1650b98fb78`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:49:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:01:49 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 07 Apr 2026 03:01:56 GMT
ARG INFLUXDB_VERSION=1.11.8
# Tue, 07 Apr 2026 03:01:56 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:01:56 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 07 Apr 2026 03:01:56 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 07 Apr 2026 03:01:56 GMT
VOLUME [/var/lib/influxdb]
# Tue, 07 Apr 2026 03:01:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 03:01:56 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 07 Apr 2026 03:01:56 GMT
USER influxdb
# Tue, 07 Apr 2026 03:01:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 03:01:56 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af98f0879b367460715b477e9118922ba24f17d9a4ad8d70e595a9c4cf56990`  
		Last Modified: Tue, 07 Apr 2026 01:49:50 GMT  
		Size: 23.6 MB (23604705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd65e6d91f6a1a727871b1c7e06086f8011e411a5afa5713d594ba870a82f959`  
		Last Modified: Tue, 07 Apr 2026 03:02:09 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fd71220c958496c0d282817bc7e9b9633a2cc80f82608ace98dc22640aedc1`  
		Last Modified: Tue, 07 Apr 2026 03:02:10 GMT  
		Size: 41.1 MB (41122737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529a8b669261d136c2f00eb1df346db361972d8c57f993c5c25d7f8bf4d75117`  
		Last Modified: Tue, 07 Apr 2026 03:02:09 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0dfc45e30d2b702770439b705f3ee8bb268af9c64b31d0a8fcdd16c6f8c900f`  
		Last Modified: Tue, 07 Apr 2026 03:02:09 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8305d75ff815e4aa0351e6fc3f6d492c7bb62afbef9283b5bd544f0ce22a8014`  
		Last Modified: Tue, 07 Apr 2026 03:02:10 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11` - unknown; unknown

```console
$ docker pull influxdb@sha256:e8c2006211cfa0364362e46347eaae6b6e507458f9710922c23d08e07f31d966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8908216bc29ae324fc953acdb35a0d3ab544c6aab31218794baefd157067d2e3`

```dockerfile
```

-	Layers:
	-	`sha256:88c03ee9830a4196f57a9f72ecebafba102f8568c1b8d4780bfd2bba3d1a2bc9`  
		Last Modified: Tue, 07 Apr 2026 03:02:09 GMT  
		Size: 5.1 MB (5078728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8839cf0c83dcef07aef7fdbdb21565fabf4e66aad0617b3bd004c5ad9545a7c1`  
		Last Modified: Tue, 07 Apr 2026 03:02:09 GMT  
		Size: 15.6 KB (15581 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11-alpine`

```console
$ docker pull influxdb@sha256:8632b2aee90e61d03b25090e60f43291ad8c18961970d2a76ebe170fb9edede1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:18b0e900a9ef7bd527e22efae32fe7540ce10075c94e4704c00595002e0b48e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42931179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f123753da719af7e615849cf60685574ba135c84c07dafc0c4512ae2680e8f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:25:33 GMT
RUN apk add --no-cache       bash       ca-certificates       tzdata &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:25:39 GMT
ARG INFLUXDB_VERSION=1.11.8
# Wed, 28 Jan 2026 03:25:39 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN apk add --no-cache --virtual .build-deps       curl       gnupg       tar &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     case "$(apk --print-arch)" in       x86_64)  ARCH=amd64 ;;       aarch64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_TAR=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_TAR}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_TAR}" &&     tar -xf "${INFLUXDB_TAR}" -C /usr/bin       influx       influx_inspect       influxd &&     rm -rf "${INFLUXDB_TAR}"            "${INFLUXDB_ASC}" &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 03:25:39 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 28 Jan 2026 03:25:39 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Wed, 28 Jan 2026 03:25:39 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 Jan 2026 03:25:39 GMT
VOLUME [/var/lib/influxdb]
# Wed, 28 Jan 2026 03:25:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:25:40 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 28 Jan 2026 03:25:40 GMT
USER influxdb
# Wed, 28 Jan 2026 03:25:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:25:40 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49aaa256c2fea1c8d7b82042abbbe881566d13a774788fc2f2673dadb0be5ade`  
		Last Modified: Wed, 28 Jan 2026 03:25:49 GMT  
		Size: 1.2 MB (1224765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e625ddee2d605bf259f1afe9bfb1a1c019b7499ed66fe5b5709995dc352e039`  
		Last Modified: Wed, 28 Jan 2026 03:25:50 GMT  
		Size: 38.1 MB (38075834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ba877bbd5d6e9300c8f25cf4c64bc21e4768a2f8675f220c0c8618040573ff`  
		Last Modified: Wed, 28 Jan 2026 03:25:48 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7fa8bf86e7bb8232138a820b91ae5f64da53c77a33ec7009ecea62ecb4d3fd0`  
		Last Modified: Wed, 28 Jan 2026 03:25:49 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0628ad9b2208773a1caa4b083766abd5edbb2f9bd1c0ebaec5c23e6cb0e1b407`  
		Last Modified: Wed, 28 Jan 2026 03:25:50 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ee7358201d8d00b5531a19b69e5d44af7f1494147b1242bd02009957592bde`  
		Last Modified: Wed, 28 Jan 2026 03:25:50 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:594ad6109cea6a457966bd968837e36de65aa4722589a2969b5735fa05d9ff98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.3 KB (760316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a4287008743080ecb92eda2534b9170c8b6ab01f3a2a02c55e4994dfa75208`

```dockerfile
```

-	Layers:
	-	`sha256:8f9a0d76d31827559bd06701701b5929317882f4493616d244c1a37de2c34d9a`  
		Last Modified: Wed, 28 Jan 2026 03:25:49 GMT  
		Size: 742.5 KB (742482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c993bbbc918316ab7ddefcdd0dcbea3674931c55da0ef119f9b1673771b7d172`  
		Last Modified: Wed, 28 Jan 2026 03:25:49 GMT  
		Size: 17.8 KB (17834 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:13d98b40f88d68bb9bb24e099c309f0eea5ae527c67128e146fe97e6db0d2039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40945594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fde6b75da97afba60a3df5426d35f696d1bc59f250d2ecc3a83113c26daf17f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:19 GMT
ADD alpine-minirootfs-3.20.9-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:19 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:15:16 GMT
RUN apk add --no-cache       bash       ca-certificates       tzdata &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:15:23 GMT
ARG INFLUXDB_VERSION=1.11.8
# Wed, 28 Jan 2026 03:15:23 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN apk add --no-cache --virtual .build-deps       curl       gnupg       tar &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     case "$(apk --print-arch)" in       x86_64)  ARCH=amd64 ;;       aarch64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_TAR=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_TAR}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_TAR}" &&     tar -xf "${INFLUXDB_TAR}" -C /usr/bin       influx       influx_inspect       influxd &&     rm -rf "${INFLUXDB_TAR}"            "${INFLUXDB_ASC}" &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 03:15:23 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 28 Jan 2026 03:15:23 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Wed, 28 Jan 2026 03:15:23 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 Jan 2026 03:15:23 GMT
VOLUME [/var/lib/influxdb]
# Wed, 28 Jan 2026 03:15:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:15:23 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 28 Jan 2026 03:15:23 GMT
USER influxdb
# Wed, 28 Jan 2026 03:15:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:15:23 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:83b2d7e29698161422a104647ffb26568fe86648ff3609d1b60a4f9e9de38074`  
		Last Modified: Wed, 28 Jan 2026 01:18:24 GMT  
		Size: 4.1 MB (4089958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259e398369be67daddeb4ff7983b9be6161412ec09dce4a3ea618736039d652a`  
		Last Modified: Wed, 28 Jan 2026 03:15:32 GMT  
		Size: 1.3 MB (1304796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43db76d8b85d7162a919f9a4660fa2a439664ab43fe4f6762ad6075b94c1cd3b`  
		Last Modified: Wed, 28 Jan 2026 03:15:33 GMT  
		Size: 35.5 MB (35548123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bee56c9fe82fe02899d828e40db149d5630cb99f8d4b1059da46b27bf916096`  
		Last Modified: Wed, 28 Jan 2026 03:15:32 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f12a5d75e7f56eea39d82380cbe4a85dffe9c2a569aed233564f2d602d2beb`  
		Last Modified: Wed, 28 Jan 2026 03:15:32 GMT  
		Size: 1000.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4d0c790d6348482dc5ead4b2e098f4a44ad8fedc6d3676b07bb0efd18d3212`  
		Last Modified: Wed, 28 Jan 2026 03:15:33 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9fadd1909545912e8e5a7b4345961fe2a7419e4fccd0bd11177e3314b0fd1e`  
		Last Modified: Wed, 28 Jan 2026 03:15:33 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:a3f06b2b71e748389eece6e7ae27a401b4a1ddf6c1b597d025e7bda5bd150779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.7 KB (759653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9527bc42b25341df02b03ea0015db4b21eaece4f3fac0f6aad4216a0eb65076`

```dockerfile
```

-	Layers:
	-	`sha256:8b26a7c1292b91ca48e8fb9e660db26bff0ef5e3cbbe1a2518554ae663de4075`  
		Last Modified: Wed, 28 Jan 2026 03:15:32 GMT  
		Size: 741.7 KB (741709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76a44a8eaa3f69c139fc2f80d23792c493cb6d37dc65c27016d78067d76cd6e2`  
		Last Modified: Wed, 28 Jan 2026 03:15:32 GMT  
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
$ docker pull influxdb@sha256:9d0b51aeab711df34e37e895e2d1469ec43a29095ece120902603c3cf21efa38
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:02153a74beabb3f96b259f8507d7421339482549e50cc5d2258f0b2ce9e6c864
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (46960587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70f4d43e203a1a92b5ff368450db5c6fe8325a6b765befd58abf19f686fea967`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:25:50 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:25:51 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:25:55 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Wed, 28 Jan 2026 03:25:55 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 03:25:56 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 28 Jan 2026 03:25:56 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 Jan 2026 03:25:56 GMT
VOLUME [/var/lib/influxdb]
# Wed, 28 Jan 2026 03:25:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:25:56 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 28 Jan 2026 03:25:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:25:56 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0263a1e24ffa0829b1f805a2d6c158c33fea253d7ef254f2494681fa2d006a`  
		Last Modified: Wed, 28 Jan 2026 03:26:05 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9672fa9124cf983f0543c61ea1dde339b6705eb7d1e2b05d760b6b5938097078`  
		Last Modified: Wed, 28 Jan 2026 03:26:05 GMT  
		Size: 1.2 MB (1224754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f2e30e450bd646642d30a6713818d18161df47157ce401b61f69011dc8633f`  
		Last Modified: Wed, 28 Jan 2026 03:26:06 GMT  
		Size: 42.1 MB (42105918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187f04de5a1e581d806f89cfbb2942929a3f7241a270158df81e7c34383fd931`  
		Last Modified: Wed, 28 Jan 2026 03:26:05 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68edddde0b5f46997714b4dde35e1dc7f0e2fc457f720dd8975b0492c124bb0`  
		Last Modified: Wed, 28 Jan 2026 03:26:06 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80a545e019203b789e56a39b97bb112b148b5a35d4bfa4e5e047435ac01313c`  
		Last Modified: Wed, 28 Jan 2026 03:26:06 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:f1fe57771330dc344971ded307b8c5957352e6c41c6b4052a3a2de810fed9266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.6 KB (785589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a4234b2573554d959bb8763239bdda077e7007d27002de0f9dab694364e51b`

```dockerfile
```

-	Layers:
	-	`sha256:86054862a078c59646ba2b5c08117a00b07c42589123f4297ea77aab085bb20d`  
		Last Modified: Wed, 28 Jan 2026 03:26:05 GMT  
		Size: 769.0 KB (768993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f041e72a4e9d944868da8607a414ca998a5a43702d92dd969cde2a705e241ca`  
		Last Modified: Wed, 28 Jan 2026 03:26:05 GMT  
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
$ docker pull influxdb@sha256:249c7bd6c3cb8f7bbba327cf37a3b1005d6cd347d8a692c8ceaff56d18fb7891
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:44ad70f43101c494e4d04ab932049e45759c24ed812f029b96c79c7e18b7f5e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23403364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c9203475562a7d8b438ef3bdf218f4cdb0516b9023ca9c4f7beb027b1dd551`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:26:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:26:45 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:26:49 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Wed, 28 Jan 2026 03:26:49 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 03:26:49 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Wed, 28 Jan 2026 03:26:49 GMT
EXPOSE map[8091/tcp:{}]
# Wed, 28 Jan 2026 03:26:49 GMT
VOLUME [/var/lib/influxdb]
# Wed, 28 Jan 2026 03:26:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:26:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:26:49 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ce9bebb946b2c426c9224e7360d845b78bd397b82149cb1f1fa0be2b2e876c`  
		Last Modified: Wed, 28 Jan 2026 03:26:56 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a219cf2dafb437a398f6465d6bb676c776f0a32983a6488d2a5a52da44ff00`  
		Last Modified: Wed, 28 Jan 2026 03:26:56 GMT  
		Size: 1.2 MB (1224764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b99563435aacc7f0c7f9f7b4b1850b98aa7b8f25747307c2be2310f2a08d95`  
		Last Modified: Wed, 28 Jan 2026 03:26:57 GMT  
		Size: 18.5 MB (18549891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4a807e577681eeebd1dcac3ab7d414179b8fe0902833964ccc7e1f2fc51789`  
		Last Modified: Wed, 28 Jan 2026 03:26:56 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9608b4806a31ae3e7d94b72f7606acf6161b5a5c2d16ac725d6c236e2b7a93`  
		Last Modified: Wed, 28 Jan 2026 03:26:57 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:0b3947f754f901b0eee6981e99cd9d177d98f9208d60e99599a2182ee456cb48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.6 KB (691589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baf3c479b5f2c96864cbcd1eeccb783380ad8a72539788725799c866d6198c2b`

```dockerfile
```

-	Layers:
	-	`sha256:01b16cc3b5518976d91b8bddbc7009f186a3aef03547cabb60c8a13ddbbc8227`  
		Last Modified: Wed, 28 Jan 2026 03:26:56 GMT  
		Size: 676.6 KB (676622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1541f8caff84dbcdb88fbc06c12d3a170bfb849a19f16feb4f4857708b70317a`  
		Last Modified: Wed, 28 Jan 2026 03:26:56 GMT  
		Size: 15.0 KB (14967 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.8`

```console
$ docker pull influxdb@sha256:0844ff5a67f9c6f9a1547074cb7d64ce00556016a98d029b7ab96e1c031b526d
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
$ docker pull influxdb@sha256:add7694223af746863dd0c86fe651780611efe8b87c65c247dab8119d5eaa8de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113103613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775c7ea618b3c090597e4855f8209f7f850ddc0b623a8ad3f162b1650b98fb78`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:49:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:01:49 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 07 Apr 2026 03:01:56 GMT
ARG INFLUXDB_VERSION=1.11.8
# Tue, 07 Apr 2026 03:01:56 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:01:56 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 07 Apr 2026 03:01:56 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 07 Apr 2026 03:01:56 GMT
VOLUME [/var/lib/influxdb]
# Tue, 07 Apr 2026 03:01:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 03:01:56 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 07 Apr 2026 03:01:56 GMT
USER influxdb
# Tue, 07 Apr 2026 03:01:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 03:01:56 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af98f0879b367460715b477e9118922ba24f17d9a4ad8d70e595a9c4cf56990`  
		Last Modified: Tue, 07 Apr 2026 01:49:50 GMT  
		Size: 23.6 MB (23604705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd65e6d91f6a1a727871b1c7e06086f8011e411a5afa5713d594ba870a82f959`  
		Last Modified: Tue, 07 Apr 2026 03:02:09 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fd71220c958496c0d282817bc7e9b9633a2cc80f82608ace98dc22640aedc1`  
		Last Modified: Tue, 07 Apr 2026 03:02:10 GMT  
		Size: 41.1 MB (41122737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529a8b669261d136c2f00eb1df346db361972d8c57f993c5c25d7f8bf4d75117`  
		Last Modified: Tue, 07 Apr 2026 03:02:09 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0dfc45e30d2b702770439b705f3ee8bb268af9c64b31d0a8fcdd16c6f8c900f`  
		Last Modified: Tue, 07 Apr 2026 03:02:09 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8305d75ff815e4aa0351e6fc3f6d492c7bb62afbef9283b5bd544f0ce22a8014`  
		Last Modified: Tue, 07 Apr 2026 03:02:10 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:e8c2006211cfa0364362e46347eaae6b6e507458f9710922c23d08e07f31d966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8908216bc29ae324fc953acdb35a0d3ab544c6aab31218794baefd157067d2e3`

```dockerfile
```

-	Layers:
	-	`sha256:88c03ee9830a4196f57a9f72ecebafba102f8568c1b8d4780bfd2bba3d1a2bc9`  
		Last Modified: Tue, 07 Apr 2026 03:02:09 GMT  
		Size: 5.1 MB (5078728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8839cf0c83dcef07aef7fdbdb21565fabf4e66aad0617b3bd004c5ad9545a7c1`  
		Last Modified: Tue, 07 Apr 2026 03:02:09 GMT  
		Size: 15.6 KB (15581 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.11.8-alpine`

```console
$ docker pull influxdb@sha256:8632b2aee90e61d03b25090e60f43291ad8c18961970d2a76ebe170fb9edede1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11.8-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:18b0e900a9ef7bd527e22efae32fe7540ce10075c94e4704c00595002e0b48e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42931179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f123753da719af7e615849cf60685574ba135c84c07dafc0c4512ae2680e8f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:25:33 GMT
RUN apk add --no-cache       bash       ca-certificates       tzdata &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:25:39 GMT
ARG INFLUXDB_VERSION=1.11.8
# Wed, 28 Jan 2026 03:25:39 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN apk add --no-cache --virtual .build-deps       curl       gnupg       tar &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     case "$(apk --print-arch)" in       x86_64)  ARCH=amd64 ;;       aarch64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_TAR=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_TAR}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_TAR}" &&     tar -xf "${INFLUXDB_TAR}" -C /usr/bin       influx       influx_inspect       influxd &&     rm -rf "${INFLUXDB_TAR}"            "${INFLUXDB_ASC}" &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 03:25:39 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 28 Jan 2026 03:25:39 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Wed, 28 Jan 2026 03:25:39 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 Jan 2026 03:25:39 GMT
VOLUME [/var/lib/influxdb]
# Wed, 28 Jan 2026 03:25:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:25:40 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 28 Jan 2026 03:25:40 GMT
USER influxdb
# Wed, 28 Jan 2026 03:25:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:25:40 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49aaa256c2fea1c8d7b82042abbbe881566d13a774788fc2f2673dadb0be5ade`  
		Last Modified: Wed, 28 Jan 2026 03:25:49 GMT  
		Size: 1.2 MB (1224765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e625ddee2d605bf259f1afe9bfb1a1c019b7499ed66fe5b5709995dc352e039`  
		Last Modified: Wed, 28 Jan 2026 03:25:50 GMT  
		Size: 38.1 MB (38075834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ba877bbd5d6e9300c8f25cf4c64bc21e4768a2f8675f220c0c8618040573ff`  
		Last Modified: Wed, 28 Jan 2026 03:25:48 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7fa8bf86e7bb8232138a820b91ae5f64da53c77a33ec7009ecea62ecb4d3fd0`  
		Last Modified: Wed, 28 Jan 2026 03:25:49 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0628ad9b2208773a1caa4b083766abd5edbb2f9bd1c0ebaec5c23e6cb0e1b407`  
		Last Modified: Wed, 28 Jan 2026 03:25:50 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ee7358201d8d00b5531a19b69e5d44af7f1494147b1242bd02009957592bde`  
		Last Modified: Wed, 28 Jan 2026 03:25:50 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:594ad6109cea6a457966bd968837e36de65aa4722589a2969b5735fa05d9ff98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.3 KB (760316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a4287008743080ecb92eda2534b9170c8b6ab01f3a2a02c55e4994dfa75208`

```dockerfile
```

-	Layers:
	-	`sha256:8f9a0d76d31827559bd06701701b5929317882f4493616d244c1a37de2c34d9a`  
		Last Modified: Wed, 28 Jan 2026 03:25:49 GMT  
		Size: 742.5 KB (742482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c993bbbc918316ab7ddefcdd0dcbea3674931c55da0ef119f9b1673771b7d172`  
		Last Modified: Wed, 28 Jan 2026 03:25:49 GMT  
		Size: 17.8 KB (17834 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11.8-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:13d98b40f88d68bb9bb24e099c309f0eea5ae527c67128e146fe97e6db0d2039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40945594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fde6b75da97afba60a3df5426d35f696d1bc59f250d2ecc3a83113c26daf17f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:19 GMT
ADD alpine-minirootfs-3.20.9-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:19 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:15:16 GMT
RUN apk add --no-cache       bash       ca-certificates       tzdata &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:15:23 GMT
ARG INFLUXDB_VERSION=1.11.8
# Wed, 28 Jan 2026 03:15:23 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN apk add --no-cache --virtual .build-deps       curl       gnupg       tar &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     case "$(apk --print-arch)" in       x86_64)  ARCH=amd64 ;;       aarch64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_TAR=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_TAR}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_TAR}" &&     tar -xf "${INFLUXDB_TAR}" -C /usr/bin       influx       influx_inspect       influxd &&     rm -rf "${INFLUXDB_TAR}"            "${INFLUXDB_ASC}" &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 03:15:23 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 28 Jan 2026 03:15:23 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Wed, 28 Jan 2026 03:15:23 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 Jan 2026 03:15:23 GMT
VOLUME [/var/lib/influxdb]
# Wed, 28 Jan 2026 03:15:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:15:23 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 28 Jan 2026 03:15:23 GMT
USER influxdb
# Wed, 28 Jan 2026 03:15:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:15:23 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:83b2d7e29698161422a104647ffb26568fe86648ff3609d1b60a4f9e9de38074`  
		Last Modified: Wed, 28 Jan 2026 01:18:24 GMT  
		Size: 4.1 MB (4089958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259e398369be67daddeb4ff7983b9be6161412ec09dce4a3ea618736039d652a`  
		Last Modified: Wed, 28 Jan 2026 03:15:32 GMT  
		Size: 1.3 MB (1304796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43db76d8b85d7162a919f9a4660fa2a439664ab43fe4f6762ad6075b94c1cd3b`  
		Last Modified: Wed, 28 Jan 2026 03:15:33 GMT  
		Size: 35.5 MB (35548123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bee56c9fe82fe02899d828e40db149d5630cb99f8d4b1059da46b27bf916096`  
		Last Modified: Wed, 28 Jan 2026 03:15:32 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f12a5d75e7f56eea39d82380cbe4a85dffe9c2a569aed233564f2d602d2beb`  
		Last Modified: Wed, 28 Jan 2026 03:15:32 GMT  
		Size: 1000.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4d0c790d6348482dc5ead4b2e098f4a44ad8fedc6d3676b07bb0efd18d3212`  
		Last Modified: Wed, 28 Jan 2026 03:15:33 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9fadd1909545912e8e5a7b4345961fe2a7419e4fccd0bd11177e3314b0fd1e`  
		Last Modified: Wed, 28 Jan 2026 03:15:33 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:a3f06b2b71e748389eece6e7ae27a401b4a1ddf6c1b597d025e7bda5bd150779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.7 KB (759653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9527bc42b25341df02b03ea0015db4b21eaece4f3fac0f6aad4216a0eb65076`

```dockerfile
```

-	Layers:
	-	`sha256:8b26a7c1292b91ca48e8fb9e660db26bff0ef5e3cbbe1a2518554ae663de4075`  
		Last Modified: Wed, 28 Jan 2026 03:15:32 GMT  
		Size: 741.7 KB (741709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76a44a8eaa3f69c139fc2f80d23792c493cb6d37dc65c27016d78067d76cd6e2`  
		Last Modified: Wed, 28 Jan 2026 03:15:32 GMT  
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
$ docker pull influxdb@sha256:9d0b51aeab711df34e37e895e2d1469ec43a29095ece120902603c3cf21efa38
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.9-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:02153a74beabb3f96b259f8507d7421339482549e50cc5d2258f0b2ce9e6c864
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (46960587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70f4d43e203a1a92b5ff368450db5c6fe8325a6b765befd58abf19f686fea967`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:25:50 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:25:51 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:25:55 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Wed, 28 Jan 2026 03:25:55 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 03:25:56 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 28 Jan 2026 03:25:56 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 Jan 2026 03:25:56 GMT
VOLUME [/var/lib/influxdb]
# Wed, 28 Jan 2026 03:25:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:25:56 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 28 Jan 2026 03:25:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:25:56 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0263a1e24ffa0829b1f805a2d6c158c33fea253d7ef254f2494681fa2d006a`  
		Last Modified: Wed, 28 Jan 2026 03:26:05 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9672fa9124cf983f0543c61ea1dde339b6705eb7d1e2b05d760b6b5938097078`  
		Last Modified: Wed, 28 Jan 2026 03:26:05 GMT  
		Size: 1.2 MB (1224754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f2e30e450bd646642d30a6713818d18161df47157ce401b61f69011dc8633f`  
		Last Modified: Wed, 28 Jan 2026 03:26:06 GMT  
		Size: 42.1 MB (42105918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187f04de5a1e581d806f89cfbb2942929a3f7241a270158df81e7c34383fd931`  
		Last Modified: Wed, 28 Jan 2026 03:26:05 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68edddde0b5f46997714b4dde35e1dc7f0e2fc457f720dd8975b0492c124bb0`  
		Last Modified: Wed, 28 Jan 2026 03:26:06 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80a545e019203b789e56a39b97bb112b148b5a35d4bfa4e5e047435ac01313c`  
		Last Modified: Wed, 28 Jan 2026 03:26:06 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.9-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:f1fe57771330dc344971ded307b8c5957352e6c41c6b4052a3a2de810fed9266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.6 KB (785589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a4234b2573554d959bb8763239bdda077e7007d27002de0f9dab694364e51b`

```dockerfile
```

-	Layers:
	-	`sha256:86054862a078c59646ba2b5c08117a00b07c42589123f4297ea77aab085bb20d`  
		Last Modified: Wed, 28 Jan 2026 03:26:05 GMT  
		Size: 769.0 KB (768993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f041e72a4e9d944868da8607a414ca998a5a43702d92dd969cde2a705e241ca`  
		Last Modified: Wed, 28 Jan 2026 03:26:05 GMT  
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
$ docker pull influxdb@sha256:249c7bd6c3cb8f7bbba327cf37a3b1005d6cd347d8a692c8ceaff56d18fb7891
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.9-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:44ad70f43101c494e4d04ab932049e45759c24ed812f029b96c79c7e18b7f5e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23403364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c9203475562a7d8b438ef3bdf218f4cdb0516b9023ca9c4f7beb027b1dd551`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:26:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:26:45 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:26:49 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Wed, 28 Jan 2026 03:26:49 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/usr/bin/* &&     cp -a /usr/src/influxdb-*/usr/bin/. /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 03:26:49 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Wed, 28 Jan 2026 03:26:49 GMT
EXPOSE map[8091/tcp:{}]
# Wed, 28 Jan 2026 03:26:49 GMT
VOLUME [/var/lib/influxdb]
# Wed, 28 Jan 2026 03:26:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:26:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:26:49 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ce9bebb946b2c426c9224e7360d845b78bd397b82149cb1f1fa0be2b2e876c`  
		Last Modified: Wed, 28 Jan 2026 03:26:56 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a219cf2dafb437a398f6465d6bb676c776f0a32983a6488d2a5a52da44ff00`  
		Last Modified: Wed, 28 Jan 2026 03:26:56 GMT  
		Size: 1.2 MB (1224764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b99563435aacc7f0c7f9f7b4b1850b98aa7b8f25747307c2be2310f2a08d95`  
		Last Modified: Wed, 28 Jan 2026 03:26:57 GMT  
		Size: 18.5 MB (18549891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4a807e577681eeebd1dcac3ab7d414179b8fe0902833964ccc7e1f2fc51789`  
		Last Modified: Wed, 28 Jan 2026 03:26:56 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9608b4806a31ae3e7d94b72f7606acf6161b5a5c2d16ac725d6c236e2b7a93`  
		Last Modified: Wed, 28 Jan 2026 03:26:57 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.9-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:0b3947f754f901b0eee6981e99cd9d177d98f9208d60e99599a2182ee456cb48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.6 KB (691589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baf3c479b5f2c96864cbcd1eeccb783380ad8a72539788725799c866d6198c2b`

```dockerfile
```

-	Layers:
	-	`sha256:01b16cc3b5518976d91b8bddbc7009f186a3aef03547cabb60c8a13ddbbc8227`  
		Last Modified: Wed, 28 Jan 2026 03:26:56 GMT  
		Size: 676.6 KB (676622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1541f8caff84dbcdb88fbc06c12d3a170bfb849a19f16feb4f4857708b70317a`  
		Last Modified: Wed, 28 Jan 2026 03:26:56 GMT  
		Size: 15.0 KB (14967 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12`

```console
$ docker pull influxdb@sha256:af052b05a9347fcc3e58db9255a2580d3d9fd5ee6a4ac6ba4743745add0e2545
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
$ docker pull influxdb@sha256:008d88c028b0891a7c2c224fc4a93b404008a66bc50d43612e98e5711c0db25a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110735296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6065a06d76957339401244517ee764233f2d07e25eae4927239d6cebee06e39c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:49:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Apr 2026 22:22:33 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Mon, 13 Apr 2026 22:22:39 GMT
ENV INFLUXDB_VERSION=1.12.4
# Mon, 13 Apr 2026 22:22:39 GMT
ENV INFLUXDB_PR=-1
# Mon, 13 Apr 2026 22:22:39 GMT
ENV INFLUXDB_PV=1.12.4-1
# Mon, 13 Apr 2026 22:22:39 GMT
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_PV}_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Mon, 13 Apr 2026 22:22:40 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Mon, 13 Apr 2026 22:22:40 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 13 Apr 2026 22:22:40 GMT
VOLUME [/var/lib/influxdb]
# Mon, 13 Apr 2026 22:22:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 13 Apr 2026 22:22:40 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Mon, 13 Apr 2026 22:22:40 GMT
USER influxdb
# Mon, 13 Apr 2026 22:22:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 13 Apr 2026 22:22:40 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af98f0879b367460715b477e9118922ba24f17d9a4ad8d70e595a9c4cf56990`  
		Last Modified: Tue, 07 Apr 2026 01:49:50 GMT  
		Size: 23.6 MB (23604705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5f35a5e42bfad2e917666e77e1b25d2972767bf359090ebae32f74334ec006`  
		Last Modified: Mon, 13 Apr 2026 22:22:51 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c469645d5ad9af724e531c907ef47681764a17b1f7ea9d287b5e1c3b607ba3f`  
		Last Modified: Mon, 13 Apr 2026 22:22:53 GMT  
		Size: 38.8 MB (38754418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7644d7e5042e73d11edddcb66173eb98e322ce8c5defcd7d90b295be5cc0f00e`  
		Last Modified: Mon, 13 Apr 2026 22:22:51 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060ab21f30c8f996d7580b3c6bb0254d0ff57e5c5d94d73dd833b17c485c4f36`  
		Last Modified: Mon, 13 Apr 2026 22:22:51 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6eab66781d8a62125e297cda4b5fb7bcfc0264b48c25aa22cae2c59c5629f1`  
		Last Modified: Mon, 13 Apr 2026 22:22:52 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:8d7f6a6d8cd167c0902c560659ff072e2a811e4c70591d6c5765b96717cdd3b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b26088e24001296457cc5a2ffd24b3545b51f208609324ca3a26203a3c5a37`

```dockerfile
```

-	Layers:
	-	`sha256:37a8d4a7c406dd649d962b4b5232af85b5295f86d877dc9bc25aa2950dff6f86`  
		Last Modified: Mon, 13 Apr 2026 22:22:51 GMT  
		Size: 4.7 MB (4677589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6539f38cad80de050f1759379faa8df8d6b94adbc019df5a379f762717edc674`  
		Last Modified: Mon, 13 Apr 2026 22:22:51 GMT  
		Size: 16.6 KB (16624 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12-alpine`

```console
$ docker pull influxdb@sha256:47dc95505ebba09dc12277d98a998949e200771da78aaa9e53d3e27566516d33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.12-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:62be838c3c5982a3e1535b0585d97dedb52201ed9904e970af55bb9b87ec78bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46926689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dd2af07f2fd8a79c1b78a0f8333de5a4de1917e2e2cbc917c8e79e122d6c767`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Mon, 13 Apr 2026 22:49:47 GMT
RUN apk add --no-cache bash ca-certificates tzdata &&     update-ca-certificates # buildkit
# Mon, 13 Apr 2026 22:49:52 GMT
ENV INFLUXDB_VERSION=1.12.4
# Mon, 13 Apr 2026 22:49:52 GMT
ENV INFLUXDB_PR=
# Mon, 13 Apr 2026 22:49:52 GMT
ENV INFLUXDB_PV=1.12.4
# Mon, 13 Apr 2026 22:49:52 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     case "$(apk --print-arch)" in         x86_64)  ARCH=amd64 ;;         aarch64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz.asc"         "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz" &&     tar -xvf "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz"         -C /usr/bin --strip-components 1 --wildcards             'influxdb-*/influx'             'influxdb-*/influx_inspect'             'influxdb-*/influxd' &&     rm "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz.asc"        "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz" &&     apk del .build-deps # buildkit
# Mon, 13 Apr 2026 22:49:52 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Mon, 13 Apr 2026 22:49:52 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Mon, 13 Apr 2026 22:49:52 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 13 Apr 2026 22:49:52 GMT
VOLUME [/var/lib/influxdb]
# Mon, 13 Apr 2026 22:49:52 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 13 Apr 2026 22:49:52 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Mon, 13 Apr 2026 22:49:52 GMT
USER influxdb
# Mon, 13 Apr 2026 22:49:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 13 Apr 2026 22:49:52 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8cde42a0fd19c0c0c67c4db59c816a1b3776ceae96bbfc98cc1a16c6cf0e957`  
		Last Modified: Mon, 13 Apr 2026 22:50:02 GMT  
		Size: 1.2 MB (1225281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50de563b9e21e627365f511a8466a86fea8b00c91a0a834d958b2d8537bd2dde`  
		Last Modified: Mon, 13 Apr 2026 22:50:04 GMT  
		Size: 42.1 MB (42054957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0e382c61f57fc1a580dafad445f61e03af36dc13b27bede6a51808962e230c`  
		Last Modified: Mon, 13 Apr 2026 22:50:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948df802a5fc643b8437c97014b9bc5888c5d6547a7bf65db3ea800eccd0a63c`  
		Last Modified: Mon, 13 Apr 2026 22:50:02 GMT  
		Size: 995.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af3f988464372ee62b91ef6614ef4e6c68c6259a4a9d45c8b5d1c90ac4d4ae1`  
		Last Modified: Mon, 13 Apr 2026 22:50:03 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a257e6a5e6796794ab5be0829d9c6867b10c66f9ead78b32ddcba685382f26`  
		Last Modified: Mon, 13 Apr 2026 22:50:04 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:a73efc8c9e63319bda9b3585663f2d88f5dd1fb7c9fca5e3157e60e8311731d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **780.6 KB (780592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d0162dc83ddd6f4fe895e16168c0ecfe9df9f5369c2ad53afdb92ce14091ea`

```dockerfile
```

-	Layers:
	-	`sha256:9418b511e94bad748d434cae63799c9cfdc281346b6f170dcf3b53faa5eb607e`  
		Last Modified: Mon, 13 Apr 2026 22:50:02 GMT  
		Size: 761.9 KB (761875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac4ab01923cfebe199ea6c5d67c6403b3af5d40caafdf4e6e890e120a4d2e321`  
		Last Modified: Mon, 13 Apr 2026 22:50:02 GMT  
		Size: 18.7 KB (18717 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.12-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:8f4757a880a48f0bca11ae292da2705f40158be2417d8b98260e4771eb0797ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (43967106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f1f4c102b7c621fafcf9a330d435a413481c87e1a49009e1bccd2c9e80e8f2a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:07 GMT
ADD alpine-minirootfs-3.21.6-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:07 GMT
CMD ["/bin/sh"]
# Mon, 13 Apr 2026 22:23:00 GMT
RUN apk add --no-cache bash ca-certificates tzdata &&     update-ca-certificates # buildkit
# Mon, 13 Apr 2026 22:23:05 GMT
ENV INFLUXDB_VERSION=1.12.4
# Mon, 13 Apr 2026 22:23:05 GMT
ENV INFLUXDB_PR=
# Mon, 13 Apr 2026 22:23:05 GMT
ENV INFLUXDB_PV=1.12.4
# Mon, 13 Apr 2026 22:23:05 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     case "$(apk --print-arch)" in         x86_64)  ARCH=amd64 ;;         aarch64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz.asc"         "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz" &&     tar -xvf "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz"         -C /usr/bin --strip-components 1 --wildcards             'influxdb-*/influx'             'influxdb-*/influx_inspect'             'influxdb-*/influxd' &&     rm "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz.asc"        "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz" &&     apk del .build-deps # buildkit
# Mon, 13 Apr 2026 22:23:05 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Mon, 13 Apr 2026 22:23:05 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Mon, 13 Apr 2026 22:23:05 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 13 Apr 2026 22:23:05 GMT
VOLUME [/var/lib/influxdb]
# Mon, 13 Apr 2026 22:23:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 13 Apr 2026 22:23:05 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Mon, 13 Apr 2026 22:23:05 GMT
USER influxdb
# Mon, 13 Apr 2026 22:23:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 13 Apr 2026 22:23:05 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:a447a5de8f4eb4a987d81c0afa14d459cc714599c020c08f45fafa9c6c904b30`  
		Last Modified: Wed, 28 Jan 2026 01:18:13 GMT  
		Size: 4.0 MB (3992880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9d657a3e85e367e47d46f850fe005abf79470173ac068ef85d0eece46336fe`  
		Last Modified: Mon, 13 Apr 2026 22:23:15 GMT  
		Size: 1.3 MB (1290529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40c2657bb386cbfe18546b4d58753de127e04498eb2b44afa8e0c6be9c2efbd`  
		Last Modified: Mon, 13 Apr 2026 22:23:15 GMT  
		Size: 38.7 MB (38680985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04966b83870e70f614e9fa716c821830f84367e6dc000a3e579ab327b69a7c89`  
		Last Modified: Mon, 13 Apr 2026 22:23:14 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c4456be041285db6ca13454f98ea3fba2a2867e27030bda766349d507f32bc5`  
		Last Modified: Mon, 13 Apr 2026 22:23:14 GMT  
		Size: 995.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d80b402cee4c08e573826aad8735183e4e63f0e4bfb044e623ff3779a115e4`  
		Last Modified: Mon, 13 Apr 2026 22:23:15 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5404b4c0318bf24481c23063e7808d06d5020397385c72e36d2b2b68a14fd75`  
		Last Modified: Mon, 13 Apr 2026 22:23:16 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:5a47ae098328627a9969ad5c0a6f9b6fd55d570e258f0aa70372696bd641b16d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **779.9 KB (779930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45d26be1be46da5fb54ea63104265263415829f462980cdd181f783d85405810`

```dockerfile
```

-	Layers:
	-	`sha256:951ff5c9b77416da68f7b4f7063f325d87de515b1142a1d2d7889338041caa9d`  
		Last Modified: Mon, 13 Apr 2026 22:23:15 GMT  
		Size: 761.1 KB (761102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:625b0ef7da2eac7f0cdcbd0eb51d87ffd14ab210e668b84982f060df4b75c5b6`  
		Last Modified: Mon, 13 Apr 2026 22:23:14 GMT  
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
$ docker pull influxdb@sha256:5b6490fb8c705497ee0e6f583dee7917d7dd852d1bdf5f1f18727b624771bc45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:fe193b88d165027d157676c49a50c373727427dd781423044c379b9357900490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47995269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1400d4cce180749da87d26bc2280d46b2b35a19829e902f86b8e549d201c9114`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Mon, 13 Apr 2026 22:50:03 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Mon, 13 Apr 2026 22:50:09 GMT
ENV INFLUXDB_VERSION=1.12.4-c1.12.4
# Mon, 13 Apr 2026 22:50:09 GMT
ENV INFLUXDB_PR=
# Mon, 13 Apr 2026 22:50:09 GMT
ENV INFLUXDB_PV=1.12.4-c1.12.4
# Mon, 13 Apr 2026 22:50:09 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"         "influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     tar -xvf "influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz"         -C /usr/bin --strip-components 1 --wildcards             'influxdb-*/influx'             'influxdb-*/influx_inspect'             'influxdb-*/influxd' &&     rm "influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"        "influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     apk del .build-deps # buildkit
# Mon, 13 Apr 2026 22:50:09 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Mon, 13 Apr 2026 22:50:09 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 13 Apr 2026 22:50:09 GMT
VOLUME [/var/lib/influxdb]
# Mon, 13 Apr 2026 22:50:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 13 Apr 2026 22:50:09 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Mon, 13 Apr 2026 22:50:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 13 Apr 2026 22:50:09 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1afc286d5bbdcb39f8904b0877ed84b34af0919b60bce9f69f0ab35ec5154772`  
		Last Modified: Mon, 13 Apr 2026 22:50:19 GMT  
		Size: 1.2 MB (1225270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc54203a742edc2fd769d3f38e557a9917ab1f043d1233ce97b8608e761ba4ab`  
		Last Modified: Mon, 13 Apr 2026 22:50:22 GMT  
		Size: 43.1 MB (43124483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5245460d9ba02acba430a33f494e80717d0362863c758ed339e69e58a939b0`  
		Last Modified: Mon, 13 Apr 2026 22:50:19 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182feea32d5f2c7e97b3a1a34fddb9941f3533f2fadd5a0f119c5e7be39d00f9`  
		Last Modified: Mon, 13 Apr 2026 22:50:19 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4789a2ccda4a0bbd39eaad69aa88ebb2099cd6eaca3ef2874630e0ac768aa819`  
		Last Modified: Mon, 13 Apr 2026 22:50:20 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:9d164657b0efe2ae196ced0eda911b7a1fcbc779fb8bbc65f2d6351d97fefb0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **796.7 KB (796748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbfcc232ecf429847315cca44df9cad68816e1741d0715fd745035e1c6965d3b`

```dockerfile
```

-	Layers:
	-	`sha256:77d162daee65dc57dff3ff43aeda16b21d1567502c1f4fad2780b80bdb6a6b00`  
		Last Modified: Mon, 13 Apr 2026 22:50:19 GMT  
		Size: 781.2 KB (781219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5ffb7540edde9c28eb60306b5d916f01c6bac56019896348af85ef93f45d46c`  
		Last Modified: Mon, 13 Apr 2026 22:50:19 GMT  
		Size: 15.5 KB (15529 bytes)  
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
$ docker pull influxdb@sha256:1399838a53ee3703c9af37eb577087eb0f40291fc8e09b53479a929d4764b7c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:d61de40a52297aaa56d18e3010debca632a688d8a5004fbcd7322079d79441e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.2 MB (24199708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0ff78b350c66a25df1e373fe78cb97d5c91c2d22e68c533165046e9055a5ec2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Mon, 13 Apr 2026 22:50:08 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Mon, 13 Apr 2026 22:50:12 GMT
ENV INFLUXDB_VERSION=1.12.4-c1.12.4
# Mon, 13 Apr 2026 22:50:12 GMT
ENV INFLUXDB_PR=
# Mon, 13 Apr 2026 22:50:12 GMT
ENV INFLUXDB_PV=1.12.4-c1.12.4
# Mon, 13 Apr 2026 22:50:12 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"         "influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     tar -xvf "influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz"         -C /usr/bin --strip-components 1 --wildcards             'influxdb-*/influxd-ctl'             'influxdb-*/influxd-meta' &&     rm "influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"        "influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     apk del .build-deps # buildkit
# Mon, 13 Apr 2026 22:50:12 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Mon, 13 Apr 2026 22:50:12 GMT
EXPOSE map[8091/tcp:{}]
# Mon, 13 Apr 2026 22:50:12 GMT
VOLUME [/var/lib/influxdb]
# Mon, 13 Apr 2026 22:50:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 13 Apr 2026 22:50:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 13 Apr 2026 22:50:12 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2621d562714dca58ddfd6c4f47184a3ba159e3f4d4a937ecf8f9adc5cd75586a`  
		Last Modified: Mon, 13 Apr 2026 22:50:19 GMT  
		Size: 1.2 MB (1225273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1cb56bf705dcad92203f7b0c67545d82c8b16c77c1eea340c7d6648c9830c0`  
		Last Modified: Mon, 13 Apr 2026 22:50:19 GMT  
		Size: 19.3 MB (19330125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98de269dd02db91fae1c0a7ce0ce65a5bac22e3a52bbda9ed9d37d93a3425b0`  
		Last Modified: Mon, 13 Apr 2026 22:50:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff45c438882348bd8c049b59f200d17aa2d0dae0ece0137cd114c93a269762d`  
		Last Modified: Mon, 13 Apr 2026 22:50:19 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:685fe20a7d219baa28f470f7e133a5dcc2d37d866e9bf968947f2e128be977c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **696.0 KB (696003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85d63424599170db739dbb576f478daa13ceda6baed477feebaeb8d2a1ea2e6`

```dockerfile
```

-	Layers:
	-	`sha256:b0245f6ef920020b4e4d70605bb41e363e046c6419f79506ce6b732d401652c1`  
		Last Modified: Mon, 13 Apr 2026 22:50:19 GMT  
		Size: 682.1 KB (682073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a894730f95f327149e8766dc9f0bd2d99a0f470d67dc85191716d144cd280b0c`  
		Last Modified: Mon, 13 Apr 2026 22:50:19 GMT  
		Size: 13.9 KB (13930 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12.4`

```console
$ docker pull influxdb@sha256:af052b05a9347fcc3e58db9255a2580d3d9fd5ee6a4ac6ba4743745add0e2545
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
$ docker pull influxdb@sha256:008d88c028b0891a7c2c224fc4a93b404008a66bc50d43612e98e5711c0db25a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110735296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6065a06d76957339401244517ee764233f2d07e25eae4927239d6cebee06e39c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:49:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Apr 2026 22:22:33 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Mon, 13 Apr 2026 22:22:39 GMT
ENV INFLUXDB_VERSION=1.12.4
# Mon, 13 Apr 2026 22:22:39 GMT
ENV INFLUXDB_PR=-1
# Mon, 13 Apr 2026 22:22:39 GMT
ENV INFLUXDB_PV=1.12.4-1
# Mon, 13 Apr 2026 22:22:39 GMT
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_PV}_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Mon, 13 Apr 2026 22:22:40 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Mon, 13 Apr 2026 22:22:40 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 13 Apr 2026 22:22:40 GMT
VOLUME [/var/lib/influxdb]
# Mon, 13 Apr 2026 22:22:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 13 Apr 2026 22:22:40 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Mon, 13 Apr 2026 22:22:40 GMT
USER influxdb
# Mon, 13 Apr 2026 22:22:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 13 Apr 2026 22:22:40 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af98f0879b367460715b477e9118922ba24f17d9a4ad8d70e595a9c4cf56990`  
		Last Modified: Tue, 07 Apr 2026 01:49:50 GMT  
		Size: 23.6 MB (23604705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5f35a5e42bfad2e917666e77e1b25d2972767bf359090ebae32f74334ec006`  
		Last Modified: Mon, 13 Apr 2026 22:22:51 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c469645d5ad9af724e531c907ef47681764a17b1f7ea9d287b5e1c3b607ba3f`  
		Last Modified: Mon, 13 Apr 2026 22:22:53 GMT  
		Size: 38.8 MB (38754418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7644d7e5042e73d11edddcb66173eb98e322ce8c5defcd7d90b295be5cc0f00e`  
		Last Modified: Mon, 13 Apr 2026 22:22:51 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060ab21f30c8f996d7580b3c6bb0254d0ff57e5c5d94d73dd833b17c485c4f36`  
		Last Modified: Mon, 13 Apr 2026 22:22:51 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6eab66781d8a62125e297cda4b5fb7bcfc0264b48c25aa22cae2c59c5629f1`  
		Last Modified: Mon, 13 Apr 2026 22:22:52 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.4` - unknown; unknown

```console
$ docker pull influxdb@sha256:8d7f6a6d8cd167c0902c560659ff072e2a811e4c70591d6c5765b96717cdd3b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b26088e24001296457cc5a2ffd24b3545b51f208609324ca3a26203a3c5a37`

```dockerfile
```

-	Layers:
	-	`sha256:37a8d4a7c406dd649d962b4b5232af85b5295f86d877dc9bc25aa2950dff6f86`  
		Last Modified: Mon, 13 Apr 2026 22:22:51 GMT  
		Size: 4.7 MB (4677589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6539f38cad80de050f1759379faa8df8d6b94adbc019df5a379f762717edc674`  
		Last Modified: Mon, 13 Apr 2026 22:22:51 GMT  
		Size: 16.6 KB (16624 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12.4-alpine`

```console
$ docker pull influxdb@sha256:47dc95505ebba09dc12277d98a998949e200771da78aaa9e53d3e27566516d33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.12.4-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:62be838c3c5982a3e1535b0585d97dedb52201ed9904e970af55bb9b87ec78bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46926689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dd2af07f2fd8a79c1b78a0f8333de5a4de1917e2e2cbc917c8e79e122d6c767`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Mon, 13 Apr 2026 22:49:47 GMT
RUN apk add --no-cache bash ca-certificates tzdata &&     update-ca-certificates # buildkit
# Mon, 13 Apr 2026 22:49:52 GMT
ENV INFLUXDB_VERSION=1.12.4
# Mon, 13 Apr 2026 22:49:52 GMT
ENV INFLUXDB_PR=
# Mon, 13 Apr 2026 22:49:52 GMT
ENV INFLUXDB_PV=1.12.4
# Mon, 13 Apr 2026 22:49:52 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     case "$(apk --print-arch)" in         x86_64)  ARCH=amd64 ;;         aarch64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz.asc"         "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz" &&     tar -xvf "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz"         -C /usr/bin --strip-components 1 --wildcards             'influxdb-*/influx'             'influxdb-*/influx_inspect'             'influxdb-*/influxd' &&     rm "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz.asc"        "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz" &&     apk del .build-deps # buildkit
# Mon, 13 Apr 2026 22:49:52 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Mon, 13 Apr 2026 22:49:52 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Mon, 13 Apr 2026 22:49:52 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 13 Apr 2026 22:49:52 GMT
VOLUME [/var/lib/influxdb]
# Mon, 13 Apr 2026 22:49:52 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 13 Apr 2026 22:49:52 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Mon, 13 Apr 2026 22:49:52 GMT
USER influxdb
# Mon, 13 Apr 2026 22:49:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 13 Apr 2026 22:49:52 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8cde42a0fd19c0c0c67c4db59c816a1b3776ceae96bbfc98cc1a16c6cf0e957`  
		Last Modified: Mon, 13 Apr 2026 22:50:02 GMT  
		Size: 1.2 MB (1225281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50de563b9e21e627365f511a8466a86fea8b00c91a0a834d958b2d8537bd2dde`  
		Last Modified: Mon, 13 Apr 2026 22:50:04 GMT  
		Size: 42.1 MB (42054957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0e382c61f57fc1a580dafad445f61e03af36dc13b27bede6a51808962e230c`  
		Last Modified: Mon, 13 Apr 2026 22:50:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948df802a5fc643b8437c97014b9bc5888c5d6547a7bf65db3ea800eccd0a63c`  
		Last Modified: Mon, 13 Apr 2026 22:50:02 GMT  
		Size: 995.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af3f988464372ee62b91ef6614ef4e6c68c6259a4a9d45c8b5d1c90ac4d4ae1`  
		Last Modified: Mon, 13 Apr 2026 22:50:03 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a257e6a5e6796794ab5be0829d9c6867b10c66f9ead78b32ddcba685382f26`  
		Last Modified: Mon, 13 Apr 2026 22:50:04 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.4-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:a73efc8c9e63319bda9b3585663f2d88f5dd1fb7c9fca5e3157e60e8311731d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **780.6 KB (780592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d0162dc83ddd6f4fe895e16168c0ecfe9df9f5369c2ad53afdb92ce14091ea`

```dockerfile
```

-	Layers:
	-	`sha256:9418b511e94bad748d434cae63799c9cfdc281346b6f170dcf3b53faa5eb607e`  
		Last Modified: Mon, 13 Apr 2026 22:50:02 GMT  
		Size: 761.9 KB (761875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac4ab01923cfebe199ea6c5d67c6403b3af5d40caafdf4e6e890e120a4d2e321`  
		Last Modified: Mon, 13 Apr 2026 22:50:02 GMT  
		Size: 18.7 KB (18717 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.12.4-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:8f4757a880a48f0bca11ae292da2705f40158be2417d8b98260e4771eb0797ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (43967106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f1f4c102b7c621fafcf9a330d435a413481c87e1a49009e1bccd2c9e80e8f2a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:07 GMT
ADD alpine-minirootfs-3.21.6-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:07 GMT
CMD ["/bin/sh"]
# Mon, 13 Apr 2026 22:23:00 GMT
RUN apk add --no-cache bash ca-certificates tzdata &&     update-ca-certificates # buildkit
# Mon, 13 Apr 2026 22:23:05 GMT
ENV INFLUXDB_VERSION=1.12.4
# Mon, 13 Apr 2026 22:23:05 GMT
ENV INFLUXDB_PR=
# Mon, 13 Apr 2026 22:23:05 GMT
ENV INFLUXDB_PV=1.12.4
# Mon, 13 Apr 2026 22:23:05 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     case "$(apk --print-arch)" in         x86_64)  ARCH=amd64 ;;         aarch64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz.asc"         "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz" &&     tar -xvf "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz"         -C /usr/bin --strip-components 1 --wildcards             'influxdb-*/influx'             'influxdb-*/influx_inspect'             'influxdb-*/influxd' &&     rm "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz.asc"        "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz" &&     apk del .build-deps # buildkit
# Mon, 13 Apr 2026 22:23:05 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Mon, 13 Apr 2026 22:23:05 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Mon, 13 Apr 2026 22:23:05 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 13 Apr 2026 22:23:05 GMT
VOLUME [/var/lib/influxdb]
# Mon, 13 Apr 2026 22:23:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 13 Apr 2026 22:23:05 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Mon, 13 Apr 2026 22:23:05 GMT
USER influxdb
# Mon, 13 Apr 2026 22:23:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 13 Apr 2026 22:23:05 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:a447a5de8f4eb4a987d81c0afa14d459cc714599c020c08f45fafa9c6c904b30`  
		Last Modified: Wed, 28 Jan 2026 01:18:13 GMT  
		Size: 4.0 MB (3992880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9d657a3e85e367e47d46f850fe005abf79470173ac068ef85d0eece46336fe`  
		Last Modified: Mon, 13 Apr 2026 22:23:15 GMT  
		Size: 1.3 MB (1290529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40c2657bb386cbfe18546b4d58753de127e04498eb2b44afa8e0c6be9c2efbd`  
		Last Modified: Mon, 13 Apr 2026 22:23:15 GMT  
		Size: 38.7 MB (38680985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04966b83870e70f614e9fa716c821830f84367e6dc000a3e579ab327b69a7c89`  
		Last Modified: Mon, 13 Apr 2026 22:23:14 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c4456be041285db6ca13454f98ea3fba2a2867e27030bda766349d507f32bc5`  
		Last Modified: Mon, 13 Apr 2026 22:23:14 GMT  
		Size: 995.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d80b402cee4c08e573826aad8735183e4e63f0e4bfb044e623ff3779a115e4`  
		Last Modified: Mon, 13 Apr 2026 22:23:15 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5404b4c0318bf24481c23063e7808d06d5020397385c72e36d2b2b68a14fd75`  
		Last Modified: Mon, 13 Apr 2026 22:23:16 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.4-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:5a47ae098328627a9969ad5c0a6f9b6fd55d570e258f0aa70372696bd641b16d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **779.9 KB (779930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45d26be1be46da5fb54ea63104265263415829f462980cdd181f783d85405810`

```dockerfile
```

-	Layers:
	-	`sha256:951ff5c9b77416da68f7b4f7063f325d87de515b1142a1d2d7889338041caa9d`  
		Last Modified: Mon, 13 Apr 2026 22:23:15 GMT  
		Size: 761.1 KB (761102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:625b0ef7da2eac7f0cdcbd0eb51d87ffd14ab210e668b84982f060df4b75c5b6`  
		Last Modified: Mon, 13 Apr 2026 22:23:14 GMT  
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
$ docker pull influxdb@sha256:5b6490fb8c705497ee0e6f583dee7917d7dd852d1bdf5f1f18727b624771bc45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12.4-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:fe193b88d165027d157676c49a50c373727427dd781423044c379b9357900490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47995269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1400d4cce180749da87d26bc2280d46b2b35a19829e902f86b8e549d201c9114`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Mon, 13 Apr 2026 22:50:03 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Mon, 13 Apr 2026 22:50:09 GMT
ENV INFLUXDB_VERSION=1.12.4-c1.12.4
# Mon, 13 Apr 2026 22:50:09 GMT
ENV INFLUXDB_PR=
# Mon, 13 Apr 2026 22:50:09 GMT
ENV INFLUXDB_PV=1.12.4-c1.12.4
# Mon, 13 Apr 2026 22:50:09 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"         "influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     tar -xvf "influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz"         -C /usr/bin --strip-components 1 --wildcards             'influxdb-*/influx'             'influxdb-*/influx_inspect'             'influxdb-*/influxd' &&     rm "influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"        "influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     apk del .build-deps # buildkit
# Mon, 13 Apr 2026 22:50:09 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Mon, 13 Apr 2026 22:50:09 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 13 Apr 2026 22:50:09 GMT
VOLUME [/var/lib/influxdb]
# Mon, 13 Apr 2026 22:50:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 13 Apr 2026 22:50:09 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Mon, 13 Apr 2026 22:50:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 13 Apr 2026 22:50:09 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1afc286d5bbdcb39f8904b0877ed84b34af0919b60bce9f69f0ab35ec5154772`  
		Last Modified: Mon, 13 Apr 2026 22:50:19 GMT  
		Size: 1.2 MB (1225270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc54203a742edc2fd769d3f38e557a9917ab1f043d1233ce97b8608e761ba4ab`  
		Last Modified: Mon, 13 Apr 2026 22:50:22 GMT  
		Size: 43.1 MB (43124483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5245460d9ba02acba430a33f494e80717d0362863c758ed339e69e58a939b0`  
		Last Modified: Mon, 13 Apr 2026 22:50:19 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182feea32d5f2c7e97b3a1a34fddb9941f3533f2fadd5a0f119c5e7be39d00f9`  
		Last Modified: Mon, 13 Apr 2026 22:50:19 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4789a2ccda4a0bbd39eaad69aa88ebb2099cd6eaca3ef2874630e0ac768aa819`  
		Last Modified: Mon, 13 Apr 2026 22:50:20 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.4-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:9d164657b0efe2ae196ced0eda911b7a1fcbc779fb8bbc65f2d6351d97fefb0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **796.7 KB (796748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbfcc232ecf429847315cca44df9cad68816e1741d0715fd745035e1c6965d3b`

```dockerfile
```

-	Layers:
	-	`sha256:77d162daee65dc57dff3ff43aeda16b21d1567502c1f4fad2780b80bdb6a6b00`  
		Last Modified: Mon, 13 Apr 2026 22:50:19 GMT  
		Size: 781.2 KB (781219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5ffb7540edde9c28eb60306b5d916f01c6bac56019896348af85ef93f45d46c`  
		Last Modified: Mon, 13 Apr 2026 22:50:19 GMT  
		Size: 15.5 KB (15529 bytes)  
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
$ docker pull influxdb@sha256:1399838a53ee3703c9af37eb577087eb0f40291fc8e09b53479a929d4764b7c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12.4-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:d61de40a52297aaa56d18e3010debca632a688d8a5004fbcd7322079d79441e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.2 MB (24199708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0ff78b350c66a25df1e373fe78cb97d5c91c2d22e68c533165046e9055a5ec2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Mon, 13 Apr 2026 22:50:08 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Mon, 13 Apr 2026 22:50:12 GMT
ENV INFLUXDB_VERSION=1.12.4-c1.12.4
# Mon, 13 Apr 2026 22:50:12 GMT
ENV INFLUXDB_PR=
# Mon, 13 Apr 2026 22:50:12 GMT
ENV INFLUXDB_PV=1.12.4-c1.12.4
# Mon, 13 Apr 2026 22:50:12 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"         "influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     tar -xvf "influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz"         -C /usr/bin --strip-components 1 --wildcards             'influxdb-*/influxd-ctl'             'influxdb-*/influxd-meta' &&     rm "influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"        "influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     apk del .build-deps # buildkit
# Mon, 13 Apr 2026 22:50:12 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Mon, 13 Apr 2026 22:50:12 GMT
EXPOSE map[8091/tcp:{}]
# Mon, 13 Apr 2026 22:50:12 GMT
VOLUME [/var/lib/influxdb]
# Mon, 13 Apr 2026 22:50:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 13 Apr 2026 22:50:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 13 Apr 2026 22:50:12 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2621d562714dca58ddfd6c4f47184a3ba159e3f4d4a937ecf8f9adc5cd75586a`  
		Last Modified: Mon, 13 Apr 2026 22:50:19 GMT  
		Size: 1.2 MB (1225273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1cb56bf705dcad92203f7b0c67545d82c8b16c77c1eea340c7d6648c9830c0`  
		Last Modified: Mon, 13 Apr 2026 22:50:19 GMT  
		Size: 19.3 MB (19330125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98de269dd02db91fae1c0a7ce0ce65a5bac22e3a52bbda9ed9d37d93a3425b0`  
		Last Modified: Mon, 13 Apr 2026 22:50:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff45c438882348bd8c049b59f200d17aa2d0dae0ece0137cd114c93a269762d`  
		Last Modified: Mon, 13 Apr 2026 22:50:19 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.4-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:685fe20a7d219baa28f470f7e133a5dcc2d37d866e9bf968947f2e128be977c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **696.0 KB (696003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85d63424599170db739dbb576f478daa13ceda6baed477feebaeb8d2a1ea2e6`

```dockerfile
```

-	Layers:
	-	`sha256:b0245f6ef920020b4e4d70605bb41e363e046c6419f79506ce6b732d401652c1`  
		Last Modified: Mon, 13 Apr 2026 22:50:19 GMT  
		Size: 682.1 KB (682073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a894730f95f327149e8766dc9f0bd2d99a0f470d67dc85191716d144cd280b0c`  
		Last Modified: Mon, 13 Apr 2026 22:50:19 GMT  
		Size: 13.9 KB (13930 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2`

```console
$ docker pull influxdb@sha256:96410d41a98c02fa5fcddc44cf708e297c8afcf02cd5bb6c620d4ae6a6d12390
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2` - linux; amd64

```console
$ docker pull influxdb@sha256:68ed01481f413495fe1bba1ed283af3a1935d833676e0f5047aa24fb77906a92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107240605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d26ea8f3e6e87bd75cdf5cebdfbf8314a0498fa64c3d76e817023ca0ce9bf3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:58:14 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:58:14 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 07 Apr 2026 01:58:14 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 07 Apr 2026 01:58:16 GMT
ENV GOSU_VER=1.19
# Tue, 07 Apr 2026 01:58:16 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 07 Apr 2026 01:58:16 GMT
ENV INFLUXDB_VERSION=2.8.0
# Tue, 07 Apr 2026 01:58:16 GMT
ENV INFLUXDB_PR=-2
# Tue, 07 Apr 2026 01:58:16 GMT
ENV INFLUXDB_PV=2.8.0-2
# Tue, 07 Apr 2026 01:58:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 07 Apr 2026 01:58:18 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 07 Apr 2026 01:58:19 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 07 Apr 2026 01:58:19 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 07 Apr 2026 01:58:19 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 07 Apr 2026 01:58:19 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 07 Apr 2026 01:58:19 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:58:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 01:58:19 GMT
CMD ["influxd"]
# Tue, 07 Apr 2026 01:58:19 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 07 Apr 2026 01:58:19 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 07 Apr 2026 01:58:19 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 07 Apr 2026 01:58:19 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 07 Apr 2026 01:58:19 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a116bfcd84372702b219d6bae2ee7f1bdb1e6020d05189bc3c26e279e7ab2364`  
		Last Modified: Tue, 07 Apr 2026 01:58:31 GMT  
		Size: 9.8 MB (9798183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:474de9ab304f8664364821fd54a509679041419851afe35980fbd7c13a2c3d97`  
		Last Modified: Tue, 07 Apr 2026 01:58:31 GMT  
		Size: 6.2 MB (6156974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b83865bdaccd9bb5e11b4016b8576733196b451a7ccbd76483a142c59c43d9a`  
		Last Modified: Tue, 07 Apr 2026 01:58:31 GMT  
		Size: 3.2 KB (3232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8f0f8d0f417d9c4f8e42e10838b3c5356ffe44db60dbd713c090b865a36a8f`  
		Last Modified: Tue, 07 Apr 2026 01:58:31 GMT  
		Size: 811.5 KB (811482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb6e598a64d1bb4e5c2b149548399300221b418b182dd8be2b3dc236d88198b`  
		Last Modified: Tue, 07 Apr 2026 01:58:34 GMT  
		Size: 50.5 MB (50451807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeeb37736cabf4a78a0dbde353fe1882f8add4378e667aa82cd363e1e8a03075`  
		Last Modified: Tue, 07 Apr 2026 01:58:33 GMT  
		Size: 11.8 MB (11775867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4badd18ae9f94083936d589b872c729022b8ebd1e531bbfb4095b4c12794edaa`  
		Last Modified: Tue, 07 Apr 2026 01:58:33 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8568054b22810d03f8d0a1cca53fbf9dbc964499c9d672bb65efdf9fbdc3bc`  
		Last Modified: Tue, 07 Apr 2026 01:58:33 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe60089c21668a33bf2ca8e336cf38c667a4f9d13cd9a87462169d50423a93a`  
		Last Modified: Tue, 07 Apr 2026 01:58:34 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:9ad39b5f4622e6dd7b1921af3eef50210a48ca52dcdf489e17ccec5e88499ebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81fcded457e0dde721973237e4f4609db993674c5a1d6e1d50d47d10728485a3`

```dockerfile
```

-	Layers:
	-	`sha256:9d436efb5b4b564ec8f9e830616391ca4e4bf3aa27df1b3060eb7e944e247d3a`  
		Last Modified: Tue, 07 Apr 2026 01:58:31 GMT  
		Size: 2.9 MB (2934237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3eb7467cb3329a9d9c05e5832575b1eaa8f1ed181e6e49c6d4eab15a218e04f`  
		Last Modified: Tue, 07 Apr 2026 01:58:31 GMT  
		Size: 33.6 KB (33620 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:2311605af7772ef47b927d03db36c3fb215b3ce87982712b8d72a5525a18a82d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103639786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:202eb409813be9db84b84bba7249daa05613ed232209b3ee3565c150f8865387`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:01:47 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:01:48 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 07 Apr 2026 02:01:48 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 07 Apr 2026 02:01:49 GMT
ENV GOSU_VER=1.19
# Tue, 07 Apr 2026 02:01:49 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 07 Apr 2026 02:01:49 GMT
ENV INFLUXDB_VERSION=2.8.0
# Tue, 07 Apr 2026 02:01:49 GMT
ENV INFLUXDB_PR=-2
# Tue, 07 Apr 2026 02:01:49 GMT
ENV INFLUXDB_PV=2.8.0-2
# Tue, 07 Apr 2026 02:01:52 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 07 Apr 2026 02:01:52 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 07 Apr 2026 02:01:53 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 07 Apr 2026 02:01:53 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 07 Apr 2026 02:01:53 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 07 Apr 2026 02:01:53 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 07 Apr 2026 02:01:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 02:01:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 02:01:53 GMT
CMD ["influxd"]
# Tue, 07 Apr 2026 02:01:53 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 07 Apr 2026 02:01:53 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 07 Apr 2026 02:01:53 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 07 Apr 2026 02:01:53 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 07 Apr 2026 02:01:53 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00120dc253bd72ad4cf1854724026a81aaf4970b1b00f051ae589a8ecb399dc`  
		Last Modified: Tue, 07 Apr 2026 02:02:04 GMT  
		Size: 9.6 MB (9626917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c98a25d698b6f70d76994e2a0c41ebc991071438847d492e353d6db4eed8965`  
		Last Modified: Tue, 07 Apr 2026 02:02:04 GMT  
		Size: 5.8 MB (5790427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd92e0afeff73eda856e070de3a3920326d1d3d47ebd9a96e265d21ee7d7fad`  
		Last Modified: Tue, 07 Apr 2026 02:02:04 GMT  
		Size: 3.2 KB (3231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85d5b89607330aaceaf098690c579352497d8af3213a534e4ab8e4e0cc055f3`  
		Last Modified: Tue, 07 Apr 2026 02:02:04 GMT  
		Size: 766.4 KB (766371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24f1e34c12a55ea2e93376696df4031d1e98d9471c477cebb06f2e344ccd9fd`  
		Last Modified: Tue, 07 Apr 2026 02:02:07 GMT  
		Size: 48.2 MB (48229552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f058781f0fcd0beafff67981c71ad42c14fb858d6878c0a9e13dc27cc9738b26`  
		Last Modified: Tue, 07 Apr 2026 02:02:06 GMT  
		Size: 11.1 MB (11100394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7aaae010a587cf5a601d46a07d45b378f37c219e996cf7da04e3451ce40f09`  
		Last Modified: Tue, 07 Apr 2026 02:02:06 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f3da28a5bb0e301c7a7a0f4878ec11e653083ea8a0485b114f2c4661c6e5e3`  
		Last Modified: Tue, 07 Apr 2026 02:02:06 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52e0436c606da832d52ceec71b1cf5d5ff170863a1cb76baac382d62f44cfee`  
		Last Modified: Tue, 07 Apr 2026 02:02:07 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:dd3c5e7b9b9671abe2a59b0efea0f7c021b79ea63ba3dbc48760c622647406d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cc341b69e5b33632b785cffba7cbde4509e4ef6926df182df78220fa500ed06`

```dockerfile
```

-	Layers:
	-	`sha256:570e1645673b88b50800b3b86275be91a90a2b107aa8c21d1cb94112ea3f7419`  
		Last Modified: Tue, 07 Apr 2026 02:02:04 GMT  
		Size: 2.9 MB (2933717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb943467e2459ff3405858d9c0df13744923b5ad93d4dddad5d6de90e6559d5f`  
		Last Modified: Tue, 07 Apr 2026 02:02:04 GMT  
		Size: 33.8 KB (33815 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2-alpine`

```console
$ docker pull influxdb@sha256:f15dfc604753f53b180364a331b46c2f4bc5c08a665d025982b301efa69bc2f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:e224ef04c67e6587c0b6f9f0d5e125f291bdc080b17e6d498b0fa10f60c9eccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81900321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b6866841a1a833e0595336141bd26bc5088eafcd30cd7576f2382ddbfd53eea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:26:53 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:26:55 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:26:55 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 28 Jan 2026 03:26:55 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 28 Jan 2026 03:26:59 GMT
ENV INFLUXDB_VERSION=2.8.0
# Wed, 28 Jan 2026 03:26:59 GMT
ENV INFLUXDB_PR=-2
# Wed, 28 Jan 2026 03:26:59 GMT
ENV INFLUXDB_PV=2.8.0-2
# Wed, 28 Jan 2026 03:26:59 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 28 Jan 2026 03:26:59 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 28 Jan 2026 03:27:00 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 28 Jan 2026 03:27:00 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 28 Jan 2026 03:27:00 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 28 Jan 2026 03:27:00 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 28 Jan 2026 03:27:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:27:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:27:00 GMT
CMD ["influxd"]
# Wed, 28 Jan 2026 03:27:00 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 Jan 2026 03:27:00 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 28 Jan 2026 03:27:00 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 28 Jan 2026 03:27:00 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 28 Jan 2026 03:27:00 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da2f69740401b1208019e15e303957ef5e65950b9f1a7b4939e5fc136f96a3f`  
		Last Modified: Wed, 28 Jan 2026 03:27:10 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a44134f5fc0c6cdf52aa1278b3f3f6eee8a5c2a452dd4aff61503e192f645e`  
		Last Modified: Wed, 28 Jan 2026 03:27:10 GMT  
		Size: 9.9 MB (9863904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005d64a40f5cb225c3bc69263c0469aa02ab005ed8b21e6e7a89b3675ec50b07`  
		Last Modified: Wed, 28 Jan 2026 03:27:10 GMT  
		Size: 6.2 MB (6156984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201d3a17f0762d441938d9cd05ad8c611220953a6d8de6a93072a25f16c4692b`  
		Last Modified: Wed, 28 Jan 2026 03:27:10 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15a968cb865edd4609ac8b32d717b03922a73cb3f7590c30780bad10277e537`  
		Last Modified: Wed, 28 Jan 2026 03:27:12 GMT  
		Size: 50.5 MB (50451881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75205be004b2b555f72327c5eb07d199aae883c0df672642e69dfcdc4dab8cf`  
		Last Modified: Wed, 28 Jan 2026 03:27:12 GMT  
		Size: 11.8 MB (11775858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f48dd36db7dbb28ea6f0a2d7958ef354180d24d56cf270dc22a547a09111687`  
		Last Modified: Wed, 28 Jan 2026 03:27:12 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc78f60a45d07493bbb7618a6d38e70f86076b21dc6487f08ed2684b1ee56b8`  
		Last Modified: Wed, 28 Jan 2026 03:27:12 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b85aa016614d9f14630b36f109832ec79194ab3adcd5994b8868dec4259eef`  
		Last Modified: Wed, 28 Jan 2026 03:27:06 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:47754c46831f8311db55db258098d6bd94c0b23caf15316fd1bb193490033dff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **946.7 KB (946732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a8f0be80fc287fb05cf358d3814bac779c2ad698308821166b0c53f73f17340`

```dockerfile
```

-	Layers:
	-	`sha256:aa884cdf050c202632293939e889ccbda051a7d2d9e8139c8fb38b9f0383362f`  
		Last Modified: Wed, 28 Jan 2026 03:27:10 GMT  
		Size: 915.9 KB (915886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80b43ac4284db4608a9e3f907899268737ae652fd8183dab50b925feb71dbeb7`  
		Last Modified: Wed, 28 Jan 2026 03:27:10 GMT  
		Size: 30.8 KB (30846 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ff96fbac0d6cf44eb703e9cd7e5f2a09bfd2f78e814185c58f2a34d9fecd5cf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78945372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2200d46793614389922d59d788c241bf4d159c9f22de8fb362b4321d920953e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:07 GMT
ADD alpine-minirootfs-3.21.6-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:07 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:15:25 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:15:26 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:15:27 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 28 Jan 2026 03:15:27 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 28 Jan 2026 03:15:31 GMT
ENV INFLUXDB_VERSION=2.8.0
# Wed, 28 Jan 2026 03:15:31 GMT
ENV INFLUXDB_PR=-2
# Wed, 28 Jan 2026 03:15:31 GMT
ENV INFLUXDB_PV=2.8.0-2
# Wed, 28 Jan 2026 03:15:31 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 28 Jan 2026 03:15:31 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 28 Jan 2026 03:15:33 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 28 Jan 2026 03:15:33 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 28 Jan 2026 03:15:33 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 28 Jan 2026 03:15:33 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 28 Jan 2026 03:15:33 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:15:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:15:33 GMT
CMD ["influxd"]
# Wed, 28 Jan 2026 03:15:33 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 Jan 2026 03:15:33 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 28 Jan 2026 03:15:33 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 28 Jan 2026 03:15:33 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 28 Jan 2026 03:15:33 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:a447a5de8f4eb4a987d81c0afa14d459cc714599c020c08f45fafa9c6c904b30`  
		Last Modified: Wed, 28 Jan 2026 01:18:13 GMT  
		Size: 4.0 MB (3992880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6ab2286a7a1f7b2a657fa5f9cd5794c5eaaecea283f7e8ed6df6e1726525eb`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6584e15e052556418670992187d03a8d302b4b08e86a35c3c202d8b763a116`  
		Last Modified: Wed, 28 Jan 2026 03:15:44 GMT  
		Size: 9.8 MB (9824174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b868f1d2c50be9be813066470ac1cbfefc67a3ade4ac5caf84ad8f9f92c7b3c0`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 5.8 MB (5790429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf13e4c27ec5340b32d6db93325cde6c1a76b1bfb444f82b0281a2afaebc423f`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e19b47fb98adca37cda31bb666000a1068add6e40bc68415d079e0810ba271`  
		Last Modified: Wed, 28 Jan 2026 03:15:46 GMT  
		Size: 48.2 MB (48229537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef6ef542d7aecf40c7fa27129ae016a248041943f6f2cf02e5fbdbf2ec3481a`  
		Last Modified: Wed, 28 Jan 2026 03:15:45 GMT  
		Size: 11.1 MB (11100399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728e7d19219b3f2895b7e6f75ee30c3eb1ca3198fc8b91d24484f0d7ae29a970`  
		Last Modified: Wed, 28 Jan 2026 03:15:44 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feabd2445240c8db64c9188502a45203d8bf4fa862e1facd65af80a0a4a05b90`  
		Last Modified: Wed, 28 Jan 2026 03:15:44 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4988bef482c19d2f614d4ec49ed4b57867cbbe8b263aad5779a7cd1a46621fe9`  
		Last Modified: Wed, 28 Jan 2026 03:15:45 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:73ce168dd0f62068e66e3be9e245c1622a2cedfa2c9f879b63d105a81e2f4fa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **946.2 KB (946177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b1de55895028e279fbba3d674a6062cd263237cc82dedc0669e211c20457f0a`

```dockerfile
```

-	Layers:
	-	`sha256:70ed507d37e4c0a2fb8cca40b6a791937d6585d05bfba4bcc080d71d0ca360f7`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 915.1 KB (915137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26164e792c84253eddb0c7007db1811569868d2bf2dd4d2a7056ec4ae310fca0`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 31.0 KB (31040 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7`

```console
$ docker pull influxdb@sha256:d20f6e4394e50af81453a8c86f28fcc5f9b0a9cace8f1e017c61466f9ad49941
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7` - linux; amd64

```console
$ docker pull influxdb@sha256:a94e948be1c9dcb0191f55ae3a205b729a8adf2f6e50bf078ee9c7639e6e8f6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157235560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b7eda5e339cbdee9057690142deb4d5d8626e45f9752b63cfbadd31c02216b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:58:11 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:58:11 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 07 Apr 2026 01:58:11 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 07 Apr 2026 01:58:13 GMT
ENV GOSU_VER=1.16
# Tue, 07 Apr 2026 01:58:13 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 07 Apr 2026 01:58:13 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 07 Apr 2026 01:58:16 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 07 Apr 2026 01:58:16 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 07 Apr 2026 01:58:17 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 07 Apr 2026 01:58:18 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 07 Apr 2026 01:58:18 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 07 Apr 2026 01:58:18 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 07 Apr 2026 01:58:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:58:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 01:58:18 GMT
CMD ["influxd"]
# Tue, 07 Apr 2026 01:58:18 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 07 Apr 2026 01:58:18 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 07 Apr 2026 01:58:18 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 07 Apr 2026 01:58:18 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 07 Apr 2026 01:58:18 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf4732300c22d8f938d8980620035a143693bfa2f00b333cc89844a3d56762c`  
		Last Modified: Tue, 07 Apr 2026 01:58:32 GMT  
		Size: 9.8 MB (9798223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f64705036e93f4fef27b8e07a1cd36efb537d4b812660c1cbcb9feb895229b5`  
		Last Modified: Tue, 07 Apr 2026 01:58:32 GMT  
		Size: 6.2 MB (6156966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4205b0463abbf4cbdfbe889b36327a4e05f8af19efab10d949abfc06e6be4aa`  
		Last Modified: Tue, 07 Apr 2026 01:58:32 GMT  
		Size: 3.2 KB (3231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d67d300e0f29e3b5fb31cdd9040fa4dd845a2862fd87a61c0a9616f33068d73`  
		Last Modified: Tue, 07 Apr 2026 01:58:32 GMT  
		Size: 1.0 MB (1012036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:973ceab516ab6a1b5e3d15abe1d92d813092f2098959e8d31765c82457e331d4`  
		Last Modified: Tue, 07 Apr 2026 01:58:36 GMT  
		Size: 100.2 MB (100246171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bcdac1ee166e17eb1a8995c0a6d5fe90fafcaf1e4500c88be5f148599f0ca69`  
		Last Modified: Tue, 07 Apr 2026 01:58:34 GMT  
		Size: 11.8 MB (11775873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1857888e478b1530dd89966733aefc2c6d3f3240de89094fdbf3d33cadfe58b8`  
		Last Modified: Tue, 07 Apr 2026 01:58:34 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a511af0a03d0a01d0770028bc327baef425a8ae3a4c258ae7243aa2fa23591`  
		Last Modified: Tue, 07 Apr 2026 01:58:34 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af85ab63796cba0ec1da2ea72dc996f6a77710ab26442ee52c64156eb476da1`  
		Last Modified: Tue, 07 Apr 2026 01:58:35 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:a1fd98dbfb47ac4ab8c3b4146f1c7a5f9aad77ef8410b8372940faf21e6d0701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3014384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95a2e41d1c12a4b211a45da67cb00aa4721b81eca47cc866e433ad7b19861787`

```dockerfile
```

-	Layers:
	-	`sha256:6a809d556ac48a1a5168377456cf8321593876bbdc8b387ca6dcbf1362a70133`  
		Last Modified: Tue, 07 Apr 2026 01:58:32 GMT  
		Size: 3.0 MB (2981484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a47095f9ccd88970a436515d939fbd2c4a71ec655ca8330331c337d69c9a0a38`  
		Last Modified: Tue, 07 Apr 2026 01:58:32 GMT  
		Size: 32.9 KB (32900 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:cc84bdcba1b7314ff3c8e073d9d12f2d0121c752daa56b53cd1d9fabcbff8d2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151624418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d55a73f83ccebe62b08efbd2ce1e6ad692374733a10c7ca214e206807b7e1432`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:01:44 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:01:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 07 Apr 2026 02:01:45 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 07 Apr 2026 02:01:47 GMT
ENV GOSU_VER=1.16
# Tue, 07 Apr 2026 02:01:47 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 07 Apr 2026 02:01:47 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 07 Apr 2026 02:01:50 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 07 Apr 2026 02:01:50 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 07 Apr 2026 02:01:52 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 07 Apr 2026 02:01:52 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 07 Apr 2026 02:01:52 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 07 Apr 2026 02:01:52 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 07 Apr 2026 02:01:52 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 02:01:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 02:01:52 GMT
CMD ["influxd"]
# Tue, 07 Apr 2026 02:01:52 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 07 Apr 2026 02:01:52 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 07 Apr 2026 02:01:52 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 07 Apr 2026 02:01:52 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 07 Apr 2026 02:01:52 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ffece9d96d8da53b3b26ca46f441ac71f64d36e91cad87eb8dda2cc13fdc00`  
		Last Modified: Tue, 07 Apr 2026 02:02:07 GMT  
		Size: 9.6 MB (9626877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc4f3130e44196c1264b5a40fb84e36d1e38aa99cddca3d3d34a9ddee50dcd5`  
		Last Modified: Tue, 07 Apr 2026 02:02:07 GMT  
		Size: 5.8 MB (5790427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2577656addd3eb0c01e77bbecdaeea966652cf54d5dede1aef7784bc62d7cfe`  
		Last Modified: Tue, 07 Apr 2026 02:02:07 GMT  
		Size: 3.2 KB (3231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69de5bf8fefd9f974f7406d19fcb344885d1782056b8dc092a70ecc106c3c4ad`  
		Last Modified: Tue, 07 Apr 2026 02:02:07 GMT  
		Size: 938.9 KB (938875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245ffad88d15fdccb00e2438da09f36a8926be0f27adaeb7b9c023696c4c062c`  
		Last Modified: Tue, 07 Apr 2026 02:02:11 GMT  
		Size: 96.0 MB (96041727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2167ea73b0e70b5d28cff57c02f70b55a7a911803949f8ef00de8b925393a949`  
		Last Modified: Tue, 07 Apr 2026 02:02:09 GMT  
		Size: 11.1 MB (11100387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d09dd627dfffa299d1682ba498d72932d4ef8e15848d1dfd5db8fe6bc950b2`  
		Last Modified: Tue, 07 Apr 2026 02:02:08 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07349993a3fc4d39931664b429d53ce4f650a8607fd5a50ce6b06869760f6f03`  
		Last Modified: Tue, 07 Apr 2026 02:02:09 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c90a118d996d96557a83080a006bda132a928a40becd3a28e1911e3d00a1471`  
		Last Modified: Tue, 07 Apr 2026 02:02:10 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:7dd4221822b2eeaab0f30d34fb84e68d46a92ee2f8797689e07d98ced3058546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3013748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42d3393ea86d576c1a7350bab7853bb1765b7beb3c1cd1c28633c07a27f2c716`

```dockerfile
```

-	Layers:
	-	`sha256:c73f31e1a7fa3eaca91b54e3fe41e4f153cac0dc3b70c9123833219eba72248b`  
		Last Modified: Tue, 07 Apr 2026 02:02:07 GMT  
		Size: 3.0 MB (2980688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c95bb569b7b984856d0d7a96b8525ead6c941ca89a7d2961f2e4eb1b7b856e3f`  
		Last Modified: Tue, 07 Apr 2026 02:02:07 GMT  
		Size: 33.1 KB (33060 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7-alpine`

```console
$ docker pull influxdb@sha256:5455e9b8bb42dcb8aa0b8a0354b5f0758d0b4a01f595b8dc03e3f850aa5829e9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:612bcecc00e60a884615b0bd7669b8b331a01c07d112836f5d3f3cad84971230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81569491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a0018b5d72a9c991652b75314e7d9b73175e415b37350cd8eaab65503a2c8d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:26:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:26:47 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:26:48 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 28 Jan 2026 03:26:48 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 28 Jan 2026 03:26:52 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 28 Jan 2026 03:26:52 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 28 Jan 2026 03:26:52 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 28 Jan 2026 03:26:53 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 28 Jan 2026 03:26:53 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 28 Jan 2026 03:26:53 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 28 Jan 2026 03:26:53 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 28 Jan 2026 03:26:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:26:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:26:53 GMT
CMD ["influxd"]
# Wed, 28 Jan 2026 03:26:53 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 Jan 2026 03:26:53 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 28 Jan 2026 03:26:53 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 28 Jan 2026 03:26:53 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 28 Jan 2026 03:26:53 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436196594d4787e25464422fdb786add8269452b390137ac52f5f0c3b20fe340`  
		Last Modified: Wed, 28 Jan 2026 03:27:03 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65542906c81e1ee0ded9601017966688d38e3f3ba962f11243b8a411fd4535ca`  
		Last Modified: Wed, 28 Jan 2026 03:27:03 GMT  
		Size: 9.9 MB (9863993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90c50d107939cea71fc35dbf93f01704d677ca32b2051b919eb9136a5f487ad`  
		Last Modified: Wed, 28 Jan 2026 03:27:03 GMT  
		Size: 6.2 MB (6156987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fde6197f3551b6d05c09ee7576bc43cf7380140d15febded656f5185fbd790`  
		Last Modified: Wed, 28 Jan 2026 03:27:03 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b54bd449211eb719855d1847f0b0b113acfda9d5ed514fcbcc8f28647044559`  
		Last Modified: Wed, 28 Jan 2026 03:27:06 GMT  
		Size: 50.1 MB (50120944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bdb9f2210214e2c0c35256e9c44d4d291216b29b6ff21f59a59bac77b114739`  
		Last Modified: Wed, 28 Jan 2026 03:27:05 GMT  
		Size: 11.8 MB (11775874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d2f24bb888e86c07489b545d9e09c1377251edb528fc8cc88982fee57a3768`  
		Last Modified: Wed, 28 Jan 2026 03:27:04 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f94aa619c7c02f89e7b19a001712c66a63863bed83dd526e2badf77d4560ee`  
		Last Modified: Wed, 28 Jan 2026 03:27:05 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b85aa016614d9f14630b36f109832ec79194ab3adcd5994b8868dec4259eef`  
		Last Modified: Wed, 28 Jan 2026 03:27:06 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:391d0a4a7f2210a76562d45f9b8a72b749d3493384e2594e5d47c4649c51b562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **943.3 KB (943325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36133270ef7c6d804c39b533fd629a82efc6fcb842431934f6c6ceea3a9915d2`

```dockerfile
```

-	Layers:
	-	`sha256:5f45889a2a23271ed96f6449e51d557d7e9860daabd60659a82044c7e9f551b9`  
		Last Modified: Wed, 28 Jan 2026 03:27:03 GMT  
		Size: 913.2 KB (913207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2327d640b31f1db13e558b092ae53d65dd362980ace231384d913410b807ca09`  
		Last Modified: Wed, 28 Jan 2026 03:27:03 GMT  
		Size: 30.1 KB (30118 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:73f3e9affdb305c04861bf10abfb2fa71e56e1bde5819ec1839a7c5eef6ddb7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78733892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c45ed053eaae26a5733f93e13d74cf1a800f771b22b2556958ef785f4b80bf7a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:07 GMT
ADD alpine-minirootfs-3.21.6-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:07 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:15:25 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:15:26 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:15:27 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 28 Jan 2026 03:15:27 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 28 Jan 2026 03:15:31 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 28 Jan 2026 03:15:31 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 28 Jan 2026 03:15:31 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 28 Jan 2026 03:15:33 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 28 Jan 2026 03:15:33 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 28 Jan 2026 03:15:33 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 28 Jan 2026 03:15:33 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 28 Jan 2026 03:15:33 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:15:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:15:33 GMT
CMD ["influxd"]
# Wed, 28 Jan 2026 03:15:33 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 Jan 2026 03:15:33 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 28 Jan 2026 03:15:33 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 28 Jan 2026 03:15:33 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 28 Jan 2026 03:15:33 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:a447a5de8f4eb4a987d81c0afa14d459cc714599c020c08f45fafa9c6c904b30`  
		Last Modified: Wed, 28 Jan 2026 01:18:13 GMT  
		Size: 4.0 MB (3992880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6ab2286a7a1f7b2a657fa5f9cd5794c5eaaecea283f7e8ed6df6e1726525eb`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca9a4aa64e00b6010beac8d9d65eee65d986a04c1e66e51c04fe91ed4293f8c`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 9.8 MB (9824203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbafc709ae0f6eccc66e9b498035cab2fb8cfbebf52a09baececda75ed40a9c2`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 5.8 MB (5790433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf13e4c27ec5340b32d6db93325cde6c1a76b1bfb444f82b0281a2afaebc423f`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b3d5de4828e332fd8e67bc21023a4790edaa370cd3b2b93b9b3b185243b251`  
		Last Modified: Wed, 28 Jan 2026 03:15:45 GMT  
		Size: 48.0 MB (48018004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bbf421b3460db3778b6ef941792140c1a2f05bd3ead30e5d52cd52f861e1422`  
		Last Modified: Wed, 28 Jan 2026 03:15:44 GMT  
		Size: 11.1 MB (11100419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728e7d19219b3f2895b7e6f75ee30c3eb1ca3198fc8b91d24484f0d7ae29a970`  
		Last Modified: Wed, 28 Jan 2026 03:15:44 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feabd2445240c8db64c9188502a45203d8bf4fa862e1facd65af80a0a4a05b90`  
		Last Modified: Wed, 28 Jan 2026 03:15:44 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4988bef482c19d2f614d4ec49ed4b57867cbbe8b263aad5779a7cd1a46621fe9`  
		Last Modified: Wed, 28 Jan 2026 03:15:45 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:f6aa3cd15a9f2092e624e447a80fcbaf5ec708f9439108d58b48beda56ed8d7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **942.7 KB (942722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f2c902e2eb2482e9375c138928510fd89d3c1d1c0a05eae47348822ef543f5`

```dockerfile
```

-	Layers:
	-	`sha256:43b1e61f4f7b667e09b16ac67562eb1e3873695e3a201da43cd36bf5e86399d6`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 912.4 KB (912434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cd7104ff5c58dfbd9314d1b3a2d32ee08e317ca67041a22e548bdff47207103`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 30.3 KB (30288 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7.12`

```console
$ docker pull influxdb@sha256:d20f6e4394e50af81453a8c86f28fcc5f9b0a9cace8f1e017c61466f9ad49941
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.12` - linux; amd64

```console
$ docker pull influxdb@sha256:a94e948be1c9dcb0191f55ae3a205b729a8adf2f6e50bf078ee9c7639e6e8f6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157235560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b7eda5e339cbdee9057690142deb4d5d8626e45f9752b63cfbadd31c02216b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:58:11 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:58:11 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 07 Apr 2026 01:58:11 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 07 Apr 2026 01:58:13 GMT
ENV GOSU_VER=1.16
# Tue, 07 Apr 2026 01:58:13 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 07 Apr 2026 01:58:13 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 07 Apr 2026 01:58:16 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 07 Apr 2026 01:58:16 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 07 Apr 2026 01:58:17 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 07 Apr 2026 01:58:18 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 07 Apr 2026 01:58:18 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 07 Apr 2026 01:58:18 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 07 Apr 2026 01:58:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:58:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 01:58:18 GMT
CMD ["influxd"]
# Tue, 07 Apr 2026 01:58:18 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 07 Apr 2026 01:58:18 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 07 Apr 2026 01:58:18 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 07 Apr 2026 01:58:18 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 07 Apr 2026 01:58:18 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf4732300c22d8f938d8980620035a143693bfa2f00b333cc89844a3d56762c`  
		Last Modified: Tue, 07 Apr 2026 01:58:32 GMT  
		Size: 9.8 MB (9798223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f64705036e93f4fef27b8e07a1cd36efb537d4b812660c1cbcb9feb895229b5`  
		Last Modified: Tue, 07 Apr 2026 01:58:32 GMT  
		Size: 6.2 MB (6156966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4205b0463abbf4cbdfbe889b36327a4e05f8af19efab10d949abfc06e6be4aa`  
		Last Modified: Tue, 07 Apr 2026 01:58:32 GMT  
		Size: 3.2 KB (3231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d67d300e0f29e3b5fb31cdd9040fa4dd845a2862fd87a61c0a9616f33068d73`  
		Last Modified: Tue, 07 Apr 2026 01:58:32 GMT  
		Size: 1.0 MB (1012036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:973ceab516ab6a1b5e3d15abe1d92d813092f2098959e8d31765c82457e331d4`  
		Last Modified: Tue, 07 Apr 2026 01:58:36 GMT  
		Size: 100.2 MB (100246171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bcdac1ee166e17eb1a8995c0a6d5fe90fafcaf1e4500c88be5f148599f0ca69`  
		Last Modified: Tue, 07 Apr 2026 01:58:34 GMT  
		Size: 11.8 MB (11775873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1857888e478b1530dd89966733aefc2c6d3f3240de89094fdbf3d33cadfe58b8`  
		Last Modified: Tue, 07 Apr 2026 01:58:34 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a511af0a03d0a01d0770028bc327baef425a8ae3a4c258ae7243aa2fa23591`  
		Last Modified: Tue, 07 Apr 2026 01:58:34 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af85ab63796cba0ec1da2ea72dc996f6a77710ab26442ee52c64156eb476da1`  
		Last Modified: Tue, 07 Apr 2026 01:58:35 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:a1fd98dbfb47ac4ab8c3b4146f1c7a5f9aad77ef8410b8372940faf21e6d0701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3014384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95a2e41d1c12a4b211a45da67cb00aa4721b81eca47cc866e433ad7b19861787`

```dockerfile
```

-	Layers:
	-	`sha256:6a809d556ac48a1a5168377456cf8321593876bbdc8b387ca6dcbf1362a70133`  
		Last Modified: Tue, 07 Apr 2026 01:58:32 GMT  
		Size: 3.0 MB (2981484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a47095f9ccd88970a436515d939fbd2c4a71ec655ca8330331c337d69c9a0a38`  
		Last Modified: Tue, 07 Apr 2026 01:58:32 GMT  
		Size: 32.9 KB (32900 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7.12` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:cc84bdcba1b7314ff3c8e073d9d12f2d0121c752daa56b53cd1d9fabcbff8d2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151624418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d55a73f83ccebe62b08efbd2ce1e6ad692374733a10c7ca214e206807b7e1432`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:01:44 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:01:45 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 07 Apr 2026 02:01:45 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 07 Apr 2026 02:01:47 GMT
ENV GOSU_VER=1.16
# Tue, 07 Apr 2026 02:01:47 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 07 Apr 2026 02:01:47 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 07 Apr 2026 02:01:50 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 07 Apr 2026 02:01:50 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 07 Apr 2026 02:01:52 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 07 Apr 2026 02:01:52 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 07 Apr 2026 02:01:52 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 07 Apr 2026 02:01:52 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 07 Apr 2026 02:01:52 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 02:01:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 02:01:52 GMT
CMD ["influxd"]
# Tue, 07 Apr 2026 02:01:52 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 07 Apr 2026 02:01:52 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 07 Apr 2026 02:01:52 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 07 Apr 2026 02:01:52 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 07 Apr 2026 02:01:52 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ffece9d96d8da53b3b26ca46f441ac71f64d36e91cad87eb8dda2cc13fdc00`  
		Last Modified: Tue, 07 Apr 2026 02:02:07 GMT  
		Size: 9.6 MB (9626877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc4f3130e44196c1264b5a40fb84e36d1e38aa99cddca3d3d34a9ddee50dcd5`  
		Last Modified: Tue, 07 Apr 2026 02:02:07 GMT  
		Size: 5.8 MB (5790427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2577656addd3eb0c01e77bbecdaeea966652cf54d5dede1aef7784bc62d7cfe`  
		Last Modified: Tue, 07 Apr 2026 02:02:07 GMT  
		Size: 3.2 KB (3231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69de5bf8fefd9f974f7406d19fcb344885d1782056b8dc092a70ecc106c3c4ad`  
		Last Modified: Tue, 07 Apr 2026 02:02:07 GMT  
		Size: 938.9 KB (938875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245ffad88d15fdccb00e2438da09f36a8926be0f27adaeb7b9c023696c4c062c`  
		Last Modified: Tue, 07 Apr 2026 02:02:11 GMT  
		Size: 96.0 MB (96041727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2167ea73b0e70b5d28cff57c02f70b55a7a911803949f8ef00de8b925393a949`  
		Last Modified: Tue, 07 Apr 2026 02:02:09 GMT  
		Size: 11.1 MB (11100387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d09dd627dfffa299d1682ba498d72932d4ef8e15848d1dfd5db8fe6bc950b2`  
		Last Modified: Tue, 07 Apr 2026 02:02:08 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07349993a3fc4d39931664b429d53ce4f650a8607fd5a50ce6b06869760f6f03`  
		Last Modified: Tue, 07 Apr 2026 02:02:09 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c90a118d996d96557a83080a006bda132a928a40becd3a28e1911e3d00a1471`  
		Last Modified: Tue, 07 Apr 2026 02:02:10 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:7dd4221822b2eeaab0f30d34fb84e68d46a92ee2f8797689e07d98ced3058546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3013748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42d3393ea86d576c1a7350bab7853bb1765b7beb3c1cd1c28633c07a27f2c716`

```dockerfile
```

-	Layers:
	-	`sha256:c73f31e1a7fa3eaca91b54e3fe41e4f153cac0dc3b70c9123833219eba72248b`  
		Last Modified: Tue, 07 Apr 2026 02:02:07 GMT  
		Size: 3.0 MB (2980688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c95bb569b7b984856d0d7a96b8525ead6c941ca89a7d2961f2e4eb1b7b856e3f`  
		Last Modified: Tue, 07 Apr 2026 02:02:07 GMT  
		Size: 33.1 KB (33060 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.7.12-alpine`

```console
$ docker pull influxdb@sha256:5455e9b8bb42dcb8aa0b8a0354b5f0758d0b4a01f595b8dc03e3f850aa5829e9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.12-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:612bcecc00e60a884615b0bd7669b8b331a01c07d112836f5d3f3cad84971230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81569491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a0018b5d72a9c991652b75314e7d9b73175e415b37350cd8eaab65503a2c8d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:26:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:26:47 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:26:48 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 28 Jan 2026 03:26:48 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 28 Jan 2026 03:26:52 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 28 Jan 2026 03:26:52 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 28 Jan 2026 03:26:52 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 28 Jan 2026 03:26:53 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 28 Jan 2026 03:26:53 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 28 Jan 2026 03:26:53 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 28 Jan 2026 03:26:53 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 28 Jan 2026 03:26:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:26:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:26:53 GMT
CMD ["influxd"]
# Wed, 28 Jan 2026 03:26:53 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 Jan 2026 03:26:53 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 28 Jan 2026 03:26:53 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 28 Jan 2026 03:26:53 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 28 Jan 2026 03:26:53 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436196594d4787e25464422fdb786add8269452b390137ac52f5f0c3b20fe340`  
		Last Modified: Wed, 28 Jan 2026 03:27:03 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65542906c81e1ee0ded9601017966688d38e3f3ba962f11243b8a411fd4535ca`  
		Last Modified: Wed, 28 Jan 2026 03:27:03 GMT  
		Size: 9.9 MB (9863993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90c50d107939cea71fc35dbf93f01704d677ca32b2051b919eb9136a5f487ad`  
		Last Modified: Wed, 28 Jan 2026 03:27:03 GMT  
		Size: 6.2 MB (6156987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fde6197f3551b6d05c09ee7576bc43cf7380140d15febded656f5185fbd790`  
		Last Modified: Wed, 28 Jan 2026 03:27:03 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b54bd449211eb719855d1847f0b0b113acfda9d5ed514fcbcc8f28647044559`  
		Last Modified: Wed, 28 Jan 2026 03:27:06 GMT  
		Size: 50.1 MB (50120944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bdb9f2210214e2c0c35256e9c44d4d291216b29b6ff21f59a59bac77b114739`  
		Last Modified: Wed, 28 Jan 2026 03:27:05 GMT  
		Size: 11.8 MB (11775874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d2f24bb888e86c07489b545d9e09c1377251edb528fc8cc88982fee57a3768`  
		Last Modified: Wed, 28 Jan 2026 03:27:04 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f94aa619c7c02f89e7b19a001712c66a63863bed83dd526e2badf77d4560ee`  
		Last Modified: Wed, 28 Jan 2026 03:27:05 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b85aa016614d9f14630b36f109832ec79194ab3adcd5994b8868dec4259eef`  
		Last Modified: Wed, 28 Jan 2026 03:27:06 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:391d0a4a7f2210a76562d45f9b8a72b749d3493384e2594e5d47c4649c51b562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **943.3 KB (943325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36133270ef7c6d804c39b533fd629a82efc6fcb842431934f6c6ceea3a9915d2`

```dockerfile
```

-	Layers:
	-	`sha256:5f45889a2a23271ed96f6449e51d557d7e9860daabd60659a82044c7e9f551b9`  
		Last Modified: Wed, 28 Jan 2026 03:27:03 GMT  
		Size: 913.2 KB (913207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2327d640b31f1db13e558b092ae53d65dd362980ace231384d913410b807ca09`  
		Last Modified: Wed, 28 Jan 2026 03:27:03 GMT  
		Size: 30.1 KB (30118 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7.12-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:73f3e9affdb305c04861bf10abfb2fa71e56e1bde5819ec1839a7c5eef6ddb7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78733892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c45ed053eaae26a5733f93e13d74cf1a800f771b22b2556958ef785f4b80bf7a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:07 GMT
ADD alpine-minirootfs-3.21.6-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:07 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:15:25 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:15:26 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:15:27 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 28 Jan 2026 03:15:27 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 28 Jan 2026 03:15:31 GMT
ENV INFLUXDB_VERSION=2.7.12
# Wed, 28 Jan 2026 03:15:31 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 28 Jan 2026 03:15:31 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 28 Jan 2026 03:15:33 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 28 Jan 2026 03:15:33 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 28 Jan 2026 03:15:33 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 28 Jan 2026 03:15:33 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 28 Jan 2026 03:15:33 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:15:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:15:33 GMT
CMD ["influxd"]
# Wed, 28 Jan 2026 03:15:33 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 Jan 2026 03:15:33 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 28 Jan 2026 03:15:33 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 28 Jan 2026 03:15:33 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 28 Jan 2026 03:15:33 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:a447a5de8f4eb4a987d81c0afa14d459cc714599c020c08f45fafa9c6c904b30`  
		Last Modified: Wed, 28 Jan 2026 01:18:13 GMT  
		Size: 4.0 MB (3992880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6ab2286a7a1f7b2a657fa5f9cd5794c5eaaecea283f7e8ed6df6e1726525eb`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca9a4aa64e00b6010beac8d9d65eee65d986a04c1e66e51c04fe91ed4293f8c`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 9.8 MB (9824203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbafc709ae0f6eccc66e9b498035cab2fb8cfbebf52a09baececda75ed40a9c2`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 5.8 MB (5790433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf13e4c27ec5340b32d6db93325cde6c1a76b1bfb444f82b0281a2afaebc423f`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b3d5de4828e332fd8e67bc21023a4790edaa370cd3b2b93b9b3b185243b251`  
		Last Modified: Wed, 28 Jan 2026 03:15:45 GMT  
		Size: 48.0 MB (48018004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bbf421b3460db3778b6ef941792140c1a2f05bd3ead30e5d52cd52f861e1422`  
		Last Modified: Wed, 28 Jan 2026 03:15:44 GMT  
		Size: 11.1 MB (11100419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728e7d19219b3f2895b7e6f75ee30c3eb1ca3198fc8b91d24484f0d7ae29a970`  
		Last Modified: Wed, 28 Jan 2026 03:15:44 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feabd2445240c8db64c9188502a45203d8bf4fa862e1facd65af80a0a4a05b90`  
		Last Modified: Wed, 28 Jan 2026 03:15:44 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4988bef482c19d2f614d4ec49ed4b57867cbbe8b263aad5779a7cd1a46621fe9`  
		Last Modified: Wed, 28 Jan 2026 03:15:45 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:f6aa3cd15a9f2092e624e447a80fcbaf5ec708f9439108d58b48beda56ed8d7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **942.7 KB (942722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f2c902e2eb2482e9375c138928510fd89d3c1d1c0a05eae47348822ef543f5`

```dockerfile
```

-	Layers:
	-	`sha256:43b1e61f4f7b667e09b16ac67562eb1e3873695e3a201da43cd36bf5e86399d6`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 912.4 KB (912434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cd7104ff5c58dfbd9314d1b3a2d32ee08e317ca67041a22e548bdff47207103`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 30.3 KB (30288 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.8`

```console
$ docker pull influxdb@sha256:96410d41a98c02fa5fcddc44cf708e297c8afcf02cd5bb6c620d4ae6a6d12390
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.8` - linux; amd64

```console
$ docker pull influxdb@sha256:68ed01481f413495fe1bba1ed283af3a1935d833676e0f5047aa24fb77906a92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107240605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d26ea8f3e6e87bd75cdf5cebdfbf8314a0498fa64c3d76e817023ca0ce9bf3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:58:14 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:58:14 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 07 Apr 2026 01:58:14 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 07 Apr 2026 01:58:16 GMT
ENV GOSU_VER=1.19
# Tue, 07 Apr 2026 01:58:16 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 07 Apr 2026 01:58:16 GMT
ENV INFLUXDB_VERSION=2.8.0
# Tue, 07 Apr 2026 01:58:16 GMT
ENV INFLUXDB_PR=-2
# Tue, 07 Apr 2026 01:58:16 GMT
ENV INFLUXDB_PV=2.8.0-2
# Tue, 07 Apr 2026 01:58:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 07 Apr 2026 01:58:18 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 07 Apr 2026 01:58:19 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 07 Apr 2026 01:58:19 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 07 Apr 2026 01:58:19 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 07 Apr 2026 01:58:19 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 07 Apr 2026 01:58:19 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:58:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 01:58:19 GMT
CMD ["influxd"]
# Tue, 07 Apr 2026 01:58:19 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 07 Apr 2026 01:58:19 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 07 Apr 2026 01:58:19 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 07 Apr 2026 01:58:19 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 07 Apr 2026 01:58:19 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a116bfcd84372702b219d6bae2ee7f1bdb1e6020d05189bc3c26e279e7ab2364`  
		Last Modified: Tue, 07 Apr 2026 01:58:31 GMT  
		Size: 9.8 MB (9798183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:474de9ab304f8664364821fd54a509679041419851afe35980fbd7c13a2c3d97`  
		Last Modified: Tue, 07 Apr 2026 01:58:31 GMT  
		Size: 6.2 MB (6156974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b83865bdaccd9bb5e11b4016b8576733196b451a7ccbd76483a142c59c43d9a`  
		Last Modified: Tue, 07 Apr 2026 01:58:31 GMT  
		Size: 3.2 KB (3232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8f0f8d0f417d9c4f8e42e10838b3c5356ffe44db60dbd713c090b865a36a8f`  
		Last Modified: Tue, 07 Apr 2026 01:58:31 GMT  
		Size: 811.5 KB (811482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb6e598a64d1bb4e5c2b149548399300221b418b182dd8be2b3dc236d88198b`  
		Last Modified: Tue, 07 Apr 2026 01:58:34 GMT  
		Size: 50.5 MB (50451807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeeb37736cabf4a78a0dbde353fe1882f8add4378e667aa82cd363e1e8a03075`  
		Last Modified: Tue, 07 Apr 2026 01:58:33 GMT  
		Size: 11.8 MB (11775867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4badd18ae9f94083936d589b872c729022b8ebd1e531bbfb4095b4c12794edaa`  
		Last Modified: Tue, 07 Apr 2026 01:58:33 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8568054b22810d03f8d0a1cca53fbf9dbc964499c9d672bb65efdf9fbdc3bc`  
		Last Modified: Tue, 07 Apr 2026 01:58:33 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe60089c21668a33bf2ca8e336cf38c667a4f9d13cd9a87462169d50423a93a`  
		Last Modified: Tue, 07 Apr 2026 01:58:34 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:9ad39b5f4622e6dd7b1921af3eef50210a48ca52dcdf489e17ccec5e88499ebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81fcded457e0dde721973237e4f4609db993674c5a1d6e1d50d47d10728485a3`

```dockerfile
```

-	Layers:
	-	`sha256:9d436efb5b4b564ec8f9e830616391ca4e4bf3aa27df1b3060eb7e944e247d3a`  
		Last Modified: Tue, 07 Apr 2026 01:58:31 GMT  
		Size: 2.9 MB (2934237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3eb7467cb3329a9d9c05e5832575b1eaa8f1ed181e6e49c6d4eab15a218e04f`  
		Last Modified: Tue, 07 Apr 2026 01:58:31 GMT  
		Size: 33.6 KB (33620 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:2311605af7772ef47b927d03db36c3fb215b3ce87982712b8d72a5525a18a82d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103639786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:202eb409813be9db84b84bba7249daa05613ed232209b3ee3565c150f8865387`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:01:47 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:01:48 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 07 Apr 2026 02:01:48 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 07 Apr 2026 02:01:49 GMT
ENV GOSU_VER=1.19
# Tue, 07 Apr 2026 02:01:49 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 07 Apr 2026 02:01:49 GMT
ENV INFLUXDB_VERSION=2.8.0
# Tue, 07 Apr 2026 02:01:49 GMT
ENV INFLUXDB_PR=-2
# Tue, 07 Apr 2026 02:01:49 GMT
ENV INFLUXDB_PV=2.8.0-2
# Tue, 07 Apr 2026 02:01:52 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 07 Apr 2026 02:01:52 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 07 Apr 2026 02:01:53 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 07 Apr 2026 02:01:53 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 07 Apr 2026 02:01:53 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 07 Apr 2026 02:01:53 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 07 Apr 2026 02:01:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 02:01:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 02:01:53 GMT
CMD ["influxd"]
# Tue, 07 Apr 2026 02:01:53 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 07 Apr 2026 02:01:53 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 07 Apr 2026 02:01:53 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 07 Apr 2026 02:01:53 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 07 Apr 2026 02:01:53 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00120dc253bd72ad4cf1854724026a81aaf4970b1b00f051ae589a8ecb399dc`  
		Last Modified: Tue, 07 Apr 2026 02:02:04 GMT  
		Size: 9.6 MB (9626917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c98a25d698b6f70d76994e2a0c41ebc991071438847d492e353d6db4eed8965`  
		Last Modified: Tue, 07 Apr 2026 02:02:04 GMT  
		Size: 5.8 MB (5790427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd92e0afeff73eda856e070de3a3920326d1d3d47ebd9a96e265d21ee7d7fad`  
		Last Modified: Tue, 07 Apr 2026 02:02:04 GMT  
		Size: 3.2 KB (3231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85d5b89607330aaceaf098690c579352497d8af3213a534e4ab8e4e0cc055f3`  
		Last Modified: Tue, 07 Apr 2026 02:02:04 GMT  
		Size: 766.4 KB (766371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24f1e34c12a55ea2e93376696df4031d1e98d9471c477cebb06f2e344ccd9fd`  
		Last Modified: Tue, 07 Apr 2026 02:02:07 GMT  
		Size: 48.2 MB (48229552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f058781f0fcd0beafff67981c71ad42c14fb858d6878c0a9e13dc27cc9738b26`  
		Last Modified: Tue, 07 Apr 2026 02:02:06 GMT  
		Size: 11.1 MB (11100394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7aaae010a587cf5a601d46a07d45b378f37c219e996cf7da04e3451ce40f09`  
		Last Modified: Tue, 07 Apr 2026 02:02:06 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f3da28a5bb0e301c7a7a0f4878ec11e653083ea8a0485b114f2c4661c6e5e3`  
		Last Modified: Tue, 07 Apr 2026 02:02:06 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52e0436c606da832d52ceec71b1cf5d5ff170863a1cb76baac382d62f44cfee`  
		Last Modified: Tue, 07 Apr 2026 02:02:07 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:dd3c5e7b9b9671abe2a59b0efea0f7c021b79ea63ba3dbc48760c622647406d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cc341b69e5b33632b785cffba7cbde4509e4ef6926df182df78220fa500ed06`

```dockerfile
```

-	Layers:
	-	`sha256:570e1645673b88b50800b3b86275be91a90a2b107aa8c21d1cb94112ea3f7419`  
		Last Modified: Tue, 07 Apr 2026 02:02:04 GMT  
		Size: 2.9 MB (2933717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb943467e2459ff3405858d9c0df13744923b5ad93d4dddad5d6de90e6559d5f`  
		Last Modified: Tue, 07 Apr 2026 02:02:04 GMT  
		Size: 33.8 KB (33815 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.8-alpine`

```console
$ docker pull influxdb@sha256:f15dfc604753f53b180364a331b46c2f4bc5c08a665d025982b301efa69bc2f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.8-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:e224ef04c67e6587c0b6f9f0d5e125f291bdc080b17e6d498b0fa10f60c9eccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81900321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b6866841a1a833e0595336141bd26bc5088eafcd30cd7576f2382ddbfd53eea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:26:53 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:26:55 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:26:55 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 28 Jan 2026 03:26:55 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 28 Jan 2026 03:26:59 GMT
ENV INFLUXDB_VERSION=2.8.0
# Wed, 28 Jan 2026 03:26:59 GMT
ENV INFLUXDB_PR=-2
# Wed, 28 Jan 2026 03:26:59 GMT
ENV INFLUXDB_PV=2.8.0-2
# Wed, 28 Jan 2026 03:26:59 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 28 Jan 2026 03:26:59 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 28 Jan 2026 03:27:00 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 28 Jan 2026 03:27:00 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 28 Jan 2026 03:27:00 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 28 Jan 2026 03:27:00 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 28 Jan 2026 03:27:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:27:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:27:00 GMT
CMD ["influxd"]
# Wed, 28 Jan 2026 03:27:00 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 Jan 2026 03:27:00 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 28 Jan 2026 03:27:00 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 28 Jan 2026 03:27:00 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 28 Jan 2026 03:27:00 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da2f69740401b1208019e15e303957ef5e65950b9f1a7b4939e5fc136f96a3f`  
		Last Modified: Wed, 28 Jan 2026 03:27:10 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a44134f5fc0c6cdf52aa1278b3f3f6eee8a5c2a452dd4aff61503e192f645e`  
		Last Modified: Wed, 28 Jan 2026 03:27:10 GMT  
		Size: 9.9 MB (9863904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005d64a40f5cb225c3bc69263c0469aa02ab005ed8b21e6e7a89b3675ec50b07`  
		Last Modified: Wed, 28 Jan 2026 03:27:10 GMT  
		Size: 6.2 MB (6156984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201d3a17f0762d441938d9cd05ad8c611220953a6d8de6a93072a25f16c4692b`  
		Last Modified: Wed, 28 Jan 2026 03:27:10 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15a968cb865edd4609ac8b32d717b03922a73cb3f7590c30780bad10277e537`  
		Last Modified: Wed, 28 Jan 2026 03:27:12 GMT  
		Size: 50.5 MB (50451881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75205be004b2b555f72327c5eb07d199aae883c0df672642e69dfcdc4dab8cf`  
		Last Modified: Wed, 28 Jan 2026 03:27:12 GMT  
		Size: 11.8 MB (11775858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f48dd36db7dbb28ea6f0a2d7958ef354180d24d56cf270dc22a547a09111687`  
		Last Modified: Wed, 28 Jan 2026 03:27:12 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc78f60a45d07493bbb7618a6d38e70f86076b21dc6487f08ed2684b1ee56b8`  
		Last Modified: Wed, 28 Jan 2026 03:27:12 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b85aa016614d9f14630b36f109832ec79194ab3adcd5994b8868dec4259eef`  
		Last Modified: Wed, 28 Jan 2026 03:27:06 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:47754c46831f8311db55db258098d6bd94c0b23caf15316fd1bb193490033dff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **946.7 KB (946732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a8f0be80fc287fb05cf358d3814bac779c2ad698308821166b0c53f73f17340`

```dockerfile
```

-	Layers:
	-	`sha256:aa884cdf050c202632293939e889ccbda051a7d2d9e8139c8fb38b9f0383362f`  
		Last Modified: Wed, 28 Jan 2026 03:27:10 GMT  
		Size: 915.9 KB (915886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80b43ac4284db4608a9e3f907899268737ae652fd8183dab50b925feb71dbeb7`  
		Last Modified: Wed, 28 Jan 2026 03:27:10 GMT  
		Size: 30.8 KB (30846 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.8-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ff96fbac0d6cf44eb703e9cd7e5f2a09bfd2f78e814185c58f2a34d9fecd5cf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78945372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2200d46793614389922d59d788c241bf4d159c9f22de8fb362b4321d920953e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:07 GMT
ADD alpine-minirootfs-3.21.6-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:07 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:15:25 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:15:26 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:15:27 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 28 Jan 2026 03:15:27 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 28 Jan 2026 03:15:31 GMT
ENV INFLUXDB_VERSION=2.8.0
# Wed, 28 Jan 2026 03:15:31 GMT
ENV INFLUXDB_PR=-2
# Wed, 28 Jan 2026 03:15:31 GMT
ENV INFLUXDB_PV=2.8.0-2
# Wed, 28 Jan 2026 03:15:31 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 28 Jan 2026 03:15:31 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 28 Jan 2026 03:15:33 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 28 Jan 2026 03:15:33 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 28 Jan 2026 03:15:33 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 28 Jan 2026 03:15:33 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 28 Jan 2026 03:15:33 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:15:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:15:33 GMT
CMD ["influxd"]
# Wed, 28 Jan 2026 03:15:33 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 Jan 2026 03:15:33 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 28 Jan 2026 03:15:33 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 28 Jan 2026 03:15:33 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 28 Jan 2026 03:15:33 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:a447a5de8f4eb4a987d81c0afa14d459cc714599c020c08f45fafa9c6c904b30`  
		Last Modified: Wed, 28 Jan 2026 01:18:13 GMT  
		Size: 4.0 MB (3992880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6ab2286a7a1f7b2a657fa5f9cd5794c5eaaecea283f7e8ed6df6e1726525eb`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6584e15e052556418670992187d03a8d302b4b08e86a35c3c202d8b763a116`  
		Last Modified: Wed, 28 Jan 2026 03:15:44 GMT  
		Size: 9.8 MB (9824174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b868f1d2c50be9be813066470ac1cbfefc67a3ade4ac5caf84ad8f9f92c7b3c0`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 5.8 MB (5790429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf13e4c27ec5340b32d6db93325cde6c1a76b1bfb444f82b0281a2afaebc423f`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e19b47fb98adca37cda31bb666000a1068add6e40bc68415d079e0810ba271`  
		Last Modified: Wed, 28 Jan 2026 03:15:46 GMT  
		Size: 48.2 MB (48229537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef6ef542d7aecf40c7fa27129ae016a248041943f6f2cf02e5fbdbf2ec3481a`  
		Last Modified: Wed, 28 Jan 2026 03:15:45 GMT  
		Size: 11.1 MB (11100399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728e7d19219b3f2895b7e6f75ee30c3eb1ca3198fc8b91d24484f0d7ae29a970`  
		Last Modified: Wed, 28 Jan 2026 03:15:44 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feabd2445240c8db64c9188502a45203d8bf4fa862e1facd65af80a0a4a05b90`  
		Last Modified: Wed, 28 Jan 2026 03:15:44 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4988bef482c19d2f614d4ec49ed4b57867cbbe8b263aad5779a7cd1a46621fe9`  
		Last Modified: Wed, 28 Jan 2026 03:15:45 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:73ce168dd0f62068e66e3be9e245c1622a2cedfa2c9f879b63d105a81e2f4fa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **946.2 KB (946177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b1de55895028e279fbba3d674a6062cd263237cc82dedc0669e211c20457f0a`

```dockerfile
```

-	Layers:
	-	`sha256:70ed507d37e4c0a2fb8cca40b6a791937d6585d05bfba4bcc080d71d0ca360f7`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 915.1 KB (915137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26164e792c84253eddb0c7007db1811569868d2bf2dd4d2a7056ec4ae310fca0`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 31.0 KB (31040 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.8.0`

```console
$ docker pull influxdb@sha256:96410d41a98c02fa5fcddc44cf708e297c8afcf02cd5bb6c620d4ae6a6d12390
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.8.0` - linux; amd64

```console
$ docker pull influxdb@sha256:68ed01481f413495fe1bba1ed283af3a1935d833676e0f5047aa24fb77906a92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107240605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d26ea8f3e6e87bd75cdf5cebdfbf8314a0498fa64c3d76e817023ca0ce9bf3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:58:14 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:58:14 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 07 Apr 2026 01:58:14 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 07 Apr 2026 01:58:16 GMT
ENV GOSU_VER=1.19
# Tue, 07 Apr 2026 01:58:16 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 07 Apr 2026 01:58:16 GMT
ENV INFLUXDB_VERSION=2.8.0
# Tue, 07 Apr 2026 01:58:16 GMT
ENV INFLUXDB_PR=-2
# Tue, 07 Apr 2026 01:58:16 GMT
ENV INFLUXDB_PV=2.8.0-2
# Tue, 07 Apr 2026 01:58:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 07 Apr 2026 01:58:18 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 07 Apr 2026 01:58:19 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 07 Apr 2026 01:58:19 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 07 Apr 2026 01:58:19 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 07 Apr 2026 01:58:19 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 07 Apr 2026 01:58:19 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:58:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 01:58:19 GMT
CMD ["influxd"]
# Tue, 07 Apr 2026 01:58:19 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 07 Apr 2026 01:58:19 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 07 Apr 2026 01:58:19 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 07 Apr 2026 01:58:19 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 07 Apr 2026 01:58:19 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a116bfcd84372702b219d6bae2ee7f1bdb1e6020d05189bc3c26e279e7ab2364`  
		Last Modified: Tue, 07 Apr 2026 01:58:31 GMT  
		Size: 9.8 MB (9798183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:474de9ab304f8664364821fd54a509679041419851afe35980fbd7c13a2c3d97`  
		Last Modified: Tue, 07 Apr 2026 01:58:31 GMT  
		Size: 6.2 MB (6156974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b83865bdaccd9bb5e11b4016b8576733196b451a7ccbd76483a142c59c43d9a`  
		Last Modified: Tue, 07 Apr 2026 01:58:31 GMT  
		Size: 3.2 KB (3232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8f0f8d0f417d9c4f8e42e10838b3c5356ffe44db60dbd713c090b865a36a8f`  
		Last Modified: Tue, 07 Apr 2026 01:58:31 GMT  
		Size: 811.5 KB (811482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb6e598a64d1bb4e5c2b149548399300221b418b182dd8be2b3dc236d88198b`  
		Last Modified: Tue, 07 Apr 2026 01:58:34 GMT  
		Size: 50.5 MB (50451807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeeb37736cabf4a78a0dbde353fe1882f8add4378e667aa82cd363e1e8a03075`  
		Last Modified: Tue, 07 Apr 2026 01:58:33 GMT  
		Size: 11.8 MB (11775867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4badd18ae9f94083936d589b872c729022b8ebd1e531bbfb4095b4c12794edaa`  
		Last Modified: Tue, 07 Apr 2026 01:58:33 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8568054b22810d03f8d0a1cca53fbf9dbc964499c9d672bb65efdf9fbdc3bc`  
		Last Modified: Tue, 07 Apr 2026 01:58:33 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe60089c21668a33bf2ca8e336cf38c667a4f9d13cd9a87462169d50423a93a`  
		Last Modified: Tue, 07 Apr 2026 01:58:34 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8.0` - unknown; unknown

```console
$ docker pull influxdb@sha256:9ad39b5f4622e6dd7b1921af3eef50210a48ca52dcdf489e17ccec5e88499ebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81fcded457e0dde721973237e4f4609db993674c5a1d6e1d50d47d10728485a3`

```dockerfile
```

-	Layers:
	-	`sha256:9d436efb5b4b564ec8f9e830616391ca4e4bf3aa27df1b3060eb7e944e247d3a`  
		Last Modified: Tue, 07 Apr 2026 01:58:31 GMT  
		Size: 2.9 MB (2934237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3eb7467cb3329a9d9c05e5832575b1eaa8f1ed181e6e49c6d4eab15a218e04f`  
		Last Modified: Tue, 07 Apr 2026 01:58:31 GMT  
		Size: 33.6 KB (33620 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.8.0` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:2311605af7772ef47b927d03db36c3fb215b3ce87982712b8d72a5525a18a82d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103639786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:202eb409813be9db84b84bba7249daa05613ed232209b3ee3565c150f8865387`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:01:47 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:01:48 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 07 Apr 2026 02:01:48 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 07 Apr 2026 02:01:49 GMT
ENV GOSU_VER=1.19
# Tue, 07 Apr 2026 02:01:49 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 07 Apr 2026 02:01:49 GMT
ENV INFLUXDB_VERSION=2.8.0
# Tue, 07 Apr 2026 02:01:49 GMT
ENV INFLUXDB_PR=-2
# Tue, 07 Apr 2026 02:01:49 GMT
ENV INFLUXDB_PV=2.8.0-2
# Tue, 07 Apr 2026 02:01:52 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 07 Apr 2026 02:01:52 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 07 Apr 2026 02:01:53 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 07 Apr 2026 02:01:53 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 07 Apr 2026 02:01:53 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 07 Apr 2026 02:01:53 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 07 Apr 2026 02:01:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 02:01:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 02:01:53 GMT
CMD ["influxd"]
# Tue, 07 Apr 2026 02:01:53 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 07 Apr 2026 02:01:53 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 07 Apr 2026 02:01:53 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 07 Apr 2026 02:01:53 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 07 Apr 2026 02:01:53 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00120dc253bd72ad4cf1854724026a81aaf4970b1b00f051ae589a8ecb399dc`  
		Last Modified: Tue, 07 Apr 2026 02:02:04 GMT  
		Size: 9.6 MB (9626917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c98a25d698b6f70d76994e2a0c41ebc991071438847d492e353d6db4eed8965`  
		Last Modified: Tue, 07 Apr 2026 02:02:04 GMT  
		Size: 5.8 MB (5790427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd92e0afeff73eda856e070de3a3920326d1d3d47ebd9a96e265d21ee7d7fad`  
		Last Modified: Tue, 07 Apr 2026 02:02:04 GMT  
		Size: 3.2 KB (3231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85d5b89607330aaceaf098690c579352497d8af3213a534e4ab8e4e0cc055f3`  
		Last Modified: Tue, 07 Apr 2026 02:02:04 GMT  
		Size: 766.4 KB (766371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24f1e34c12a55ea2e93376696df4031d1e98d9471c477cebb06f2e344ccd9fd`  
		Last Modified: Tue, 07 Apr 2026 02:02:07 GMT  
		Size: 48.2 MB (48229552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f058781f0fcd0beafff67981c71ad42c14fb858d6878c0a9e13dc27cc9738b26`  
		Last Modified: Tue, 07 Apr 2026 02:02:06 GMT  
		Size: 11.1 MB (11100394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7aaae010a587cf5a601d46a07d45b378f37c219e996cf7da04e3451ce40f09`  
		Last Modified: Tue, 07 Apr 2026 02:02:06 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f3da28a5bb0e301c7a7a0f4878ec11e653083ea8a0485b114f2c4661c6e5e3`  
		Last Modified: Tue, 07 Apr 2026 02:02:06 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52e0436c606da832d52ceec71b1cf5d5ff170863a1cb76baac382d62f44cfee`  
		Last Modified: Tue, 07 Apr 2026 02:02:07 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8.0` - unknown; unknown

```console
$ docker pull influxdb@sha256:dd3c5e7b9b9671abe2a59b0efea0f7c021b79ea63ba3dbc48760c622647406d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cc341b69e5b33632b785cffba7cbde4509e4ef6926df182df78220fa500ed06`

```dockerfile
```

-	Layers:
	-	`sha256:570e1645673b88b50800b3b86275be91a90a2b107aa8c21d1cb94112ea3f7419`  
		Last Modified: Tue, 07 Apr 2026 02:02:04 GMT  
		Size: 2.9 MB (2933717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb943467e2459ff3405858d9c0df13744923b5ad93d4dddad5d6de90e6559d5f`  
		Last Modified: Tue, 07 Apr 2026 02:02:04 GMT  
		Size: 33.8 KB (33815 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2.8.0-alpine`

```console
$ docker pull influxdb@sha256:f15dfc604753f53b180364a331b46c2f4bc5c08a665d025982b301efa69bc2f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.8.0-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:e224ef04c67e6587c0b6f9f0d5e125f291bdc080b17e6d498b0fa10f60c9eccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81900321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b6866841a1a833e0595336141bd26bc5088eafcd30cd7576f2382ddbfd53eea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:26:53 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:26:55 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:26:55 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 28 Jan 2026 03:26:55 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 28 Jan 2026 03:26:59 GMT
ENV INFLUXDB_VERSION=2.8.0
# Wed, 28 Jan 2026 03:26:59 GMT
ENV INFLUXDB_PR=-2
# Wed, 28 Jan 2026 03:26:59 GMT
ENV INFLUXDB_PV=2.8.0-2
# Wed, 28 Jan 2026 03:26:59 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 28 Jan 2026 03:26:59 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 28 Jan 2026 03:27:00 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 28 Jan 2026 03:27:00 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 28 Jan 2026 03:27:00 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 28 Jan 2026 03:27:00 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 28 Jan 2026 03:27:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:27:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:27:00 GMT
CMD ["influxd"]
# Wed, 28 Jan 2026 03:27:00 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 Jan 2026 03:27:00 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 28 Jan 2026 03:27:00 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 28 Jan 2026 03:27:00 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 28 Jan 2026 03:27:00 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da2f69740401b1208019e15e303957ef5e65950b9f1a7b4939e5fc136f96a3f`  
		Last Modified: Wed, 28 Jan 2026 03:27:10 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a44134f5fc0c6cdf52aa1278b3f3f6eee8a5c2a452dd4aff61503e192f645e`  
		Last Modified: Wed, 28 Jan 2026 03:27:10 GMT  
		Size: 9.9 MB (9863904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005d64a40f5cb225c3bc69263c0469aa02ab005ed8b21e6e7a89b3675ec50b07`  
		Last Modified: Wed, 28 Jan 2026 03:27:10 GMT  
		Size: 6.2 MB (6156984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201d3a17f0762d441938d9cd05ad8c611220953a6d8de6a93072a25f16c4692b`  
		Last Modified: Wed, 28 Jan 2026 03:27:10 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15a968cb865edd4609ac8b32d717b03922a73cb3f7590c30780bad10277e537`  
		Last Modified: Wed, 28 Jan 2026 03:27:12 GMT  
		Size: 50.5 MB (50451881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75205be004b2b555f72327c5eb07d199aae883c0df672642e69dfcdc4dab8cf`  
		Last Modified: Wed, 28 Jan 2026 03:27:12 GMT  
		Size: 11.8 MB (11775858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f48dd36db7dbb28ea6f0a2d7958ef354180d24d56cf270dc22a547a09111687`  
		Last Modified: Wed, 28 Jan 2026 03:27:12 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc78f60a45d07493bbb7618a6d38e70f86076b21dc6487f08ed2684b1ee56b8`  
		Last Modified: Wed, 28 Jan 2026 03:27:12 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b85aa016614d9f14630b36f109832ec79194ab3adcd5994b8868dec4259eef`  
		Last Modified: Wed, 28 Jan 2026 03:27:06 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8.0-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:47754c46831f8311db55db258098d6bd94c0b23caf15316fd1bb193490033dff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **946.7 KB (946732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a8f0be80fc287fb05cf358d3814bac779c2ad698308821166b0c53f73f17340`

```dockerfile
```

-	Layers:
	-	`sha256:aa884cdf050c202632293939e889ccbda051a7d2d9e8139c8fb38b9f0383362f`  
		Last Modified: Wed, 28 Jan 2026 03:27:10 GMT  
		Size: 915.9 KB (915886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80b43ac4284db4608a9e3f907899268737ae652fd8183dab50b925feb71dbeb7`  
		Last Modified: Wed, 28 Jan 2026 03:27:10 GMT  
		Size: 30.8 KB (30846 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.8.0-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ff96fbac0d6cf44eb703e9cd7e5f2a09bfd2f78e814185c58f2a34d9fecd5cf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78945372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2200d46793614389922d59d788c241bf4d159c9f22de8fb362b4321d920953e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:07 GMT
ADD alpine-minirootfs-3.21.6-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:07 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:15:25 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:15:26 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:15:27 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 28 Jan 2026 03:15:27 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 28 Jan 2026 03:15:31 GMT
ENV INFLUXDB_VERSION=2.8.0
# Wed, 28 Jan 2026 03:15:31 GMT
ENV INFLUXDB_PR=-2
# Wed, 28 Jan 2026 03:15:31 GMT
ENV INFLUXDB_PV=2.8.0-2
# Wed, 28 Jan 2026 03:15:31 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 28 Jan 2026 03:15:31 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 28 Jan 2026 03:15:33 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 28 Jan 2026 03:15:33 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 28 Jan 2026 03:15:33 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 28 Jan 2026 03:15:33 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 28 Jan 2026 03:15:33 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:15:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:15:33 GMT
CMD ["influxd"]
# Wed, 28 Jan 2026 03:15:33 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 Jan 2026 03:15:33 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 28 Jan 2026 03:15:33 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 28 Jan 2026 03:15:33 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 28 Jan 2026 03:15:33 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:a447a5de8f4eb4a987d81c0afa14d459cc714599c020c08f45fafa9c6c904b30`  
		Last Modified: Wed, 28 Jan 2026 01:18:13 GMT  
		Size: 4.0 MB (3992880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6ab2286a7a1f7b2a657fa5f9cd5794c5eaaecea283f7e8ed6df6e1726525eb`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6584e15e052556418670992187d03a8d302b4b08e86a35c3c202d8b763a116`  
		Last Modified: Wed, 28 Jan 2026 03:15:44 GMT  
		Size: 9.8 MB (9824174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b868f1d2c50be9be813066470ac1cbfefc67a3ade4ac5caf84ad8f9f92c7b3c0`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 5.8 MB (5790429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf13e4c27ec5340b32d6db93325cde6c1a76b1bfb444f82b0281a2afaebc423f`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e19b47fb98adca37cda31bb666000a1068add6e40bc68415d079e0810ba271`  
		Last Modified: Wed, 28 Jan 2026 03:15:46 GMT  
		Size: 48.2 MB (48229537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef6ef542d7aecf40c7fa27129ae016a248041943f6f2cf02e5fbdbf2ec3481a`  
		Last Modified: Wed, 28 Jan 2026 03:15:45 GMT  
		Size: 11.1 MB (11100399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728e7d19219b3f2895b7e6f75ee30c3eb1ca3198fc8b91d24484f0d7ae29a970`  
		Last Modified: Wed, 28 Jan 2026 03:15:44 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feabd2445240c8db64c9188502a45203d8bf4fa862e1facd65af80a0a4a05b90`  
		Last Modified: Wed, 28 Jan 2026 03:15:44 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4988bef482c19d2f614d4ec49ed4b57867cbbe8b263aad5779a7cd1a46621fe9`  
		Last Modified: Wed, 28 Jan 2026 03:15:45 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8.0-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:73ce168dd0f62068e66e3be9e245c1622a2cedfa2c9f879b63d105a81e2f4fa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **946.2 KB (946177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b1de55895028e279fbba3d674a6062cd263237cc82dedc0669e211c20457f0a`

```dockerfile
```

-	Layers:
	-	`sha256:70ed507d37e4c0a2fb8cca40b6a791937d6585d05bfba4bcc080d71d0ca360f7`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 915.1 KB (915137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26164e792c84253eddb0c7007db1811569868d2bf2dd4d2a7056ec4ae310fca0`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 31.0 KB (31040 bytes)  
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
$ docker pull influxdb@sha256:f15dfc604753f53b180364a331b46c2f4bc5c08a665d025982b301efa69bc2f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:e224ef04c67e6587c0b6f9f0d5e125f291bdc080b17e6d498b0fa10f60c9eccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81900321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b6866841a1a833e0595336141bd26bc5088eafcd30cd7576f2382ddbfd53eea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:26:53 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:26:55 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:26:55 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 28 Jan 2026 03:26:55 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 28 Jan 2026 03:26:59 GMT
ENV INFLUXDB_VERSION=2.8.0
# Wed, 28 Jan 2026 03:26:59 GMT
ENV INFLUXDB_PR=-2
# Wed, 28 Jan 2026 03:26:59 GMT
ENV INFLUXDB_PV=2.8.0-2
# Wed, 28 Jan 2026 03:26:59 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 28 Jan 2026 03:26:59 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 28 Jan 2026 03:27:00 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 28 Jan 2026 03:27:00 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 28 Jan 2026 03:27:00 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 28 Jan 2026 03:27:00 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 28 Jan 2026 03:27:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:27:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:27:00 GMT
CMD ["influxd"]
# Wed, 28 Jan 2026 03:27:00 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 Jan 2026 03:27:00 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 28 Jan 2026 03:27:00 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 28 Jan 2026 03:27:00 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 28 Jan 2026 03:27:00 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da2f69740401b1208019e15e303957ef5e65950b9f1a7b4939e5fc136f96a3f`  
		Last Modified: Wed, 28 Jan 2026 03:27:10 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a44134f5fc0c6cdf52aa1278b3f3f6eee8a5c2a452dd4aff61503e192f645e`  
		Last Modified: Wed, 28 Jan 2026 03:27:10 GMT  
		Size: 9.9 MB (9863904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005d64a40f5cb225c3bc69263c0469aa02ab005ed8b21e6e7a89b3675ec50b07`  
		Last Modified: Wed, 28 Jan 2026 03:27:10 GMT  
		Size: 6.2 MB (6156984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201d3a17f0762d441938d9cd05ad8c611220953a6d8de6a93072a25f16c4692b`  
		Last Modified: Wed, 28 Jan 2026 03:27:10 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15a968cb865edd4609ac8b32d717b03922a73cb3f7590c30780bad10277e537`  
		Last Modified: Wed, 28 Jan 2026 03:27:12 GMT  
		Size: 50.5 MB (50451881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75205be004b2b555f72327c5eb07d199aae883c0df672642e69dfcdc4dab8cf`  
		Last Modified: Wed, 28 Jan 2026 03:27:12 GMT  
		Size: 11.8 MB (11775858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f48dd36db7dbb28ea6f0a2d7958ef354180d24d56cf270dc22a547a09111687`  
		Last Modified: Wed, 28 Jan 2026 03:27:12 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc78f60a45d07493bbb7618a6d38e70f86076b21dc6487f08ed2684b1ee56b8`  
		Last Modified: Wed, 28 Jan 2026 03:27:12 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b85aa016614d9f14630b36f109832ec79194ab3adcd5994b8868dec4259eef`  
		Last Modified: Wed, 28 Jan 2026 03:27:06 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:47754c46831f8311db55db258098d6bd94c0b23caf15316fd1bb193490033dff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **946.7 KB (946732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a8f0be80fc287fb05cf358d3814bac779c2ad698308821166b0c53f73f17340`

```dockerfile
```

-	Layers:
	-	`sha256:aa884cdf050c202632293939e889ccbda051a7d2d9e8139c8fb38b9f0383362f`  
		Last Modified: Wed, 28 Jan 2026 03:27:10 GMT  
		Size: 915.9 KB (915886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80b43ac4284db4608a9e3f907899268737ae652fd8183dab50b925feb71dbeb7`  
		Last Modified: Wed, 28 Jan 2026 03:27:10 GMT  
		Size: 30.8 KB (30846 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ff96fbac0d6cf44eb703e9cd7e5f2a09bfd2f78e814185c58f2a34d9fecd5cf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78945372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2200d46793614389922d59d788c241bf4d159c9f22de8fb362b4321d920953e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:07 GMT
ADD alpine-minirootfs-3.21.6-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:07 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:15:25 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:15:26 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:15:27 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Wed, 28 Jan 2026 03:15:27 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Wed, 28 Jan 2026 03:15:31 GMT
ENV INFLUXDB_VERSION=2.8.0
# Wed, 28 Jan 2026 03:15:31 GMT
ENV INFLUXDB_PR=-2
# Wed, 28 Jan 2026 03:15:31 GMT
ENV INFLUXDB_PV=2.8.0-2
# Wed, 28 Jan 2026 03:15:31 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Wed, 28 Jan 2026 03:15:31 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Wed, 28 Jan 2026 03:15:33 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Wed, 28 Jan 2026 03:15:33 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Wed, 28 Jan 2026 03:15:33 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Wed, 28 Jan 2026 03:15:33 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Wed, 28 Jan 2026 03:15:33 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:15:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:15:33 GMT
CMD ["influxd"]
# Wed, 28 Jan 2026 03:15:33 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 Jan 2026 03:15:33 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Wed, 28 Jan 2026 03:15:33 GMT
ENV INFLUXD_INIT_PORT=9999
# Wed, 28 Jan 2026 03:15:33 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Wed, 28 Jan 2026 03:15:33 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:a447a5de8f4eb4a987d81c0afa14d459cc714599c020c08f45fafa9c6c904b30`  
		Last Modified: Wed, 28 Jan 2026 01:18:13 GMT  
		Size: 4.0 MB (3992880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6ab2286a7a1f7b2a657fa5f9cd5794c5eaaecea283f7e8ed6df6e1726525eb`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6584e15e052556418670992187d03a8d302b4b08e86a35c3c202d8b763a116`  
		Last Modified: Wed, 28 Jan 2026 03:15:44 GMT  
		Size: 9.8 MB (9824174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b868f1d2c50be9be813066470ac1cbfefc67a3ade4ac5caf84ad8f9f92c7b3c0`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 5.8 MB (5790429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf13e4c27ec5340b32d6db93325cde6c1a76b1bfb444f82b0281a2afaebc423f`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e19b47fb98adca37cda31bb666000a1068add6e40bc68415d079e0810ba271`  
		Last Modified: Wed, 28 Jan 2026 03:15:46 GMT  
		Size: 48.2 MB (48229537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef6ef542d7aecf40c7fa27129ae016a248041943f6f2cf02e5fbdbf2ec3481a`  
		Last Modified: Wed, 28 Jan 2026 03:15:45 GMT  
		Size: 11.1 MB (11100399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728e7d19219b3f2895b7e6f75ee30c3eb1ca3198fc8b91d24484f0d7ae29a970`  
		Last Modified: Wed, 28 Jan 2026 03:15:44 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feabd2445240c8db64c9188502a45203d8bf4fa862e1facd65af80a0a4a05b90`  
		Last Modified: Wed, 28 Jan 2026 03:15:44 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4988bef482c19d2f614d4ec49ed4b57867cbbe8b263aad5779a7cd1a46621fe9`  
		Last Modified: Wed, 28 Jan 2026 03:15:45 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:73ce168dd0f62068e66e3be9e245c1622a2cedfa2c9f879b63d105a81e2f4fa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **946.2 KB (946177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b1de55895028e279fbba3d674a6062cd263237cc82dedc0669e211c20457f0a`

```dockerfile
```

-	Layers:
	-	`sha256:70ed507d37e4c0a2fb8cca40b6a791937d6585d05bfba4bcc080d71d0ca360f7`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 915.1 KB (915137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26164e792c84253eddb0c7007db1811569868d2bf2dd4d2a7056ec4ae310fca0`  
		Last Modified: Wed, 28 Jan 2026 03:15:43 GMT  
		Size: 31.0 KB (31040 bytes)  
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
$ docker pull influxdb@sha256:5b6490fb8c705497ee0e6f583dee7917d7dd852d1bdf5f1f18727b624771bc45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:fe193b88d165027d157676c49a50c373727427dd781423044c379b9357900490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47995269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1400d4cce180749da87d26bc2280d46b2b35a19829e902f86b8e549d201c9114`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Mon, 13 Apr 2026 22:50:03 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Mon, 13 Apr 2026 22:50:09 GMT
ENV INFLUXDB_VERSION=1.12.4-c1.12.4
# Mon, 13 Apr 2026 22:50:09 GMT
ENV INFLUXDB_PR=
# Mon, 13 Apr 2026 22:50:09 GMT
ENV INFLUXDB_PV=1.12.4-c1.12.4
# Mon, 13 Apr 2026 22:50:09 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"         "influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     tar -xvf "influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz"         -C /usr/bin --strip-components 1 --wildcards             'influxdb-*/influx'             'influxdb-*/influx_inspect'             'influxdb-*/influxd' &&     rm "influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"        "influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     apk del .build-deps # buildkit
# Mon, 13 Apr 2026 22:50:09 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Mon, 13 Apr 2026 22:50:09 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 13 Apr 2026 22:50:09 GMT
VOLUME [/var/lib/influxdb]
# Mon, 13 Apr 2026 22:50:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 13 Apr 2026 22:50:09 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Mon, 13 Apr 2026 22:50:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 13 Apr 2026 22:50:09 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1afc286d5bbdcb39f8904b0877ed84b34af0919b60bce9f69f0ab35ec5154772`  
		Last Modified: Mon, 13 Apr 2026 22:50:19 GMT  
		Size: 1.2 MB (1225270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc54203a742edc2fd769d3f38e557a9917ab1f043d1233ce97b8608e761ba4ab`  
		Last Modified: Mon, 13 Apr 2026 22:50:22 GMT  
		Size: 43.1 MB (43124483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5245460d9ba02acba430a33f494e80717d0362863c758ed339e69e58a939b0`  
		Last Modified: Mon, 13 Apr 2026 22:50:19 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182feea32d5f2c7e97b3a1a34fddb9941f3533f2fadd5a0f119c5e7be39d00f9`  
		Last Modified: Mon, 13 Apr 2026 22:50:19 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4789a2ccda4a0bbd39eaad69aa88ebb2099cd6eaca3ef2874630e0ac768aa819`  
		Last Modified: Mon, 13 Apr 2026 22:50:20 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:9d164657b0efe2ae196ced0eda911b7a1fcbc779fb8bbc65f2d6351d97fefb0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **796.7 KB (796748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbfcc232ecf429847315cca44df9cad68816e1741d0715fd745035e1c6965d3b`

```dockerfile
```

-	Layers:
	-	`sha256:77d162daee65dc57dff3ff43aeda16b21d1567502c1f4fad2780b80bdb6a6b00`  
		Last Modified: Mon, 13 Apr 2026 22:50:19 GMT  
		Size: 781.2 KB (781219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5ffb7540edde9c28eb60306b5d916f01c6bac56019896348af85ef93f45d46c`  
		Last Modified: Mon, 13 Apr 2026 22:50:19 GMT  
		Size: 15.5 KB (15529 bytes)  
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
$ docker pull influxdb@sha256:96410d41a98c02fa5fcddc44cf708e297c8afcf02cd5bb6c620d4ae6a6d12390
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:68ed01481f413495fe1bba1ed283af3a1935d833676e0f5047aa24fb77906a92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107240605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d26ea8f3e6e87bd75cdf5cebdfbf8314a0498fa64c3d76e817023ca0ce9bf3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:58:14 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:58:14 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 07 Apr 2026 01:58:14 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 07 Apr 2026 01:58:16 GMT
ENV GOSU_VER=1.19
# Tue, 07 Apr 2026 01:58:16 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 07 Apr 2026 01:58:16 GMT
ENV INFLUXDB_VERSION=2.8.0
# Tue, 07 Apr 2026 01:58:16 GMT
ENV INFLUXDB_PR=-2
# Tue, 07 Apr 2026 01:58:16 GMT
ENV INFLUXDB_PV=2.8.0-2
# Tue, 07 Apr 2026 01:58:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 07 Apr 2026 01:58:18 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 07 Apr 2026 01:58:19 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 07 Apr 2026 01:58:19 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 07 Apr 2026 01:58:19 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 07 Apr 2026 01:58:19 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 07 Apr 2026 01:58:19 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 01:58:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 01:58:19 GMT
CMD ["influxd"]
# Tue, 07 Apr 2026 01:58:19 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 07 Apr 2026 01:58:19 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 07 Apr 2026 01:58:19 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 07 Apr 2026 01:58:19 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 07 Apr 2026 01:58:19 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a116bfcd84372702b219d6bae2ee7f1bdb1e6020d05189bc3c26e279e7ab2364`  
		Last Modified: Tue, 07 Apr 2026 01:58:31 GMT  
		Size: 9.8 MB (9798183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:474de9ab304f8664364821fd54a509679041419851afe35980fbd7c13a2c3d97`  
		Last Modified: Tue, 07 Apr 2026 01:58:31 GMT  
		Size: 6.2 MB (6156974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b83865bdaccd9bb5e11b4016b8576733196b451a7ccbd76483a142c59c43d9a`  
		Last Modified: Tue, 07 Apr 2026 01:58:31 GMT  
		Size: 3.2 KB (3232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8f0f8d0f417d9c4f8e42e10838b3c5356ffe44db60dbd713c090b865a36a8f`  
		Last Modified: Tue, 07 Apr 2026 01:58:31 GMT  
		Size: 811.5 KB (811482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb6e598a64d1bb4e5c2b149548399300221b418b182dd8be2b3dc236d88198b`  
		Last Modified: Tue, 07 Apr 2026 01:58:34 GMT  
		Size: 50.5 MB (50451807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeeb37736cabf4a78a0dbde353fe1882f8add4378e667aa82cd363e1e8a03075`  
		Last Modified: Tue, 07 Apr 2026 01:58:33 GMT  
		Size: 11.8 MB (11775867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4badd18ae9f94083936d589b872c729022b8ebd1e531bbfb4095b4c12794edaa`  
		Last Modified: Tue, 07 Apr 2026 01:58:33 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8568054b22810d03f8d0a1cca53fbf9dbc964499c9d672bb65efdf9fbdc3bc`  
		Last Modified: Tue, 07 Apr 2026 01:58:33 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe60089c21668a33bf2ca8e336cf38c667a4f9d13cd9a87462169d50423a93a`  
		Last Modified: Tue, 07 Apr 2026 01:58:34 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:9ad39b5f4622e6dd7b1921af3eef50210a48ca52dcdf489e17ccec5e88499ebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81fcded457e0dde721973237e4f4609db993674c5a1d6e1d50d47d10728485a3`

```dockerfile
```

-	Layers:
	-	`sha256:9d436efb5b4b564ec8f9e830616391ca4e4bf3aa27df1b3060eb7e944e247d3a`  
		Last Modified: Tue, 07 Apr 2026 01:58:31 GMT  
		Size: 2.9 MB (2934237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3eb7467cb3329a9d9c05e5832575b1eaa8f1ed181e6e49c6d4eab15a218e04f`  
		Last Modified: Tue, 07 Apr 2026 01:58:31 GMT  
		Size: 33.6 KB (33620 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:2311605af7772ef47b927d03db36c3fb215b3ce87982712b8d72a5525a18a82d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103639786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:202eb409813be9db84b84bba7249daa05613ed232209b3ee3565c150f8865387`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:01:47 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:01:48 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 07 Apr 2026 02:01:48 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 07 Apr 2026 02:01:49 GMT
ENV GOSU_VER=1.19
# Tue, 07 Apr 2026 02:01:49 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 07 Apr 2026 02:01:49 GMT
ENV INFLUXDB_VERSION=2.8.0
# Tue, 07 Apr 2026 02:01:49 GMT
ENV INFLUXDB_PR=-2
# Tue, 07 Apr 2026 02:01:49 GMT
ENV INFLUXDB_PV=2.8.0-2
# Tue, 07 Apr 2026 02:01:52 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 07 Apr 2026 02:01:52 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 07 Apr 2026 02:01:53 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 07 Apr 2026 02:01:53 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 07 Apr 2026 02:01:53 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 07 Apr 2026 02:01:53 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 07 Apr 2026 02:01:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 02:01:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 02:01:53 GMT
CMD ["influxd"]
# Tue, 07 Apr 2026 02:01:53 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 07 Apr 2026 02:01:53 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 07 Apr 2026 02:01:53 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 07 Apr 2026 02:01:53 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 07 Apr 2026 02:01:53 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00120dc253bd72ad4cf1854724026a81aaf4970b1b00f051ae589a8ecb399dc`  
		Last Modified: Tue, 07 Apr 2026 02:02:04 GMT  
		Size: 9.6 MB (9626917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c98a25d698b6f70d76994e2a0c41ebc991071438847d492e353d6db4eed8965`  
		Last Modified: Tue, 07 Apr 2026 02:02:04 GMT  
		Size: 5.8 MB (5790427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd92e0afeff73eda856e070de3a3920326d1d3d47ebd9a96e265d21ee7d7fad`  
		Last Modified: Tue, 07 Apr 2026 02:02:04 GMT  
		Size: 3.2 KB (3231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85d5b89607330aaceaf098690c579352497d8af3213a534e4ab8e4e0cc055f3`  
		Last Modified: Tue, 07 Apr 2026 02:02:04 GMT  
		Size: 766.4 KB (766371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24f1e34c12a55ea2e93376696df4031d1e98d9471c477cebb06f2e344ccd9fd`  
		Last Modified: Tue, 07 Apr 2026 02:02:07 GMT  
		Size: 48.2 MB (48229552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f058781f0fcd0beafff67981c71ad42c14fb858d6878c0a9e13dc27cc9738b26`  
		Last Modified: Tue, 07 Apr 2026 02:02:06 GMT  
		Size: 11.1 MB (11100394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7aaae010a587cf5a601d46a07d45b378f37c219e996cf7da04e3451ce40f09`  
		Last Modified: Tue, 07 Apr 2026 02:02:06 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f3da28a5bb0e301c7a7a0f4878ec11e653083ea8a0485b114f2c4661c6e5e3`  
		Last Modified: Tue, 07 Apr 2026 02:02:06 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52e0436c606da832d52ceec71b1cf5d5ff170863a1cb76baac382d62f44cfee`  
		Last Modified: Tue, 07 Apr 2026 02:02:07 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:dd3c5e7b9b9671abe2a59b0efea0f7c021b79ea63ba3dbc48760c622647406d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cc341b69e5b33632b785cffba7cbde4509e4ef6926df182df78220fa500ed06`

```dockerfile
```

-	Layers:
	-	`sha256:570e1645673b88b50800b3b86275be91a90a2b107aa8c21d1cb94112ea3f7419`  
		Last Modified: Tue, 07 Apr 2026 02:02:04 GMT  
		Size: 2.9 MB (2933717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb943467e2459ff3405858d9c0df13744923b5ad93d4dddad5d6de90e6559d5f`  
		Last Modified: Tue, 07 Apr 2026 02:02:04 GMT  
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
$ docker pull influxdb@sha256:1399838a53ee3703c9af37eb577087eb0f40291fc8e09b53479a929d4764b7c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:d61de40a52297aaa56d18e3010debca632a688d8a5004fbcd7322079d79441e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.2 MB (24199708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0ff78b350c66a25df1e373fe78cb97d5c91c2d22e68c533165046e9055a5ec2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Mon, 13 Apr 2026 22:50:08 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Mon, 13 Apr 2026 22:50:12 GMT
ENV INFLUXDB_VERSION=1.12.4-c1.12.4
# Mon, 13 Apr 2026 22:50:12 GMT
ENV INFLUXDB_PR=
# Mon, 13 Apr 2026 22:50:12 GMT
ENV INFLUXDB_PV=1.12.4-c1.12.4
# Mon, 13 Apr 2026 22:50:12 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"         "influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     tar -xvf "influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz"         -C /usr/bin --strip-components 1 --wildcards             'influxdb-*/influxd-ctl'             'influxdb-*/influxd-meta' &&     rm "influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"        "influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     apk del .build-deps # buildkit
# Mon, 13 Apr 2026 22:50:12 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Mon, 13 Apr 2026 22:50:12 GMT
EXPOSE map[8091/tcp:{}]
# Mon, 13 Apr 2026 22:50:12 GMT
VOLUME [/var/lib/influxdb]
# Mon, 13 Apr 2026 22:50:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 13 Apr 2026 22:50:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 13 Apr 2026 22:50:12 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2621d562714dca58ddfd6c4f47184a3ba159e3f4d4a937ecf8f9adc5cd75586a`  
		Last Modified: Mon, 13 Apr 2026 22:50:19 GMT  
		Size: 1.2 MB (1225273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1cb56bf705dcad92203f7b0c67545d82c8b16c77c1eea340c7d6648c9830c0`  
		Last Modified: Mon, 13 Apr 2026 22:50:19 GMT  
		Size: 19.3 MB (19330125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98de269dd02db91fae1c0a7ce0ce65a5bac22e3a52bbda9ed9d37d93a3425b0`  
		Last Modified: Mon, 13 Apr 2026 22:50:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff45c438882348bd8c049b59f200d17aa2d0dae0ece0137cd114c93a269762d`  
		Last Modified: Mon, 13 Apr 2026 22:50:19 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:685fe20a7d219baa28f470f7e133a5dcc2d37d866e9bf968947f2e128be977c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **696.0 KB (696003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85d63424599170db739dbb576f478daa13ceda6baed477feebaeb8d2a1ea2e6`

```dockerfile
```

-	Layers:
	-	`sha256:b0245f6ef920020b4e4d70605bb41e363e046c6419f79506ce6b732d401652c1`  
		Last Modified: Mon, 13 Apr 2026 22:50:19 GMT  
		Size: 682.1 KB (682073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a894730f95f327149e8766dc9f0bd2d99a0f470d67dc85191716d144cd280b0c`  
		Last Modified: Mon, 13 Apr 2026 22:50:19 GMT  
		Size: 13.9 KB (13930 bytes)  
		MIME: application/vnd.in-toto+json
