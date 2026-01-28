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
-	[`influxdb:2.8`](#influxdb28)
-	[`influxdb:2.8-alpine`](#influxdb28-alpine)
-	[`influxdb:2.8.0`](#influxdb280)
-	[`influxdb:2.8.0-alpine`](#influxdb280-alpine)
-	[`influxdb:3-core`](#influxdb3-core)
-	[`influxdb:3-enterprise`](#influxdb3-enterprise)
-	[`influxdb:3.8-core`](#influxdb38-core)
-	[`influxdb:3.8-enterprise`](#influxdb38-enterprise)
-	[`influxdb:3.8.0-core`](#influxdb380-core)
-	[`influxdb:3.8.0-enterprise`](#influxdb380-enterprise)
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
$ docker pull influxdb@sha256:5731d7d494216905a36521c6df6df0d12999ff2e239e73ccd3a2d4b6ed1f705e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11` - linux; amd64

```console
$ docker pull influxdb@sha256:0ac0e459bdcd39a058ebdde0dd7a07b18b14f296d7dbbd8474f861908dc602ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116177368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:828e61f2c89d9506ed944eefdc8ee3c64bd46518a0ddff5895b550d8454eb622`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:01:56 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 13 Jan 2026 04:02:04 GMT
ARG INFLUXDB_VERSION=1.11.8
# Tue, 13 Jan 2026 04:02:04 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:02:04 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 13 Jan 2026 04:02:04 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 13 Jan 2026 04:02:04 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Jan 2026 04:02:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 04:02:04 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 13 Jan 2026 04:02:04 GMT
USER influxdb
# Tue, 13 Jan 2026 04:02:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 04:02:04 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:15 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64538a062a61add8dc8b290fa69475e8902eb839c497a5f5dcd5a950422e493c`  
		Last Modified: Tue, 13 Jan 2026 02:09:00 GMT  
		Size: 24.0 MB (24036867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f990d25b7736736466cba7f38966ec5b60598ca974eb35d99a5b1403ef1561d9`  
		Last Modified: Tue, 13 Jan 2026 04:02:16 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0a470cf26ab0c24be778efca6ae49782e10e67ded787a18383970ea0b3e405`  
		Last Modified: Tue, 13 Jan 2026 04:02:18 GMT  
		Size: 43.7 MB (43655970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49de06b8b37c7df90e78454acc578dfd37e0916d8654ff35c5cf40bc714fda0f`  
		Last Modified: Tue, 13 Jan 2026 04:02:17 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e28d6ea97b2128522ae18cbac25e7ce68d4db0d79c29ccddeaaecb1a4f8e76`  
		Last Modified: Tue, 13 Jan 2026 04:02:17 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54988ba62044c342d233377088a63e7628797ac2a65b3db5f8d8808709c281a0`  
		Last Modified: Tue, 13 Jan 2026 04:02:18 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11` - unknown; unknown

```console
$ docker pull influxdb@sha256:79f168221d8056fa10b95281a33555f79cda2405b37b86cda943f776fc0d0d1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4949ad581e62a374533756810901b165accbc4952bbc0215db30868a316ad23`

```dockerfile
```

-	Layers:
	-	`sha256:07a16b4764b1e9334c04cb3c80f978e13f88a313aa8c9433f9368b0f11decf05`  
		Last Modified: Tue, 13 Jan 2026 04:02:17 GMT  
		Size: 5.1 MB (5079263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:931ec08fd4427be10bd6bda681141db62ba57cb5425111346f1eb2e35334fa02`  
		Last Modified: Tue, 13 Jan 2026 04:02:16 GMT  
		Size: 15.5 KB (15486 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:4b3b42b289a3df95e618b490efea3466de731de1c545b019c17c7195db7f15b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113096300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:292796b53d40a0c8793c5af9bdbf88435e590e492cbf8e4ab02a4b0a20ccb375`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:12:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:05:25 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 13 Jan 2026 04:05:33 GMT
ARG INFLUXDB_VERSION=1.11.8
# Tue, 13 Jan 2026 04:05:33 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:05:33 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 13 Jan 2026 04:05:33 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 13 Jan 2026 04:05:33 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Jan 2026 04:05:33 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 04:05:33 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 13 Jan 2026 04:05:33 GMT
USER influxdb
# Tue, 13 Jan 2026 04:05:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 04:05:33 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:14 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72c713ab317dd7f302a6ff5a345af5b61cddc864fca2d96a23e6ef3c90a6657`  
		Last Modified: Tue, 13 Jan 2026 02:12:45 GMT  
		Size: 23.6 MB (23604814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae3903c66c4c5bfa366d9e9df3b227da8fd5349391f7891cb4e276f8057beae`  
		Last Modified: Tue, 13 Jan 2026 04:05:49 GMT  
		Size: 1.2 KB (1205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa8a9b1238f548bde7a3026bc36dd439cacd40b3e65156d749dc726de7e8797`  
		Last Modified: Tue, 13 Jan 2026 04:05:51 GMT  
		Size: 41.1 MB (41122496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ee0d5104330a4f3e73b3e9ff16a5013460b493da916f686fdd6431abc7c072`  
		Last Modified: Tue, 13 Jan 2026 04:05:49 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a06c08a52dc5a184b5a4a493a05ad2e2dbb0f223e131d6339ac223943615bd91`  
		Last Modified: Tue, 13 Jan 2026 04:05:49 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178df1da6314c40f67825e4ce91ebb175e538d25b32c3a0e08504068f299b760`  
		Last Modified: Tue, 13 Jan 2026 04:05:50 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11` - unknown; unknown

```console
$ docker pull influxdb@sha256:1886ec18bba46a2a49ac4edd1ccf5c2a2111a6bc02b7b8ab49bdc5833154cfc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58267ac50e542c89e214e200ae3f253684c7a56867c3ccab00db745f39e11277`

```dockerfile
```

-	Layers:
	-	`sha256:a5cb518f206e7b7aeedf9f8e2da7e47e51ae6090cca2dfe3ce308d54cef202fd`  
		Last Modified: Tue, 13 Jan 2026 04:05:49 GMT  
		Size: 5.1 MB (5078728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37b3e3e7e6e23be89b170c865dcc150d13444b9a4536dc428b44b4408216a388`  
		Last Modified: Tue, 13 Jan 2026 04:05:48 GMT  
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
$ docker pull influxdb@sha256:cf02295d0e71597f02b0209a70a21e67beafb9dda19c21c35b883ccfafb74e81
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data` - linux; amd64

```console
$ docker pull influxdb@sha256:c47b46d4cd11f7aeb784b6afec384c0b62d1d5d92b4a36dcbe38fa2e53766c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114691038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c39d3c8f71d4af247579725fff7fe13447c99d1ede675ff563caa9ae0080deee`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:02:10 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 04:02:13 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Tue, 13 Jan 2026 04:02:13 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 13 Jan 2026 04:02:13 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 13 Jan 2026 04:02:13 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 13 Jan 2026 04:02:13 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Jan 2026 04:02:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 04:02:13 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 13 Jan 2026 04:02:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 04:02:13 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:15 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64538a062a61add8dc8b290fa69475e8902eb839c497a5f5dcd5a950422e493c`  
		Last Modified: Tue, 13 Jan 2026 02:09:00 GMT  
		Size: 24.0 MB (24036867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725b26fb2b36dd4f2a5f615acd7dff70ad03b02006a86dced12e04b338667995`  
		Last Modified: Tue, 13 Jan 2026 04:02:25 GMT  
		Size: 5.1 KB (5069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0879436a1a448f71f3a5423cf6ccd1e8ba5bc68d47daecb98dade59ae44e2d10`  
		Last Modified: Tue, 13 Jan 2026 04:02:26 GMT  
		Size: 42.2 MB (42165705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e04de71dced00ac7bb0b91a5b1c8a11fe2e4c600c4df8f2658daa2fe5a36dab`  
		Last Modified: Tue, 13 Jan 2026 04:02:25 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0896035861b9d64b002c8437885efe5970b0f8d1f913f00b2b2f8809db13b2`  
		Last Modified: Tue, 13 Jan 2026 04:02:25 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9412fe76db1a8d0debd4745f307f06b231740d4ca94dd7ee3cfe4068931199`  
		Last Modified: Tue, 13 Jan 2026 04:02:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:8cc7e76ce1936a96c6637127aae3f33565d1d6fca63c00a02a2ae0737b4dfb3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4699071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82ab2bdc246e44c9058db1f530a2f60ce8b57e2fc2d3c1e4a30be31384159a2e`

```dockerfile
```

-	Layers:
	-	`sha256:466e7d9c39e293259dd5958ab1e5f47fdda043fc6db0c7d06c4cdea713e4e00d`  
		Last Modified: Tue, 13 Jan 2026 04:02:26 GMT  
		Size: 4.7 MB (4684406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0f3c3efc31aeb55ade2b3690d807b5daa2988686246cb1520eabe0e26252f4d`  
		Last Modified: Tue, 13 Jan 2026 04:02:25 GMT  
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
$ docker pull influxdb@sha256:72b79b0e5c647abeea019461ee85942088cd2f4d6824b9976fceedae844ed396
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:fa6104c04fd38a3a0d3c30235cf259b129111044660099c20d62c77e1b79f58f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91120264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7358e66dc8837847576ef42f15f1864e39e08bfd9bfda6aac878a48ffd5ee3e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:02:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 04:02:22 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Tue, 13 Jan 2026 04:02:22 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 13 Jan 2026 04:02:22 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 13 Jan 2026 04:02:22 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 13 Jan 2026 04:02:22 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Jan 2026 04:02:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 04:02:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 04:02:22 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:15 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64538a062a61add8dc8b290fa69475e8902eb839c497a5f5dcd5a950422e493c`  
		Last Modified: Tue, 13 Jan 2026 02:09:00 GMT  
		Size: 24.0 MB (24036867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742fe9ffa44988147584c258c838556baa2829de4562d711252d64e35aa51acd`  
		Last Modified: Tue, 13 Jan 2026 04:02:31 GMT  
		Size: 5.1 KB (5055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e133e4a1f3889d73daec291d302cafcc4899ca6d2aaa3e8777bb93723ed75aa9`  
		Last Modified: Tue, 13 Jan 2026 04:02:32 GMT  
		Size: 18.6 MB (18596154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f0d90c9a55fc5d40a291700ed3241a6641296699bd5c38a3a9a9e1000176a6`  
		Last Modified: Tue, 13 Jan 2026 04:02:31 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a23e96a64c373830c3112d5ea37a79c3993a929e3c490146c6a0941d586dba3`  
		Last Modified: Tue, 13 Jan 2026 04:02:31 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:75b38829f940c43183ab18a17324cde6a51c9e9d6bc314ecb658a9487376f2d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4604273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df44d252e17db65e3a40ec56adb044673bdb6cd4162c3336cb8f381a6a592c57`

```dockerfile
```

-	Layers:
	-	`sha256:493a985ef35b82a4b4f5890722fbaaef6746336fbfb45c36d5ec42c643f23532`  
		Last Modified: Tue, 13 Jan 2026 04:02:31 GMT  
		Size: 4.6 MB (4591249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e6550cdbcfce5974370dfda3978e51be51af752edf5b24411a54a04db03405d`  
		Last Modified: Tue, 13 Jan 2026 04:02:31 GMT  
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
$ docker pull influxdb@sha256:5731d7d494216905a36521c6df6df0d12999ff2e239e73ccd3a2d4b6ed1f705e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11.8` - linux; amd64

```console
$ docker pull influxdb@sha256:0ac0e459bdcd39a058ebdde0dd7a07b18b14f296d7dbbd8474f861908dc602ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116177368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:828e61f2c89d9506ed944eefdc8ee3c64bd46518a0ddff5895b550d8454eb622`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:01:56 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 13 Jan 2026 04:02:04 GMT
ARG INFLUXDB_VERSION=1.11.8
# Tue, 13 Jan 2026 04:02:04 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:02:04 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 13 Jan 2026 04:02:04 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 13 Jan 2026 04:02:04 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Jan 2026 04:02:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 04:02:04 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 13 Jan 2026 04:02:04 GMT
USER influxdb
# Tue, 13 Jan 2026 04:02:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 04:02:04 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:15 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64538a062a61add8dc8b290fa69475e8902eb839c497a5f5dcd5a950422e493c`  
		Last Modified: Tue, 13 Jan 2026 02:09:00 GMT  
		Size: 24.0 MB (24036867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f990d25b7736736466cba7f38966ec5b60598ca974eb35d99a5b1403ef1561d9`  
		Last Modified: Tue, 13 Jan 2026 04:02:16 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0a470cf26ab0c24be778efca6ae49782e10e67ded787a18383970ea0b3e405`  
		Last Modified: Tue, 13 Jan 2026 04:02:18 GMT  
		Size: 43.7 MB (43655970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49de06b8b37c7df90e78454acc578dfd37e0916d8654ff35c5cf40bc714fda0f`  
		Last Modified: Tue, 13 Jan 2026 04:02:17 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e28d6ea97b2128522ae18cbac25e7ce68d4db0d79c29ccddeaaecb1a4f8e76`  
		Last Modified: Tue, 13 Jan 2026 04:02:17 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54988ba62044c342d233377088a63e7628797ac2a65b3db5f8d8808709c281a0`  
		Last Modified: Tue, 13 Jan 2026 04:02:18 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:79f168221d8056fa10b95281a33555f79cda2405b37b86cda943f776fc0d0d1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4949ad581e62a374533756810901b165accbc4952bbc0215db30868a316ad23`

```dockerfile
```

-	Layers:
	-	`sha256:07a16b4764b1e9334c04cb3c80f978e13f88a313aa8c9433f9368b0f11decf05`  
		Last Modified: Tue, 13 Jan 2026 04:02:17 GMT  
		Size: 5.1 MB (5079263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:931ec08fd4427be10bd6bda681141db62ba57cb5425111346f1eb2e35334fa02`  
		Last Modified: Tue, 13 Jan 2026 04:02:16 GMT  
		Size: 15.5 KB (15486 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:4b3b42b289a3df95e618b490efea3466de731de1c545b019c17c7195db7f15b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113096300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:292796b53d40a0c8793c5af9bdbf88435e590e492cbf8e4ab02a4b0a20ccb375`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:12:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:05:25 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 13 Jan 2026 04:05:33 GMT
ARG INFLUXDB_VERSION=1.11.8
# Tue, 13 Jan 2026 04:05:33 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:05:33 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 13 Jan 2026 04:05:33 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 13 Jan 2026 04:05:33 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Jan 2026 04:05:33 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 04:05:33 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 13 Jan 2026 04:05:33 GMT
USER influxdb
# Tue, 13 Jan 2026 04:05:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 04:05:33 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:14 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72c713ab317dd7f302a6ff5a345af5b61cddc864fca2d96a23e6ef3c90a6657`  
		Last Modified: Tue, 13 Jan 2026 02:12:45 GMT  
		Size: 23.6 MB (23604814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae3903c66c4c5bfa366d9e9df3b227da8fd5349391f7891cb4e276f8057beae`  
		Last Modified: Tue, 13 Jan 2026 04:05:49 GMT  
		Size: 1.2 KB (1205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa8a9b1238f548bde7a3026bc36dd439cacd40b3e65156d749dc726de7e8797`  
		Last Modified: Tue, 13 Jan 2026 04:05:51 GMT  
		Size: 41.1 MB (41122496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ee0d5104330a4f3e73b3e9ff16a5013460b493da916f686fdd6431abc7c072`  
		Last Modified: Tue, 13 Jan 2026 04:05:49 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a06c08a52dc5a184b5a4a493a05ad2e2dbb0f223e131d6339ac223943615bd91`  
		Last Modified: Tue, 13 Jan 2026 04:05:49 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178df1da6314c40f67825e4ce91ebb175e538d25b32c3a0e08504068f299b760`  
		Last Modified: Tue, 13 Jan 2026 04:05:50 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:1886ec18bba46a2a49ac4edd1ccf5c2a2111a6bc02b7b8ab49bdc5833154cfc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58267ac50e542c89e214e200ae3f253684c7a56867c3ccab00db745f39e11277`

```dockerfile
```

-	Layers:
	-	`sha256:a5cb518f206e7b7aeedf9f8e2da7e47e51ae6090cca2dfe3ce308d54cef202fd`  
		Last Modified: Tue, 13 Jan 2026 04:05:49 GMT  
		Size: 5.1 MB (5078728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37b3e3e7e6e23be89b170c865dcc150d13444b9a4536dc428b44b4408216a388`  
		Last Modified: Tue, 13 Jan 2026 04:05:48 GMT  
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
$ docker pull influxdb@sha256:cf02295d0e71597f02b0209a70a21e67beafb9dda19c21c35b883ccfafb74e81
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.9-data` - linux; amd64

```console
$ docker pull influxdb@sha256:c47b46d4cd11f7aeb784b6afec384c0b62d1d5d92b4a36dcbe38fa2e53766c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114691038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c39d3c8f71d4af247579725fff7fe13447c99d1ede675ff563caa9ae0080deee`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:02:10 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 04:02:13 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Tue, 13 Jan 2026 04:02:13 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 13 Jan 2026 04:02:13 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 13 Jan 2026 04:02:13 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 13 Jan 2026 04:02:13 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Jan 2026 04:02:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 04:02:13 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 13 Jan 2026 04:02:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 04:02:13 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:15 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64538a062a61add8dc8b290fa69475e8902eb839c497a5f5dcd5a950422e493c`  
		Last Modified: Tue, 13 Jan 2026 02:09:00 GMT  
		Size: 24.0 MB (24036867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725b26fb2b36dd4f2a5f615acd7dff70ad03b02006a86dced12e04b338667995`  
		Last Modified: Tue, 13 Jan 2026 04:02:25 GMT  
		Size: 5.1 KB (5069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0879436a1a448f71f3a5423cf6ccd1e8ba5bc68d47daecb98dade59ae44e2d10`  
		Last Modified: Tue, 13 Jan 2026 04:02:26 GMT  
		Size: 42.2 MB (42165705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e04de71dced00ac7bb0b91a5b1c8a11fe2e4c600c4df8f2658daa2fe5a36dab`  
		Last Modified: Tue, 13 Jan 2026 04:02:25 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0896035861b9d64b002c8437885efe5970b0f8d1f913f00b2b2f8809db13b2`  
		Last Modified: Tue, 13 Jan 2026 04:02:25 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9412fe76db1a8d0debd4745f307f06b231740d4ca94dd7ee3cfe4068931199`  
		Last Modified: Tue, 13 Jan 2026 04:02:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.9-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:8cc7e76ce1936a96c6637127aae3f33565d1d6fca63c00a02a2ae0737b4dfb3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4699071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82ab2bdc246e44c9058db1f530a2f60ce8b57e2fc2d3c1e4a30be31384159a2e`

```dockerfile
```

-	Layers:
	-	`sha256:466e7d9c39e293259dd5958ab1e5f47fdda043fc6db0c7d06c4cdea713e4e00d`  
		Last Modified: Tue, 13 Jan 2026 04:02:26 GMT  
		Size: 4.7 MB (4684406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0f3c3efc31aeb55ade2b3690d807b5daa2988686246cb1520eabe0e26252f4d`  
		Last Modified: Tue, 13 Jan 2026 04:02:25 GMT  
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
$ docker pull influxdb@sha256:72b79b0e5c647abeea019461ee85942088cd2f4d6824b9976fceedae844ed396
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.9-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:fa6104c04fd38a3a0d3c30235cf259b129111044660099c20d62c77e1b79f58f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91120264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7358e66dc8837847576ef42f15f1864e39e08bfd9bfda6aac878a48ffd5ee3e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:02:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 13 Jan 2026 04:02:22 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Tue, 13 Jan 2026 04:02:22 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 13 Jan 2026 04:02:22 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 13 Jan 2026 04:02:22 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 13 Jan 2026 04:02:22 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Jan 2026 04:02:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 04:02:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 04:02:22 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:15 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64538a062a61add8dc8b290fa69475e8902eb839c497a5f5dcd5a950422e493c`  
		Last Modified: Tue, 13 Jan 2026 02:09:00 GMT  
		Size: 24.0 MB (24036867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742fe9ffa44988147584c258c838556baa2829de4562d711252d64e35aa51acd`  
		Last Modified: Tue, 13 Jan 2026 04:02:31 GMT  
		Size: 5.1 KB (5055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e133e4a1f3889d73daec291d302cafcc4899ca6d2aaa3e8777bb93723ed75aa9`  
		Last Modified: Tue, 13 Jan 2026 04:02:32 GMT  
		Size: 18.6 MB (18596154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f0d90c9a55fc5d40a291700ed3241a6641296699bd5c38a3a9a9e1000176a6`  
		Last Modified: Tue, 13 Jan 2026 04:02:31 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a23e96a64c373830c3112d5ea37a79c3993a929e3c490146c6a0941d586dba3`  
		Last Modified: Tue, 13 Jan 2026 04:02:31 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.9-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:75b38829f940c43183ab18a17324cde6a51c9e9d6bc314ecb658a9487376f2d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4604273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df44d252e17db65e3a40ec56adb044673bdb6cd4162c3336cb8f381a6a592c57`

```dockerfile
```

-	Layers:
	-	`sha256:493a985ef35b82a4b4f5890722fbaaef6746336fbfb45c36d5ec42c643f23532`  
		Last Modified: Tue, 13 Jan 2026 04:02:31 GMT  
		Size: 4.6 MB (4591249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e6550cdbcfce5974370dfda3978e51be51af752edf5b24411a54a04db03405d`  
		Last Modified: Tue, 13 Jan 2026 04:02:31 GMT  
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
$ docker pull influxdb@sha256:f3afe89c4dc35f146be3ea51c5dedd656c254a9add1ae07eeadca3515029e9fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.12` - linux; amd64

```console
$ docker pull influxdb@sha256:6917c61f7b7985f4ee4f962f70470841a7f407ba70bc0265d7165fae33f0237d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.9 MB (113854585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaa7fc75a9556b81328dc3e6283b047adab59d448dc7fd1fc564917a8df739c7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:01:32 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 13 Jan 2026 04:01:39 GMT
ARG INFLUXDB_VERSION=1.12.2
# Tue, 13 Jan 2026 04:01:39 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:01:39 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 13 Jan 2026 04:01:39 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 13 Jan 2026 04:01:39 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Jan 2026 04:01:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 04:01:39 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 13 Jan 2026 04:01:39 GMT
USER influxdb
# Tue, 13 Jan 2026 04:01:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 04:01:39 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:15 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64538a062a61add8dc8b290fa69475e8902eb839c497a5f5dcd5a950422e493c`  
		Last Modified: Tue, 13 Jan 2026 02:09:00 GMT  
		Size: 24.0 MB (24036867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c22b05fa882dbbd60440b09a3ec476ebe474cfda3f322e86ea99a39773311ff`  
		Last Modified: Tue, 13 Jan 2026 04:01:52 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095de93a216193ad71ad56a36c80d3a1f63af494f8902a1813bb1c4dfa0b4154`  
		Last Modified: Tue, 13 Jan 2026 04:01:53 GMT  
		Size: 41.3 MB (41333184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090738da3a915b0cc95274040b43fc1908bec3499fd47aa8a111af60fe706ff5`  
		Last Modified: Tue, 13 Jan 2026 04:01:52 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a939c63c8c824c090a62a1de1e4d53b256966ad574511bcab52c98624386f4`  
		Last Modified: Tue, 13 Jan 2026 04:01:52 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b12a0f18a42fce4393789e9c7988aa7c323463de50edd44e9bfdbf54c645517`  
		Last Modified: Tue, 13 Jan 2026 04:01:53 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:13980e20fb6e543b9dcc1eeee545e0d8fe3f62f29f0acc073063e5bfb4c3e9c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4692912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d14bd9b0fe140f81efb9caba62a6357953e030b7955e0056d17e2ec0ac7545f`

```dockerfile
```

-	Layers:
	-	`sha256:10380ebb8bbb2eccfa008e53390f65b9c8802135c15975af4b5f4d9cd2a7bc13`  
		Last Modified: Tue, 13 Jan 2026 04:01:52 GMT  
		Size: 4.7 MB (4676456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54c700714a2269c9a3a2cca268e744abb97bc1e3143b40e6812d8ed1b70a67c1`  
		Last Modified: Tue, 13 Jan 2026 04:01:52 GMT  
		Size: 16.5 KB (16456 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.12` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:9a2002e3287172532d89974ca043b0c46c8f4767ec681d4f8d02ed223775eafc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110110739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3bb24c68ad0344728ae758051895414b4adb8a39ab42006eaa32c336a19513`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:12:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:05:12 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 13 Jan 2026 04:05:18 GMT
ARG INFLUXDB_VERSION=1.12.2
# Tue, 13 Jan 2026 04:05:18 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:05:18 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 13 Jan 2026 04:05:18 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 13 Jan 2026 04:05:18 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Jan 2026 04:05:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 04:05:18 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 13 Jan 2026 04:05:18 GMT
USER influxdb
# Tue, 13 Jan 2026 04:05:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 04:05:18 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:14 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72c713ab317dd7f302a6ff5a345af5b61cddc864fca2d96a23e6ef3c90a6657`  
		Last Modified: Tue, 13 Jan 2026 02:12:45 GMT  
		Size: 23.6 MB (23604814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32711d9c6895fb4667fedd16e8277c5c89718586b3637e933bba65e2679be49d`  
		Last Modified: Tue, 13 Jan 2026 04:05:33 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2128fdd094a63cf7cc6275615289a80c9a482b4be8e1660f09b6643846a1c5c`  
		Last Modified: Tue, 13 Jan 2026 04:05:35 GMT  
		Size: 38.1 MB (38136943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a02bbdfec69d3b4321b6643a7949f4cb795ef901faeef0fadb8934f1a6578d7`  
		Last Modified: Tue, 13 Jan 2026 04:05:33 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547c0dc17c88c1cac835a1f7bbe1c0a8b7a4decd7893434b122de77e4a311cbb`  
		Last Modified: Tue, 13 Jan 2026 04:05:33 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44c2d7d11424c30bcb720acc76e1451af022c394c98bc9848ecd7ec5d7e35ad`  
		Last Modified: Tue, 13 Jan 2026 04:05:35 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:7c69b1070116ae9939b524b2267b4698ac77e72c88210b8035c026a40fbe45f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4692465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55276b8e215debe8243590e8486a973cd66458ff1318527ae5f6404c49b04014`

```dockerfile
```

-	Layers:
	-	`sha256:36b5c1ecb3646c63822a8cf440a84b5715a76637b080cf479735e45fca7a34ef`  
		Last Modified: Tue, 13 Jan 2026 04:05:34 GMT  
		Size: 4.7 MB (4675914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5535ab390cd8e5f3d81737bc4a15dabffbbb67fa983a0cc4c4693d1a41ef21c6`  
		Last Modified: Tue, 13 Jan 2026 04:05:33 GMT  
		Size: 16.6 KB (16551 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12-alpine`

```console
$ docker pull influxdb@sha256:1ed16e0f6a44ab61a30357566845efbb9757556851e6ff97227f939bf9ef9ace
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.12-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:697aba0e3c65d5d7bd8c0165468ba9ee24657f504bb4366fece150b28f019a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46124218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb897a5f792495e87d9871b6a4cfc773bd6606d7bc580daf4ff262360e9c04d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:23:21 GMT
RUN apk add --no-cache bash ca-certificates tzdata &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:23:26 GMT
ARG INFLUXDB_VERSION=1.12.2
# Wed, 28 Jan 2026 03:23:26 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     case "$(apk --print-arch)" in         x86_64)  ARCH=amd64 ;;         aarch64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar -xvf "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz"         -C / --strip-components 1 --wildcards             'influxdb-*/usr/bin/influx'             'influxdb-*/usr/bin/influx_inspect'             'influxdb-*/usr/bin/influxd' &&     rm "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"        "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 03:23:26 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 28 Jan 2026 03:23:26 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Wed, 28 Jan 2026 03:23:26 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 Jan 2026 03:23:26 GMT
VOLUME [/var/lib/influxdb]
# Wed, 28 Jan 2026 03:23:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:23:26 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 28 Jan 2026 03:23:26 GMT
USER influxdb
# Wed, 28 Jan 2026 03:23:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:23:26 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61ad874caf1ce155d9c06c85c089035ff4b41fea8f68219cb60604fecea628f`  
		Last Modified: Wed, 28 Jan 2026 03:23:36 GMT  
		Size: 1.2 MB (1225476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f59042c15009bf41c0b1fa6c4d2d2d13d0250f49e1409fb7b663adc462759b`  
		Last Modified: Wed, 28 Jan 2026 03:23:37 GMT  
		Size: 41.3 MB (41252292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed17935cb0b9555361ea5defc075520b1cdccd69d5a58d7e269415bee692cee`  
		Last Modified: Wed, 28 Jan 2026 03:23:36 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d76182047c6a6ca57e871f8736596a2ae48b8a3c50277aedeeb7987a622c6f`  
		Last Modified: Wed, 28 Jan 2026 03:23:36 GMT  
		Size: 994.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4fb1c6df23e845268a733a445e5db0893ba7589591cadeabba1bdf3adf782c`  
		Last Modified: Wed, 28 Jan 2026 03:23:37 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ba8b159859dfc44049e5332e08c60d8b36b38fc5e1d118748fe8e3e1543924`  
		Last Modified: Wed, 28 Jan 2026 03:23:37 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:af2b5dd8ad0d3b16b3907ff491d74d1f2eff068de322e7489c77bd75466cd8a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **780.5 KB (780479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51dc09838f56b2799381d5dd1c3400f40ea2244acca53eabafae485097494bf9`

```dockerfile
```

-	Layers:
	-	`sha256:f39e15f06b57000511387e30703a81694cd535187db4291a2e8f5bcefece88a6`  
		Last Modified: Wed, 28 Jan 2026 03:23:36 GMT  
		Size: 761.9 KB (761859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9426c81519fa2e633147ad49e1850cde661e950ff86aefd90f840a0cd91d5c96`  
		Last Modified: Wed, 28 Jan 2026 03:23:36 GMT  
		Size: 18.6 KB (18620 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.12-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:a15f5bc8b2ce1d70a31b981c371a1ddd88c6fc05c655c7e01b57eecaf60fbbd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 MB (43343070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4654f5bc4db16a713150f336f9aac2a58bc3dfb28052ad26fdc2db98f8d1d717`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:07 GMT
ADD alpine-minirootfs-3.21.6-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:07 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:15:34 GMT
RUN apk add --no-cache bash ca-certificates tzdata &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:15:40 GMT
ARG INFLUXDB_VERSION=1.12.2
# Wed, 28 Jan 2026 03:15:40 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     case "$(apk --print-arch)" in         x86_64)  ARCH=amd64 ;;         aarch64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar -xvf "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz"         -C / --strip-components 1 --wildcards             'influxdb-*/usr/bin/influx'             'influxdb-*/usr/bin/influx_inspect'             'influxdb-*/usr/bin/influxd' &&     rm "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"        "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 03:15:40 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 28 Jan 2026 03:15:40 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Wed, 28 Jan 2026 03:15:40 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 Jan 2026 03:15:40 GMT
VOLUME [/var/lib/influxdb]
# Wed, 28 Jan 2026 03:15:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:15:40 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 28 Jan 2026 03:15:40 GMT
USER influxdb
# Wed, 28 Jan 2026 03:15:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:15:40 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:a447a5de8f4eb4a987d81c0afa14d459cc714599c020c08f45fafa9c6c904b30`  
		Last Modified: Wed, 28 Jan 2026 01:18:13 GMT  
		Size: 4.0 MB (3992880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad49504157754b82690dc411a4cbb1be979c94a1504554cc7508eb53848d9aaa`  
		Last Modified: Wed, 28 Jan 2026 03:15:50 GMT  
		Size: 1.3 MB (1290781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5d1cb0eb9bcf36e7b5a1a4000c5aece49077b899de952de6fdbd89c9c1f44b`  
		Last Modified: Wed, 28 Jan 2026 03:15:51 GMT  
		Size: 38.1 MB (38056702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1137d619a385938b5d7d7306b62a613a6dbb383adfd1ec3a55ce047164213cd1`  
		Last Modified: Wed, 28 Jan 2026 03:15:49 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef4649756164c4e09b5e20f42da696b65fd206aa9a9e69d940360af42044b28`  
		Last Modified: Wed, 28 Jan 2026 03:15:49 GMT  
		Size: 993.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1622ae5fef1f8a1581c49244f92707dde2199a2db553408fb31beec7b70b181e`  
		Last Modified: Wed, 28 Jan 2026 03:15:50 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946d050ae0ebead10e2f4ab1c542a8b9ddf94d0784aa98106e5c9bd7dbd02631`  
		Last Modified: Wed, 28 Jan 2026 03:15:51 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:edfd9ff1eb419bbf315b4102159bb5d501769546111a9c02e7e64d25684fa482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **779.8 KB (779816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08bd24f011bd6bdf62cee047d5433e2b6dba99042b7d6c09aa052a11bb91f17f`

```dockerfile
```

-	Layers:
	-	`sha256:a51c507fdc8870eba3993722731f2c5c18c27320de1587e98a2662a90b734787`  
		Last Modified: Wed, 28 Jan 2026 03:15:49 GMT  
		Size: 761.1 KB (761088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94d21d56468ffa602372ea8026b8acdae37f5ee8aab4afbb5aeda345db5c31f9`  
		Last Modified: Wed, 28 Jan 2026 03:15:49 GMT  
		Size: 18.7 KB (18728 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12-data`

```console
$ docker pull influxdb@sha256:be4700d7692b8a727eb6cc5f1c32c7ebe704bdac03d39a06e16fc86e8006e65b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12-data` - linux; amd64

```console
$ docker pull influxdb@sha256:d1ec024b86aa737221977a5040dc3b66815147f5741819488120fc87a6c9580f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114840077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77eee634dfccb1cbf60ff3500a7cdd422b7fe57ac29c0834e043952fe5171695`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:01:52 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Tue, 13 Jan 2026 04:01:52 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"         "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     rm -r "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"           "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:01:52 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 13 Jan 2026 04:01:52 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 13 Jan 2026 04:01:52 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Jan 2026 04:01:52 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 04:01:52 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 13 Jan 2026 04:01:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 04:01:52 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:15 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64538a062a61add8dc8b290fa69475e8902eb839c497a5f5dcd5a950422e493c`  
		Last Modified: Tue, 13 Jan 2026 02:09:00 GMT  
		Size: 24.0 MB (24036867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66c83e9d2d95ae7bb8cae9f8b46bff3d99ebbbdce310b651807fcd051a37ba0`  
		Last Modified: Tue, 13 Jan 2026 04:02:06 GMT  
		Size: 42.3 MB (42319809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485ded8552cc8df9c3417e10f8333c7f5f414f71250ce6145d55fc4b15698edd`  
		Last Modified: Tue, 13 Jan 2026 04:02:05 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3948a1f32b313d88999deaa596d64ebb9423cb1c3aa9be6cfe4be40e635ac3`  
		Last Modified: Tue, 13 Jan 2026 04:02:05 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18ad3cf56c36afce2bd43874b271d452c70a98b369b3108ea1a68c2d1093e92`  
		Last Modified: Tue, 13 Jan 2026 04:02:05 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:4be6b6094085a1d6722283c42c361a38cfcfa77db9f25275413122a8aa260d88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4700469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb24414afd5c068a73d4ec08d1a75579ed8094de9c7f4d21bb46345a51a6b924`

```dockerfile
```

-	Layers:
	-	`sha256:5dfa793211611cb151c8c0f1f35f084eae3bb9a6d3793a1c3e8de1ff7a66a120`  
		Last Modified: Tue, 13 Jan 2026 04:02:05 GMT  
		Size: 4.7 MB (4686392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:593d647c6647a10283a9515111c55e17f9854ceede24aefe8268425e17a1497a`  
		Last Modified: Tue, 13 Jan 2026 04:02:04 GMT  
		Size: 14.1 KB (14077 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12-data-alpine`

```console
$ docker pull influxdb@sha256:230aced0d72a917905c28e8370266348fb49894a4e1d090c47765a1488e94bff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:40d2fef5a316bf72ec0b29c322a7cf01fbd7046fad6e09edef3afd6a2a51f192
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47123756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8324e71acc24adb0423f7eb4de13354493b40f765bdb36448d77ce375caa87c3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:24:06 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:24:11 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Wed, 28 Jan 2026 03:24:11 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"         "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     tar -xvf "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz"         -C / --strip-components 1 --wildcards             'influxdb-*/usr/bin/influx'             'influxdb-*/usr/bin/influx_inspect'             'influxdb-*/usr/bin/influxd' &&     rm "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"        "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 03:24:11 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 28 Jan 2026 03:24:11 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 Jan 2026 03:24:11 GMT
VOLUME [/var/lib/influxdb]
# Wed, 28 Jan 2026 03:24:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:24:11 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 28 Jan 2026 03:24:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:24:11 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adc499747d2c1716d5193ed87e0f6684b5f7da3ad6b0d2bdfc84d65ed106d36`  
		Last Modified: Wed, 28 Jan 2026 03:24:21 GMT  
		Size: 1.2 MB (1225465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a172153dcef0bec4a9c7bb4c587f4400c9485a79c347dec788239589954f4770`  
		Last Modified: Wed, 28 Jan 2026 03:24:22 GMT  
		Size: 42.3 MB (42252778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b330c6f2273441c4cece26de32b1b56b5641f92928b4b5256a15fd7ef0db1a6`  
		Last Modified: Wed, 28 Jan 2026 03:24:21 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb3efac6bd9c420eddfe57595ec744fa728401020c9af575cb9cdbe12776f5f`  
		Last Modified: Wed, 28 Jan 2026 03:24:21 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1f1384e53b8afac073280a7d6b42b05cfeb3ad8ff3c328242a61d8f88d4018`  
		Last Modified: Wed, 28 Jan 2026 03:24:22 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:fff49aac562db0793d72005156712fb335c4f0488b91b3f35e434498d2e282a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **791.6 KB (791580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05cbe541688ac6e58740d2ecbecb6eaa4446654bb8c3635d47c1614319c2135d`

```dockerfile
```

-	Layers:
	-	`sha256:7746afe39499c0509347119e90a393e2f741f8c2e4a54628af8774335219ffeb`  
		Last Modified: Wed, 28 Jan 2026 03:24:21 GMT  
		Size: 776.1 KB (776122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a10bcf68f284ed3ad3af63a4766b3825d0a6fb102c1dc2b1199ddd247f8f9cef`  
		Last Modified: Wed, 28 Jan 2026 03:24:21 GMT  
		Size: 15.5 KB (15458 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12-meta`

```console
$ docker pull influxdb@sha256:5eb24e671873d2663ef0c00ebde2c425db825a47e36f9a93b19dd18752354a0d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:9ec905fa99e678b7a46d0f8e84f7cbdcad71b5f480e6e7c398e5eaa965ac6e20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91299873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a552f12602ad1bedee2244e93fed92a53903cba13ca8b81e04d628e2c85a4228`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:01:51 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Tue, 13 Jan 2026 04:01:51 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"         "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     rm -r "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"           "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:01:51 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 13 Jan 2026 04:01:51 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 13 Jan 2026 04:01:51 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Jan 2026 04:01:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 04:01:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 04:01:51 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:15 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64538a062a61add8dc8b290fa69475e8902eb839c497a5f5dcd5a950422e493c`  
		Last Modified: Tue, 13 Jan 2026 02:09:00 GMT  
		Size: 24.0 MB (24036867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8226584456c231e3329e2f781db217386df170900017ccf5ad54f649f3a4892`  
		Last Modified: Tue, 13 Jan 2026 04:02:01 GMT  
		Size: 18.8 MB (18780819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61622d86659aed4ba8f4ef77c6784a2201f76664031c14b2cfc4382d1fad188c`  
		Last Modified: Tue, 13 Jan 2026 04:02:00 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91888eb7d9961fd828a172be924f04fc445944a4a20a7c1b5d0cdba26ca1429`  
		Last Modified: Tue, 13 Jan 2026 04:02:01 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:fc34f0e0037afbb0dd07c5569c82c110b8ee9270e8a27fd45a0f0ff815adbade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4604146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05bf3ef5c6c6a490e1a87aeeee4ccd065070ed262594888f4ab79e55e3e7df88`

```dockerfile
```

-	Layers:
	-	`sha256:ef9b998d76c6a317d3d028cff8c5607da4ac015da97d036c8556b540b4eed402`  
		Last Modified: Tue, 13 Jan 2026 04:02:01 GMT  
		Size: 4.6 MB (4591555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90bcc4be344b12d86469f9015e7e36c92c0e18c887c79c28a6183d38f7a71dc1`  
		Last Modified: Tue, 13 Jan 2026 04:02:00 GMT  
		Size: 12.6 KB (12591 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12-meta-alpine`

```console
$ docker pull influxdb@sha256:aecaf75c0592866bc0a7c2639bb83f72193dda8ca322e9434210831a02a4857a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:334fda21d7660dabebf415a7630e82d71c49a482457d86edd5a02adf9ade1164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23592932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97dfff6219d548cae54fee570f6f3b37ac16ff0e9424df4cfe959bcf9b715512`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:24:06 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:24:58 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Wed, 28 Jan 2026 03:24:58 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"         "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     tar -xvf "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz"         -C / --strip-components 1 --wildcards             'influxdb-*/usr/bin/influxd-ctl'             'influxdb-*/usr/bin/influxd-meta' &&     rm "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"        "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 03:24:58 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Wed, 28 Jan 2026 03:24:58 GMT
EXPOSE map[8091/tcp:{}]
# Wed, 28 Jan 2026 03:24:58 GMT
VOLUME [/var/lib/influxdb]
# Wed, 28 Jan 2026 03:24:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:24:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:24:58 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adc499747d2c1716d5193ed87e0f6684b5f7da3ad6b0d2bdfc84d65ed106d36`  
		Last Modified: Wed, 28 Jan 2026 03:24:21 GMT  
		Size: 1.2 MB (1225465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bdedda1ccaa8c658e38e6dd03b7ae881fe041e412d88964c2eeb69cacaa9d72`  
		Last Modified: Wed, 28 Jan 2026 03:25:05 GMT  
		Size: 18.7 MB (18723159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c532d4cfc611beb0d944a9d3a0ecb4f69dfd08641f9c026a71b9183ba72aeb`  
		Last Modified: Wed, 28 Jan 2026 03:25:04 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0374a0e06643bd5572653262d38d90caf085dff084fc64403ebb1555477ec00e`  
		Last Modified: Wed, 28 Jan 2026 03:25:05 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:627437226023c906b3c6b7de5bce011926f537ee0fa9a386d09b87721cc83460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **695.9 KB (695917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987b431e9e9fe1201a9d3d2a53cbb79bad12a66fe71f7caaa35c13d123e4b70f`

```dockerfile
```

-	Layers:
	-	`sha256:6969b9ff35276f6935e71043cc1ec394f9218dd77481815cd0b8d155f1a4a451`  
		Last Modified: Wed, 28 Jan 2026 03:25:04 GMT  
		Size: 682.1 KB (682071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d790fe636454d04353dbcafa3c3eb838b08379bec575783d2659976da7381a07`  
		Last Modified: Wed, 28 Jan 2026 03:25:04 GMT  
		Size: 13.8 KB (13846 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12.2`

```console
$ docker pull influxdb@sha256:f3afe89c4dc35f146be3ea51c5dedd656c254a9add1ae07eeadca3515029e9fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.12.2` - linux; amd64

```console
$ docker pull influxdb@sha256:6917c61f7b7985f4ee4f962f70470841a7f407ba70bc0265d7165fae33f0237d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.9 MB (113854585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaa7fc75a9556b81328dc3e6283b047adab59d448dc7fd1fc564917a8df739c7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:01:32 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 13 Jan 2026 04:01:39 GMT
ARG INFLUXDB_VERSION=1.12.2
# Tue, 13 Jan 2026 04:01:39 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:01:39 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 13 Jan 2026 04:01:39 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 13 Jan 2026 04:01:39 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Jan 2026 04:01:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 04:01:39 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 13 Jan 2026 04:01:39 GMT
USER influxdb
# Tue, 13 Jan 2026 04:01:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 04:01:39 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:15 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64538a062a61add8dc8b290fa69475e8902eb839c497a5f5dcd5a950422e493c`  
		Last Modified: Tue, 13 Jan 2026 02:09:00 GMT  
		Size: 24.0 MB (24036867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c22b05fa882dbbd60440b09a3ec476ebe474cfda3f322e86ea99a39773311ff`  
		Last Modified: Tue, 13 Jan 2026 04:01:52 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095de93a216193ad71ad56a36c80d3a1f63af494f8902a1813bb1c4dfa0b4154`  
		Last Modified: Tue, 13 Jan 2026 04:01:53 GMT  
		Size: 41.3 MB (41333184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090738da3a915b0cc95274040b43fc1908bec3499fd47aa8a111af60fe706ff5`  
		Last Modified: Tue, 13 Jan 2026 04:01:52 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a939c63c8c824c090a62a1de1e4d53b256966ad574511bcab52c98624386f4`  
		Last Modified: Tue, 13 Jan 2026 04:01:52 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b12a0f18a42fce4393789e9c7988aa7c323463de50edd44e9bfdbf54c645517`  
		Last Modified: Tue, 13 Jan 2026 04:01:53 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2` - unknown; unknown

```console
$ docker pull influxdb@sha256:13980e20fb6e543b9dcc1eeee545e0d8fe3f62f29f0acc073063e5bfb4c3e9c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4692912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d14bd9b0fe140f81efb9caba62a6357953e030b7955e0056d17e2ec0ac7545f`

```dockerfile
```

-	Layers:
	-	`sha256:10380ebb8bbb2eccfa008e53390f65b9c8802135c15975af4b5f4d9cd2a7bc13`  
		Last Modified: Tue, 13 Jan 2026 04:01:52 GMT  
		Size: 4.7 MB (4676456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54c700714a2269c9a3a2cca268e744abb97bc1e3143b40e6812d8ed1b70a67c1`  
		Last Modified: Tue, 13 Jan 2026 04:01:52 GMT  
		Size: 16.5 KB (16456 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.12.2` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:9a2002e3287172532d89974ca043b0c46c8f4767ec681d4f8d02ed223775eafc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110110739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3bb24c68ad0344728ae758051895414b4adb8a39ab42006eaa32c336a19513`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:12:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:05:12 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 13 Jan 2026 04:05:18 GMT
ARG INFLUXDB_VERSION=1.12.2
# Tue, 13 Jan 2026 04:05:18 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:05:18 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 13 Jan 2026 04:05:18 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 13 Jan 2026 04:05:18 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Jan 2026 04:05:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 04:05:18 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 13 Jan 2026 04:05:18 GMT
USER influxdb
# Tue, 13 Jan 2026 04:05:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 04:05:18 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:14 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72c713ab317dd7f302a6ff5a345af5b61cddc864fca2d96a23e6ef3c90a6657`  
		Last Modified: Tue, 13 Jan 2026 02:12:45 GMT  
		Size: 23.6 MB (23604814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32711d9c6895fb4667fedd16e8277c5c89718586b3637e933bba65e2679be49d`  
		Last Modified: Tue, 13 Jan 2026 04:05:33 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2128fdd094a63cf7cc6275615289a80c9a482b4be8e1660f09b6643846a1c5c`  
		Last Modified: Tue, 13 Jan 2026 04:05:35 GMT  
		Size: 38.1 MB (38136943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a02bbdfec69d3b4321b6643a7949f4cb795ef901faeef0fadb8934f1a6578d7`  
		Last Modified: Tue, 13 Jan 2026 04:05:33 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547c0dc17c88c1cac835a1f7bbe1c0a8b7a4decd7893434b122de77e4a311cbb`  
		Last Modified: Tue, 13 Jan 2026 04:05:33 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44c2d7d11424c30bcb720acc76e1451af022c394c98bc9848ecd7ec5d7e35ad`  
		Last Modified: Tue, 13 Jan 2026 04:05:35 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2` - unknown; unknown

```console
$ docker pull influxdb@sha256:7c69b1070116ae9939b524b2267b4698ac77e72c88210b8035c026a40fbe45f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4692465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55276b8e215debe8243590e8486a973cd66458ff1318527ae5f6404c49b04014`

```dockerfile
```

-	Layers:
	-	`sha256:36b5c1ecb3646c63822a8cf440a84b5715a76637b080cf479735e45fca7a34ef`  
		Last Modified: Tue, 13 Jan 2026 04:05:34 GMT  
		Size: 4.7 MB (4675914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5535ab390cd8e5f3d81737bc4a15dabffbbb67fa983a0cc4c4693d1a41ef21c6`  
		Last Modified: Tue, 13 Jan 2026 04:05:33 GMT  
		Size: 16.6 KB (16551 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12.2-alpine`

```console
$ docker pull influxdb@sha256:1ed16e0f6a44ab61a30357566845efbb9757556851e6ff97227f939bf9ef9ace
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.12.2-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:697aba0e3c65d5d7bd8c0165468ba9ee24657f504bb4366fece150b28f019a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46124218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb897a5f792495e87d9871b6a4cfc773bd6606d7bc580daf4ff262360e9c04d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:23:21 GMT
RUN apk add --no-cache bash ca-certificates tzdata &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:23:26 GMT
ARG INFLUXDB_VERSION=1.12.2
# Wed, 28 Jan 2026 03:23:26 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     case "$(apk --print-arch)" in         x86_64)  ARCH=amd64 ;;         aarch64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar -xvf "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz"         -C / --strip-components 1 --wildcards             'influxdb-*/usr/bin/influx'             'influxdb-*/usr/bin/influx_inspect'             'influxdb-*/usr/bin/influxd' &&     rm "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"        "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 03:23:26 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 28 Jan 2026 03:23:26 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Wed, 28 Jan 2026 03:23:26 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 Jan 2026 03:23:26 GMT
VOLUME [/var/lib/influxdb]
# Wed, 28 Jan 2026 03:23:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:23:26 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 28 Jan 2026 03:23:26 GMT
USER influxdb
# Wed, 28 Jan 2026 03:23:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:23:26 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61ad874caf1ce155d9c06c85c089035ff4b41fea8f68219cb60604fecea628f`  
		Last Modified: Wed, 28 Jan 2026 03:23:36 GMT  
		Size: 1.2 MB (1225476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f59042c15009bf41c0b1fa6c4d2d2d13d0250f49e1409fb7b663adc462759b`  
		Last Modified: Wed, 28 Jan 2026 03:23:37 GMT  
		Size: 41.3 MB (41252292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed17935cb0b9555361ea5defc075520b1cdccd69d5a58d7e269415bee692cee`  
		Last Modified: Wed, 28 Jan 2026 03:23:36 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d76182047c6a6ca57e871f8736596a2ae48b8a3c50277aedeeb7987a622c6f`  
		Last Modified: Wed, 28 Jan 2026 03:23:36 GMT  
		Size: 994.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4fb1c6df23e845268a733a445e5db0893ba7589591cadeabba1bdf3adf782c`  
		Last Modified: Wed, 28 Jan 2026 03:23:37 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ba8b159859dfc44049e5332e08c60d8b36b38fc5e1d118748fe8e3e1543924`  
		Last Modified: Wed, 28 Jan 2026 03:23:37 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:af2b5dd8ad0d3b16b3907ff491d74d1f2eff068de322e7489c77bd75466cd8a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **780.5 KB (780479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51dc09838f56b2799381d5dd1c3400f40ea2244acca53eabafae485097494bf9`

```dockerfile
```

-	Layers:
	-	`sha256:f39e15f06b57000511387e30703a81694cd535187db4291a2e8f5bcefece88a6`  
		Last Modified: Wed, 28 Jan 2026 03:23:36 GMT  
		Size: 761.9 KB (761859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9426c81519fa2e633147ad49e1850cde661e950ff86aefd90f840a0cd91d5c96`  
		Last Modified: Wed, 28 Jan 2026 03:23:36 GMT  
		Size: 18.6 KB (18620 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.12.2-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:a15f5bc8b2ce1d70a31b981c371a1ddd88c6fc05c655c7e01b57eecaf60fbbd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.3 MB (43343070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4654f5bc4db16a713150f336f9aac2a58bc3dfb28052ad26fdc2db98f8d1d717`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:07 GMT
ADD alpine-minirootfs-3.21.6-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:07 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:15:34 GMT
RUN apk add --no-cache bash ca-certificates tzdata &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:15:40 GMT
ARG INFLUXDB_VERSION=1.12.2
# Wed, 28 Jan 2026 03:15:40 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     case "$(apk --print-arch)" in         x86_64)  ARCH=amd64 ;;         aarch64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar -xvf "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz"         -C / --strip-components 1 --wildcards             'influxdb-*/usr/bin/influx'             'influxdb-*/usr/bin/influx_inspect'             'influxdb-*/usr/bin/influxd' &&     rm "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"        "influxdb-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 03:15:40 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 28 Jan 2026 03:15:40 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Wed, 28 Jan 2026 03:15:40 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 Jan 2026 03:15:40 GMT
VOLUME [/var/lib/influxdb]
# Wed, 28 Jan 2026 03:15:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:15:40 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 28 Jan 2026 03:15:40 GMT
USER influxdb
# Wed, 28 Jan 2026 03:15:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:15:40 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:a447a5de8f4eb4a987d81c0afa14d459cc714599c020c08f45fafa9c6c904b30`  
		Last Modified: Wed, 28 Jan 2026 01:18:13 GMT  
		Size: 4.0 MB (3992880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad49504157754b82690dc411a4cbb1be979c94a1504554cc7508eb53848d9aaa`  
		Last Modified: Wed, 28 Jan 2026 03:15:50 GMT  
		Size: 1.3 MB (1290781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5d1cb0eb9bcf36e7b5a1a4000c5aece49077b899de952de6fdbd89c9c1f44b`  
		Last Modified: Wed, 28 Jan 2026 03:15:51 GMT  
		Size: 38.1 MB (38056702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1137d619a385938b5d7d7306b62a613a6dbb383adfd1ec3a55ce047164213cd1`  
		Last Modified: Wed, 28 Jan 2026 03:15:49 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef4649756164c4e09b5e20f42da696b65fd206aa9a9e69d940360af42044b28`  
		Last Modified: Wed, 28 Jan 2026 03:15:49 GMT  
		Size: 993.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1622ae5fef1f8a1581c49244f92707dde2199a2db553408fb31beec7b70b181e`  
		Last Modified: Wed, 28 Jan 2026 03:15:50 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946d050ae0ebead10e2f4ab1c542a8b9ddf94d0784aa98106e5c9bd7dbd02631`  
		Last Modified: Wed, 28 Jan 2026 03:15:51 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:edfd9ff1eb419bbf315b4102159bb5d501769546111a9c02e7e64d25684fa482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **779.8 KB (779816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08bd24f011bd6bdf62cee047d5433e2b6dba99042b7d6c09aa052a11bb91f17f`

```dockerfile
```

-	Layers:
	-	`sha256:a51c507fdc8870eba3993722731f2c5c18c27320de1587e98a2662a90b734787`  
		Last Modified: Wed, 28 Jan 2026 03:15:49 GMT  
		Size: 761.1 KB (761088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94d21d56468ffa602372ea8026b8acdae37f5ee8aab4afbb5aeda345db5c31f9`  
		Last Modified: Wed, 28 Jan 2026 03:15:49 GMT  
		Size: 18.7 KB (18728 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12.2-data`

```console
$ docker pull influxdb@sha256:be4700d7692b8a727eb6cc5f1c32c7ebe704bdac03d39a06e16fc86e8006e65b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12.2-data` - linux; amd64

```console
$ docker pull influxdb@sha256:d1ec024b86aa737221977a5040dc3b66815147f5741819488120fc87a6c9580f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114840077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77eee634dfccb1cbf60ff3500a7cdd422b7fe57ac29c0834e043952fe5171695`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:01:52 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Tue, 13 Jan 2026 04:01:52 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"         "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     rm -r "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"           "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:01:52 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 13 Jan 2026 04:01:52 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 13 Jan 2026 04:01:52 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Jan 2026 04:01:52 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 04:01:52 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 13 Jan 2026 04:01:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 04:01:52 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:15 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64538a062a61add8dc8b290fa69475e8902eb839c497a5f5dcd5a950422e493c`  
		Last Modified: Tue, 13 Jan 2026 02:09:00 GMT  
		Size: 24.0 MB (24036867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66c83e9d2d95ae7bb8cae9f8b46bff3d99ebbbdce310b651807fcd051a37ba0`  
		Last Modified: Tue, 13 Jan 2026 04:02:06 GMT  
		Size: 42.3 MB (42319809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485ded8552cc8df9c3417e10f8333c7f5f414f71250ce6145d55fc4b15698edd`  
		Last Modified: Tue, 13 Jan 2026 04:02:05 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3948a1f32b313d88999deaa596d64ebb9423cb1c3aa9be6cfe4be40e635ac3`  
		Last Modified: Tue, 13 Jan 2026 04:02:05 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18ad3cf56c36afce2bd43874b271d452c70a98b369b3108ea1a68c2d1093e92`  
		Last Modified: Tue, 13 Jan 2026 04:02:05 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:4be6b6094085a1d6722283c42c361a38cfcfa77db9f25275413122a8aa260d88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4700469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb24414afd5c068a73d4ec08d1a75579ed8094de9c7f4d21bb46345a51a6b924`

```dockerfile
```

-	Layers:
	-	`sha256:5dfa793211611cb151c8c0f1f35f084eae3bb9a6d3793a1c3e8de1ff7a66a120`  
		Last Modified: Tue, 13 Jan 2026 04:02:05 GMT  
		Size: 4.7 MB (4686392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:593d647c6647a10283a9515111c55e17f9854ceede24aefe8268425e17a1497a`  
		Last Modified: Tue, 13 Jan 2026 04:02:04 GMT  
		Size: 14.1 KB (14077 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12.2-data-alpine`

```console
$ docker pull influxdb@sha256:230aced0d72a917905c28e8370266348fb49894a4e1d090c47765a1488e94bff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12.2-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:40d2fef5a316bf72ec0b29c322a7cf01fbd7046fad6e09edef3afd6a2a51f192
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47123756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8324e71acc24adb0423f7eb4de13354493b40f765bdb36448d77ce375caa87c3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:24:06 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:24:11 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Wed, 28 Jan 2026 03:24:11 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"         "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     tar -xvf "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz"         -C / --strip-components 1 --wildcards             'influxdb-*/usr/bin/influx'             'influxdb-*/usr/bin/influx_inspect'             'influxdb-*/usr/bin/influxd' &&     rm "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"        "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 03:24:11 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 28 Jan 2026 03:24:11 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 Jan 2026 03:24:11 GMT
VOLUME [/var/lib/influxdb]
# Wed, 28 Jan 2026 03:24:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:24:11 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 28 Jan 2026 03:24:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:24:11 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adc499747d2c1716d5193ed87e0f6684b5f7da3ad6b0d2bdfc84d65ed106d36`  
		Last Modified: Wed, 28 Jan 2026 03:24:21 GMT  
		Size: 1.2 MB (1225465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a172153dcef0bec4a9c7bb4c587f4400c9485a79c347dec788239589954f4770`  
		Last Modified: Wed, 28 Jan 2026 03:24:22 GMT  
		Size: 42.3 MB (42252778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b330c6f2273441c4cece26de32b1b56b5641f92928b4b5256a15fd7ef0db1a6`  
		Last Modified: Wed, 28 Jan 2026 03:24:21 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb3efac6bd9c420eddfe57595ec744fa728401020c9af575cb9cdbe12776f5f`  
		Last Modified: Wed, 28 Jan 2026 03:24:21 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1f1384e53b8afac073280a7d6b42b05cfeb3ad8ff3c328242a61d8f88d4018`  
		Last Modified: Wed, 28 Jan 2026 03:24:22 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:fff49aac562db0793d72005156712fb335c4f0488b91b3f35e434498d2e282a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **791.6 KB (791580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05cbe541688ac6e58740d2ecbecb6eaa4446654bb8c3635d47c1614319c2135d`

```dockerfile
```

-	Layers:
	-	`sha256:7746afe39499c0509347119e90a393e2f741f8c2e4a54628af8774335219ffeb`  
		Last Modified: Wed, 28 Jan 2026 03:24:21 GMT  
		Size: 776.1 KB (776122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a10bcf68f284ed3ad3af63a4766b3825d0a6fb102c1dc2b1199ddd247f8f9cef`  
		Last Modified: Wed, 28 Jan 2026 03:24:21 GMT  
		Size: 15.5 KB (15458 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12.2-meta`

```console
$ docker pull influxdb@sha256:5eb24e671873d2663ef0c00ebde2c425db825a47e36f9a93b19dd18752354a0d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12.2-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:9ec905fa99e678b7a46d0f8e84f7cbdcad71b5f480e6e7c398e5eaa965ac6e20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91299873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a552f12602ad1bedee2244e93fed92a53903cba13ca8b81e04d628e2c85a4228`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:01:51 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Tue, 13 Jan 2026 04:01:51 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"         "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     rm -r "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"           "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:01:51 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 13 Jan 2026 04:01:51 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 13 Jan 2026 04:01:51 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Jan 2026 04:01:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 04:01:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 04:01:51 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:15 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64538a062a61add8dc8b290fa69475e8902eb839c497a5f5dcd5a950422e493c`  
		Last Modified: Tue, 13 Jan 2026 02:09:00 GMT  
		Size: 24.0 MB (24036867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8226584456c231e3329e2f781db217386df170900017ccf5ad54f649f3a4892`  
		Last Modified: Tue, 13 Jan 2026 04:02:01 GMT  
		Size: 18.8 MB (18780819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61622d86659aed4ba8f4ef77c6784a2201f76664031c14b2cfc4382d1fad188c`  
		Last Modified: Tue, 13 Jan 2026 04:02:00 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91888eb7d9961fd828a172be924f04fc445944a4a20a7c1b5d0cdba26ca1429`  
		Last Modified: Tue, 13 Jan 2026 04:02:01 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:fc34f0e0037afbb0dd07c5569c82c110b8ee9270e8a27fd45a0f0ff815adbade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4604146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05bf3ef5c6c6a490e1a87aeeee4ccd065070ed262594888f4ab79e55e3e7df88`

```dockerfile
```

-	Layers:
	-	`sha256:ef9b998d76c6a317d3d028cff8c5607da4ac015da97d036c8556b540b4eed402`  
		Last Modified: Tue, 13 Jan 2026 04:02:01 GMT  
		Size: 4.6 MB (4591555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90bcc4be344b12d86469f9015e7e36c92c0e18c887c79c28a6183d38f7a71dc1`  
		Last Modified: Tue, 13 Jan 2026 04:02:00 GMT  
		Size: 12.6 KB (12591 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12.2-meta-alpine`

```console
$ docker pull influxdb@sha256:aecaf75c0592866bc0a7c2639bb83f72193dda8ca322e9434210831a02a4857a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12.2-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:334fda21d7660dabebf415a7630e82d71c49a482457d86edd5a02adf9ade1164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23592932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97dfff6219d548cae54fee570f6f3b37ac16ff0e9424df4cfe959bcf9b715512`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:24:06 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:24:58 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Wed, 28 Jan 2026 03:24:58 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"         "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     tar -xvf "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz"         -C / --strip-components 1 --wildcards             'influxdb-*/usr/bin/influxd-ctl'             'influxdb-*/usr/bin/influxd-meta' &&     rm "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"        "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 03:24:58 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Wed, 28 Jan 2026 03:24:58 GMT
EXPOSE map[8091/tcp:{}]
# Wed, 28 Jan 2026 03:24:58 GMT
VOLUME [/var/lib/influxdb]
# Wed, 28 Jan 2026 03:24:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:24:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:24:58 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adc499747d2c1716d5193ed87e0f6684b5f7da3ad6b0d2bdfc84d65ed106d36`  
		Last Modified: Wed, 28 Jan 2026 03:24:21 GMT  
		Size: 1.2 MB (1225465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bdedda1ccaa8c658e38e6dd03b7ae881fe041e412d88964c2eeb69cacaa9d72`  
		Last Modified: Wed, 28 Jan 2026 03:25:05 GMT  
		Size: 18.7 MB (18723159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c532d4cfc611beb0d944a9d3a0ecb4f69dfd08641f9c026a71b9183ba72aeb`  
		Last Modified: Wed, 28 Jan 2026 03:25:04 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0374a0e06643bd5572653262d38d90caf085dff084fc64403ebb1555477ec00e`  
		Last Modified: Wed, 28 Jan 2026 03:25:05 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:627437226023c906b3c6b7de5bce011926f537ee0fa9a386d09b87721cc83460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **695.9 KB (695917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987b431e9e9fe1201a9d3d2a53cbb79bad12a66fe71f7caaa35c13d123e4b70f`

```dockerfile
```

-	Layers:
	-	`sha256:6969b9ff35276f6935e71043cc1ec394f9218dd77481815cd0b8d155f1a4a451`  
		Last Modified: Wed, 28 Jan 2026 03:25:04 GMT  
		Size: 682.1 KB (682071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d790fe636454d04353dbcafa3c3eb838b08379bec575783d2659976da7381a07`  
		Last Modified: Wed, 28 Jan 2026 03:25:04 GMT  
		Size: 13.8 KB (13846 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2`

```console
$ docker pull influxdb@sha256:47d5ee97ca868e0d669db8ec37bdb72373d11a1fdd16e6ee712447a865d4d119
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2` - linux; amd64

```console
$ docker pull influxdb@sha256:fbbbb123e62858a14dc1f0b2f146640b7aee3f83b8e3e8d16706ea2a0961223d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107232235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8b79bd46f3ad2285f42e7222b0061406c2d3443d0ee0d1dbc18b9e6e238e4f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:27:12 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:27:12 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 13 Jan 2026 02:27:12 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 13 Jan 2026 02:27:14 GMT
ENV GOSU_VER=1.19
# Tue, 13 Jan 2026 02:27:14 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 13 Jan 2026 02:27:14 GMT
ENV INFLUXDB_VERSION=2.8.0
# Tue, 13 Jan 2026 02:27:14 GMT
ENV INFLUXDB_PR=-2
# Tue, 13 Jan 2026 02:27:14 GMT
ENV INFLUXDB_PV=2.8.0-2
# Tue, 13 Jan 2026 02:27:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 13 Jan 2026 02:27:18 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 13 Jan 2026 02:27:19 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 13 Jan 2026 02:27:19 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 13 Jan 2026 02:27:19 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 13 Jan 2026 02:27:19 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 13 Jan 2026 02:27:19 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 02:27:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 02:27:19 GMT
CMD ["influxd"]
# Tue, 13 Jan 2026 02:27:19 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 13 Jan 2026 02:27:19 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 13 Jan 2026 02:27:19 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 13 Jan 2026 02:27:19 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 13 Jan 2026 02:27:19 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dcddc3d3c23c1c56b07e1355ca795cd4e1fd6a750e12250b364a39908314603`  
		Last Modified: Tue, 13 Jan 2026 02:27:31 GMT  
		Size: 9.8 MB (9797566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69611437006e7e5d57518505b16149f02d6de08bb4fd641a35b57ff9538e7019`  
		Last Modified: Tue, 13 Jan 2026 02:27:31 GMT  
		Size: 6.2 MB (6156960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c709ee61b6d0aa5181b6f1bd280d67fb9c9c47f750adaeb54071159645ed361`  
		Last Modified: Tue, 13 Jan 2026 02:27:30 GMT  
		Size: 3.2 KB (3222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac01bb46173c8f94318c49396692514d025f567953e9c10e9861bcd55cbaae7`  
		Last Modified: Tue, 13 Jan 2026 02:27:31 GMT  
		Size: 811.5 KB (811477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7f5e8c960d80d311f115d887a80722c31f9018ba0067431f173e26de26051e`  
		Last Modified: Tue, 13 Jan 2026 02:27:33 GMT  
		Size: 50.5 MB (50451829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99ba881f7de4d8bf0add7733db05bf697e3ace7f5cffc314be099705f02ea79`  
		Last Modified: Tue, 13 Jan 2026 02:27:33 GMT  
		Size: 11.8 MB (11775880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeac49fa47842b0d7d0dc90119df9ea3676af835768d021a2069c65930300b22`  
		Last Modified: Tue, 13 Jan 2026 02:27:33 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a223dfcf1aa0f4fbeddf0e9fa404d2c2e4b6a2d3c2e7322e8a17944a7e78db49`  
		Last Modified: Tue, 13 Jan 2026 02:27:33 GMT  
		Size: 235.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e10ef99f06088a71bab9bbf3532907e25691b3728cdf97a2d8169e4dc90fa6`  
		Last Modified: Tue, 13 Jan 2026 02:27:34 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:28a7ecfc57c3de3aa44548980c3ef7dd74b7ee294cc9f0994710c794f950d9bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:608bef8307d19f25a454085edc672001fc860618884e40fdcffa437a205d03a0`

```dockerfile
```

-	Layers:
	-	`sha256:6de1637cff31caef959bd3292964ba38d361879667a8db6c0102bb53b202d6ea`  
		Last Modified: Tue, 13 Jan 2026 02:27:31 GMT  
		Size: 2.9 MB (2934237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5351d7eccf2ca31733a58fd915c8306fe6c56d099cacb0cd37cfb83eb801a79c`  
		Last Modified: Tue, 13 Jan 2026 02:27:31 GMT  
		Size: 33.6 KB (33621 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:a9256736de2e2596be881fbb2b62224cbd49865cf97aee4d784f56ba728f5052
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103631551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e041a58a0f2da6742d7ddd660fcb4524980ee351e3046bf0036ea534511843`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:29:35 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:29:36 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 13 Jan 2026 02:29:36 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 13 Jan 2026 02:30:48 GMT
ENV GOSU_VER=1.19
# Tue, 13 Jan 2026 02:30:48 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 13 Jan 2026 02:30:48 GMT
ENV INFLUXDB_VERSION=2.8.0
# Tue, 13 Jan 2026 02:30:48 GMT
ENV INFLUXDB_PR=-2
# Tue, 13 Jan 2026 02:30:48 GMT
ENV INFLUXDB_PV=2.8.0-2
# Tue, 13 Jan 2026 02:30:52 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 13 Jan 2026 02:30:52 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 13 Jan 2026 02:30:53 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 13 Jan 2026 02:30:53 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 13 Jan 2026 02:30:53 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 13 Jan 2026 02:30:53 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 13 Jan 2026 02:30:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 02:30:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 02:30:53 GMT
CMD ["influxd"]
# Tue, 13 Jan 2026 02:30:53 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 13 Jan 2026 02:30:53 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 13 Jan 2026 02:30:53 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 13 Jan 2026 02:30:53 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 13 Jan 2026 02:30:53 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff72e9f0d8c78a6aaa8d48cd6cbe9ae48d8da7536f200e4be1224b028abec803`  
		Last Modified: Tue, 13 Jan 2026 02:29:57 GMT  
		Size: 9.6 MB (9626944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3248cb6f7828f084a214ae8053bb4436f265efa780f883e495a508b864e7510a`  
		Last Modified: Tue, 13 Jan 2026 02:29:57 GMT  
		Size: 5.8 MB (5790415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd971a07829912a852596669fe5089a772f917e244ce57921e1296659f61c45`  
		Last Modified: Tue, 13 Jan 2026 02:29:57 GMT  
		Size: 3.2 KB (3228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0cd106ca7e593dcab49c86754e35bd79b48a1d3007438049e89614659564b5`  
		Last Modified: Tue, 13 Jan 2026 02:31:03 GMT  
		Size: 766.4 KB (766370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53a3a9efe7fd59838f76f744fc33e7b7848a8077bf8e265caf35bf5d731caa4`  
		Last Modified: Tue, 13 Jan 2026 02:31:05 GMT  
		Size: 48.2 MB (48229552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68b008dfe291566d50ddf5c7020299a3060b1d20c79012275b130b78a36b807`  
		Last Modified: Tue, 13 Jan 2026 02:31:04 GMT  
		Size: 11.1 MB (11100424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4e2ae9c66b1fec75a22ff096205beb69e7b188d5500259b911d01e597dd96b`  
		Last Modified: Tue, 13 Jan 2026 02:31:03 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda15609a2fc5f59147422f52e5939c25b23cc4c2c60cbda90d140c87e221ae2`  
		Last Modified: Tue, 13 Jan 2026 02:31:04 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfb8e20ecdd7ab27d51281c854cb806d337db33b27147ad8a379c1c40f8ffad`  
		Last Modified: Tue, 13 Jan 2026 02:31:05 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:8ce104bbae7ace138e9444b0f394ca033069f1e6c54b28661c9c4705c9a56ce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6906ffeb91245c75565f0400dc5303d54f04391d8cfc6aec374c069265b9014b`

```dockerfile
```

-	Layers:
	-	`sha256:47cb60b1b3f39493774cf7056e3a9b3cf2d90c19a28bbb9a3bb641ee28e3fe80`  
		Last Modified: Tue, 13 Jan 2026 02:31:03 GMT  
		Size: 2.9 MB (2933717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12eb99a3526a426649d9677b3db7da8c00a4a9079eafcb7355e98aec58817018`  
		Last Modified: Tue, 13 Jan 2026 02:31:03 GMT  
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
$ docker pull influxdb@sha256:04145304bf1166b372476360b3f5a077ef04ad9f4651ece2570930d1988fb3e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7` - linux; amd64

```console
$ docker pull influxdb@sha256:4c4039b79bcb59e047d675aed9509b3abdd63caa4ade29e4596361fa3f0d9951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157227169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc931f62260d90df0e3ab93e43013b732929e2d8653b15da94339892ec612d1d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:25:29 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:25:29 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 13 Jan 2026 02:25:30 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 13 Jan 2026 02:25:32 GMT
ENV GOSU_VER=1.16
# Tue, 13 Jan 2026 02:25:32 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 13 Jan 2026 02:25:32 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 13 Jan 2026 02:25:35 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 13 Jan 2026 02:25:35 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 13 Jan 2026 02:25:36 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 13 Jan 2026 02:25:36 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 13 Jan 2026 02:25:36 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 13 Jan 2026 02:25:36 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 13 Jan 2026 02:25:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 02:25:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 02:25:36 GMT
CMD ["influxd"]
# Tue, 13 Jan 2026 02:25:36 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 13 Jan 2026 02:25:36 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 13 Jan 2026 02:25:36 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 13 Jan 2026 02:25:36 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 13 Jan 2026 02:25:36 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d33cd1ee483afd415e8718435719246598e9763df03230e0111102030e0b30`  
		Last Modified: Tue, 13 Jan 2026 02:25:51 GMT  
		Size: 9.8 MB (9797608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a51431b46e084a15ff007a34fecd48d3e7195b270136e58beffb5c3aa1788e2`  
		Last Modified: Tue, 13 Jan 2026 02:25:51 GMT  
		Size: 6.2 MB (6156948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833535523fe14972a499abd06da9a931c255b921d8cac94598fd45eba9762e79`  
		Last Modified: Tue, 13 Jan 2026 02:25:51 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332c159a27a1da2abbe5673bdaaae5ec4032a5c5001b11062a629daa347497ad`  
		Last Modified: Tue, 13 Jan 2026 02:25:51 GMT  
		Size: 1.0 MB (1012039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db699770bd0f83d68f705e2711254edb50a46ab3d57d0b6a36fadb9d6db2a6a`  
		Last Modified: Tue, 13 Jan 2026 02:25:55 GMT  
		Size: 100.2 MB (100246167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9534ab686709ee0ac5e10282ab4858eb110757e635e51655e7afc130532e92c9`  
		Last Modified: Tue, 13 Jan 2026 02:25:53 GMT  
		Size: 11.8 MB (11775886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c657c3cd1a492fd3d596b28e8112ae5d564f9f4136d3ae71cf923ee8f692ab9d`  
		Last Modified: Tue, 13 Jan 2026 02:25:53 GMT  
		Size: 207.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777d2808f71e7a654cbefb59a369679c79dddbaa1045293b793b32936cba08d6`  
		Last Modified: Tue, 13 Jan 2026 02:25:53 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e70b88d2be0f67826728e054ad05b2eec09fb666ac2086e45d3b43f020cb25`  
		Last Modified: Tue, 13 Jan 2026 02:25:54 GMT  
		Size: 6.3 KB (6284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:af6e1f89810b1f669e4ac0a52fbf4f7bedeaf4fa3f058dc1d02f748b9e4928df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3014385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bf58263ee95eb770d8c3cb42ac1aa0941bf77e04e973d5d8025d7b1cafe32ad`

```dockerfile
```

-	Layers:
	-	`sha256:5826ca4565fb666986bc12b4ca20afec53a6adb39f9bebdf3f6c16c506c979da`  
		Last Modified: Tue, 13 Jan 2026 02:25:51 GMT  
		Size: 3.0 MB (2981484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd4b7b41ef097635ebe81bfd09d63def06a891de3750e73911644724ca524236`  
		Last Modified: Tue, 13 Jan 2026 02:25:51 GMT  
		Size: 32.9 KB (32901 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:a9b791d75c9a850e0833194f9a7fc05d9a4ee66d50c371518ff328c2f0e98bf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151616191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:601e9dc01e870cc99cf93a993a91af30283c3db18202534280adf3fc0fa8304e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:29:35 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:29:36 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 13 Jan 2026 02:29:36 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 13 Jan 2026 02:29:38 GMT
ENV GOSU_VER=1.16
# Tue, 13 Jan 2026 02:29:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 13 Jan 2026 02:29:38 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 13 Jan 2026 02:29:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 13 Jan 2026 02:29:41 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 13 Jan 2026 02:29:42 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 13 Jan 2026 02:29:42 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 13 Jan 2026 02:29:42 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 13 Jan 2026 02:29:42 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 13 Jan 2026 02:29:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 02:29:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 02:29:42 GMT
CMD ["influxd"]
# Tue, 13 Jan 2026 02:29:42 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 13 Jan 2026 02:29:42 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 13 Jan 2026 02:29:42 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 13 Jan 2026 02:29:42 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 13 Jan 2026 02:29:42 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff72e9f0d8c78a6aaa8d48cd6cbe9ae48d8da7536f200e4be1224b028abec803`  
		Last Modified: Tue, 13 Jan 2026 02:29:57 GMT  
		Size: 9.6 MB (9626944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3248cb6f7828f084a214ae8053bb4436f265efa780f883e495a508b864e7510a`  
		Last Modified: Tue, 13 Jan 2026 02:29:57 GMT  
		Size: 5.8 MB (5790415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd971a07829912a852596669fe5089a772f917e244ce57921e1296659f61c45`  
		Last Modified: Tue, 13 Jan 2026 02:29:57 GMT  
		Size: 3.2 KB (3228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc242a33f501041765cea896670bfe19085f61cbe1072b7c975d47ef46477ab`  
		Last Modified: Tue, 13 Jan 2026 02:29:57 GMT  
		Size: 938.9 KB (938877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907845f7a4c6550859ec77329810dccfe6e013e5130ff40fa5a80a4a21424943`  
		Last Modified: Tue, 13 Jan 2026 02:30:01 GMT  
		Size: 96.0 MB (96041726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b8d55e3a2731c65ad178e0976341eaba8019e957fa61cb2a949b8274ff333a`  
		Last Modified: Tue, 13 Jan 2026 02:29:59 GMT  
		Size: 11.1 MB (11100385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b27d2ff162212e313a199c6085e72e0066d54afa10a2348b46cf9315a8f55b7`  
		Last Modified: Tue, 13 Jan 2026 02:29:59 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b377c1318942bc3a9d9573fb5c1e71f81aa4a87016356d5166bd1a184324b5c5`  
		Last Modified: Tue, 13 Jan 2026 02:29:59 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fe7c7cbaa7a85a5f52487deba1494326bfd479121521028d9adc3d675a48be`  
		Last Modified: Tue, 13 Jan 2026 02:30:00 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:64225db0a7da812715a0fc4d8f8eaebbcaa56fc32c99f7571a4d33abd06205db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3013748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc446d5bdd43f7c7ecc1255970a012474c586c731cfa7be300b31230670797ac`

```dockerfile
```

-	Layers:
	-	`sha256:561aeaff019d3dd0d9abb07c0a646c57b506975bb3718cd924de97d6be0d03e3`  
		Last Modified: Tue, 13 Jan 2026 02:29:57 GMT  
		Size: 3.0 MB (2980688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc16ee2543a777bc76cc1cf7ff12d22d945fcf6589e92df997e2893618926e22`  
		Last Modified: Tue, 13 Jan 2026 02:29:57 GMT  
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
$ docker pull influxdb@sha256:04145304bf1166b372476360b3f5a077ef04ad9f4651ece2570930d1988fb3e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.12` - linux; amd64

```console
$ docker pull influxdb@sha256:4c4039b79bcb59e047d675aed9509b3abdd63caa4ade29e4596361fa3f0d9951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157227169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc931f62260d90df0e3ab93e43013b732929e2d8653b15da94339892ec612d1d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:25:29 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:25:29 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 13 Jan 2026 02:25:30 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 13 Jan 2026 02:25:32 GMT
ENV GOSU_VER=1.16
# Tue, 13 Jan 2026 02:25:32 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 13 Jan 2026 02:25:32 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 13 Jan 2026 02:25:35 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 13 Jan 2026 02:25:35 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 13 Jan 2026 02:25:36 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 13 Jan 2026 02:25:36 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 13 Jan 2026 02:25:36 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 13 Jan 2026 02:25:36 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 13 Jan 2026 02:25:36 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 02:25:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 02:25:36 GMT
CMD ["influxd"]
# Tue, 13 Jan 2026 02:25:36 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 13 Jan 2026 02:25:36 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 13 Jan 2026 02:25:36 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 13 Jan 2026 02:25:36 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 13 Jan 2026 02:25:36 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d33cd1ee483afd415e8718435719246598e9763df03230e0111102030e0b30`  
		Last Modified: Tue, 13 Jan 2026 02:25:51 GMT  
		Size: 9.8 MB (9797608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a51431b46e084a15ff007a34fecd48d3e7195b270136e58beffb5c3aa1788e2`  
		Last Modified: Tue, 13 Jan 2026 02:25:51 GMT  
		Size: 6.2 MB (6156948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833535523fe14972a499abd06da9a931c255b921d8cac94598fd45eba9762e79`  
		Last Modified: Tue, 13 Jan 2026 02:25:51 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332c159a27a1da2abbe5673bdaaae5ec4032a5c5001b11062a629daa347497ad`  
		Last Modified: Tue, 13 Jan 2026 02:25:51 GMT  
		Size: 1.0 MB (1012039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db699770bd0f83d68f705e2711254edb50a46ab3d57d0b6a36fadb9d6db2a6a`  
		Last Modified: Tue, 13 Jan 2026 02:25:55 GMT  
		Size: 100.2 MB (100246167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9534ab686709ee0ac5e10282ab4858eb110757e635e51655e7afc130532e92c9`  
		Last Modified: Tue, 13 Jan 2026 02:25:53 GMT  
		Size: 11.8 MB (11775886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c657c3cd1a492fd3d596b28e8112ae5d564f9f4136d3ae71cf923ee8f692ab9d`  
		Last Modified: Tue, 13 Jan 2026 02:25:53 GMT  
		Size: 207.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777d2808f71e7a654cbefb59a369679c79dddbaa1045293b793b32936cba08d6`  
		Last Modified: Tue, 13 Jan 2026 02:25:53 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e70b88d2be0f67826728e054ad05b2eec09fb666ac2086e45d3b43f020cb25`  
		Last Modified: Tue, 13 Jan 2026 02:25:54 GMT  
		Size: 6.3 KB (6284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:af6e1f89810b1f669e4ac0a52fbf4f7bedeaf4fa3f058dc1d02f748b9e4928df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3014385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bf58263ee95eb770d8c3cb42ac1aa0941bf77e04e973d5d8025d7b1cafe32ad`

```dockerfile
```

-	Layers:
	-	`sha256:5826ca4565fb666986bc12b4ca20afec53a6adb39f9bebdf3f6c16c506c979da`  
		Last Modified: Tue, 13 Jan 2026 02:25:51 GMT  
		Size: 3.0 MB (2981484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd4b7b41ef097635ebe81bfd09d63def06a891de3750e73911644724ca524236`  
		Last Modified: Tue, 13 Jan 2026 02:25:51 GMT  
		Size: 32.9 KB (32901 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7.12` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:a9b791d75c9a850e0833194f9a7fc05d9a4ee66d50c371518ff328c2f0e98bf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151616191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:601e9dc01e870cc99cf93a993a91af30283c3db18202534280adf3fc0fa8304e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:29:35 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:29:36 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 13 Jan 2026 02:29:36 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 13 Jan 2026 02:29:38 GMT
ENV GOSU_VER=1.16
# Tue, 13 Jan 2026 02:29:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 13 Jan 2026 02:29:38 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 13 Jan 2026 02:29:41 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 13 Jan 2026 02:29:41 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 13 Jan 2026 02:29:42 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 13 Jan 2026 02:29:42 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 13 Jan 2026 02:29:42 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 13 Jan 2026 02:29:42 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 13 Jan 2026 02:29:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 02:29:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 02:29:42 GMT
CMD ["influxd"]
# Tue, 13 Jan 2026 02:29:42 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 13 Jan 2026 02:29:42 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 13 Jan 2026 02:29:42 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 13 Jan 2026 02:29:42 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 13 Jan 2026 02:29:42 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff72e9f0d8c78a6aaa8d48cd6cbe9ae48d8da7536f200e4be1224b028abec803`  
		Last Modified: Tue, 13 Jan 2026 02:29:57 GMT  
		Size: 9.6 MB (9626944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3248cb6f7828f084a214ae8053bb4436f265efa780f883e495a508b864e7510a`  
		Last Modified: Tue, 13 Jan 2026 02:29:57 GMT  
		Size: 5.8 MB (5790415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd971a07829912a852596669fe5089a772f917e244ce57921e1296659f61c45`  
		Last Modified: Tue, 13 Jan 2026 02:29:57 GMT  
		Size: 3.2 KB (3228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc242a33f501041765cea896670bfe19085f61cbe1072b7c975d47ef46477ab`  
		Last Modified: Tue, 13 Jan 2026 02:29:57 GMT  
		Size: 938.9 KB (938877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907845f7a4c6550859ec77329810dccfe6e013e5130ff40fa5a80a4a21424943`  
		Last Modified: Tue, 13 Jan 2026 02:30:01 GMT  
		Size: 96.0 MB (96041726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b8d55e3a2731c65ad178e0976341eaba8019e957fa61cb2a949b8274ff333a`  
		Last Modified: Tue, 13 Jan 2026 02:29:59 GMT  
		Size: 11.1 MB (11100385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b27d2ff162212e313a199c6085e72e0066d54afa10a2348b46cf9315a8f55b7`  
		Last Modified: Tue, 13 Jan 2026 02:29:59 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b377c1318942bc3a9d9573fb5c1e71f81aa4a87016356d5166bd1a184324b5c5`  
		Last Modified: Tue, 13 Jan 2026 02:29:59 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fe7c7cbaa7a85a5f52487deba1494326bfd479121521028d9adc3d675a48be`  
		Last Modified: Tue, 13 Jan 2026 02:30:00 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:64225db0a7da812715a0fc4d8f8eaebbcaa56fc32c99f7571a4d33abd06205db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3013748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc446d5bdd43f7c7ecc1255970a012474c586c731cfa7be300b31230670797ac`

```dockerfile
```

-	Layers:
	-	`sha256:561aeaff019d3dd0d9abb07c0a646c57b506975bb3718cd924de97d6be0d03e3`  
		Last Modified: Tue, 13 Jan 2026 02:29:57 GMT  
		Size: 3.0 MB (2980688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc16ee2543a777bc76cc1cf7ff12d22d945fcf6589e92df997e2893618926e22`  
		Last Modified: Tue, 13 Jan 2026 02:29:57 GMT  
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
$ docker pull influxdb@sha256:47d5ee97ca868e0d669db8ec37bdb72373d11a1fdd16e6ee712447a865d4d119
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.8` - linux; amd64

```console
$ docker pull influxdb@sha256:fbbbb123e62858a14dc1f0b2f146640b7aee3f83b8e3e8d16706ea2a0961223d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107232235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8b79bd46f3ad2285f42e7222b0061406c2d3443d0ee0d1dbc18b9e6e238e4f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:27:12 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:27:12 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 13 Jan 2026 02:27:12 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 13 Jan 2026 02:27:14 GMT
ENV GOSU_VER=1.19
# Tue, 13 Jan 2026 02:27:14 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 13 Jan 2026 02:27:14 GMT
ENV INFLUXDB_VERSION=2.8.0
# Tue, 13 Jan 2026 02:27:14 GMT
ENV INFLUXDB_PR=-2
# Tue, 13 Jan 2026 02:27:14 GMT
ENV INFLUXDB_PV=2.8.0-2
# Tue, 13 Jan 2026 02:27:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 13 Jan 2026 02:27:18 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 13 Jan 2026 02:27:19 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 13 Jan 2026 02:27:19 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 13 Jan 2026 02:27:19 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 13 Jan 2026 02:27:19 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 13 Jan 2026 02:27:19 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 02:27:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 02:27:19 GMT
CMD ["influxd"]
# Tue, 13 Jan 2026 02:27:19 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 13 Jan 2026 02:27:19 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 13 Jan 2026 02:27:19 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 13 Jan 2026 02:27:19 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 13 Jan 2026 02:27:19 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dcddc3d3c23c1c56b07e1355ca795cd4e1fd6a750e12250b364a39908314603`  
		Last Modified: Tue, 13 Jan 2026 02:27:31 GMT  
		Size: 9.8 MB (9797566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69611437006e7e5d57518505b16149f02d6de08bb4fd641a35b57ff9538e7019`  
		Last Modified: Tue, 13 Jan 2026 02:27:31 GMT  
		Size: 6.2 MB (6156960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c709ee61b6d0aa5181b6f1bd280d67fb9c9c47f750adaeb54071159645ed361`  
		Last Modified: Tue, 13 Jan 2026 02:27:30 GMT  
		Size: 3.2 KB (3222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac01bb46173c8f94318c49396692514d025f567953e9c10e9861bcd55cbaae7`  
		Last Modified: Tue, 13 Jan 2026 02:27:31 GMT  
		Size: 811.5 KB (811477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7f5e8c960d80d311f115d887a80722c31f9018ba0067431f173e26de26051e`  
		Last Modified: Tue, 13 Jan 2026 02:27:33 GMT  
		Size: 50.5 MB (50451829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99ba881f7de4d8bf0add7733db05bf697e3ace7f5cffc314be099705f02ea79`  
		Last Modified: Tue, 13 Jan 2026 02:27:33 GMT  
		Size: 11.8 MB (11775880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeac49fa47842b0d7d0dc90119df9ea3676af835768d021a2069c65930300b22`  
		Last Modified: Tue, 13 Jan 2026 02:27:33 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a223dfcf1aa0f4fbeddf0e9fa404d2c2e4b6a2d3c2e7322e8a17944a7e78db49`  
		Last Modified: Tue, 13 Jan 2026 02:27:33 GMT  
		Size: 235.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e10ef99f06088a71bab9bbf3532907e25691b3728cdf97a2d8169e4dc90fa6`  
		Last Modified: Tue, 13 Jan 2026 02:27:34 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:28a7ecfc57c3de3aa44548980c3ef7dd74b7ee294cc9f0994710c794f950d9bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:608bef8307d19f25a454085edc672001fc860618884e40fdcffa437a205d03a0`

```dockerfile
```

-	Layers:
	-	`sha256:6de1637cff31caef959bd3292964ba38d361879667a8db6c0102bb53b202d6ea`  
		Last Modified: Tue, 13 Jan 2026 02:27:31 GMT  
		Size: 2.9 MB (2934237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5351d7eccf2ca31733a58fd915c8306fe6c56d099cacb0cd37cfb83eb801a79c`  
		Last Modified: Tue, 13 Jan 2026 02:27:31 GMT  
		Size: 33.6 KB (33621 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:a9256736de2e2596be881fbb2b62224cbd49865cf97aee4d784f56ba728f5052
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103631551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e041a58a0f2da6742d7ddd660fcb4524980ee351e3046bf0036ea534511843`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:29:35 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:29:36 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 13 Jan 2026 02:29:36 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 13 Jan 2026 02:30:48 GMT
ENV GOSU_VER=1.19
# Tue, 13 Jan 2026 02:30:48 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 13 Jan 2026 02:30:48 GMT
ENV INFLUXDB_VERSION=2.8.0
# Tue, 13 Jan 2026 02:30:48 GMT
ENV INFLUXDB_PR=-2
# Tue, 13 Jan 2026 02:30:48 GMT
ENV INFLUXDB_PV=2.8.0-2
# Tue, 13 Jan 2026 02:30:52 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 13 Jan 2026 02:30:52 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 13 Jan 2026 02:30:53 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 13 Jan 2026 02:30:53 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 13 Jan 2026 02:30:53 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 13 Jan 2026 02:30:53 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 13 Jan 2026 02:30:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 02:30:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 02:30:53 GMT
CMD ["influxd"]
# Tue, 13 Jan 2026 02:30:53 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 13 Jan 2026 02:30:53 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 13 Jan 2026 02:30:53 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 13 Jan 2026 02:30:53 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 13 Jan 2026 02:30:53 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff72e9f0d8c78a6aaa8d48cd6cbe9ae48d8da7536f200e4be1224b028abec803`  
		Last Modified: Tue, 13 Jan 2026 02:29:57 GMT  
		Size: 9.6 MB (9626944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3248cb6f7828f084a214ae8053bb4436f265efa780f883e495a508b864e7510a`  
		Last Modified: Tue, 13 Jan 2026 02:29:57 GMT  
		Size: 5.8 MB (5790415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd971a07829912a852596669fe5089a772f917e244ce57921e1296659f61c45`  
		Last Modified: Tue, 13 Jan 2026 02:29:57 GMT  
		Size: 3.2 KB (3228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0cd106ca7e593dcab49c86754e35bd79b48a1d3007438049e89614659564b5`  
		Last Modified: Tue, 13 Jan 2026 02:31:03 GMT  
		Size: 766.4 KB (766370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53a3a9efe7fd59838f76f744fc33e7b7848a8077bf8e265caf35bf5d731caa4`  
		Last Modified: Tue, 13 Jan 2026 02:31:05 GMT  
		Size: 48.2 MB (48229552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68b008dfe291566d50ddf5c7020299a3060b1d20c79012275b130b78a36b807`  
		Last Modified: Tue, 13 Jan 2026 02:31:04 GMT  
		Size: 11.1 MB (11100424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4e2ae9c66b1fec75a22ff096205beb69e7b188d5500259b911d01e597dd96b`  
		Last Modified: Tue, 13 Jan 2026 02:31:03 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda15609a2fc5f59147422f52e5939c25b23cc4c2c60cbda90d140c87e221ae2`  
		Last Modified: Tue, 13 Jan 2026 02:31:04 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfb8e20ecdd7ab27d51281c854cb806d337db33b27147ad8a379c1c40f8ffad`  
		Last Modified: Tue, 13 Jan 2026 02:31:05 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:8ce104bbae7ace138e9444b0f394ca033069f1e6c54b28661c9c4705c9a56ce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6906ffeb91245c75565f0400dc5303d54f04391d8cfc6aec374c069265b9014b`

```dockerfile
```

-	Layers:
	-	`sha256:47cb60b1b3f39493774cf7056e3a9b3cf2d90c19a28bbb9a3bb641ee28e3fe80`  
		Last Modified: Tue, 13 Jan 2026 02:31:03 GMT  
		Size: 2.9 MB (2933717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12eb99a3526a426649d9677b3db7da8c00a4a9079eafcb7355e98aec58817018`  
		Last Modified: Tue, 13 Jan 2026 02:31:03 GMT  
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
$ docker pull influxdb@sha256:47d5ee97ca868e0d669db8ec37bdb72373d11a1fdd16e6ee712447a865d4d119
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.8.0` - linux; amd64

```console
$ docker pull influxdb@sha256:fbbbb123e62858a14dc1f0b2f146640b7aee3f83b8e3e8d16706ea2a0961223d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107232235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8b79bd46f3ad2285f42e7222b0061406c2d3443d0ee0d1dbc18b9e6e238e4f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:27:12 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:27:12 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 13 Jan 2026 02:27:12 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 13 Jan 2026 02:27:14 GMT
ENV GOSU_VER=1.19
# Tue, 13 Jan 2026 02:27:14 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 13 Jan 2026 02:27:14 GMT
ENV INFLUXDB_VERSION=2.8.0
# Tue, 13 Jan 2026 02:27:14 GMT
ENV INFLUXDB_PR=-2
# Tue, 13 Jan 2026 02:27:14 GMT
ENV INFLUXDB_PV=2.8.0-2
# Tue, 13 Jan 2026 02:27:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 13 Jan 2026 02:27:18 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 13 Jan 2026 02:27:19 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 13 Jan 2026 02:27:19 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 13 Jan 2026 02:27:19 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 13 Jan 2026 02:27:19 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 13 Jan 2026 02:27:19 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 02:27:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 02:27:19 GMT
CMD ["influxd"]
# Tue, 13 Jan 2026 02:27:19 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 13 Jan 2026 02:27:19 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 13 Jan 2026 02:27:19 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 13 Jan 2026 02:27:19 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 13 Jan 2026 02:27:19 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dcddc3d3c23c1c56b07e1355ca795cd4e1fd6a750e12250b364a39908314603`  
		Last Modified: Tue, 13 Jan 2026 02:27:31 GMT  
		Size: 9.8 MB (9797566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69611437006e7e5d57518505b16149f02d6de08bb4fd641a35b57ff9538e7019`  
		Last Modified: Tue, 13 Jan 2026 02:27:31 GMT  
		Size: 6.2 MB (6156960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c709ee61b6d0aa5181b6f1bd280d67fb9c9c47f750adaeb54071159645ed361`  
		Last Modified: Tue, 13 Jan 2026 02:27:30 GMT  
		Size: 3.2 KB (3222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac01bb46173c8f94318c49396692514d025f567953e9c10e9861bcd55cbaae7`  
		Last Modified: Tue, 13 Jan 2026 02:27:31 GMT  
		Size: 811.5 KB (811477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7f5e8c960d80d311f115d887a80722c31f9018ba0067431f173e26de26051e`  
		Last Modified: Tue, 13 Jan 2026 02:27:33 GMT  
		Size: 50.5 MB (50451829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99ba881f7de4d8bf0add7733db05bf697e3ace7f5cffc314be099705f02ea79`  
		Last Modified: Tue, 13 Jan 2026 02:27:33 GMT  
		Size: 11.8 MB (11775880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeac49fa47842b0d7d0dc90119df9ea3676af835768d021a2069c65930300b22`  
		Last Modified: Tue, 13 Jan 2026 02:27:33 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a223dfcf1aa0f4fbeddf0e9fa404d2c2e4b6a2d3c2e7322e8a17944a7e78db49`  
		Last Modified: Tue, 13 Jan 2026 02:27:33 GMT  
		Size: 235.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e10ef99f06088a71bab9bbf3532907e25691b3728cdf97a2d8169e4dc90fa6`  
		Last Modified: Tue, 13 Jan 2026 02:27:34 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8.0` - unknown; unknown

```console
$ docker pull influxdb@sha256:28a7ecfc57c3de3aa44548980c3ef7dd74b7ee294cc9f0994710c794f950d9bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:608bef8307d19f25a454085edc672001fc860618884e40fdcffa437a205d03a0`

```dockerfile
```

-	Layers:
	-	`sha256:6de1637cff31caef959bd3292964ba38d361879667a8db6c0102bb53b202d6ea`  
		Last Modified: Tue, 13 Jan 2026 02:27:31 GMT  
		Size: 2.9 MB (2934237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5351d7eccf2ca31733a58fd915c8306fe6c56d099cacb0cd37cfb83eb801a79c`  
		Last Modified: Tue, 13 Jan 2026 02:27:31 GMT  
		Size: 33.6 KB (33621 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.8.0` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:a9256736de2e2596be881fbb2b62224cbd49865cf97aee4d784f56ba728f5052
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103631551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e041a58a0f2da6742d7ddd660fcb4524980ee351e3046bf0036ea534511843`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:29:35 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:29:36 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 13 Jan 2026 02:29:36 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 13 Jan 2026 02:30:48 GMT
ENV GOSU_VER=1.19
# Tue, 13 Jan 2026 02:30:48 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 13 Jan 2026 02:30:48 GMT
ENV INFLUXDB_VERSION=2.8.0
# Tue, 13 Jan 2026 02:30:48 GMT
ENV INFLUXDB_PR=-2
# Tue, 13 Jan 2026 02:30:48 GMT
ENV INFLUXDB_PV=2.8.0-2
# Tue, 13 Jan 2026 02:30:52 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 13 Jan 2026 02:30:52 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 13 Jan 2026 02:30:53 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 13 Jan 2026 02:30:53 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 13 Jan 2026 02:30:53 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 13 Jan 2026 02:30:53 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 13 Jan 2026 02:30:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 02:30:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 02:30:53 GMT
CMD ["influxd"]
# Tue, 13 Jan 2026 02:30:53 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 13 Jan 2026 02:30:53 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 13 Jan 2026 02:30:53 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 13 Jan 2026 02:30:53 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 13 Jan 2026 02:30:53 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff72e9f0d8c78a6aaa8d48cd6cbe9ae48d8da7536f200e4be1224b028abec803`  
		Last Modified: Tue, 13 Jan 2026 02:29:57 GMT  
		Size: 9.6 MB (9626944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3248cb6f7828f084a214ae8053bb4436f265efa780f883e495a508b864e7510a`  
		Last Modified: Tue, 13 Jan 2026 02:29:57 GMT  
		Size: 5.8 MB (5790415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd971a07829912a852596669fe5089a772f917e244ce57921e1296659f61c45`  
		Last Modified: Tue, 13 Jan 2026 02:29:57 GMT  
		Size: 3.2 KB (3228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0cd106ca7e593dcab49c86754e35bd79b48a1d3007438049e89614659564b5`  
		Last Modified: Tue, 13 Jan 2026 02:31:03 GMT  
		Size: 766.4 KB (766370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53a3a9efe7fd59838f76f744fc33e7b7848a8077bf8e265caf35bf5d731caa4`  
		Last Modified: Tue, 13 Jan 2026 02:31:05 GMT  
		Size: 48.2 MB (48229552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68b008dfe291566d50ddf5c7020299a3060b1d20c79012275b130b78a36b807`  
		Last Modified: Tue, 13 Jan 2026 02:31:04 GMT  
		Size: 11.1 MB (11100424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4e2ae9c66b1fec75a22ff096205beb69e7b188d5500259b911d01e597dd96b`  
		Last Modified: Tue, 13 Jan 2026 02:31:03 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda15609a2fc5f59147422f52e5939c25b23cc4c2c60cbda90d140c87e221ae2`  
		Last Modified: Tue, 13 Jan 2026 02:31:04 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfb8e20ecdd7ab27d51281c854cb806d337db33b27147ad8a379c1c40f8ffad`  
		Last Modified: Tue, 13 Jan 2026 02:31:05 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8.0` - unknown; unknown

```console
$ docker pull influxdb@sha256:8ce104bbae7ace138e9444b0f394ca033069f1e6c54b28661c9c4705c9a56ce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6906ffeb91245c75565f0400dc5303d54f04391d8cfc6aec374c069265b9014b`

```dockerfile
```

-	Layers:
	-	`sha256:47cb60b1b3f39493774cf7056e3a9b3cf2d90c19a28bbb9a3bb641ee28e3fe80`  
		Last Modified: Tue, 13 Jan 2026 02:31:03 GMT  
		Size: 2.9 MB (2933717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12eb99a3526a426649d9677b3db7da8c00a4a9079eafcb7355e98aec58817018`  
		Last Modified: Tue, 13 Jan 2026 02:31:03 GMT  
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
$ docker pull influxdb@sha256:2757db64af5f331bbfb0e25d6731c8cf65c5a515d027c8bc5a48b258fa008c8b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-core` - linux; amd64

```console
$ docker pull influxdb@sha256:8f36abf47ed33e424b8f9b238694a7bcc082bd0e74d97cec7d6d7c7db47d6552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.3 MB (119311374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f3d35e10e7aed87113e0a46df8b64bf71b7f74180eee35877ee5d6d4b2fab9`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:29:31 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 15 Jan 2026 22:29:31 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 15 Jan 2026 22:29:35 GMT
ENV INFLUXDB_VERSION=3.8.0
# Thu, 15 Jan 2026 22:29:35 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 15 Jan 2026 22:29:35 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:29:35 GMT
USER influxdb3
# Thu, 15 Jan 2026 22:29:35 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 15 Jan 2026 22:29:35 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 15 Jan 2026 22:29:35 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 15 Jan 2026 22:29:35 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Thu, 15 Jan 2026 22:29:35 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 15 Jan 2026 22:29:35 GMT
ENV LOG_FILTER=info
# Thu, 15 Jan 2026 22:29:35 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 15 Jan 2026 22:29:35 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 15 Jan 2026 22:29:35 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb421340cf49eb838ba5a93e97c5a79263668d6c63b6e2bdec9f12f9cb2bbe70`  
		Last Modified: Thu, 15 Jan 2026 22:29:50 GMT  
		Size: 6.7 MB (6666455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c5db002efd1716598d0b566d19a173dfe7126f0914b12e1fdc180f8a7a14e2`  
		Last Modified: Thu, 15 Jan 2026 22:29:50 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6bfc81f68fb579269742625ae883af1e68a469bdc3e47f9cb250ea7d67ceeb1`  
		Last Modified: Thu, 15 Jan 2026 22:29:52 GMT  
		Size: 82.9 MB (82914588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e85a99980b8d4fa689879cdc5ef70054bed61905df3549de46260caf0e47d7b`  
		Last Modified: Thu, 15 Jan 2026 22:29:50 GMT  
		Size: 519.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe51c7ce377562ca9379f5ea9def930b1be0d7d2ec4c48e18fb742a156f46361`  
		Last Modified: Thu, 15 Jan 2026 22:29:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:fd004e1dab8b1efc281255b5815cb666fe08ed4498b2c7431f2381b9ac7e4d23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7eb254fbbd5847cc94d322f7ef8c2404eddc14d107a5f050d4e3991237a7e23`

```dockerfile
```

-	Layers:
	-	`sha256:93cae582c7522611a439a6c7a2a6faa7e7b2e6675c9c78f5786ffa27d2d6f7fd`  
		Last Modified: Thu, 15 Jan 2026 22:29:50 GMT  
		Size: 2.3 MB (2310563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb0a5f390a10ab6cf064a1f5fcd498996c18aba1bfb713c33773b1ba72a7f421`  
		Last Modified: Thu, 15 Jan 2026 22:29:50 GMT  
		Size: 17.6 KB (17617 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:87433bdbd8e99019e7fc9dfecda86de557a2fc32b4cffa293bc27efb05d6ef27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (110028972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e1d2cc20717830f048ed113983a79ebf82d22879f31666972296654e226055e`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:31:35 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 15 Jan 2026 22:31:35 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 15 Jan 2026 22:31:39 GMT
ENV INFLUXDB_VERSION=3.8.0
# Thu, 15 Jan 2026 22:31:39 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 15 Jan 2026 22:31:39 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:31:39 GMT
USER influxdb3
# Thu, 15 Jan 2026 22:31:39 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 15 Jan 2026 22:31:39 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 15 Jan 2026 22:31:39 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 15 Jan 2026 22:31:39 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Thu, 15 Jan 2026 22:31:39 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 15 Jan 2026 22:31:39 GMT
ENV LOG_FILTER=info
# Thu, 15 Jan 2026 22:31:39 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 15 Jan 2026 22:31:39 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 15 Jan 2026 22:31:39 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b85d29ef9d1a5b609c04250a98480155038f067e295c06a12bb03a0b163bcb6`  
		Last Modified: Thu, 15 Jan 2026 22:31:53 GMT  
		Size: 6.7 MB (6678025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12879279037976dcf03bcb89fd8ca0258ae28a49fd3fca4e1d918ebf5f58334d`  
		Last Modified: Thu, 15 Jan 2026 22:31:52 GMT  
		Size: 3.6 KB (3648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08f5a1efb52cbac7d7d853d373b78cb1ba1da5dfb15cf3b70ff94110acc1144`  
		Last Modified: Thu, 15 Jan 2026 22:31:54 GMT  
		Size: 74.5 MB (74482805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a655526e5e0376a0214f1b43fa2b17d9d392ec41f8cdc1cb75eb970f43d84d48`  
		Last Modified: Thu, 15 Jan 2026 22:31:52 GMT  
		Size: 521.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff65ff8d1ea9fed765acd863744a83581bdc65244d1022c09ce2991a129a056`  
		Last Modified: Thu, 15 Jan 2026 22:31:54 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:92a66a28c2cacf75f73de64fbc20b8f8a5872763b614692db0f69f380c2ce7ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:910fae9c7c765bca133a238b5b06f22cea8258cae915a0bcf97be00ba26d6b24`

```dockerfile
```

-	Layers:
	-	`sha256:e39d496af0bf62266e9b9be68acf22ce4ea001066b55cf8ed24f202031f749c2`  
		Last Modified: Thu, 15 Jan 2026 22:31:52 GMT  
		Size: 2.3 MB (2311645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50900617900957d671f02b3d04cb4b737068c8a4c247e6954ab2762edcfedfae`  
		Last Modified: Thu, 15 Jan 2026 22:31:52 GMT  
		Size: 17.8 KB (17766 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3-enterprise`

```console
$ docker pull influxdb@sha256:10d40128d7fb12259a57cee239c5dc600f99ab6ddb5d08d7e6bd072fa68011ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:6f80d482e72e674d39ff987c9339b71f28341e6a98a6f358a9086f9fe7745051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127592285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df6d7e2d453e9995658fa8751f2b6e84a64212eeee685595977f5ff7e512afd5`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:29:53 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 15 Jan 2026 22:29:53 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 15 Jan 2026 22:29:58 GMT
ENV INFLUXDB_VERSION=3.8.0
# Thu, 15 Jan 2026 22:29:58 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 15 Jan 2026 22:29:58 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:29:58 GMT
USER influxdb3
# Thu, 15 Jan 2026 22:29:58 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 15 Jan 2026 22:29:58 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 15 Jan 2026 22:29:58 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 15 Jan 2026 22:29:58 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Thu, 15 Jan 2026 22:29:58 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 15 Jan 2026 22:29:58 GMT
ENV LOG_FILTER=info
# Thu, 15 Jan 2026 22:29:58 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 15 Jan 2026 22:29:58 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 15 Jan 2026 22:29:58 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d80b8916ac9be25ca39f63d725fbecdb5221cc992a8f8edc501e20aa7f6cdd`  
		Last Modified: Thu, 15 Jan 2026 22:30:15 GMT  
		Size: 6.7 MB (6666466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86baf47ce3b1fa8c7b1d7b1ba023420e80d040d1a773b90f1a3f1444d5398b8`  
		Last Modified: Thu, 15 Jan 2026 22:30:14 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75782d754446062a195fd74ec4f45355abd9b48844b421553b76d0d92c2e9e6`  
		Last Modified: Thu, 15 Jan 2026 22:30:17 GMT  
		Size: 91.2 MB (91195488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0552eea07c1a62aaa4c8a941aa4d914694ed7a40fa2f205e24255b406514ab`  
		Last Modified: Thu, 15 Jan 2026 22:30:14 GMT  
		Size: 518.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e9ae2043b745909b42322ca040a8bc78dae54020dbf787084712e77c63a890`  
		Last Modified: Thu, 15 Jan 2026 22:30:16 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:cb631e30f9aa3075f21e34d43d947684a1e2cf8b6db12b3870f5925ba45592bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c0859ea2244b0defc0d27a58cd00c57d441a00b51b6c00983526ef8516503d2`

```dockerfile
```

-	Layers:
	-	`sha256:eb1c0fc56bdfe5de760e79c005402e18989d63559ec2f437944b534243db1c91`  
		Last Modified: Thu, 15 Jan 2026 22:30:15 GMT  
		Size: 2.3 MB (2310611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf90cea5e6b638571c01c3c00fe6a8b6e65cbff58a178ba08a0c4a0f3c9fc4d5`  
		Last Modified: Thu, 15 Jan 2026 22:30:14 GMT  
		Size: 17.8 KB (17797 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ad6e83f930d0ab312e7f5a2b347d9b8aa7f6b4132db0409cf404e4bdaa0a67cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118244315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d65a5b3e4ed077bc1ba501bc9ce80427816521ff052532109d778edee858bf2`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:31:56 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 15 Jan 2026 22:31:57 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 15 Jan 2026 22:32:03 GMT
ENV INFLUXDB_VERSION=3.8.0
# Thu, 15 Jan 2026 22:32:03 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 15 Jan 2026 22:32:03 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:32:03 GMT
USER influxdb3
# Thu, 15 Jan 2026 22:32:03 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 15 Jan 2026 22:32:03 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 15 Jan 2026 22:32:03 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 15 Jan 2026 22:32:03 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Thu, 15 Jan 2026 22:32:03 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 15 Jan 2026 22:32:03 GMT
ENV LOG_FILTER=info
# Thu, 15 Jan 2026 22:32:03 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 15 Jan 2026 22:32:03 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 15 Jan 2026 22:32:03 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bd4240eafafe3f7fe3f9bc5d3b023ea3b76cd522bea0a947b3358df8986ed0`  
		Last Modified: Thu, 15 Jan 2026 22:32:18 GMT  
		Size: 6.7 MB (6678021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a2eb424397e2fd233b9e3e45d8e2e2ff184ac156d640257caac83c500bd03b`  
		Last Modified: Thu, 15 Jan 2026 22:32:17 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c9c7ab39edbfbc219f93a01abd342c7aa9ae427a6e3c461e19bc610c55633c`  
		Last Modified: Thu, 15 Jan 2026 22:32:19 GMT  
		Size: 82.7 MB (82698149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124f15f88b8a4272c18117de13ad2ba7f3853d372748c6fea818c9336b9023fb`  
		Last Modified: Thu, 15 Jan 2026 22:32:17 GMT  
		Size: 518.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a262b7c40609324279929b50e3eff0cb9505cd033e5cf2e2dc7a38c8c4e0199d`  
		Last Modified: Thu, 15 Jan 2026 22:32:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:0265bf65e9e0e0e1d1997518bf6b88e6df9698f769f086ef60bbaf2e790d4070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9a5cb8b7911fa2587aea0afc1d4c89be70eb8e24cab810c6172cc216e9d911`

```dockerfile
```

-	Layers:
	-	`sha256:9430335ba47f250a06bcaca7da5899e1461955a18254643114311ddb1acedd5f`  
		Last Modified: Thu, 15 Jan 2026 22:32:17 GMT  
		Size: 2.3 MB (2311693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e36fbb81eb4a33ce5bfce27a827062a0b8d553c1d9ca2e76dc9b865f51041ac`  
		Last Modified: Thu, 15 Jan 2026 22:32:17 GMT  
		Size: 17.9 KB (17946 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.8-core`

```console
$ docker pull influxdb@sha256:2757db64af5f331bbfb0e25d6731c8cf65c5a515d027c8bc5a48b258fa008c8b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.8-core` - linux; amd64

```console
$ docker pull influxdb@sha256:8f36abf47ed33e424b8f9b238694a7bcc082bd0e74d97cec7d6d7c7db47d6552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.3 MB (119311374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f3d35e10e7aed87113e0a46df8b64bf71b7f74180eee35877ee5d6d4b2fab9`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:29:31 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 15 Jan 2026 22:29:31 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 15 Jan 2026 22:29:35 GMT
ENV INFLUXDB_VERSION=3.8.0
# Thu, 15 Jan 2026 22:29:35 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 15 Jan 2026 22:29:35 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:29:35 GMT
USER influxdb3
# Thu, 15 Jan 2026 22:29:35 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 15 Jan 2026 22:29:35 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 15 Jan 2026 22:29:35 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 15 Jan 2026 22:29:35 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Thu, 15 Jan 2026 22:29:35 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 15 Jan 2026 22:29:35 GMT
ENV LOG_FILTER=info
# Thu, 15 Jan 2026 22:29:35 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 15 Jan 2026 22:29:35 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 15 Jan 2026 22:29:35 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb421340cf49eb838ba5a93e97c5a79263668d6c63b6e2bdec9f12f9cb2bbe70`  
		Last Modified: Thu, 15 Jan 2026 22:29:50 GMT  
		Size: 6.7 MB (6666455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c5db002efd1716598d0b566d19a173dfe7126f0914b12e1fdc180f8a7a14e2`  
		Last Modified: Thu, 15 Jan 2026 22:29:50 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6bfc81f68fb579269742625ae883af1e68a469bdc3e47f9cb250ea7d67ceeb1`  
		Last Modified: Thu, 15 Jan 2026 22:29:52 GMT  
		Size: 82.9 MB (82914588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e85a99980b8d4fa689879cdc5ef70054bed61905df3549de46260caf0e47d7b`  
		Last Modified: Thu, 15 Jan 2026 22:29:50 GMT  
		Size: 519.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe51c7ce377562ca9379f5ea9def930b1be0d7d2ec4c48e18fb742a156f46361`  
		Last Modified: Thu, 15 Jan 2026 22:29:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.8-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:fd004e1dab8b1efc281255b5815cb666fe08ed4498b2c7431f2381b9ac7e4d23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7eb254fbbd5847cc94d322f7ef8c2404eddc14d107a5f050d4e3991237a7e23`

```dockerfile
```

-	Layers:
	-	`sha256:93cae582c7522611a439a6c7a2a6faa7e7b2e6675c9c78f5786ffa27d2d6f7fd`  
		Last Modified: Thu, 15 Jan 2026 22:29:50 GMT  
		Size: 2.3 MB (2310563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb0a5f390a10ab6cf064a1f5fcd498996c18aba1bfb713c33773b1ba72a7f421`  
		Last Modified: Thu, 15 Jan 2026 22:29:50 GMT  
		Size: 17.6 KB (17617 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.8-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:87433bdbd8e99019e7fc9dfecda86de557a2fc32b4cffa293bc27efb05d6ef27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (110028972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e1d2cc20717830f048ed113983a79ebf82d22879f31666972296654e226055e`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:31:35 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 15 Jan 2026 22:31:35 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 15 Jan 2026 22:31:39 GMT
ENV INFLUXDB_VERSION=3.8.0
# Thu, 15 Jan 2026 22:31:39 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 15 Jan 2026 22:31:39 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:31:39 GMT
USER influxdb3
# Thu, 15 Jan 2026 22:31:39 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 15 Jan 2026 22:31:39 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 15 Jan 2026 22:31:39 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 15 Jan 2026 22:31:39 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Thu, 15 Jan 2026 22:31:39 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 15 Jan 2026 22:31:39 GMT
ENV LOG_FILTER=info
# Thu, 15 Jan 2026 22:31:39 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 15 Jan 2026 22:31:39 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 15 Jan 2026 22:31:39 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b85d29ef9d1a5b609c04250a98480155038f067e295c06a12bb03a0b163bcb6`  
		Last Modified: Thu, 15 Jan 2026 22:31:53 GMT  
		Size: 6.7 MB (6678025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12879279037976dcf03bcb89fd8ca0258ae28a49fd3fca4e1d918ebf5f58334d`  
		Last Modified: Thu, 15 Jan 2026 22:31:52 GMT  
		Size: 3.6 KB (3648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08f5a1efb52cbac7d7d853d373b78cb1ba1da5dfb15cf3b70ff94110acc1144`  
		Last Modified: Thu, 15 Jan 2026 22:31:54 GMT  
		Size: 74.5 MB (74482805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a655526e5e0376a0214f1b43fa2b17d9d392ec41f8cdc1cb75eb970f43d84d48`  
		Last Modified: Thu, 15 Jan 2026 22:31:52 GMT  
		Size: 521.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff65ff8d1ea9fed765acd863744a83581bdc65244d1022c09ce2991a129a056`  
		Last Modified: Thu, 15 Jan 2026 22:31:54 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.8-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:92a66a28c2cacf75f73de64fbc20b8f8a5872763b614692db0f69f380c2ce7ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:910fae9c7c765bca133a238b5b06f22cea8258cae915a0bcf97be00ba26d6b24`

```dockerfile
```

-	Layers:
	-	`sha256:e39d496af0bf62266e9b9be68acf22ce4ea001066b55cf8ed24f202031f749c2`  
		Last Modified: Thu, 15 Jan 2026 22:31:52 GMT  
		Size: 2.3 MB (2311645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50900617900957d671f02b3d04cb4b737068c8a4c247e6954ab2762edcfedfae`  
		Last Modified: Thu, 15 Jan 2026 22:31:52 GMT  
		Size: 17.8 KB (17766 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.8-enterprise`

```console
$ docker pull influxdb@sha256:10d40128d7fb12259a57cee239c5dc600f99ab6ddb5d08d7e6bd072fa68011ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.8-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:6f80d482e72e674d39ff987c9339b71f28341e6a98a6f358a9086f9fe7745051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127592285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df6d7e2d453e9995658fa8751f2b6e84a64212eeee685595977f5ff7e512afd5`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:29:53 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 15 Jan 2026 22:29:53 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 15 Jan 2026 22:29:58 GMT
ENV INFLUXDB_VERSION=3.8.0
# Thu, 15 Jan 2026 22:29:58 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 15 Jan 2026 22:29:58 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:29:58 GMT
USER influxdb3
# Thu, 15 Jan 2026 22:29:58 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 15 Jan 2026 22:29:58 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 15 Jan 2026 22:29:58 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 15 Jan 2026 22:29:58 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Thu, 15 Jan 2026 22:29:58 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 15 Jan 2026 22:29:58 GMT
ENV LOG_FILTER=info
# Thu, 15 Jan 2026 22:29:58 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 15 Jan 2026 22:29:58 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 15 Jan 2026 22:29:58 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d80b8916ac9be25ca39f63d725fbecdb5221cc992a8f8edc501e20aa7f6cdd`  
		Last Modified: Thu, 15 Jan 2026 22:30:15 GMT  
		Size: 6.7 MB (6666466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86baf47ce3b1fa8c7b1d7b1ba023420e80d040d1a773b90f1a3f1444d5398b8`  
		Last Modified: Thu, 15 Jan 2026 22:30:14 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75782d754446062a195fd74ec4f45355abd9b48844b421553b76d0d92c2e9e6`  
		Last Modified: Thu, 15 Jan 2026 22:30:17 GMT  
		Size: 91.2 MB (91195488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0552eea07c1a62aaa4c8a941aa4d914694ed7a40fa2f205e24255b406514ab`  
		Last Modified: Thu, 15 Jan 2026 22:30:14 GMT  
		Size: 518.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e9ae2043b745909b42322ca040a8bc78dae54020dbf787084712e77c63a890`  
		Last Modified: Thu, 15 Jan 2026 22:30:16 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.8-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:cb631e30f9aa3075f21e34d43d947684a1e2cf8b6db12b3870f5925ba45592bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c0859ea2244b0defc0d27a58cd00c57d441a00b51b6c00983526ef8516503d2`

```dockerfile
```

-	Layers:
	-	`sha256:eb1c0fc56bdfe5de760e79c005402e18989d63559ec2f437944b534243db1c91`  
		Last Modified: Thu, 15 Jan 2026 22:30:15 GMT  
		Size: 2.3 MB (2310611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf90cea5e6b638571c01c3c00fe6a8b6e65cbff58a178ba08a0c4a0f3c9fc4d5`  
		Last Modified: Thu, 15 Jan 2026 22:30:14 GMT  
		Size: 17.8 KB (17797 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.8-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ad6e83f930d0ab312e7f5a2b347d9b8aa7f6b4132db0409cf404e4bdaa0a67cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118244315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d65a5b3e4ed077bc1ba501bc9ce80427816521ff052532109d778edee858bf2`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:31:56 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 15 Jan 2026 22:31:57 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 15 Jan 2026 22:32:03 GMT
ENV INFLUXDB_VERSION=3.8.0
# Thu, 15 Jan 2026 22:32:03 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 15 Jan 2026 22:32:03 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:32:03 GMT
USER influxdb3
# Thu, 15 Jan 2026 22:32:03 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 15 Jan 2026 22:32:03 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 15 Jan 2026 22:32:03 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 15 Jan 2026 22:32:03 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Thu, 15 Jan 2026 22:32:03 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 15 Jan 2026 22:32:03 GMT
ENV LOG_FILTER=info
# Thu, 15 Jan 2026 22:32:03 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 15 Jan 2026 22:32:03 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 15 Jan 2026 22:32:03 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bd4240eafafe3f7fe3f9bc5d3b023ea3b76cd522bea0a947b3358df8986ed0`  
		Last Modified: Thu, 15 Jan 2026 22:32:18 GMT  
		Size: 6.7 MB (6678021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a2eb424397e2fd233b9e3e45d8e2e2ff184ac156d640257caac83c500bd03b`  
		Last Modified: Thu, 15 Jan 2026 22:32:17 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c9c7ab39edbfbc219f93a01abd342c7aa9ae427a6e3c461e19bc610c55633c`  
		Last Modified: Thu, 15 Jan 2026 22:32:19 GMT  
		Size: 82.7 MB (82698149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124f15f88b8a4272c18117de13ad2ba7f3853d372748c6fea818c9336b9023fb`  
		Last Modified: Thu, 15 Jan 2026 22:32:17 GMT  
		Size: 518.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a262b7c40609324279929b50e3eff0cb9505cd033e5cf2e2dc7a38c8c4e0199d`  
		Last Modified: Thu, 15 Jan 2026 22:32:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.8-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:0265bf65e9e0e0e1d1997518bf6b88e6df9698f769f086ef60bbaf2e790d4070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9a5cb8b7911fa2587aea0afc1d4c89be70eb8e24cab810c6172cc216e9d911`

```dockerfile
```

-	Layers:
	-	`sha256:9430335ba47f250a06bcaca7da5899e1461955a18254643114311ddb1acedd5f`  
		Last Modified: Thu, 15 Jan 2026 22:32:17 GMT  
		Size: 2.3 MB (2311693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e36fbb81eb4a33ce5bfce27a827062a0b8d553c1d9ca2e76dc9b865f51041ac`  
		Last Modified: Thu, 15 Jan 2026 22:32:17 GMT  
		Size: 17.9 KB (17946 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.8.0-core`

```console
$ docker pull influxdb@sha256:2757db64af5f331bbfb0e25d6731c8cf65c5a515d027c8bc5a48b258fa008c8b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.8.0-core` - linux; amd64

```console
$ docker pull influxdb@sha256:8f36abf47ed33e424b8f9b238694a7bcc082bd0e74d97cec7d6d7c7db47d6552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.3 MB (119311374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f3d35e10e7aed87113e0a46df8b64bf71b7f74180eee35877ee5d6d4b2fab9`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:29:31 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 15 Jan 2026 22:29:31 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 15 Jan 2026 22:29:35 GMT
ENV INFLUXDB_VERSION=3.8.0
# Thu, 15 Jan 2026 22:29:35 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 15 Jan 2026 22:29:35 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:29:35 GMT
USER influxdb3
# Thu, 15 Jan 2026 22:29:35 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 15 Jan 2026 22:29:35 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 15 Jan 2026 22:29:35 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 15 Jan 2026 22:29:35 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Thu, 15 Jan 2026 22:29:35 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 15 Jan 2026 22:29:35 GMT
ENV LOG_FILTER=info
# Thu, 15 Jan 2026 22:29:35 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 15 Jan 2026 22:29:35 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 15 Jan 2026 22:29:35 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb421340cf49eb838ba5a93e97c5a79263668d6c63b6e2bdec9f12f9cb2bbe70`  
		Last Modified: Thu, 15 Jan 2026 22:29:50 GMT  
		Size: 6.7 MB (6666455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c5db002efd1716598d0b566d19a173dfe7126f0914b12e1fdc180f8a7a14e2`  
		Last Modified: Thu, 15 Jan 2026 22:29:50 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6bfc81f68fb579269742625ae883af1e68a469bdc3e47f9cb250ea7d67ceeb1`  
		Last Modified: Thu, 15 Jan 2026 22:29:52 GMT  
		Size: 82.9 MB (82914588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e85a99980b8d4fa689879cdc5ef70054bed61905df3549de46260caf0e47d7b`  
		Last Modified: Thu, 15 Jan 2026 22:29:50 GMT  
		Size: 519.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe51c7ce377562ca9379f5ea9def930b1be0d7d2ec4c48e18fb742a156f46361`  
		Last Modified: Thu, 15 Jan 2026 22:29:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.8.0-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:fd004e1dab8b1efc281255b5815cb666fe08ed4498b2c7431f2381b9ac7e4d23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7eb254fbbd5847cc94d322f7ef8c2404eddc14d107a5f050d4e3991237a7e23`

```dockerfile
```

-	Layers:
	-	`sha256:93cae582c7522611a439a6c7a2a6faa7e7b2e6675c9c78f5786ffa27d2d6f7fd`  
		Last Modified: Thu, 15 Jan 2026 22:29:50 GMT  
		Size: 2.3 MB (2310563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb0a5f390a10ab6cf064a1f5fcd498996c18aba1bfb713c33773b1ba72a7f421`  
		Last Modified: Thu, 15 Jan 2026 22:29:50 GMT  
		Size: 17.6 KB (17617 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.8.0-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:87433bdbd8e99019e7fc9dfecda86de557a2fc32b4cffa293bc27efb05d6ef27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (110028972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e1d2cc20717830f048ed113983a79ebf82d22879f31666972296654e226055e`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:31:35 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 15 Jan 2026 22:31:35 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 15 Jan 2026 22:31:39 GMT
ENV INFLUXDB_VERSION=3.8.0
# Thu, 15 Jan 2026 22:31:39 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 15 Jan 2026 22:31:39 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:31:39 GMT
USER influxdb3
# Thu, 15 Jan 2026 22:31:39 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 15 Jan 2026 22:31:39 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 15 Jan 2026 22:31:39 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 15 Jan 2026 22:31:39 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Thu, 15 Jan 2026 22:31:39 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 15 Jan 2026 22:31:39 GMT
ENV LOG_FILTER=info
# Thu, 15 Jan 2026 22:31:39 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 15 Jan 2026 22:31:39 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 15 Jan 2026 22:31:39 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b85d29ef9d1a5b609c04250a98480155038f067e295c06a12bb03a0b163bcb6`  
		Last Modified: Thu, 15 Jan 2026 22:31:53 GMT  
		Size: 6.7 MB (6678025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12879279037976dcf03bcb89fd8ca0258ae28a49fd3fca4e1d918ebf5f58334d`  
		Last Modified: Thu, 15 Jan 2026 22:31:52 GMT  
		Size: 3.6 KB (3648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08f5a1efb52cbac7d7d853d373b78cb1ba1da5dfb15cf3b70ff94110acc1144`  
		Last Modified: Thu, 15 Jan 2026 22:31:54 GMT  
		Size: 74.5 MB (74482805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a655526e5e0376a0214f1b43fa2b17d9d392ec41f8cdc1cb75eb970f43d84d48`  
		Last Modified: Thu, 15 Jan 2026 22:31:52 GMT  
		Size: 521.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff65ff8d1ea9fed765acd863744a83581bdc65244d1022c09ce2991a129a056`  
		Last Modified: Thu, 15 Jan 2026 22:31:54 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.8.0-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:92a66a28c2cacf75f73de64fbc20b8f8a5872763b614692db0f69f380c2ce7ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:910fae9c7c765bca133a238b5b06f22cea8258cae915a0bcf97be00ba26d6b24`

```dockerfile
```

-	Layers:
	-	`sha256:e39d496af0bf62266e9b9be68acf22ce4ea001066b55cf8ed24f202031f749c2`  
		Last Modified: Thu, 15 Jan 2026 22:31:52 GMT  
		Size: 2.3 MB (2311645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50900617900957d671f02b3d04cb4b737068c8a4c247e6954ab2762edcfedfae`  
		Last Modified: Thu, 15 Jan 2026 22:31:52 GMT  
		Size: 17.8 KB (17766 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.8.0-enterprise`

```console
$ docker pull influxdb@sha256:10d40128d7fb12259a57cee239c5dc600f99ab6ddb5d08d7e6bd072fa68011ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.8.0-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:6f80d482e72e674d39ff987c9339b71f28341e6a98a6f358a9086f9fe7745051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127592285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df6d7e2d453e9995658fa8751f2b6e84a64212eeee685595977f5ff7e512afd5`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:29:53 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 15 Jan 2026 22:29:53 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 15 Jan 2026 22:29:58 GMT
ENV INFLUXDB_VERSION=3.8.0
# Thu, 15 Jan 2026 22:29:58 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 15 Jan 2026 22:29:58 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:29:58 GMT
USER influxdb3
# Thu, 15 Jan 2026 22:29:58 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 15 Jan 2026 22:29:58 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 15 Jan 2026 22:29:58 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 15 Jan 2026 22:29:58 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Thu, 15 Jan 2026 22:29:58 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 15 Jan 2026 22:29:58 GMT
ENV LOG_FILTER=info
# Thu, 15 Jan 2026 22:29:58 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 15 Jan 2026 22:29:58 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 15 Jan 2026 22:29:58 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d80b8916ac9be25ca39f63d725fbecdb5221cc992a8f8edc501e20aa7f6cdd`  
		Last Modified: Thu, 15 Jan 2026 22:30:15 GMT  
		Size: 6.7 MB (6666466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86baf47ce3b1fa8c7b1d7b1ba023420e80d040d1a773b90f1a3f1444d5398b8`  
		Last Modified: Thu, 15 Jan 2026 22:30:14 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75782d754446062a195fd74ec4f45355abd9b48844b421553b76d0d92c2e9e6`  
		Last Modified: Thu, 15 Jan 2026 22:30:17 GMT  
		Size: 91.2 MB (91195488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0552eea07c1a62aaa4c8a941aa4d914694ed7a40fa2f205e24255b406514ab`  
		Last Modified: Thu, 15 Jan 2026 22:30:14 GMT  
		Size: 518.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e9ae2043b745909b42322ca040a8bc78dae54020dbf787084712e77c63a890`  
		Last Modified: Thu, 15 Jan 2026 22:30:16 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.8.0-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:cb631e30f9aa3075f21e34d43d947684a1e2cf8b6db12b3870f5925ba45592bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c0859ea2244b0defc0d27a58cd00c57d441a00b51b6c00983526ef8516503d2`

```dockerfile
```

-	Layers:
	-	`sha256:eb1c0fc56bdfe5de760e79c005402e18989d63559ec2f437944b534243db1c91`  
		Last Modified: Thu, 15 Jan 2026 22:30:15 GMT  
		Size: 2.3 MB (2310611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf90cea5e6b638571c01c3c00fe6a8b6e65cbff58a178ba08a0c4a0f3c9fc4d5`  
		Last Modified: Thu, 15 Jan 2026 22:30:14 GMT  
		Size: 17.8 KB (17797 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.8.0-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ad6e83f930d0ab312e7f5a2b347d9b8aa7f6b4132db0409cf404e4bdaa0a67cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118244315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d65a5b3e4ed077bc1ba501bc9ce80427816521ff052532109d778edee858bf2`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:31:56 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 15 Jan 2026 22:31:57 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 15 Jan 2026 22:32:03 GMT
ENV INFLUXDB_VERSION=3.8.0
# Thu, 15 Jan 2026 22:32:03 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 15 Jan 2026 22:32:03 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:32:03 GMT
USER influxdb3
# Thu, 15 Jan 2026 22:32:03 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 15 Jan 2026 22:32:03 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 15 Jan 2026 22:32:03 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 15 Jan 2026 22:32:03 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Thu, 15 Jan 2026 22:32:03 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 15 Jan 2026 22:32:03 GMT
ENV LOG_FILTER=info
# Thu, 15 Jan 2026 22:32:03 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 15 Jan 2026 22:32:03 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 15 Jan 2026 22:32:03 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bd4240eafafe3f7fe3f9bc5d3b023ea3b76cd522bea0a947b3358df8986ed0`  
		Last Modified: Thu, 15 Jan 2026 22:32:18 GMT  
		Size: 6.7 MB (6678021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a2eb424397e2fd233b9e3e45d8e2e2ff184ac156d640257caac83c500bd03b`  
		Last Modified: Thu, 15 Jan 2026 22:32:17 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c9c7ab39edbfbc219f93a01abd342c7aa9ae427a6e3c461e19bc610c55633c`  
		Last Modified: Thu, 15 Jan 2026 22:32:19 GMT  
		Size: 82.7 MB (82698149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124f15f88b8a4272c18117de13ad2ba7f3853d372748c6fea818c9336b9023fb`  
		Last Modified: Thu, 15 Jan 2026 22:32:17 GMT  
		Size: 518.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a262b7c40609324279929b50e3eff0cb9505cd033e5cf2e2dc7a38c8c4e0199d`  
		Last Modified: Thu, 15 Jan 2026 22:32:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.8.0-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:0265bf65e9e0e0e1d1997518bf6b88e6df9698f769f086ef60bbaf2e790d4070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9a5cb8b7911fa2587aea0afc1d4c89be70eb8e24cab810c6172cc216e9d911`

```dockerfile
```

-	Layers:
	-	`sha256:9430335ba47f250a06bcaca7da5899e1461955a18254643114311ddb1acedd5f`  
		Last Modified: Thu, 15 Jan 2026 22:32:17 GMT  
		Size: 2.3 MB (2311693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e36fbb81eb4a33ce5bfce27a827062a0b8d553c1d9ca2e76dc9b865f51041ac`  
		Last Modified: Thu, 15 Jan 2026 22:32:17 GMT  
		Size: 17.9 KB (17946 bytes)  
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
$ docker pull influxdb@sha256:2757db64af5f331bbfb0e25d6731c8cf65c5a515d027c8bc5a48b258fa008c8b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:core` - linux; amd64

```console
$ docker pull influxdb@sha256:8f36abf47ed33e424b8f9b238694a7bcc082bd0e74d97cec7d6d7c7db47d6552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.3 MB (119311374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f3d35e10e7aed87113e0a46df8b64bf71b7f74180eee35877ee5d6d4b2fab9`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:29:31 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 15 Jan 2026 22:29:31 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 15 Jan 2026 22:29:35 GMT
ENV INFLUXDB_VERSION=3.8.0
# Thu, 15 Jan 2026 22:29:35 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 15 Jan 2026 22:29:35 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:29:35 GMT
USER influxdb3
# Thu, 15 Jan 2026 22:29:35 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 15 Jan 2026 22:29:35 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 15 Jan 2026 22:29:35 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 15 Jan 2026 22:29:35 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Thu, 15 Jan 2026 22:29:35 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 15 Jan 2026 22:29:35 GMT
ENV LOG_FILTER=info
# Thu, 15 Jan 2026 22:29:35 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 15 Jan 2026 22:29:35 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 15 Jan 2026 22:29:35 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb421340cf49eb838ba5a93e97c5a79263668d6c63b6e2bdec9f12f9cb2bbe70`  
		Last Modified: Thu, 15 Jan 2026 22:29:50 GMT  
		Size: 6.7 MB (6666455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c5db002efd1716598d0b566d19a173dfe7126f0914b12e1fdc180f8a7a14e2`  
		Last Modified: Thu, 15 Jan 2026 22:29:50 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6bfc81f68fb579269742625ae883af1e68a469bdc3e47f9cb250ea7d67ceeb1`  
		Last Modified: Thu, 15 Jan 2026 22:29:52 GMT  
		Size: 82.9 MB (82914588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e85a99980b8d4fa689879cdc5ef70054bed61905df3549de46260caf0e47d7b`  
		Last Modified: Thu, 15 Jan 2026 22:29:50 GMT  
		Size: 519.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe51c7ce377562ca9379f5ea9def930b1be0d7d2ec4c48e18fb742a156f46361`  
		Last Modified: Thu, 15 Jan 2026 22:29:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:fd004e1dab8b1efc281255b5815cb666fe08ed4498b2c7431f2381b9ac7e4d23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7eb254fbbd5847cc94d322f7ef8c2404eddc14d107a5f050d4e3991237a7e23`

```dockerfile
```

-	Layers:
	-	`sha256:93cae582c7522611a439a6c7a2a6faa7e7b2e6675c9c78f5786ffa27d2d6f7fd`  
		Last Modified: Thu, 15 Jan 2026 22:29:50 GMT  
		Size: 2.3 MB (2310563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb0a5f390a10ab6cf064a1f5fcd498996c18aba1bfb713c33773b1ba72a7f421`  
		Last Modified: Thu, 15 Jan 2026 22:29:50 GMT  
		Size: 17.6 KB (17617 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:87433bdbd8e99019e7fc9dfecda86de557a2fc32b4cffa293bc27efb05d6ef27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (110028972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e1d2cc20717830f048ed113983a79ebf82d22879f31666972296654e226055e`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:31:35 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 15 Jan 2026 22:31:35 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 15 Jan 2026 22:31:39 GMT
ENV INFLUXDB_VERSION=3.8.0
# Thu, 15 Jan 2026 22:31:39 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 15 Jan 2026 22:31:39 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:31:39 GMT
USER influxdb3
# Thu, 15 Jan 2026 22:31:39 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 15 Jan 2026 22:31:39 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 15 Jan 2026 22:31:39 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 15 Jan 2026 22:31:39 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Thu, 15 Jan 2026 22:31:39 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 15 Jan 2026 22:31:39 GMT
ENV LOG_FILTER=info
# Thu, 15 Jan 2026 22:31:39 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 15 Jan 2026 22:31:39 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 15 Jan 2026 22:31:39 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b85d29ef9d1a5b609c04250a98480155038f067e295c06a12bb03a0b163bcb6`  
		Last Modified: Thu, 15 Jan 2026 22:31:53 GMT  
		Size: 6.7 MB (6678025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12879279037976dcf03bcb89fd8ca0258ae28a49fd3fca4e1d918ebf5f58334d`  
		Last Modified: Thu, 15 Jan 2026 22:31:52 GMT  
		Size: 3.6 KB (3648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08f5a1efb52cbac7d7d853d373b78cb1ba1da5dfb15cf3b70ff94110acc1144`  
		Last Modified: Thu, 15 Jan 2026 22:31:54 GMT  
		Size: 74.5 MB (74482805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a655526e5e0376a0214f1b43fa2b17d9d392ec41f8cdc1cb75eb970f43d84d48`  
		Last Modified: Thu, 15 Jan 2026 22:31:52 GMT  
		Size: 521.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff65ff8d1ea9fed765acd863744a83581bdc65244d1022c09ce2991a129a056`  
		Last Modified: Thu, 15 Jan 2026 22:31:54 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:92a66a28c2cacf75f73de64fbc20b8f8a5872763b614692db0f69f380c2ce7ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:910fae9c7c765bca133a238b5b06f22cea8258cae915a0bcf97be00ba26d6b24`

```dockerfile
```

-	Layers:
	-	`sha256:e39d496af0bf62266e9b9be68acf22ce4ea001066b55cf8ed24f202031f749c2`  
		Last Modified: Thu, 15 Jan 2026 22:31:52 GMT  
		Size: 2.3 MB (2311645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50900617900957d671f02b3d04cb4b737068c8a4c247e6954ab2762edcfedfae`  
		Last Modified: Thu, 15 Jan 2026 22:31:52 GMT  
		Size: 17.8 KB (17766 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:data`

```console
$ docker pull influxdb@sha256:be4700d7692b8a727eb6cc5f1c32c7ebe704bdac03d39a06e16fc86e8006e65b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:data` - linux; amd64

```console
$ docker pull influxdb@sha256:d1ec024b86aa737221977a5040dc3b66815147f5741819488120fc87a6c9580f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114840077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77eee634dfccb1cbf60ff3500a7cdd422b7fe57ac29c0834e043952fe5171695`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:01:52 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Tue, 13 Jan 2026 04:01:52 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"         "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     rm -r "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"           "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:01:52 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 13 Jan 2026 04:01:52 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 13 Jan 2026 04:01:52 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Jan 2026 04:01:52 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 04:01:52 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 13 Jan 2026 04:01:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 04:01:52 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:15 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64538a062a61add8dc8b290fa69475e8902eb839c497a5f5dcd5a950422e493c`  
		Last Modified: Tue, 13 Jan 2026 02:09:00 GMT  
		Size: 24.0 MB (24036867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66c83e9d2d95ae7bb8cae9f8b46bff3d99ebbbdce310b651807fcd051a37ba0`  
		Last Modified: Tue, 13 Jan 2026 04:02:06 GMT  
		Size: 42.3 MB (42319809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485ded8552cc8df9c3417e10f8333c7f5f414f71250ce6145d55fc4b15698edd`  
		Last Modified: Tue, 13 Jan 2026 04:02:05 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3948a1f32b313d88999deaa596d64ebb9423cb1c3aa9be6cfe4be40e635ac3`  
		Last Modified: Tue, 13 Jan 2026 04:02:05 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18ad3cf56c36afce2bd43874b271d452c70a98b369b3108ea1a68c2d1093e92`  
		Last Modified: Tue, 13 Jan 2026 04:02:05 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:data` - unknown; unknown

```console
$ docker pull influxdb@sha256:4be6b6094085a1d6722283c42c361a38cfcfa77db9f25275413122a8aa260d88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4700469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb24414afd5c068a73d4ec08d1a75579ed8094de9c7f4d21bb46345a51a6b924`

```dockerfile
```

-	Layers:
	-	`sha256:5dfa793211611cb151c8c0f1f35f084eae3bb9a6d3793a1c3e8de1ff7a66a120`  
		Last Modified: Tue, 13 Jan 2026 04:02:05 GMT  
		Size: 4.7 MB (4686392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:593d647c6647a10283a9515111c55e17f9854ceede24aefe8268425e17a1497a`  
		Last Modified: Tue, 13 Jan 2026 04:02:04 GMT  
		Size: 14.1 KB (14077 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:data-alpine`

```console
$ docker pull influxdb@sha256:230aced0d72a917905c28e8370266348fb49894a4e1d090c47765a1488e94bff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:40d2fef5a316bf72ec0b29c322a7cf01fbd7046fad6e09edef3afd6a2a51f192
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47123756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8324e71acc24adb0423f7eb4de13354493b40f765bdb36448d77ce375caa87c3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:24:06 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:24:11 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Wed, 28 Jan 2026 03:24:11 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"         "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     tar -xvf "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz"         -C / --strip-components 1 --wildcards             'influxdb-*/usr/bin/influx'             'influxdb-*/usr/bin/influx_inspect'             'influxdb-*/usr/bin/influxd' &&     rm "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"        "influxdb-data-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 03:24:11 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Wed, 28 Jan 2026 03:24:11 GMT
EXPOSE map[8086/tcp:{}]
# Wed, 28 Jan 2026 03:24:11 GMT
VOLUME [/var/lib/influxdb]
# Wed, 28 Jan 2026 03:24:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:24:11 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Wed, 28 Jan 2026 03:24:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:24:11 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adc499747d2c1716d5193ed87e0f6684b5f7da3ad6b0d2bdfc84d65ed106d36`  
		Last Modified: Wed, 28 Jan 2026 03:24:21 GMT  
		Size: 1.2 MB (1225465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a172153dcef0bec4a9c7bb4c587f4400c9485a79c347dec788239589954f4770`  
		Last Modified: Wed, 28 Jan 2026 03:24:22 GMT  
		Size: 42.3 MB (42252778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b330c6f2273441c4cece26de32b1b56b5641f92928b4b5256a15fd7ef0db1a6`  
		Last Modified: Wed, 28 Jan 2026 03:24:21 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb3efac6bd9c420eddfe57595ec744fa728401020c9af575cb9cdbe12776f5f`  
		Last Modified: Wed, 28 Jan 2026 03:24:21 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1f1384e53b8afac073280a7d6b42b05cfeb3ad8ff3c328242a61d8f88d4018`  
		Last Modified: Wed, 28 Jan 2026 03:24:22 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:fff49aac562db0793d72005156712fb335c4f0488b91b3f35e434498d2e282a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **791.6 KB (791580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05cbe541688ac6e58740d2ecbecb6eaa4446654bb8c3635d47c1614319c2135d`

```dockerfile
```

-	Layers:
	-	`sha256:7746afe39499c0509347119e90a393e2f741f8c2e4a54628af8774335219ffeb`  
		Last Modified: Wed, 28 Jan 2026 03:24:21 GMT  
		Size: 776.1 KB (776122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a10bcf68f284ed3ad3af63a4766b3825d0a6fb102c1dc2b1199ddd247f8f9cef`  
		Last Modified: Wed, 28 Jan 2026 03:24:21 GMT  
		Size: 15.5 KB (15458 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:enterprise`

```console
$ docker pull influxdb@sha256:10d40128d7fb12259a57cee239c5dc600f99ab6ddb5d08d7e6bd072fa68011ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:6f80d482e72e674d39ff987c9339b71f28341e6a98a6f358a9086f9fe7745051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127592285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df6d7e2d453e9995658fa8751f2b6e84a64212eeee685595977f5ff7e512afd5`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:29:53 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 15 Jan 2026 22:29:53 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 15 Jan 2026 22:29:58 GMT
ENV INFLUXDB_VERSION=3.8.0
# Thu, 15 Jan 2026 22:29:58 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 15 Jan 2026 22:29:58 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:29:58 GMT
USER influxdb3
# Thu, 15 Jan 2026 22:29:58 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 15 Jan 2026 22:29:58 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 15 Jan 2026 22:29:58 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 15 Jan 2026 22:29:58 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Thu, 15 Jan 2026 22:29:58 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 15 Jan 2026 22:29:58 GMT
ENV LOG_FILTER=info
# Thu, 15 Jan 2026 22:29:58 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 15 Jan 2026 22:29:58 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 15 Jan 2026 22:29:58 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d80b8916ac9be25ca39f63d725fbecdb5221cc992a8f8edc501e20aa7f6cdd`  
		Last Modified: Thu, 15 Jan 2026 22:30:15 GMT  
		Size: 6.7 MB (6666466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86baf47ce3b1fa8c7b1d7b1ba023420e80d040d1a773b90f1a3f1444d5398b8`  
		Last Modified: Thu, 15 Jan 2026 22:30:14 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75782d754446062a195fd74ec4f45355abd9b48844b421553b76d0d92c2e9e6`  
		Last Modified: Thu, 15 Jan 2026 22:30:17 GMT  
		Size: 91.2 MB (91195488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0552eea07c1a62aaa4c8a941aa4d914694ed7a40fa2f205e24255b406514ab`  
		Last Modified: Thu, 15 Jan 2026 22:30:14 GMT  
		Size: 518.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e9ae2043b745909b42322ca040a8bc78dae54020dbf787084712e77c63a890`  
		Last Modified: Thu, 15 Jan 2026 22:30:16 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:cb631e30f9aa3075f21e34d43d947684a1e2cf8b6db12b3870f5925ba45592bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c0859ea2244b0defc0d27a58cd00c57d441a00b51b6c00983526ef8516503d2`

```dockerfile
```

-	Layers:
	-	`sha256:eb1c0fc56bdfe5de760e79c005402e18989d63559ec2f437944b534243db1c91`  
		Last Modified: Thu, 15 Jan 2026 22:30:15 GMT  
		Size: 2.3 MB (2310611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf90cea5e6b638571c01c3c00fe6a8b6e65cbff58a178ba08a0c4a0f3c9fc4d5`  
		Last Modified: Thu, 15 Jan 2026 22:30:14 GMT  
		Size: 17.8 KB (17797 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ad6e83f930d0ab312e7f5a2b347d9b8aa7f6b4132db0409cf404e4bdaa0a67cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118244315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d65a5b3e4ed077bc1ba501bc9ce80427816521ff052532109d778edee858bf2`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:31:56 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Thu, 15 Jan 2026 22:31:57 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Thu, 15 Jan 2026 22:32:03 GMT
ENV INFLUXDB_VERSION=3.8.0
# Thu, 15 Jan 2026 22:32:03 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Thu, 15 Jan 2026 22:32:03 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:32:03 GMT
USER influxdb3
# Thu, 15 Jan 2026 22:32:03 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Thu, 15 Jan 2026 22:32:03 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Thu, 15 Jan 2026 22:32:03 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Thu, 15 Jan 2026 22:32:03 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Thu, 15 Jan 2026 22:32:03 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Thu, 15 Jan 2026 22:32:03 GMT
ENV LOG_FILTER=info
# Thu, 15 Jan 2026 22:32:03 GMT
EXPOSE map[8181/tcp:{}]
# Thu, 15 Jan 2026 22:32:03 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Thu, 15 Jan 2026 22:32:03 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bd4240eafafe3f7fe3f9bc5d3b023ea3b76cd522bea0a947b3358df8986ed0`  
		Last Modified: Thu, 15 Jan 2026 22:32:18 GMT  
		Size: 6.7 MB (6678021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a2eb424397e2fd233b9e3e45d8e2e2ff184ac156d640257caac83c500bd03b`  
		Last Modified: Thu, 15 Jan 2026 22:32:17 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c9c7ab39edbfbc219f93a01abd342c7aa9ae427a6e3c461e19bc610c55633c`  
		Last Modified: Thu, 15 Jan 2026 22:32:19 GMT  
		Size: 82.7 MB (82698149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124f15f88b8a4272c18117de13ad2ba7f3853d372748c6fea818c9336b9023fb`  
		Last Modified: Thu, 15 Jan 2026 22:32:17 GMT  
		Size: 518.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a262b7c40609324279929b50e3eff0cb9505cd033e5cf2e2dc7a38c8c4e0199d`  
		Last Modified: Thu, 15 Jan 2026 22:32:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:0265bf65e9e0e0e1d1997518bf6b88e6df9698f769f086ef60bbaf2e790d4070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9a5cb8b7911fa2587aea0afc1d4c89be70eb8e24cab810c6172cc216e9d911`

```dockerfile
```

-	Layers:
	-	`sha256:9430335ba47f250a06bcaca7da5899e1461955a18254643114311ddb1acedd5f`  
		Last Modified: Thu, 15 Jan 2026 22:32:17 GMT  
		Size: 2.3 MB (2311693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e36fbb81eb4a33ce5bfce27a827062a0b8d553c1d9ca2e76dc9b865f51041ac`  
		Last Modified: Thu, 15 Jan 2026 22:32:17 GMT  
		Size: 17.9 KB (17946 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:latest`

```console
$ docker pull influxdb@sha256:47d5ee97ca868e0d669db8ec37bdb72373d11a1fdd16e6ee712447a865d4d119
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:fbbbb123e62858a14dc1f0b2f146640b7aee3f83b8e3e8d16706ea2a0961223d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107232235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8b79bd46f3ad2285f42e7222b0061406c2d3443d0ee0d1dbc18b9e6e238e4f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:27:12 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:27:12 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 13 Jan 2026 02:27:12 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 13 Jan 2026 02:27:14 GMT
ENV GOSU_VER=1.19
# Tue, 13 Jan 2026 02:27:14 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 13 Jan 2026 02:27:14 GMT
ENV INFLUXDB_VERSION=2.8.0
# Tue, 13 Jan 2026 02:27:14 GMT
ENV INFLUXDB_PR=-2
# Tue, 13 Jan 2026 02:27:14 GMT
ENV INFLUXDB_PV=2.8.0-2
# Tue, 13 Jan 2026 02:27:18 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 13 Jan 2026 02:27:18 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 13 Jan 2026 02:27:19 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 13 Jan 2026 02:27:19 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 13 Jan 2026 02:27:19 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 13 Jan 2026 02:27:19 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 13 Jan 2026 02:27:19 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 02:27:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 02:27:19 GMT
CMD ["influxd"]
# Tue, 13 Jan 2026 02:27:19 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 13 Jan 2026 02:27:19 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 13 Jan 2026 02:27:19 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 13 Jan 2026 02:27:19 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 13 Jan 2026 02:27:19 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dcddc3d3c23c1c56b07e1355ca795cd4e1fd6a750e12250b364a39908314603`  
		Last Modified: Tue, 13 Jan 2026 02:27:31 GMT  
		Size: 9.8 MB (9797566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69611437006e7e5d57518505b16149f02d6de08bb4fd641a35b57ff9538e7019`  
		Last Modified: Tue, 13 Jan 2026 02:27:31 GMT  
		Size: 6.2 MB (6156960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c709ee61b6d0aa5181b6f1bd280d67fb9c9c47f750adaeb54071159645ed361`  
		Last Modified: Tue, 13 Jan 2026 02:27:30 GMT  
		Size: 3.2 KB (3222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac01bb46173c8f94318c49396692514d025f567953e9c10e9861bcd55cbaae7`  
		Last Modified: Tue, 13 Jan 2026 02:27:31 GMT  
		Size: 811.5 KB (811477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7f5e8c960d80d311f115d887a80722c31f9018ba0067431f173e26de26051e`  
		Last Modified: Tue, 13 Jan 2026 02:27:33 GMT  
		Size: 50.5 MB (50451829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99ba881f7de4d8bf0add7733db05bf697e3ace7f5cffc314be099705f02ea79`  
		Last Modified: Tue, 13 Jan 2026 02:27:33 GMT  
		Size: 11.8 MB (11775880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeac49fa47842b0d7d0dc90119df9ea3676af835768d021a2069c65930300b22`  
		Last Modified: Tue, 13 Jan 2026 02:27:33 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a223dfcf1aa0f4fbeddf0e9fa404d2c2e4b6a2d3c2e7322e8a17944a7e78db49`  
		Last Modified: Tue, 13 Jan 2026 02:27:33 GMT  
		Size: 235.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e10ef99f06088a71bab9bbf3532907e25691b3728cdf97a2d8169e4dc90fa6`  
		Last Modified: Tue, 13 Jan 2026 02:27:34 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:28a7ecfc57c3de3aa44548980c3ef7dd74b7ee294cc9f0994710c794f950d9bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:608bef8307d19f25a454085edc672001fc860618884e40fdcffa437a205d03a0`

```dockerfile
```

-	Layers:
	-	`sha256:6de1637cff31caef959bd3292964ba38d361879667a8db6c0102bb53b202d6ea`  
		Last Modified: Tue, 13 Jan 2026 02:27:31 GMT  
		Size: 2.9 MB (2934237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5351d7eccf2ca31733a58fd915c8306fe6c56d099cacb0cd37cfb83eb801a79c`  
		Last Modified: Tue, 13 Jan 2026 02:27:31 GMT  
		Size: 33.6 KB (33621 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:a9256736de2e2596be881fbb2b62224cbd49865cf97aee4d784f56ba728f5052
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103631551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e041a58a0f2da6742d7ddd660fcb4524980ee351e3046bf0036ea534511843`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:29:35 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:29:36 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 13 Jan 2026 02:29:36 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 13 Jan 2026 02:30:48 GMT
ENV GOSU_VER=1.19
# Tue, 13 Jan 2026 02:30:48 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 13 Jan 2026 02:30:48 GMT
ENV INFLUXDB_VERSION=2.8.0
# Tue, 13 Jan 2026 02:30:48 GMT
ENV INFLUXDB_PR=-2
# Tue, 13 Jan 2026 02:30:48 GMT
ENV INFLUXDB_PV=2.8.0-2
# Tue, 13 Jan 2026 02:30:52 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 13 Jan 2026 02:30:52 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 13 Jan 2026 02:30:53 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 13 Jan 2026 02:30:53 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 13 Jan 2026 02:30:53 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 13 Jan 2026 02:30:53 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 13 Jan 2026 02:30:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 02:30:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 02:30:53 GMT
CMD ["influxd"]
# Tue, 13 Jan 2026 02:30:53 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 13 Jan 2026 02:30:53 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 13 Jan 2026 02:30:53 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 13 Jan 2026 02:30:53 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 13 Jan 2026 02:30:53 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff72e9f0d8c78a6aaa8d48cd6cbe9ae48d8da7536f200e4be1224b028abec803`  
		Last Modified: Tue, 13 Jan 2026 02:29:57 GMT  
		Size: 9.6 MB (9626944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3248cb6f7828f084a214ae8053bb4436f265efa780f883e495a508b864e7510a`  
		Last Modified: Tue, 13 Jan 2026 02:29:57 GMT  
		Size: 5.8 MB (5790415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd971a07829912a852596669fe5089a772f917e244ce57921e1296659f61c45`  
		Last Modified: Tue, 13 Jan 2026 02:29:57 GMT  
		Size: 3.2 KB (3228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0cd106ca7e593dcab49c86754e35bd79b48a1d3007438049e89614659564b5`  
		Last Modified: Tue, 13 Jan 2026 02:31:03 GMT  
		Size: 766.4 KB (766370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53a3a9efe7fd59838f76f744fc33e7b7848a8077bf8e265caf35bf5d731caa4`  
		Last Modified: Tue, 13 Jan 2026 02:31:05 GMT  
		Size: 48.2 MB (48229552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68b008dfe291566d50ddf5c7020299a3060b1d20c79012275b130b78a36b807`  
		Last Modified: Tue, 13 Jan 2026 02:31:04 GMT  
		Size: 11.1 MB (11100424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4e2ae9c66b1fec75a22ff096205beb69e7b188d5500259b911d01e597dd96b`  
		Last Modified: Tue, 13 Jan 2026 02:31:03 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda15609a2fc5f59147422f52e5939c25b23cc4c2c60cbda90d140c87e221ae2`  
		Last Modified: Tue, 13 Jan 2026 02:31:04 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfb8e20ecdd7ab27d51281c854cb806d337db33b27147ad8a379c1c40f8ffad`  
		Last Modified: Tue, 13 Jan 2026 02:31:05 GMT  
		Size: 6.3 KB (6286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:8ce104bbae7ace138e9444b0f394ca033069f1e6c54b28661c9c4705c9a56ce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6906ffeb91245c75565f0400dc5303d54f04391d8cfc6aec374c069265b9014b`

```dockerfile
```

-	Layers:
	-	`sha256:47cb60b1b3f39493774cf7056e3a9b3cf2d90c19a28bbb9a3bb641ee28e3fe80`  
		Last Modified: Tue, 13 Jan 2026 02:31:03 GMT  
		Size: 2.9 MB (2933717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12eb99a3526a426649d9677b3db7da8c00a4a9079eafcb7355e98aec58817018`  
		Last Modified: Tue, 13 Jan 2026 02:31:03 GMT  
		Size: 33.8 KB (33815 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:meta`

```console
$ docker pull influxdb@sha256:5eb24e671873d2663ef0c00ebde2c425db825a47e36f9a93b19dd18752354a0d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:meta` - linux; amd64

```console
$ docker pull influxdb@sha256:9ec905fa99e678b7a46d0f8e84f7cbdcad71b5f480e6e7c398e5eaa965ac6e20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91299873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a552f12602ad1bedee2244e93fed92a53903cba13ca8b81e04d628e2c85a4228`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:01:51 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Tue, 13 Jan 2026 04:01:51 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"         "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     rm -r "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"           "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:01:51 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 13 Jan 2026 04:01:51 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 13 Jan 2026 04:01:51 GMT
VOLUME [/var/lib/influxdb]
# Tue, 13 Jan 2026 04:01:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 13 Jan 2026 04:01:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jan 2026 04:01:51 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:15 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64538a062a61add8dc8b290fa69475e8902eb839c497a5f5dcd5a950422e493c`  
		Last Modified: Tue, 13 Jan 2026 02:09:00 GMT  
		Size: 24.0 MB (24036867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8226584456c231e3329e2f781db217386df170900017ccf5ad54f649f3a4892`  
		Last Modified: Tue, 13 Jan 2026 04:02:01 GMT  
		Size: 18.8 MB (18780819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61622d86659aed4ba8f4ef77c6784a2201f76664031c14b2cfc4382d1fad188c`  
		Last Modified: Tue, 13 Jan 2026 04:02:00 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91888eb7d9961fd828a172be924f04fc445944a4a20a7c1b5d0cdba26ca1429`  
		Last Modified: Tue, 13 Jan 2026 04:02:01 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:fc34f0e0037afbb0dd07c5569c82c110b8ee9270e8a27fd45a0f0ff815adbade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4604146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05bf3ef5c6c6a490e1a87aeeee4ccd065070ed262594888f4ab79e55e3e7df88`

```dockerfile
```

-	Layers:
	-	`sha256:ef9b998d76c6a317d3d028cff8c5607da4ac015da97d036c8556b540b4eed402`  
		Last Modified: Tue, 13 Jan 2026 04:02:01 GMT  
		Size: 4.6 MB (4591555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90bcc4be344b12d86469f9015e7e36c92c0e18c887c79c28a6183d38f7a71dc1`  
		Last Modified: Tue, 13 Jan 2026 04:02:00 GMT  
		Size: 12.6 KB (12591 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:meta-alpine`

```console
$ docker pull influxdb@sha256:aecaf75c0592866bc0a7c2639bb83f72193dda8ca322e9434210831a02a4857a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:334fda21d7660dabebf415a7630e82d71c49a482457d86edd5a02adf9ade1164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23592932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97dfff6219d548cae54fee570f6f3b37ac16ff0e9424df4cfe959bcf9b715512`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:24:06 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:24:58 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Wed, 28 Jan 2026 03:24:58 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"         "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     tar -xvf "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz"         -C / --strip-components 1 --wildcards             'influxdb-*/usr/bin/influxd-ctl'             'influxdb-*/usr/bin/influxd-meta' &&     rm "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz.asc"        "influxdb-meta-${INFLUXDB_VERSION}_linux_amd64.tar.gz" &&     apk del .build-deps # buildkit
# Wed, 28 Jan 2026 03:24:58 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Wed, 28 Jan 2026 03:24:58 GMT
EXPOSE map[8091/tcp:{}]
# Wed, 28 Jan 2026 03:24:58 GMT
VOLUME [/var/lib/influxdb]
# Wed, 28 Jan 2026 03:24:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:24:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:24:58 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adc499747d2c1716d5193ed87e0f6684b5f7da3ad6b0d2bdfc84d65ed106d36`  
		Last Modified: Wed, 28 Jan 2026 03:24:21 GMT  
		Size: 1.2 MB (1225465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bdedda1ccaa8c658e38e6dd03b7ae881fe041e412d88964c2eeb69cacaa9d72`  
		Last Modified: Wed, 28 Jan 2026 03:25:05 GMT  
		Size: 18.7 MB (18723159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c532d4cfc611beb0d944a9d3a0ecb4f69dfd08641f9c026a71b9183ba72aeb`  
		Last Modified: Wed, 28 Jan 2026 03:25:04 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0374a0e06643bd5572653262d38d90caf085dff084fc64403ebb1555477ec00e`  
		Last Modified: Wed, 28 Jan 2026 03:25:05 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:627437226023c906b3c6b7de5bce011926f537ee0fa9a386d09b87721cc83460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **695.9 KB (695917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987b431e9e9fe1201a9d3d2a53cbb79bad12a66fe71f7caaa35c13d123e4b70f`

```dockerfile
```

-	Layers:
	-	`sha256:6969b9ff35276f6935e71043cc1ec394f9218dd77481815cd0b8d155f1a4a451`  
		Last Modified: Wed, 28 Jan 2026 03:25:04 GMT  
		Size: 682.1 KB (682071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d790fe636454d04353dbcafa3c3eb838b08379bec575783d2659976da7381a07`  
		Last Modified: Wed, 28 Jan 2026 03:25:04 GMT  
		Size: 13.8 KB (13846 bytes)  
		MIME: application/vnd.in-toto+json
