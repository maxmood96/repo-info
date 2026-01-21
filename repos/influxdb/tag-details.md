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
		Last Modified: Tue, 13 Jan 2026 02:09:06 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:02:24 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e28d6ea97b2128522ae18cbac25e7ce68d4db0d79c29ccddeaaecb1a4f8e76`  
		Last Modified: Tue, 13 Jan 2026 04:02:23 GMT  
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
		Last Modified: Tue, 13 Jan 2026 06:21:32 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:05:55 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a06c08a52dc5a184b5a4a493a05ad2e2dbb0f223e131d6339ac223943615bd91`  
		Last Modified: Tue, 13 Jan 2026 04:05:49 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178df1da6314c40f67825e4ce91ebb175e538d25b32c3a0e08504068f299b760`  
		Last Modified: Tue, 13 Jan 2026 04:06:04 GMT  
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
		Last Modified: Sun, 07 Dec 2025 13:54:16 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c266adf412b1887190bc0baa2363569b9d17f4e6d5ef01303411eeece661fe2`  
		Last Modified: Mon, 08 Dec 2025 04:15:19 GMT  
		Size: 1.2 MB (1224596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2286d3bdb9b240a8e73a50cc45ff08cac484d9bd916b7c2731d29c6781731f1`  
		Last Modified: Wed, 08 Oct 2025 23:10:17 GMT  
		Size: 38.1 MB (38069965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bd812bdffaf5a51fdc5ad2690ccb55dec4a092395243bf366e01cf45511ac7`  
		Last Modified: Mon, 08 Dec 2025 04:15:19 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ccae7d91ef8bb0ea37a95450db36eaa796c974b09f7a0589106acf87072085a`  
		Last Modified: Wed, 08 Oct 2025 23:10:16 GMT  
		Size: 1.0 KB (1004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce755337386479f3084609d415719dae3d4f17e49deeb6a099a77ddeca8e2cb`  
		Last Modified: Mon, 08 Dec 2025 00:30:56 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e2d3d495f76618c744d89e0710cd06db610e65e6019e022899e6a4de4fc2e2`  
		Last Modified: Wed, 08 Oct 2025 23:10:17 GMT  
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
		Last Modified: Mon, 08 Dec 2025 14:34:39 GMT  
		Size: 742.5 KB (742482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2c6fe293831b00cc186f0ab8fd0030085d57e84e8eeb22c232095ac36d6ccd8`  
		Last Modified: Wed, 08 Oct 2025 23:10:16 GMT  
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
		Last Modified: Wed, 08 Oct 2025 12:02:47 GMT  
		Size: 4.1 MB (4089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f28be0243b3bb965b6c9b2e07c70b019eb69070fb075e2cc8660b856e4efba`  
		Last Modified: Wed, 08 Oct 2025 21:55:15 GMT  
		Size: 1.3 MB (1304645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f38f6a643f7a256b8eaf81222d2fb2520d2be7423f755c8fa2624e6324abf87`  
		Last Modified: Wed, 08 Oct 2025 21:55:16 GMT  
		Size: 35.5 MB (35545508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbc3962e590201f79eb734b9201590ddc739436a716accc9e14fb795530a3aa`  
		Last Modified: Wed, 08 Oct 2025 21:55:14 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7483ae23f176c3e011cc9c62d96dc29c2b740b7113fe61fb024b8c9201e25f6`  
		Last Modified: Sun, 07 Dec 2025 22:15:38 GMT  
		Size: 1.0 KB (1003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c3334a00d999c2ee2e76dd34dda278c84adead0715ce0da308c6c627e7c6e61`  
		Last Modified: Sun, 07 Dec 2025 22:15:39 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59987b4485557de9f3528ce3b0b97ae5391e16364283ca810e800de91ba5af0`  
		Last Modified: Wed, 08 Oct 2025 21:55:16 GMT  
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
		Last Modified: Mon, 08 Dec 2025 01:59:33 GMT  
		Size: 741.7 KB (741709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30a79558e16dbe151165e5e7ba57ab7f1e7e4b481fd539ff01a4ba11dc4c7e52`  
		Last Modified: Mon, 08 Dec 2025 01:59:33 GMT  
		Size: 18.0 KB (17987 bytes)  
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
		Last Modified: Tue, 13 Jan 2026 02:09:06 GMT  
		Size: 24.0 MB (24036867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725b26fb2b36dd4f2a5f615acd7dff70ad03b02006a86dced12e04b338667995`  
		Last Modified: Tue, 13 Jan 2026 04:02:33 GMT  
		Size: 5.1 KB (5069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0879436a1a448f71f3a5423cf6ccd1e8ba5bc68d47daecb98dade59ae44e2d10`  
		Last Modified: Tue, 13 Jan 2026 04:02:35 GMT  
		Size: 42.2 MB (42165705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e04de71dced00ac7bb0b91a5b1c8a11fe2e4c600c4df8f2658daa2fe5a36dab`  
		Last Modified: Tue, 13 Jan 2026 04:02:25 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0896035861b9d64b002c8437885efe5970b0f8d1f913f00b2b2f8809db13b2`  
		Last Modified: Tue, 13 Jan 2026 04:02:33 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9412fe76db1a8d0debd4745f307f06b231740d4ca94dd7ee3cfe4068931199`  
		Last Modified: Tue, 13 Jan 2026 04:02:33 GMT  
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
		Last Modified: Sun, 07 Dec 2025 13:54:16 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b7c681266c61781b5e9483f43fa6ad59b0acafe3c400aa10ba1e43ec0963a0`  
		Last Modified: Wed, 08 Oct 2025 23:10:15 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b114d197f0b29a6932d8b9d445b0628a19b4157668f6eb76571600ecaf25723`  
		Last Modified: Wed, 08 Oct 2025 23:10:16 GMT  
		Size: 1.2 MB (1224592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3358124fd2820053c690bcf986afef42d2564531fcff8ba0b814614bc23b3bbe`  
		Last Modified: Wed, 08 Oct 2025 23:10:17 GMT  
		Size: 42.1 MB (42105919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63d4466a6a2e285d8482d3dce7c47f8f5a2bbdf6c366916cfb45ea2790337a9`  
		Last Modified: Wed, 08 Oct 2025 23:10:16 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e120ca154a1d12d672fecfc7212adcc4973d001dce2328028c3ab256b7f20b9`  
		Last Modified: Tue, 09 Dec 2025 22:39:05 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a0d8b4e8d0cf5b5a88b2dc5d203d42a530f015d833f41790286c1098b9be04`  
		Last Modified: Wed, 08 Oct 2025 23:10:17 GMT  
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
		Last Modified: Mon, 15 Dec 2025 20:40:19 GMT  
		Size: 769.0 KB (768993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95c8c2a7537102693c04e00ab640a007908a8cdec2fa3201d77b6b835d83c362`  
		Last Modified: Wed, 08 Oct 2025 23:10:16 GMT  
		Size: 16.6 KB (16639 bytes)  
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
		Last Modified: Tue, 13 Jan 2026 02:09:06 GMT  
		Size: 24.0 MB (24036867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742fe9ffa44988147584c258c838556baa2829de4562d711252d64e35aa51acd`  
		Last Modified: Tue, 13 Jan 2026 04:02:37 GMT  
		Size: 5.1 KB (5055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e133e4a1f3889d73daec291d302cafcc4899ca6d2aaa3e8777bb93723ed75aa9`  
		Last Modified: Tue, 13 Jan 2026 04:02:39 GMT  
		Size: 18.6 MB (18596154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f0d90c9a55fc5d40a291700ed3241a6641296699bd5c38a3a9a9e1000176a6`  
		Last Modified: Tue, 13 Jan 2026 04:02:37 GMT  
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
		Last Modified: Tue, 13 Jan 2026 06:21:41 GMT  
		Size: 4.6 MB (4591249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e6550cdbcfce5974370dfda3978e51be51af752edf5b24411a54a04db03405d`  
		Last Modified: Tue, 13 Jan 2026 04:02:31 GMT  
		Size: 13.0 KB (13024 bytes)  
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
		Last Modified: Sun, 07 Dec 2025 13:54:16 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af74a58a446b59e39793a690435f78e585a91ea73edb6406a99a3283db12a3a2`  
		Last Modified: Wed, 08 Oct 2025 23:01:00 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be22d087a3e55404f6a8b32177effbd6c3829e421c0b5ef02b11b38be4785b3`  
		Last Modified: Mon, 15 Dec 2025 19:26:02 GMT  
		Size: 1.2 MB (1224606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d72c9781c814dfaa052605afbb9e8d8be20811f6843ddb55b2cc0645fd96a7`  
		Last Modified: Mon, 15 Dec 2025 19:26:03 GMT  
		Size: 18.5 MB (18549871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66e2e10d6786167404e416ab04e6d4485db03583db3118244df06813625bad4`  
		Last Modified: Wed, 08 Oct 2025 23:10:24 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1362d7c20d172d913583e0a7dd8615a994bb4d5c13a7df7265d4dd009dfdbe`  
		Last Modified: Tue, 09 Dec 2025 22:40:51 GMT  
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
		Last Modified: Wed, 08 Oct 2025 23:10:24 GMT  
		Size: 676.6 KB (676622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24dde11f34792d696d7baefa980d47a9bb0ec06c1640475e5f37e93aa05a49ae`  
		Last Modified: Mon, 15 Dec 2025 19:26:01 GMT  
		Size: 15.0 KB (15010 bytes)  
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
		Last Modified: Tue, 13 Jan 2026 02:09:06 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:02:24 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e28d6ea97b2128522ae18cbac25e7ce68d4db0d79c29ccddeaaecb1a4f8e76`  
		Last Modified: Tue, 13 Jan 2026 04:02:23 GMT  
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
		Last Modified: Tue, 13 Jan 2026 06:21:32 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:05:55 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a06c08a52dc5a184b5a4a493a05ad2e2dbb0f223e131d6339ac223943615bd91`  
		Last Modified: Tue, 13 Jan 2026 04:05:49 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178df1da6314c40f67825e4ce91ebb175e538d25b32c3a0e08504068f299b760`  
		Last Modified: Tue, 13 Jan 2026 04:06:04 GMT  
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
		Last Modified: Sun, 07 Dec 2025 13:54:16 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c266adf412b1887190bc0baa2363569b9d17f4e6d5ef01303411eeece661fe2`  
		Last Modified: Mon, 08 Dec 2025 04:15:19 GMT  
		Size: 1.2 MB (1224596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2286d3bdb9b240a8e73a50cc45ff08cac484d9bd916b7c2731d29c6781731f1`  
		Last Modified: Wed, 08 Oct 2025 23:10:17 GMT  
		Size: 38.1 MB (38069965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bd812bdffaf5a51fdc5ad2690ccb55dec4a092395243bf366e01cf45511ac7`  
		Last Modified: Mon, 08 Dec 2025 04:15:19 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ccae7d91ef8bb0ea37a95450db36eaa796c974b09f7a0589106acf87072085a`  
		Last Modified: Wed, 08 Oct 2025 23:10:16 GMT  
		Size: 1.0 KB (1004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce755337386479f3084609d415719dae3d4f17e49deeb6a099a77ddeca8e2cb`  
		Last Modified: Mon, 08 Dec 2025 00:30:56 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e2d3d495f76618c744d89e0710cd06db610e65e6019e022899e6a4de4fc2e2`  
		Last Modified: Wed, 08 Oct 2025 23:10:17 GMT  
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
		Last Modified: Mon, 08 Dec 2025 14:34:39 GMT  
		Size: 742.5 KB (742482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2c6fe293831b00cc186f0ab8fd0030085d57e84e8eeb22c232095ac36d6ccd8`  
		Last Modified: Wed, 08 Oct 2025 23:10:16 GMT  
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
		Last Modified: Wed, 08 Oct 2025 12:02:47 GMT  
		Size: 4.1 MB (4089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f28be0243b3bb965b6c9b2e07c70b019eb69070fb075e2cc8660b856e4efba`  
		Last Modified: Wed, 08 Oct 2025 21:55:15 GMT  
		Size: 1.3 MB (1304645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f38f6a643f7a256b8eaf81222d2fb2520d2be7423f755c8fa2624e6324abf87`  
		Last Modified: Wed, 08 Oct 2025 21:55:16 GMT  
		Size: 35.5 MB (35545508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbc3962e590201f79eb734b9201590ddc739436a716accc9e14fb795530a3aa`  
		Last Modified: Wed, 08 Oct 2025 21:55:14 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7483ae23f176c3e011cc9c62d96dc29c2b740b7113fe61fb024b8c9201e25f6`  
		Last Modified: Sun, 07 Dec 2025 22:15:38 GMT  
		Size: 1.0 KB (1003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c3334a00d999c2ee2e76dd34dda278c84adead0715ce0da308c6c627e7c6e61`  
		Last Modified: Sun, 07 Dec 2025 22:15:39 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59987b4485557de9f3528ce3b0b97ae5391e16364283ca810e800de91ba5af0`  
		Last Modified: Wed, 08 Oct 2025 21:55:16 GMT  
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
		Last Modified: Mon, 08 Dec 2025 01:59:33 GMT  
		Size: 741.7 KB (741709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30a79558e16dbe151165e5e7ba57ab7f1e7e4b481fd539ff01a4ba11dc4c7e52`  
		Last Modified: Mon, 08 Dec 2025 01:59:33 GMT  
		Size: 18.0 KB (17987 bytes)  
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
		Last Modified: Tue, 13 Jan 2026 02:09:06 GMT  
		Size: 24.0 MB (24036867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725b26fb2b36dd4f2a5f615acd7dff70ad03b02006a86dced12e04b338667995`  
		Last Modified: Tue, 13 Jan 2026 04:02:33 GMT  
		Size: 5.1 KB (5069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0879436a1a448f71f3a5423cf6ccd1e8ba5bc68d47daecb98dade59ae44e2d10`  
		Last Modified: Tue, 13 Jan 2026 04:02:35 GMT  
		Size: 42.2 MB (42165705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e04de71dced00ac7bb0b91a5b1c8a11fe2e4c600c4df8f2658daa2fe5a36dab`  
		Last Modified: Tue, 13 Jan 2026 04:02:25 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0896035861b9d64b002c8437885efe5970b0f8d1f913f00b2b2f8809db13b2`  
		Last Modified: Tue, 13 Jan 2026 04:02:33 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9412fe76db1a8d0debd4745f307f06b231740d4ca94dd7ee3cfe4068931199`  
		Last Modified: Tue, 13 Jan 2026 04:02:33 GMT  
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
		Last Modified: Sun, 07 Dec 2025 13:54:16 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b7c681266c61781b5e9483f43fa6ad59b0acafe3c400aa10ba1e43ec0963a0`  
		Last Modified: Wed, 08 Oct 2025 23:10:15 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b114d197f0b29a6932d8b9d445b0628a19b4157668f6eb76571600ecaf25723`  
		Last Modified: Wed, 08 Oct 2025 23:10:16 GMT  
		Size: 1.2 MB (1224592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3358124fd2820053c690bcf986afef42d2564531fcff8ba0b814614bc23b3bbe`  
		Last Modified: Wed, 08 Oct 2025 23:10:17 GMT  
		Size: 42.1 MB (42105919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63d4466a6a2e285d8482d3dce7c47f8f5a2bbdf6c366916cfb45ea2790337a9`  
		Last Modified: Wed, 08 Oct 2025 23:10:16 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e120ca154a1d12d672fecfc7212adcc4973d001dce2328028c3ab256b7f20b9`  
		Last Modified: Tue, 09 Dec 2025 22:39:05 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a0d8b4e8d0cf5b5a88b2dc5d203d42a530f015d833f41790286c1098b9be04`  
		Last Modified: Wed, 08 Oct 2025 23:10:17 GMT  
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
		Last Modified: Mon, 15 Dec 2025 20:40:19 GMT  
		Size: 769.0 KB (768993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95c8c2a7537102693c04e00ab640a007908a8cdec2fa3201d77b6b835d83c362`  
		Last Modified: Wed, 08 Oct 2025 23:10:16 GMT  
		Size: 16.6 KB (16639 bytes)  
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
		Last Modified: Tue, 13 Jan 2026 02:09:06 GMT  
		Size: 24.0 MB (24036867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742fe9ffa44988147584c258c838556baa2829de4562d711252d64e35aa51acd`  
		Last Modified: Tue, 13 Jan 2026 04:02:37 GMT  
		Size: 5.1 KB (5055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e133e4a1f3889d73daec291d302cafcc4899ca6d2aaa3e8777bb93723ed75aa9`  
		Last Modified: Tue, 13 Jan 2026 04:02:39 GMT  
		Size: 18.6 MB (18596154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f0d90c9a55fc5d40a291700ed3241a6641296699bd5c38a3a9a9e1000176a6`  
		Last Modified: Tue, 13 Jan 2026 04:02:37 GMT  
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
		Last Modified: Tue, 13 Jan 2026 06:21:41 GMT  
		Size: 4.6 MB (4591249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e6550cdbcfce5974370dfda3978e51be51af752edf5b24411a54a04db03405d`  
		Last Modified: Tue, 13 Jan 2026 04:02:31 GMT  
		Size: 13.0 KB (13024 bytes)  
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
		Last Modified: Sun, 07 Dec 2025 13:54:16 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af74a58a446b59e39793a690435f78e585a91ea73edb6406a99a3283db12a3a2`  
		Last Modified: Wed, 08 Oct 2025 23:01:00 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be22d087a3e55404f6a8b32177effbd6c3829e421c0b5ef02b11b38be4785b3`  
		Last Modified: Mon, 15 Dec 2025 19:26:02 GMT  
		Size: 1.2 MB (1224606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d72c9781c814dfaa052605afbb9e8d8be20811f6843ddb55b2cc0645fd96a7`  
		Last Modified: Mon, 15 Dec 2025 19:26:03 GMT  
		Size: 18.5 MB (18549871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66e2e10d6786167404e416ab04e6d4485db03583db3118244df06813625bad4`  
		Last Modified: Wed, 08 Oct 2025 23:10:24 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1362d7c20d172d913583e0a7dd8615a994bb4d5c13a7df7265d4dd009dfdbe`  
		Last Modified: Tue, 09 Dec 2025 22:40:51 GMT  
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
		Last Modified: Wed, 08 Oct 2025 23:10:24 GMT  
		Size: 676.6 KB (676622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24dde11f34792d696d7baefa980d47a9bb0ec06c1640475e5f37e93aa05a49ae`  
		Last Modified: Mon, 15 Dec 2025 19:26:01 GMT  
		Size: 15.0 KB (15010 bytes)  
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
		Last Modified: Tue, 13 Jan 2026 02:09:06 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:02:00 GMT  
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
		Last Modified: Tue, 13 Jan 2026 06:21:58 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:05:41 GMT  
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
		Last Modified: Sun, 07 Dec 2025 13:55:07 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833a534ae7d9b744b01293824d76272ab350ec43a3ea6e2461ff7af8abc50a6a`  
		Last Modified: Wed, 08 Oct 2025 23:09:27 GMT  
		Size: 1.2 MB (1225336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c347910584b08baf1a48bdf46c5c50dd24038eb1302b7007f31ce71bc927b592`  
		Last Modified: Wed, 08 Oct 2025 23:09:28 GMT  
		Size: 41.3 MB (41251703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a935c4d2c88a22b2b988a0ccac55421ea76be53d52269f7b632dcf92c515813`  
		Last Modified: Mon, 08 Dec 2025 02:21:06 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a53405a7e90893d67726045e12be0b8d6c77efc4329d83b02742c7dc703c64`  
		Last Modified: Wed, 08 Oct 2025 23:09:27 GMT  
		Size: 993.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559f188f2dcf26e5cc25cbe55a6ec7068097f6735e694bf00a27874305fe66fa`  
		Last Modified: Wed, 08 Oct 2025 23:09:28 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafd7a2e4b50b127938200eed101e836d8f93fbdeeeb0d43f571a379f42a5173`  
		Last Modified: Mon, 08 Dec 2025 02:21:06 GMT  
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
		Last Modified: Mon, 08 Dec 2025 14:17:08 GMT  
		Size: 761.9 KB (761859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efdc33ff6b4a8b7da52daf4a11c7f9b03b3ba5c78a7c13b748b4e02199fa9284`  
		Last Modified: Wed, 08 Oct 2025 23:09:27 GMT  
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
		Last Modified: Wed, 08 Oct 2025 12:04:23 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3778cd6b7947fa40773e4d96fb04b28656fd002578dc1ba35152916dba4eab3`  
		Last Modified: Wed, 08 Oct 2025 21:54:58 GMT  
		Size: 1.3 MB (1290589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193f43b6c8619cf1483f881f1bdef6dd939ea58e7d495e8416bfda3d15d098c2`  
		Last Modified: Wed, 08 Oct 2025 21:54:59 GMT  
		Size: 38.1 MB (38058839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2a6f8e76e4d9c33472e64d72f702c7962ba0b5e4d61db1c648411752212f71`  
		Last Modified: Wed, 08 Oct 2025 21:54:58 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31e522d0a6aa09c893a40e88167d5532ce096d84694b5970672f058e64bc5d6`  
		Last Modified: Wed, 08 Oct 2025 21:54:58 GMT  
		Size: 990.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf7f3756e6d6b4556e7f0ff09c0a747d1b2defff34996459ba9c9fe8623c697`  
		Last Modified: Wed, 08 Oct 2025 21:54:59 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70fba9b3a8b84fe1ceeacd36df99e6d838298f829348550376de111eaa260c5`  
		Last Modified: Mon, 08 Dec 2025 09:22:08 GMT  
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
		Last Modified: Wed, 08 Oct 2025 21:54:58 GMT  
		Size: 761.1 KB (761088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21ee247e175c8dccb7cd34515f34b1749a76fd37134eef6a64643a3885004fe1`  
		Last Modified: Wed, 08 Oct 2025 21:54:58 GMT  
		Size: 18.8 KB (18771 bytes)  
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
		Last Modified: Tue, 13 Jan 2026 02:09:06 GMT  
		Size: 24.0 MB (24036867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66c83e9d2d95ae7bb8cae9f8b46bff3d99ebbbdce310b651807fcd051a37ba0`  
		Last Modified: Tue, 13 Jan 2026 04:02:15 GMT  
		Size: 42.3 MB (42319809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485ded8552cc8df9c3417e10f8333c7f5f414f71250ce6145d55fc4b15698edd`  
		Last Modified: Tue, 13 Jan 2026 04:02:12 GMT  
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
		Last Modified: Tue, 13 Jan 2026 06:22:06 GMT  
		Size: 14.1 KB (14077 bytes)  
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
		Last Modified: Sun, 07 Dec 2025 13:55:07 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a3788b43dae292831ae0448a5ed504046ffa71fe7a9f09db40713951fbf944`  
		Last Modified: Wed, 08 Oct 2025 23:09:51 GMT  
		Size: 1.2 MB (1225329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e0170f82fea093122d3570e0d358e936d1db98ed05a0d6a48d33037501b351`  
		Last Modified: Tue, 09 Dec 2025 22:33:31 GMT  
		Size: 42.3 MB (42254311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b0661d8dbfc3b43d49ec386e18c197ae353dd5d5c77c548207da941ba2ee68`  
		Last Modified: Wed, 08 Oct 2025 23:09:51 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39225506d3b8f10fd5e6623059b8c1e0d7efadec626f71dcf9da78fee4f7e2a`  
		Last Modified: Wed, 08 Oct 2025 23:09:51 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d72d987f87daa2925154010870639046590c11fa247eb8c38fdd2ea9c6094b`  
		Last Modified: Wed, 08 Oct 2025 23:09:52 GMT  
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
		Last Modified: Mon, 15 Dec 2025 19:34:05 GMT  
		Size: 775.8 KB (775810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f65ff52ae85ef9fa76b501b5f6ab0974038c20801b32cc1c20d90c94d731471`  
		Last Modified: Wed, 08 Oct 2025 23:09:51 GMT  
		Size: 15.2 KB (15191 bytes)  
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
		Last Modified: Tue, 13 Jan 2026 02:09:06 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:02:06 GMT  
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
		Last Modified: Sun, 07 Dec 2025 13:55:07 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1506a520a1ca51f516d5068e753e243431efab0ef69c7b1634e53985ce44a2`  
		Last Modified: Wed, 08 Oct 2025 23:09:52 GMT  
		Size: 1.2 MB (1225337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8df8f8e418a27917114426b3d245a3728772fe30be9e1b0b609e79b9ccb3b1d`  
		Last Modified: Wed, 08 Oct 2025 23:09:52 GMT  
		Size: 18.7 MB (18722501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96fdeefb85b445c179f78bb53968e8210d7aaa4a30cccb4d6452d9ac4a7b000`  
		Last Modified: Wed, 08 Oct 2025 23:09:51 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5817ad78e6b46e06d7f07b733f09a0eddd15b789d78398b86fe406d8cd2fdf7`  
		Last Modified: Wed, 08 Oct 2025 23:09:52 GMT  
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
		Last Modified: Mon, 15 Dec 2025 20:39:37 GMT  
		Size: 681.8 KB (681759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e71c697656e9ce6a76bcb04d0f78aff32c9bc6715c511aa163637cbd6c96a2ac`  
		Last Modified: Mon, 15 Dec 2025 20:39:37 GMT  
		Size: 13.6 KB (13577 bytes)  
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
		Last Modified: Tue, 13 Jan 2026 02:09:06 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:02:00 GMT  
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
		Last Modified: Tue, 13 Jan 2026 06:21:58 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:05:41 GMT  
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
		Last Modified: Sun, 07 Dec 2025 13:55:07 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833a534ae7d9b744b01293824d76272ab350ec43a3ea6e2461ff7af8abc50a6a`  
		Last Modified: Wed, 08 Oct 2025 23:09:27 GMT  
		Size: 1.2 MB (1225336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c347910584b08baf1a48bdf46c5c50dd24038eb1302b7007f31ce71bc927b592`  
		Last Modified: Wed, 08 Oct 2025 23:09:28 GMT  
		Size: 41.3 MB (41251703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a935c4d2c88a22b2b988a0ccac55421ea76be53d52269f7b632dcf92c515813`  
		Last Modified: Mon, 08 Dec 2025 02:21:06 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a53405a7e90893d67726045e12be0b8d6c77efc4329d83b02742c7dc703c64`  
		Last Modified: Wed, 08 Oct 2025 23:09:27 GMT  
		Size: 993.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559f188f2dcf26e5cc25cbe55a6ec7068097f6735e694bf00a27874305fe66fa`  
		Last Modified: Wed, 08 Oct 2025 23:09:28 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafd7a2e4b50b127938200eed101e836d8f93fbdeeeb0d43f571a379f42a5173`  
		Last Modified: Mon, 08 Dec 2025 02:21:06 GMT  
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
		Last Modified: Mon, 08 Dec 2025 14:17:08 GMT  
		Size: 761.9 KB (761859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efdc33ff6b4a8b7da52daf4a11c7f9b03b3ba5c78a7c13b748b4e02199fa9284`  
		Last Modified: Wed, 08 Oct 2025 23:09:27 GMT  
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
		Last Modified: Wed, 08 Oct 2025 12:04:23 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3778cd6b7947fa40773e4d96fb04b28656fd002578dc1ba35152916dba4eab3`  
		Last Modified: Wed, 08 Oct 2025 21:54:58 GMT  
		Size: 1.3 MB (1290589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193f43b6c8619cf1483f881f1bdef6dd939ea58e7d495e8416bfda3d15d098c2`  
		Last Modified: Wed, 08 Oct 2025 21:54:59 GMT  
		Size: 38.1 MB (38058839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2a6f8e76e4d9c33472e64d72f702c7962ba0b5e4d61db1c648411752212f71`  
		Last Modified: Wed, 08 Oct 2025 21:54:58 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31e522d0a6aa09c893a40e88167d5532ce096d84694b5970672f058e64bc5d6`  
		Last Modified: Wed, 08 Oct 2025 21:54:58 GMT  
		Size: 990.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf7f3756e6d6b4556e7f0ff09c0a747d1b2defff34996459ba9c9fe8623c697`  
		Last Modified: Wed, 08 Oct 2025 21:54:59 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70fba9b3a8b84fe1ceeacd36df99e6d838298f829348550376de111eaa260c5`  
		Last Modified: Mon, 08 Dec 2025 09:22:08 GMT  
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
		Last Modified: Wed, 08 Oct 2025 21:54:58 GMT  
		Size: 761.1 KB (761088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21ee247e175c8dccb7cd34515f34b1749a76fd37134eef6a64643a3885004fe1`  
		Last Modified: Wed, 08 Oct 2025 21:54:58 GMT  
		Size: 18.8 KB (18771 bytes)  
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
		Last Modified: Tue, 13 Jan 2026 02:09:06 GMT  
		Size: 24.0 MB (24036867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66c83e9d2d95ae7bb8cae9f8b46bff3d99ebbbdce310b651807fcd051a37ba0`  
		Last Modified: Tue, 13 Jan 2026 04:02:15 GMT  
		Size: 42.3 MB (42319809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485ded8552cc8df9c3417e10f8333c7f5f414f71250ce6145d55fc4b15698edd`  
		Last Modified: Tue, 13 Jan 2026 04:02:12 GMT  
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
		Last Modified: Tue, 13 Jan 2026 06:22:06 GMT  
		Size: 14.1 KB (14077 bytes)  
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
		Last Modified: Sun, 07 Dec 2025 13:55:07 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a3788b43dae292831ae0448a5ed504046ffa71fe7a9f09db40713951fbf944`  
		Last Modified: Wed, 08 Oct 2025 23:09:51 GMT  
		Size: 1.2 MB (1225329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e0170f82fea093122d3570e0d358e936d1db98ed05a0d6a48d33037501b351`  
		Last Modified: Tue, 09 Dec 2025 22:33:31 GMT  
		Size: 42.3 MB (42254311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b0661d8dbfc3b43d49ec386e18c197ae353dd5d5c77c548207da941ba2ee68`  
		Last Modified: Wed, 08 Oct 2025 23:09:51 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39225506d3b8f10fd5e6623059b8c1e0d7efadec626f71dcf9da78fee4f7e2a`  
		Last Modified: Wed, 08 Oct 2025 23:09:51 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d72d987f87daa2925154010870639046590c11fa247eb8c38fdd2ea9c6094b`  
		Last Modified: Wed, 08 Oct 2025 23:09:52 GMT  
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
		Last Modified: Mon, 15 Dec 2025 19:34:05 GMT  
		Size: 775.8 KB (775810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f65ff52ae85ef9fa76b501b5f6ab0974038c20801b32cc1c20d90c94d731471`  
		Last Modified: Wed, 08 Oct 2025 23:09:51 GMT  
		Size: 15.2 KB (15191 bytes)  
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
		Last Modified: Tue, 13 Jan 2026 02:09:06 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:02:06 GMT  
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
		Last Modified: Sun, 07 Dec 2025 13:55:07 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1506a520a1ca51f516d5068e753e243431efab0ef69c7b1634e53985ce44a2`  
		Last Modified: Wed, 08 Oct 2025 23:09:52 GMT  
		Size: 1.2 MB (1225337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8df8f8e418a27917114426b3d245a3728772fe30be9e1b0b609e79b9ccb3b1d`  
		Last Modified: Wed, 08 Oct 2025 23:09:52 GMT  
		Size: 18.7 MB (18722501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96fdeefb85b445c179f78bb53968e8210d7aaa4a30cccb4d6452d9ac4a7b000`  
		Last Modified: Wed, 08 Oct 2025 23:09:51 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5817ad78e6b46e06d7f07b733f09a0eddd15b789d78398b86fe406d8cd2fdf7`  
		Last Modified: Wed, 08 Oct 2025 23:09:52 GMT  
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
		Last Modified: Mon, 15 Dec 2025 20:39:37 GMT  
		Size: 681.8 KB (681759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e71c697656e9ce6a76bcb04d0f78aff32c9bc6715c511aa163637cbd6c96a2ac`  
		Last Modified: Mon, 15 Dec 2025 20:39:37 GMT  
		Size: 13.6 KB (13577 bytes)  
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
		Last Modified: Tue, 13 Jan 2026 02:27:42 GMT  
		Size: 9.8 MB (9797566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69611437006e7e5d57518505b16149f02d6de08bb4fd641a35b57ff9538e7019`  
		Last Modified: Tue, 13 Jan 2026 02:27:31 GMT  
		Size: 6.2 MB (6156960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c709ee61b6d0aa5181b6f1bd280d67fb9c9c47f750adaeb54071159645ed361`  
		Last Modified: Tue, 13 Jan 2026 02:27:39 GMT  
		Size: 3.2 KB (3222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac01bb46173c8f94318c49396692514d025f567953e9c10e9861bcd55cbaae7`  
		Last Modified: Tue, 13 Jan 2026 02:27:40 GMT  
		Size: 811.5 KB (811477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7f5e8c960d80d311f115d887a80722c31f9018ba0067431f173e26de26051e`  
		Last Modified: Tue, 13 Jan 2026 02:27:55 GMT  
		Size: 50.5 MB (50451829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99ba881f7de4d8bf0add7733db05bf697e3ace7f5cffc314be099705f02ea79`  
		Last Modified: Tue, 13 Jan 2026 02:27:41 GMT  
		Size: 11.8 MB (11775880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeac49fa47842b0d7d0dc90119df9ea3676af835768d021a2069c65930300b22`  
		Last Modified: Tue, 13 Jan 2026 02:27:40 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:09 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff72e9f0d8c78a6aaa8d48cd6cbe9ae48d8da7536f200e4be1224b028abec803`  
		Last Modified: Tue, 13 Jan 2026 02:30:22 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:31:10 GMT  
		Size: 766.4 KB (766370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53a3a9efe7fd59838f76f744fc33e7b7848a8077bf8e265caf35bf5d731caa4`  
		Last Modified: Tue, 13 Jan 2026 02:31:05 GMT  
		Size: 48.2 MB (48229552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68b008dfe291566d50ddf5c7020299a3060b1d20c79012275b130b78a36b807`  
		Last Modified: Tue, 13 Jan 2026 02:31:12 GMT  
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
$ docker pull influxdb@sha256:fb537cf0d57937a57eac33efd079ae5b36a1d35437dc1eba1ecb8800a352b62a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:2e03ae8e0b59c4a7b060238e4246b8a003c7b429019bdce39c024b1d5b056afb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81890627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:926890384ff7b559be8bac4f1e03f0d4ee3ca31ece6f2d938f483b97131ce363`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Thu, 11 Dec 2025 21:21:44 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 11 Dec 2025 21:21:45 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Thu, 11 Dec 2025 21:21:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 11 Dec 2025 21:21:45 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Thu, 11 Dec 2025 21:21:47 GMT
ENV INFLUXDB_VERSION=2.8.0
# Thu, 11 Dec 2025 21:21:47 GMT
ENV INFLUXDB_PR=-2
# Thu, 11 Dec 2025 21:21:47 GMT
ENV INFLUXDB_PV=2.8.0-2
# Thu, 11 Dec 2025 21:21:47 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 11 Dec 2025 21:21:47 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Thu, 11 Dec 2025 21:21:48 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 11 Dec 2025 21:21:48 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 11 Dec 2025 21:21:48 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Dec 2025 21:21:48 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 11 Dec 2025 21:21:48 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Dec 2025 21:21:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Dec 2025 21:21:48 GMT
CMD ["influxd"]
# Thu, 11 Dec 2025 21:21:48 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Dec 2025 21:21:48 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Dec 2025 21:21:48 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Dec 2025 21:21:48 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Dec 2025 21:21:48 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Sun, 07 Dec 2025 13:55:07 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10f7056aa72ef8463a31e6afa1dec61d746d3cec587e13de9bcf28396caa037`  
		Last Modified: Thu, 11 Dec 2025 21:22:07 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d56024c76d43582ac2f12311746a23ad83f148c5b42da7c957da34b6cdac498`  
		Last Modified: Thu, 11 Dec 2025 21:21:58 GMT  
		Size: 9.9 MB (9862216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71475ef0f8f2c5f8c394cdda52333392709fc87e769397a0389fb1bb743d399b`  
		Last Modified: Thu, 11 Dec 2025 21:21:58 GMT  
		Size: 6.2 MB (6156990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a315475c1c17f7a223ea2b8a1d9a1985ce438a3bae2dae153555a5d457b051c1`  
		Last Modified: Thu, 11 Dec 2025 21:21:58 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75bc9021d0ef61725243ae72546a2a75243c5424fa7d0fc53f20c469d377cba3`  
		Last Modified: Thu, 11 Dec 2025 21:22:13 GMT  
		Size: 50.4 MB (50447116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c548f8f09a0ce506a8c2e69d75de76926e996dfe9a46448c756d6647e8a04c`  
		Last Modified: Thu, 11 Dec 2025 21:22:00 GMT  
		Size: 11.8 MB (11773781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e504a5513a054282de4e3d4006c910c7003f8804e45058cf073a0422f0212d1`  
		Last Modified: Thu, 11 Dec 2025 21:22:07 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d818200c6c4e7df4884a358b6f80bca9c959914eced87214ae2c44e58fd35b`  
		Last Modified: Thu, 11 Dec 2025 21:22:00 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d217bc1e57c2c30506373ba1fe825b2fe61e5f1ae8585753f0ea1989f9c9f31f`  
		Last Modified: Thu, 11 Dec 2025 21:22:07 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:fd0843ea7d0b590a344252c4735a3b5c3259175326169b796c7863dc7e9409fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **946.7 KB (946733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25347cf7627bd9599b9ab13a522f86bc1aeca3a4ebde0a65a1049914e53760c1`

```dockerfile
```

-	Layers:
	-	`sha256:94e7f5d4397e9c4d837b19c5727041c7f199d84bee573cb60c1f76fbfe39e3f0`  
		Last Modified: Fri, 12 Dec 2025 00:20:41 GMT  
		Size: 915.9 KB (915886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0679192f4161cc8a9733b5905a2517d3b39a4d0813431aae1e63606bfccd37e1`  
		Last Modified: Fri, 12 Dec 2025 00:20:42 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:2b5c1683b2644bc0f3962b069552a6ee4e299162cce72dc8a18758ded5d40771
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78942570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c8d9f31ecd07666432029fe547d3ee536ca6cb4dc83bd8ff55264e2f368cc8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Thu, 11 Dec 2025 21:21:24 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 11 Dec 2025 21:21:26 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Thu, 11 Dec 2025 21:21:26 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 11 Dec 2025 21:21:26 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Thu, 11 Dec 2025 21:21:28 GMT
ENV INFLUXDB_VERSION=2.8.0
# Thu, 11 Dec 2025 21:21:28 GMT
ENV INFLUXDB_PR=-2
# Thu, 11 Dec 2025 21:21:28 GMT
ENV INFLUXDB_PV=2.8.0-2
# Thu, 11 Dec 2025 21:21:28 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 11 Dec 2025 21:21:28 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Thu, 11 Dec 2025 21:21:29 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 11 Dec 2025 21:21:30 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 11 Dec 2025 21:21:30 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Dec 2025 21:21:30 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 11 Dec 2025 21:21:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Dec 2025 21:21:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Dec 2025 21:21:30 GMT
CMD ["influxd"]
# Thu, 11 Dec 2025 21:21:30 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Dec 2025 21:21:30 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Dec 2025 21:21:30 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Dec 2025 21:21:30 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Dec 2025 21:21:30 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 12:04:23 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce46991d2c4c48fd52d13891e1b5eb0777120c6d83d07fcc82f06c4340cfb6ba`  
		Last Modified: Thu, 11 Dec 2025 21:21:39 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af32475cc26ad10355d0ebd8d9c80f88c7f6c44bcf28115edc647d31b95f9884`  
		Last Modified: Thu, 11 Dec 2025 21:21:40 GMT  
		Size: 9.8 MB (9822470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaafcce51f3333786fe19ee810e7107ca5c17a1a11e4b278b34d6d8989811de7`  
		Last Modified: Thu, 11 Dec 2025 21:21:40 GMT  
		Size: 5.8 MB (5790439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519b70514028425c28cf39d8baef11c310457123a628d37c437bd6661fbaad6e`  
		Last Modified: Thu, 11 Dec 2025 21:21:40 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840f20cada75ad84d27130c93e200a873f7b2f5078d5a2049be4894b3a568aa4`  
		Last Modified: Thu, 11 Dec 2025 21:22:10 GMT  
		Size: 48.2 MB (48229359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea275cc0d43ac8b796329c90b2d0397003fdf129d2fa4b0c407b9ffb957177b`  
		Last Modified: Thu, 11 Dec 2025 21:21:41 GMT  
		Size: 11.1 MB (11099994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f18f15a6ac7b5a0a7673d362af6cd43b52cfe07914127acffa738249bb566cd`  
		Last Modified: Thu, 11 Dec 2025 21:21:41 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de188f5486eb8567f178074e890509083cc993bcfb3a37457dd2300060ec14ff`  
		Last Modified: Thu, 11 Dec 2025 21:21:41 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abede7ea0d56bd3a18f4443dc825494ff3d4993f87fee95b61f6d3153eb3f702`  
		Last Modified: Thu, 11 Dec 2025 21:21:42 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:e77a7505f9f1c8c8b7b80194b833dd81001c9138a0903c7724960f3ba8ab3144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **946.2 KB (946176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbeb577948dfa768d82764b6865eefb8962787cd5730e3e137fed9cf5446383c`

```dockerfile
```

-	Layers:
	-	`sha256:cde75b715d9b30d5cfecd23a0bdfb9e19b4e7fa446afe27e1057910a31641dfe`  
		Last Modified: Fri, 12 Dec 2025 00:20:46 GMT  
		Size: 915.1 KB (915137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7b4d294b1204d82261147c85c10da7d18f3fff5439e60155204f31729b2b191`  
		Last Modified: Fri, 12 Dec 2025 00:20:46 GMT  
		Size: 31.0 KB (31039 bytes)  
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
		Last Modified: Tue, 13 Jan 2026 02:26:02 GMT  
		Size: 6.2 MB (6156948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833535523fe14972a499abd06da9a931c255b921d8cac94598fd45eba9762e79`  
		Last Modified: Tue, 13 Jan 2026 02:26:02 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332c159a27a1da2abbe5673bdaaae5ec4032a5c5001b11062a629daa347497ad`  
		Last Modified: Tue, 13 Jan 2026 02:26:02 GMT  
		Size: 1.0 MB (1012039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db699770bd0f83d68f705e2711254edb50a46ab3d57d0b6a36fadb9d6db2a6a`  
		Last Modified: Tue, 13 Jan 2026 02:26:09 GMT  
		Size: 100.2 MB (100246167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9534ab686709ee0ac5e10282ab4858eb110757e635e51655e7afc130532e92c9`  
		Last Modified: Tue, 13 Jan 2026 02:26:03 GMT  
		Size: 11.8 MB (11775886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c657c3cd1a492fd3d596b28e8112ae5d564f9f4136d3ae71cf923ee8f692ab9d`  
		Last Modified: Tue, 13 Jan 2026 02:26:01 GMT  
		Size: 207.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777d2808f71e7a654cbefb59a369679c79dddbaa1045293b793b32936cba08d6`  
		Last Modified: Tue, 13 Jan 2026 02:26:02 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e70b88d2be0f67826728e054ad05b2eec09fb666ac2086e45d3b43f020cb25`  
		Last Modified: Tue, 13 Jan 2026 02:26:02 GMT  
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
		Last Modified: Tue, 13 Jan 2026 06:22:36 GMT  
		Size: 3.0 MB (2981484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd4b7b41ef097635ebe81bfd09d63def06a891de3750e73911644724ca524236`  
		Last Modified: Tue, 13 Jan 2026 06:22:37 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:09 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff72e9f0d8c78a6aaa8d48cd6cbe9ae48d8da7536f200e4be1224b028abec803`  
		Last Modified: Tue, 13 Jan 2026 02:30:22 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:30:07 GMT  
		Size: 938.9 KB (938877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907845f7a4c6550859ec77329810dccfe6e013e5130ff40fa5a80a4a21424943`  
		Last Modified: Tue, 13 Jan 2026 02:30:15 GMT  
		Size: 96.0 MB (96041726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b8d55e3a2731c65ad178e0976341eaba8019e957fa61cb2a949b8274ff333a`  
		Last Modified: Tue, 13 Jan 2026 02:29:59 GMT  
		Size: 11.1 MB (11100385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b27d2ff162212e313a199c6085e72e0066d54afa10a2348b46cf9315a8f55b7`  
		Last Modified: Tue, 13 Jan 2026 02:30:07 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b377c1318942bc3a9d9573fb5c1e71f81aa4a87016356d5166bd1a184324b5c5`  
		Last Modified: Tue, 13 Jan 2026 02:29:59 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fe7c7cbaa7a85a5f52487deba1494326bfd479121521028d9adc3d675a48be`  
		Last Modified: Tue, 13 Jan 2026 02:30:07 GMT  
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
		Last Modified: Tue, 13 Jan 2026 06:22:41 GMT  
		Size: 3.0 MB (2980688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc16ee2543a777bc76cc1cf7ff12d22d945fcf6589e92df997e2893618926e22`  
		Last Modified: Tue, 13 Jan 2026 06:22:42 GMT  
		Size: 33.1 KB (33060 bytes)  
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
		Last Modified: Sun, 07 Dec 2025 13:55:07 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2298af3f5be87a5532b043f27cf04fb5779734556bb16f47af70b80d01bce6f9`  
		Last Modified: Wed, 08 Oct 2025 23:10:39 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53835a8d0d20cd34e4a7681b4ff49af99d05ec1c6417ae07f5f2ab28eb1d91d7`  
		Last Modified: Mon, 08 Dec 2025 00:36:49 GMT  
		Size: 9.9 MB (9862172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68829d4164c16e8135e6bf03046861f1566a9d374a3e99a820a143903d7291a`  
		Last Modified: Mon, 08 Dec 2025 00:36:47 GMT  
		Size: 6.2 MB (6156988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9072b4a07b3f8dca037d515274838693bb0e168a1fc7b3118370baabde5fb4fb`  
		Last Modified: Mon, 08 Dec 2025 00:36:47 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7b3f5da15b92af08a9ed64ddc91ab3b683642efb4ab6f3b672da89a0e1e868`  
		Last Modified: Wed, 08 Oct 2025 23:10:42 GMT  
		Size: 50.1 MB (50118379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b2ed5e22ac99676c240cb61c758189300e7929cfc6729851c369529ad53d8d`  
		Last Modified: Wed, 08 Oct 2025 23:10:41 GMT  
		Size: 11.8 MB (11773778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68db778755a7a92ab67642d92cc7aa0c820cd21e5943b496d3b32e9fd2403de7`  
		Last Modified: Mon, 08 Dec 2025 00:36:48 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d366f9033d07efa0b056a0d9362d12bf8f19cf51deec87929bb9a095810b8c21`  
		Last Modified: Wed, 08 Oct 2025 23:10:41 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024a54836f3da745e3ea2b1a54e11d6a3a24d9402e2007b4610da65910613fe2`  
		Last Modified: Wed, 08 Oct 2025 23:10:42 GMT  
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
		Last Modified: Wed, 08 Oct 2025 23:10:40 GMT  
		Size: 913.8 KB (913815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e562735d7f12f937fbcb209933eb7986ea94c4b843ec47db133b14f1a8a2bc88`  
		Last Modified: Mon, 08 Dec 2025 05:34:12 GMT  
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
		Last Modified: Wed, 08 Oct 2025 12:04:23 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e9f8ae4bf7158674e53e799e39195db08dc922549798b1c92b5db881e75950`  
		Last Modified: Sun, 07 Dec 2025 22:41:06 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db47b23aa319f26ace574a307a140d466205a9c8792ea299825977016c72027`  
		Last Modified: Sun, 07 Dec 2025 22:41:09 GMT  
		Size: 9.8 MB (9822482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e75ad98f92c131cb2c24f50a1f955f559cb081760bb3ebaba411aff5652c0b1`  
		Last Modified: Wed, 08 Oct 2025 21:55:23 GMT  
		Size: 5.8 MB (5790429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0846ab0df2a8dd47b00f9e08910902bc9137be17fc01ecb2ab92865324a0a692`  
		Last Modified: Sun, 07 Dec 2025 22:41:06 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee341d51fc6d484c991e3e387ad2bab42cc99f8c5f0c144f3548538763046b7`  
		Last Modified: Wed, 08 Oct 2025 21:55:26 GMT  
		Size: 48.0 MB (48017161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5467babbc25c511c880690592c05bf5c8bf7eb3718a0ffcbb6bb66881d449be0`  
		Last Modified: Wed, 08 Oct 2025 21:55:25 GMT  
		Size: 11.1 MB (11099994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73275e145aac044b3ee173c0907851a448d495a9d0f964f1d943e707c8a79108`  
		Last Modified: Wed, 08 Oct 2025 21:55:25 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501e2a94b5ef2caef075bbdb0a7105d248f3f7d5e3a45540947b4843f21e8702`  
		Last Modified: Sun, 07 Dec 2025 22:41:06 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0bc70a0456678acb89ee83669fb653b9be40154e9167dec954aa525d35f87c`  
		Last Modified: Sun, 07 Dec 2025 22:41:07 GMT  
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
		Last Modified: Mon, 08 Dec 2025 00:50:44 GMT  
		Size: 913.1 KB (913066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:868968715be1dde5591f2d64233e6a60defbc05776d1a13313f5f018438e6317`  
		Last Modified: Wed, 08 Oct 2025 21:55:23 GMT  
		Size: 31.0 KB (30963 bytes)  
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
		Last Modified: Tue, 13 Jan 2026 02:26:02 GMT  
		Size: 6.2 MB (6156948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833535523fe14972a499abd06da9a931c255b921d8cac94598fd45eba9762e79`  
		Last Modified: Tue, 13 Jan 2026 02:26:02 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332c159a27a1da2abbe5673bdaaae5ec4032a5c5001b11062a629daa347497ad`  
		Last Modified: Tue, 13 Jan 2026 02:26:02 GMT  
		Size: 1.0 MB (1012039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db699770bd0f83d68f705e2711254edb50a46ab3d57d0b6a36fadb9d6db2a6a`  
		Last Modified: Tue, 13 Jan 2026 02:26:09 GMT  
		Size: 100.2 MB (100246167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9534ab686709ee0ac5e10282ab4858eb110757e635e51655e7afc130532e92c9`  
		Last Modified: Tue, 13 Jan 2026 02:26:03 GMT  
		Size: 11.8 MB (11775886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c657c3cd1a492fd3d596b28e8112ae5d564f9f4136d3ae71cf923ee8f692ab9d`  
		Last Modified: Tue, 13 Jan 2026 02:26:01 GMT  
		Size: 207.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777d2808f71e7a654cbefb59a369679c79dddbaa1045293b793b32936cba08d6`  
		Last Modified: Tue, 13 Jan 2026 02:26:02 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e70b88d2be0f67826728e054ad05b2eec09fb666ac2086e45d3b43f020cb25`  
		Last Modified: Tue, 13 Jan 2026 02:26:02 GMT  
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
		Last Modified: Tue, 13 Jan 2026 06:22:36 GMT  
		Size: 3.0 MB (2981484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd4b7b41ef097635ebe81bfd09d63def06a891de3750e73911644724ca524236`  
		Last Modified: Tue, 13 Jan 2026 06:22:37 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:09 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff72e9f0d8c78a6aaa8d48cd6cbe9ae48d8da7536f200e4be1224b028abec803`  
		Last Modified: Tue, 13 Jan 2026 02:30:22 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:30:07 GMT  
		Size: 938.9 KB (938877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907845f7a4c6550859ec77329810dccfe6e013e5130ff40fa5a80a4a21424943`  
		Last Modified: Tue, 13 Jan 2026 02:30:15 GMT  
		Size: 96.0 MB (96041726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b8d55e3a2731c65ad178e0976341eaba8019e957fa61cb2a949b8274ff333a`  
		Last Modified: Tue, 13 Jan 2026 02:29:59 GMT  
		Size: 11.1 MB (11100385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b27d2ff162212e313a199c6085e72e0066d54afa10a2348b46cf9315a8f55b7`  
		Last Modified: Tue, 13 Jan 2026 02:30:07 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b377c1318942bc3a9d9573fb5c1e71f81aa4a87016356d5166bd1a184324b5c5`  
		Last Modified: Tue, 13 Jan 2026 02:29:59 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fe7c7cbaa7a85a5f52487deba1494326bfd479121521028d9adc3d675a48be`  
		Last Modified: Tue, 13 Jan 2026 02:30:07 GMT  
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
		Last Modified: Tue, 13 Jan 2026 06:22:41 GMT  
		Size: 3.0 MB (2980688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc16ee2543a777bc76cc1cf7ff12d22d945fcf6589e92df997e2893618926e22`  
		Last Modified: Tue, 13 Jan 2026 06:22:42 GMT  
		Size: 33.1 KB (33060 bytes)  
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
		Last Modified: Sun, 07 Dec 2025 13:55:07 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2298af3f5be87a5532b043f27cf04fb5779734556bb16f47af70b80d01bce6f9`  
		Last Modified: Wed, 08 Oct 2025 23:10:39 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53835a8d0d20cd34e4a7681b4ff49af99d05ec1c6417ae07f5f2ab28eb1d91d7`  
		Last Modified: Mon, 08 Dec 2025 00:36:49 GMT  
		Size: 9.9 MB (9862172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68829d4164c16e8135e6bf03046861f1566a9d374a3e99a820a143903d7291a`  
		Last Modified: Mon, 08 Dec 2025 00:36:47 GMT  
		Size: 6.2 MB (6156988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9072b4a07b3f8dca037d515274838693bb0e168a1fc7b3118370baabde5fb4fb`  
		Last Modified: Mon, 08 Dec 2025 00:36:47 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7b3f5da15b92af08a9ed64ddc91ab3b683642efb4ab6f3b672da89a0e1e868`  
		Last Modified: Wed, 08 Oct 2025 23:10:42 GMT  
		Size: 50.1 MB (50118379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b2ed5e22ac99676c240cb61c758189300e7929cfc6729851c369529ad53d8d`  
		Last Modified: Wed, 08 Oct 2025 23:10:41 GMT  
		Size: 11.8 MB (11773778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68db778755a7a92ab67642d92cc7aa0c820cd21e5943b496d3b32e9fd2403de7`  
		Last Modified: Mon, 08 Dec 2025 00:36:48 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d366f9033d07efa0b056a0d9362d12bf8f19cf51deec87929bb9a095810b8c21`  
		Last Modified: Wed, 08 Oct 2025 23:10:41 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024a54836f3da745e3ea2b1a54e11d6a3a24d9402e2007b4610da65910613fe2`  
		Last Modified: Wed, 08 Oct 2025 23:10:42 GMT  
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
		Last Modified: Wed, 08 Oct 2025 23:10:40 GMT  
		Size: 913.8 KB (913815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e562735d7f12f937fbcb209933eb7986ea94c4b843ec47db133b14f1a8a2bc88`  
		Last Modified: Mon, 08 Dec 2025 05:34:12 GMT  
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
		Last Modified: Wed, 08 Oct 2025 12:04:23 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e9f8ae4bf7158674e53e799e39195db08dc922549798b1c92b5db881e75950`  
		Last Modified: Sun, 07 Dec 2025 22:41:06 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db47b23aa319f26ace574a307a140d466205a9c8792ea299825977016c72027`  
		Last Modified: Sun, 07 Dec 2025 22:41:09 GMT  
		Size: 9.8 MB (9822482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e75ad98f92c131cb2c24f50a1f955f559cb081760bb3ebaba411aff5652c0b1`  
		Last Modified: Wed, 08 Oct 2025 21:55:23 GMT  
		Size: 5.8 MB (5790429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0846ab0df2a8dd47b00f9e08910902bc9137be17fc01ecb2ab92865324a0a692`  
		Last Modified: Sun, 07 Dec 2025 22:41:06 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee341d51fc6d484c991e3e387ad2bab42cc99f8c5f0c144f3548538763046b7`  
		Last Modified: Wed, 08 Oct 2025 21:55:26 GMT  
		Size: 48.0 MB (48017161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5467babbc25c511c880690592c05bf5c8bf7eb3718a0ffcbb6bb66881d449be0`  
		Last Modified: Wed, 08 Oct 2025 21:55:25 GMT  
		Size: 11.1 MB (11099994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73275e145aac044b3ee173c0907851a448d495a9d0f964f1d943e707c8a79108`  
		Last Modified: Wed, 08 Oct 2025 21:55:25 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501e2a94b5ef2caef075bbdb0a7105d248f3f7d5e3a45540947b4843f21e8702`  
		Last Modified: Sun, 07 Dec 2025 22:41:06 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0bc70a0456678acb89ee83669fb653b9be40154e9167dec954aa525d35f87c`  
		Last Modified: Sun, 07 Dec 2025 22:41:07 GMT  
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
		Last Modified: Mon, 08 Dec 2025 00:50:44 GMT  
		Size: 913.1 KB (913066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:868968715be1dde5591f2d64233e6a60defbc05776d1a13313f5f018438e6317`  
		Last Modified: Wed, 08 Oct 2025 21:55:23 GMT  
		Size: 31.0 KB (30963 bytes)  
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
		Last Modified: Tue, 13 Jan 2026 02:27:42 GMT  
		Size: 9.8 MB (9797566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69611437006e7e5d57518505b16149f02d6de08bb4fd641a35b57ff9538e7019`  
		Last Modified: Tue, 13 Jan 2026 02:27:31 GMT  
		Size: 6.2 MB (6156960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c709ee61b6d0aa5181b6f1bd280d67fb9c9c47f750adaeb54071159645ed361`  
		Last Modified: Tue, 13 Jan 2026 02:27:39 GMT  
		Size: 3.2 KB (3222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac01bb46173c8f94318c49396692514d025f567953e9c10e9861bcd55cbaae7`  
		Last Modified: Tue, 13 Jan 2026 02:27:40 GMT  
		Size: 811.5 KB (811477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7f5e8c960d80d311f115d887a80722c31f9018ba0067431f173e26de26051e`  
		Last Modified: Tue, 13 Jan 2026 02:27:55 GMT  
		Size: 50.5 MB (50451829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99ba881f7de4d8bf0add7733db05bf697e3ace7f5cffc314be099705f02ea79`  
		Last Modified: Tue, 13 Jan 2026 02:27:41 GMT  
		Size: 11.8 MB (11775880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeac49fa47842b0d7d0dc90119df9ea3676af835768d021a2069c65930300b22`  
		Last Modified: Tue, 13 Jan 2026 02:27:40 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:09 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff72e9f0d8c78a6aaa8d48cd6cbe9ae48d8da7536f200e4be1224b028abec803`  
		Last Modified: Tue, 13 Jan 2026 02:30:22 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:31:10 GMT  
		Size: 766.4 KB (766370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53a3a9efe7fd59838f76f744fc33e7b7848a8077bf8e265caf35bf5d731caa4`  
		Last Modified: Tue, 13 Jan 2026 02:31:05 GMT  
		Size: 48.2 MB (48229552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68b008dfe291566d50ddf5c7020299a3060b1d20c79012275b130b78a36b807`  
		Last Modified: Tue, 13 Jan 2026 02:31:12 GMT  
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
$ docker pull influxdb@sha256:fb537cf0d57937a57eac33efd079ae5b36a1d35437dc1eba1ecb8800a352b62a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.8-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:2e03ae8e0b59c4a7b060238e4246b8a003c7b429019bdce39c024b1d5b056afb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81890627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:926890384ff7b559be8bac4f1e03f0d4ee3ca31ece6f2d938f483b97131ce363`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Thu, 11 Dec 2025 21:21:44 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 11 Dec 2025 21:21:45 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Thu, 11 Dec 2025 21:21:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 11 Dec 2025 21:21:45 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Thu, 11 Dec 2025 21:21:47 GMT
ENV INFLUXDB_VERSION=2.8.0
# Thu, 11 Dec 2025 21:21:47 GMT
ENV INFLUXDB_PR=-2
# Thu, 11 Dec 2025 21:21:47 GMT
ENV INFLUXDB_PV=2.8.0-2
# Thu, 11 Dec 2025 21:21:47 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 11 Dec 2025 21:21:47 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Thu, 11 Dec 2025 21:21:48 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 11 Dec 2025 21:21:48 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 11 Dec 2025 21:21:48 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Dec 2025 21:21:48 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 11 Dec 2025 21:21:48 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Dec 2025 21:21:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Dec 2025 21:21:48 GMT
CMD ["influxd"]
# Thu, 11 Dec 2025 21:21:48 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Dec 2025 21:21:48 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Dec 2025 21:21:48 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Dec 2025 21:21:48 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Dec 2025 21:21:48 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Sun, 07 Dec 2025 13:55:07 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10f7056aa72ef8463a31e6afa1dec61d746d3cec587e13de9bcf28396caa037`  
		Last Modified: Thu, 11 Dec 2025 21:22:07 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d56024c76d43582ac2f12311746a23ad83f148c5b42da7c957da34b6cdac498`  
		Last Modified: Thu, 11 Dec 2025 21:21:58 GMT  
		Size: 9.9 MB (9862216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71475ef0f8f2c5f8c394cdda52333392709fc87e769397a0389fb1bb743d399b`  
		Last Modified: Thu, 11 Dec 2025 21:21:58 GMT  
		Size: 6.2 MB (6156990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a315475c1c17f7a223ea2b8a1d9a1985ce438a3bae2dae153555a5d457b051c1`  
		Last Modified: Thu, 11 Dec 2025 21:21:58 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75bc9021d0ef61725243ae72546a2a75243c5424fa7d0fc53f20c469d377cba3`  
		Last Modified: Thu, 11 Dec 2025 21:22:13 GMT  
		Size: 50.4 MB (50447116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c548f8f09a0ce506a8c2e69d75de76926e996dfe9a46448c756d6647e8a04c`  
		Last Modified: Thu, 11 Dec 2025 21:22:00 GMT  
		Size: 11.8 MB (11773781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e504a5513a054282de4e3d4006c910c7003f8804e45058cf073a0422f0212d1`  
		Last Modified: Thu, 11 Dec 2025 21:22:07 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d818200c6c4e7df4884a358b6f80bca9c959914eced87214ae2c44e58fd35b`  
		Last Modified: Thu, 11 Dec 2025 21:22:00 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d217bc1e57c2c30506373ba1fe825b2fe61e5f1ae8585753f0ea1989f9c9f31f`  
		Last Modified: Thu, 11 Dec 2025 21:22:07 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:fd0843ea7d0b590a344252c4735a3b5c3259175326169b796c7863dc7e9409fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **946.7 KB (946733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25347cf7627bd9599b9ab13a522f86bc1aeca3a4ebde0a65a1049914e53760c1`

```dockerfile
```

-	Layers:
	-	`sha256:94e7f5d4397e9c4d837b19c5727041c7f199d84bee573cb60c1f76fbfe39e3f0`  
		Last Modified: Fri, 12 Dec 2025 00:20:41 GMT  
		Size: 915.9 KB (915886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0679192f4161cc8a9733b5905a2517d3b39a4d0813431aae1e63606bfccd37e1`  
		Last Modified: Fri, 12 Dec 2025 00:20:42 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.8-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:2b5c1683b2644bc0f3962b069552a6ee4e299162cce72dc8a18758ded5d40771
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78942570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c8d9f31ecd07666432029fe547d3ee536ca6cb4dc83bd8ff55264e2f368cc8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Thu, 11 Dec 2025 21:21:24 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 11 Dec 2025 21:21:26 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Thu, 11 Dec 2025 21:21:26 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 11 Dec 2025 21:21:26 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Thu, 11 Dec 2025 21:21:28 GMT
ENV INFLUXDB_VERSION=2.8.0
# Thu, 11 Dec 2025 21:21:28 GMT
ENV INFLUXDB_PR=-2
# Thu, 11 Dec 2025 21:21:28 GMT
ENV INFLUXDB_PV=2.8.0-2
# Thu, 11 Dec 2025 21:21:28 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 11 Dec 2025 21:21:28 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Thu, 11 Dec 2025 21:21:29 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 11 Dec 2025 21:21:30 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 11 Dec 2025 21:21:30 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Dec 2025 21:21:30 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 11 Dec 2025 21:21:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Dec 2025 21:21:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Dec 2025 21:21:30 GMT
CMD ["influxd"]
# Thu, 11 Dec 2025 21:21:30 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Dec 2025 21:21:30 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Dec 2025 21:21:30 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Dec 2025 21:21:30 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Dec 2025 21:21:30 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 12:04:23 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce46991d2c4c48fd52d13891e1b5eb0777120c6d83d07fcc82f06c4340cfb6ba`  
		Last Modified: Thu, 11 Dec 2025 21:21:39 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af32475cc26ad10355d0ebd8d9c80f88c7f6c44bcf28115edc647d31b95f9884`  
		Last Modified: Thu, 11 Dec 2025 21:21:40 GMT  
		Size: 9.8 MB (9822470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaafcce51f3333786fe19ee810e7107ca5c17a1a11e4b278b34d6d8989811de7`  
		Last Modified: Thu, 11 Dec 2025 21:21:40 GMT  
		Size: 5.8 MB (5790439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519b70514028425c28cf39d8baef11c310457123a628d37c437bd6661fbaad6e`  
		Last Modified: Thu, 11 Dec 2025 21:21:40 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840f20cada75ad84d27130c93e200a873f7b2f5078d5a2049be4894b3a568aa4`  
		Last Modified: Thu, 11 Dec 2025 21:22:10 GMT  
		Size: 48.2 MB (48229359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea275cc0d43ac8b796329c90b2d0397003fdf129d2fa4b0c407b9ffb957177b`  
		Last Modified: Thu, 11 Dec 2025 21:21:41 GMT  
		Size: 11.1 MB (11099994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f18f15a6ac7b5a0a7673d362af6cd43b52cfe07914127acffa738249bb566cd`  
		Last Modified: Thu, 11 Dec 2025 21:21:41 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de188f5486eb8567f178074e890509083cc993bcfb3a37457dd2300060ec14ff`  
		Last Modified: Thu, 11 Dec 2025 21:21:41 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abede7ea0d56bd3a18f4443dc825494ff3d4993f87fee95b61f6d3153eb3f702`  
		Last Modified: Thu, 11 Dec 2025 21:21:42 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:e77a7505f9f1c8c8b7b80194b833dd81001c9138a0903c7724960f3ba8ab3144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **946.2 KB (946176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbeb577948dfa768d82764b6865eefb8962787cd5730e3e137fed9cf5446383c`

```dockerfile
```

-	Layers:
	-	`sha256:cde75b715d9b30d5cfecd23a0bdfb9e19b4e7fa446afe27e1057910a31641dfe`  
		Last Modified: Fri, 12 Dec 2025 00:20:46 GMT  
		Size: 915.1 KB (915137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7b4d294b1204d82261147c85c10da7d18f3fff5439e60155204f31729b2b191`  
		Last Modified: Fri, 12 Dec 2025 00:20:46 GMT  
		Size: 31.0 KB (31039 bytes)  
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
		Last Modified: Tue, 13 Jan 2026 02:27:42 GMT  
		Size: 9.8 MB (9797566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69611437006e7e5d57518505b16149f02d6de08bb4fd641a35b57ff9538e7019`  
		Last Modified: Tue, 13 Jan 2026 02:27:31 GMT  
		Size: 6.2 MB (6156960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c709ee61b6d0aa5181b6f1bd280d67fb9c9c47f750adaeb54071159645ed361`  
		Last Modified: Tue, 13 Jan 2026 02:27:39 GMT  
		Size: 3.2 KB (3222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac01bb46173c8f94318c49396692514d025f567953e9c10e9861bcd55cbaae7`  
		Last Modified: Tue, 13 Jan 2026 02:27:40 GMT  
		Size: 811.5 KB (811477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7f5e8c960d80d311f115d887a80722c31f9018ba0067431f173e26de26051e`  
		Last Modified: Tue, 13 Jan 2026 02:27:55 GMT  
		Size: 50.5 MB (50451829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99ba881f7de4d8bf0add7733db05bf697e3ace7f5cffc314be099705f02ea79`  
		Last Modified: Tue, 13 Jan 2026 02:27:41 GMT  
		Size: 11.8 MB (11775880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeac49fa47842b0d7d0dc90119df9ea3676af835768d021a2069c65930300b22`  
		Last Modified: Tue, 13 Jan 2026 02:27:40 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:09 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff72e9f0d8c78a6aaa8d48cd6cbe9ae48d8da7536f200e4be1224b028abec803`  
		Last Modified: Tue, 13 Jan 2026 02:30:22 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:31:10 GMT  
		Size: 766.4 KB (766370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53a3a9efe7fd59838f76f744fc33e7b7848a8077bf8e265caf35bf5d731caa4`  
		Last Modified: Tue, 13 Jan 2026 02:31:05 GMT  
		Size: 48.2 MB (48229552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68b008dfe291566d50ddf5c7020299a3060b1d20c79012275b130b78a36b807`  
		Last Modified: Tue, 13 Jan 2026 02:31:12 GMT  
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
$ docker pull influxdb@sha256:fb537cf0d57937a57eac33efd079ae5b36a1d35437dc1eba1ecb8800a352b62a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.8.0-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:2e03ae8e0b59c4a7b060238e4246b8a003c7b429019bdce39c024b1d5b056afb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81890627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:926890384ff7b559be8bac4f1e03f0d4ee3ca31ece6f2d938f483b97131ce363`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Thu, 11 Dec 2025 21:21:44 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 11 Dec 2025 21:21:45 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Thu, 11 Dec 2025 21:21:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 11 Dec 2025 21:21:45 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Thu, 11 Dec 2025 21:21:47 GMT
ENV INFLUXDB_VERSION=2.8.0
# Thu, 11 Dec 2025 21:21:47 GMT
ENV INFLUXDB_PR=-2
# Thu, 11 Dec 2025 21:21:47 GMT
ENV INFLUXDB_PV=2.8.0-2
# Thu, 11 Dec 2025 21:21:47 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 11 Dec 2025 21:21:47 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Thu, 11 Dec 2025 21:21:48 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 11 Dec 2025 21:21:48 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 11 Dec 2025 21:21:48 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Dec 2025 21:21:48 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 11 Dec 2025 21:21:48 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Dec 2025 21:21:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Dec 2025 21:21:48 GMT
CMD ["influxd"]
# Thu, 11 Dec 2025 21:21:48 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Dec 2025 21:21:48 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Dec 2025 21:21:48 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Dec 2025 21:21:48 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Dec 2025 21:21:48 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Sun, 07 Dec 2025 13:55:07 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10f7056aa72ef8463a31e6afa1dec61d746d3cec587e13de9bcf28396caa037`  
		Last Modified: Thu, 11 Dec 2025 21:22:07 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d56024c76d43582ac2f12311746a23ad83f148c5b42da7c957da34b6cdac498`  
		Last Modified: Thu, 11 Dec 2025 21:21:58 GMT  
		Size: 9.9 MB (9862216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71475ef0f8f2c5f8c394cdda52333392709fc87e769397a0389fb1bb743d399b`  
		Last Modified: Thu, 11 Dec 2025 21:21:58 GMT  
		Size: 6.2 MB (6156990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a315475c1c17f7a223ea2b8a1d9a1985ce438a3bae2dae153555a5d457b051c1`  
		Last Modified: Thu, 11 Dec 2025 21:21:58 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75bc9021d0ef61725243ae72546a2a75243c5424fa7d0fc53f20c469d377cba3`  
		Last Modified: Thu, 11 Dec 2025 21:22:13 GMT  
		Size: 50.4 MB (50447116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c548f8f09a0ce506a8c2e69d75de76926e996dfe9a46448c756d6647e8a04c`  
		Last Modified: Thu, 11 Dec 2025 21:22:00 GMT  
		Size: 11.8 MB (11773781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e504a5513a054282de4e3d4006c910c7003f8804e45058cf073a0422f0212d1`  
		Last Modified: Thu, 11 Dec 2025 21:22:07 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d818200c6c4e7df4884a358b6f80bca9c959914eced87214ae2c44e58fd35b`  
		Last Modified: Thu, 11 Dec 2025 21:22:00 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d217bc1e57c2c30506373ba1fe825b2fe61e5f1ae8585753f0ea1989f9c9f31f`  
		Last Modified: Thu, 11 Dec 2025 21:22:07 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8.0-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:fd0843ea7d0b590a344252c4735a3b5c3259175326169b796c7863dc7e9409fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **946.7 KB (946733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25347cf7627bd9599b9ab13a522f86bc1aeca3a4ebde0a65a1049914e53760c1`

```dockerfile
```

-	Layers:
	-	`sha256:94e7f5d4397e9c4d837b19c5727041c7f199d84bee573cb60c1f76fbfe39e3f0`  
		Last Modified: Fri, 12 Dec 2025 00:20:41 GMT  
		Size: 915.9 KB (915886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0679192f4161cc8a9733b5905a2517d3b39a4d0813431aae1e63606bfccd37e1`  
		Last Modified: Fri, 12 Dec 2025 00:20:42 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.8.0-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:2b5c1683b2644bc0f3962b069552a6ee4e299162cce72dc8a18758ded5d40771
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78942570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c8d9f31ecd07666432029fe547d3ee536ca6cb4dc83bd8ff55264e2f368cc8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Thu, 11 Dec 2025 21:21:24 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 11 Dec 2025 21:21:26 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Thu, 11 Dec 2025 21:21:26 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 11 Dec 2025 21:21:26 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Thu, 11 Dec 2025 21:21:28 GMT
ENV INFLUXDB_VERSION=2.8.0
# Thu, 11 Dec 2025 21:21:28 GMT
ENV INFLUXDB_PR=-2
# Thu, 11 Dec 2025 21:21:28 GMT
ENV INFLUXDB_PV=2.8.0-2
# Thu, 11 Dec 2025 21:21:28 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 11 Dec 2025 21:21:28 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Thu, 11 Dec 2025 21:21:29 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 11 Dec 2025 21:21:30 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 11 Dec 2025 21:21:30 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Dec 2025 21:21:30 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 11 Dec 2025 21:21:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Dec 2025 21:21:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Dec 2025 21:21:30 GMT
CMD ["influxd"]
# Thu, 11 Dec 2025 21:21:30 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Dec 2025 21:21:30 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Dec 2025 21:21:30 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Dec 2025 21:21:30 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Dec 2025 21:21:30 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 12:04:23 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce46991d2c4c48fd52d13891e1b5eb0777120c6d83d07fcc82f06c4340cfb6ba`  
		Last Modified: Thu, 11 Dec 2025 21:21:39 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af32475cc26ad10355d0ebd8d9c80f88c7f6c44bcf28115edc647d31b95f9884`  
		Last Modified: Thu, 11 Dec 2025 21:21:40 GMT  
		Size: 9.8 MB (9822470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaafcce51f3333786fe19ee810e7107ca5c17a1a11e4b278b34d6d8989811de7`  
		Last Modified: Thu, 11 Dec 2025 21:21:40 GMT  
		Size: 5.8 MB (5790439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519b70514028425c28cf39d8baef11c310457123a628d37c437bd6661fbaad6e`  
		Last Modified: Thu, 11 Dec 2025 21:21:40 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840f20cada75ad84d27130c93e200a873f7b2f5078d5a2049be4894b3a568aa4`  
		Last Modified: Thu, 11 Dec 2025 21:22:10 GMT  
		Size: 48.2 MB (48229359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea275cc0d43ac8b796329c90b2d0397003fdf129d2fa4b0c407b9ffb957177b`  
		Last Modified: Thu, 11 Dec 2025 21:21:41 GMT  
		Size: 11.1 MB (11099994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f18f15a6ac7b5a0a7673d362af6cd43b52cfe07914127acffa738249bb566cd`  
		Last Modified: Thu, 11 Dec 2025 21:21:41 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de188f5486eb8567f178074e890509083cc993bcfb3a37457dd2300060ec14ff`  
		Last Modified: Thu, 11 Dec 2025 21:21:41 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abede7ea0d56bd3a18f4443dc825494ff3d4993f87fee95b61f6d3153eb3f702`  
		Last Modified: Thu, 11 Dec 2025 21:21:42 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8.0-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:e77a7505f9f1c8c8b7b80194b833dd81001c9138a0903c7724960f3ba8ab3144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **946.2 KB (946176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbeb577948dfa768d82764b6865eefb8962787cd5730e3e137fed9cf5446383c`

```dockerfile
```

-	Layers:
	-	`sha256:cde75b715d9b30d5cfecd23a0bdfb9e19b4e7fa446afe27e1057910a31641dfe`  
		Last Modified: Fri, 12 Dec 2025 00:20:46 GMT  
		Size: 915.1 KB (915137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7b4d294b1204d82261147c85c10da7d18f3fff5439e60155204f31729b2b191`  
		Last Modified: Fri, 12 Dec 2025 00:20:46 GMT  
		Size: 31.0 KB (31039 bytes)  
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
		Last Modified: Tue, 13 Jan 2026 07:03:32 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb421340cf49eb838ba5a93e97c5a79263668d6c63b6e2bdec9f12f9cb2bbe70`  
		Last Modified: Thu, 15 Jan 2026 22:30:00 GMT  
		Size: 6.7 MB (6666455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c5db002efd1716598d0b566d19a173dfe7126f0914b12e1fdc180f8a7a14e2`  
		Last Modified: Thu, 15 Jan 2026 22:29:50 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6bfc81f68fb579269742625ae883af1e68a469bdc3e47f9cb250ea7d67ceeb1`  
		Last Modified: Thu, 15 Jan 2026 22:30:07 GMT  
		Size: 82.9 MB (82914588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e85a99980b8d4fa689879cdc5ef70054bed61905df3549de46260caf0e47d7b`  
		Last Modified: Thu, 15 Jan 2026 22:29:59 GMT  
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
		Last Modified: Fri, 16 Jan 2026 00:23:05 GMT  
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
		Last Modified: Fri, 16 Jan 2026 00:23:11 GMT  
		Size: 2.3 MB (2311645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50900617900957d671f02b3d04cb4b737068c8a4c247e6954ab2762edcfedfae`  
		Last Modified: Fri, 16 Jan 2026 00:23:12 GMT  
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
		Last Modified: Tue, 13 Jan 2026 07:03:32 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d80b8916ac9be25ca39f63d725fbecdb5221cc992a8f8edc501e20aa7f6cdd`  
		Last Modified: Thu, 15 Jan 2026 22:30:24 GMT  
		Size: 6.7 MB (6666466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86baf47ce3b1fa8c7b1d7b1ba023420e80d040d1a773b90f1a3f1444d5398b8`  
		Last Modified: Thu, 15 Jan 2026 22:30:14 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75782d754446062a195fd74ec4f45355abd9b48844b421553b76d0d92c2e9e6`  
		Last Modified: Thu, 15 Jan 2026 22:30:32 GMT  
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
		Last Modified: Fri, 16 Jan 2026 00:23:14 GMT  
		Size: 2.3 MB (2310611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf90cea5e6b638571c01c3c00fe6a8b6e65cbff58a178ba08a0c4a0f3c9fc4d5`  
		Last Modified: Fri, 16 Jan 2026 00:23:14 GMT  
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
		Last Modified: Thu, 15 Jan 2026 22:32:25 GMT  
		Size: 6.7 MB (6678021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a2eb424397e2fd233b9e3e45d8e2e2ff184ac156d640257caac83c500bd03b`  
		Last Modified: Thu, 15 Jan 2026 22:32:24 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c9c7ab39edbfbc219f93a01abd342c7aa9ae427a6e3c461e19bc610c55633c`  
		Last Modified: Thu, 15 Jan 2026 22:32:19 GMT  
		Size: 82.7 MB (82698149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124f15f88b8a4272c18117de13ad2ba7f3853d372748c6fea818c9336b9023fb`  
		Last Modified: Thu, 15 Jan 2026 22:32:24 GMT  
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
		Last Modified: Fri, 16 Jan 2026 00:23:18 GMT  
		Size: 2.3 MB (2311693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e36fbb81eb4a33ce5bfce27a827062a0b8d553c1d9ca2e76dc9b865f51041ac`  
		Last Modified: Fri, 16 Jan 2026 00:23:19 GMT  
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
		Last Modified: Tue, 13 Jan 2026 07:03:32 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb421340cf49eb838ba5a93e97c5a79263668d6c63b6e2bdec9f12f9cb2bbe70`  
		Last Modified: Thu, 15 Jan 2026 22:30:00 GMT  
		Size: 6.7 MB (6666455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c5db002efd1716598d0b566d19a173dfe7126f0914b12e1fdc180f8a7a14e2`  
		Last Modified: Thu, 15 Jan 2026 22:29:50 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6bfc81f68fb579269742625ae883af1e68a469bdc3e47f9cb250ea7d67ceeb1`  
		Last Modified: Thu, 15 Jan 2026 22:30:07 GMT  
		Size: 82.9 MB (82914588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e85a99980b8d4fa689879cdc5ef70054bed61905df3549de46260caf0e47d7b`  
		Last Modified: Thu, 15 Jan 2026 22:29:59 GMT  
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
		Last Modified: Fri, 16 Jan 2026 00:23:05 GMT  
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
		Last Modified: Fri, 16 Jan 2026 00:23:11 GMT  
		Size: 2.3 MB (2311645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50900617900957d671f02b3d04cb4b737068c8a4c247e6954ab2762edcfedfae`  
		Last Modified: Fri, 16 Jan 2026 00:23:12 GMT  
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
		Last Modified: Tue, 13 Jan 2026 07:03:32 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d80b8916ac9be25ca39f63d725fbecdb5221cc992a8f8edc501e20aa7f6cdd`  
		Last Modified: Thu, 15 Jan 2026 22:30:24 GMT  
		Size: 6.7 MB (6666466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86baf47ce3b1fa8c7b1d7b1ba023420e80d040d1a773b90f1a3f1444d5398b8`  
		Last Modified: Thu, 15 Jan 2026 22:30:14 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75782d754446062a195fd74ec4f45355abd9b48844b421553b76d0d92c2e9e6`  
		Last Modified: Thu, 15 Jan 2026 22:30:32 GMT  
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
		Last Modified: Fri, 16 Jan 2026 00:23:14 GMT  
		Size: 2.3 MB (2310611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf90cea5e6b638571c01c3c00fe6a8b6e65cbff58a178ba08a0c4a0f3c9fc4d5`  
		Last Modified: Fri, 16 Jan 2026 00:23:14 GMT  
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
		Last Modified: Thu, 15 Jan 2026 22:32:25 GMT  
		Size: 6.7 MB (6678021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a2eb424397e2fd233b9e3e45d8e2e2ff184ac156d640257caac83c500bd03b`  
		Last Modified: Thu, 15 Jan 2026 22:32:24 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c9c7ab39edbfbc219f93a01abd342c7aa9ae427a6e3c461e19bc610c55633c`  
		Last Modified: Thu, 15 Jan 2026 22:32:19 GMT  
		Size: 82.7 MB (82698149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124f15f88b8a4272c18117de13ad2ba7f3853d372748c6fea818c9336b9023fb`  
		Last Modified: Thu, 15 Jan 2026 22:32:24 GMT  
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
		Last Modified: Fri, 16 Jan 2026 00:23:18 GMT  
		Size: 2.3 MB (2311693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e36fbb81eb4a33ce5bfce27a827062a0b8d553c1d9ca2e76dc9b865f51041ac`  
		Last Modified: Fri, 16 Jan 2026 00:23:19 GMT  
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
		Last Modified: Tue, 13 Jan 2026 07:03:32 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb421340cf49eb838ba5a93e97c5a79263668d6c63b6e2bdec9f12f9cb2bbe70`  
		Last Modified: Thu, 15 Jan 2026 22:30:00 GMT  
		Size: 6.7 MB (6666455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c5db002efd1716598d0b566d19a173dfe7126f0914b12e1fdc180f8a7a14e2`  
		Last Modified: Thu, 15 Jan 2026 22:29:50 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6bfc81f68fb579269742625ae883af1e68a469bdc3e47f9cb250ea7d67ceeb1`  
		Last Modified: Thu, 15 Jan 2026 22:30:07 GMT  
		Size: 82.9 MB (82914588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e85a99980b8d4fa689879cdc5ef70054bed61905df3549de46260caf0e47d7b`  
		Last Modified: Thu, 15 Jan 2026 22:29:59 GMT  
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
		Last Modified: Fri, 16 Jan 2026 00:23:05 GMT  
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
		Last Modified: Fri, 16 Jan 2026 00:23:11 GMT  
		Size: 2.3 MB (2311645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50900617900957d671f02b3d04cb4b737068c8a4c247e6954ab2762edcfedfae`  
		Last Modified: Fri, 16 Jan 2026 00:23:12 GMT  
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
		Last Modified: Tue, 13 Jan 2026 07:03:32 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d80b8916ac9be25ca39f63d725fbecdb5221cc992a8f8edc501e20aa7f6cdd`  
		Last Modified: Thu, 15 Jan 2026 22:30:24 GMT  
		Size: 6.7 MB (6666466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86baf47ce3b1fa8c7b1d7b1ba023420e80d040d1a773b90f1a3f1444d5398b8`  
		Last Modified: Thu, 15 Jan 2026 22:30:14 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75782d754446062a195fd74ec4f45355abd9b48844b421553b76d0d92c2e9e6`  
		Last Modified: Thu, 15 Jan 2026 22:30:32 GMT  
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
		Last Modified: Fri, 16 Jan 2026 00:23:14 GMT  
		Size: 2.3 MB (2310611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf90cea5e6b638571c01c3c00fe6a8b6e65cbff58a178ba08a0c4a0f3c9fc4d5`  
		Last Modified: Fri, 16 Jan 2026 00:23:14 GMT  
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
		Last Modified: Thu, 15 Jan 2026 22:32:25 GMT  
		Size: 6.7 MB (6678021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a2eb424397e2fd233b9e3e45d8e2e2ff184ac156d640257caac83c500bd03b`  
		Last Modified: Thu, 15 Jan 2026 22:32:24 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c9c7ab39edbfbc219f93a01abd342c7aa9ae427a6e3c461e19bc610c55633c`  
		Last Modified: Thu, 15 Jan 2026 22:32:19 GMT  
		Size: 82.7 MB (82698149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124f15f88b8a4272c18117de13ad2ba7f3853d372748c6fea818c9336b9023fb`  
		Last Modified: Thu, 15 Jan 2026 22:32:24 GMT  
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
		Last Modified: Fri, 16 Jan 2026 00:23:18 GMT  
		Size: 2.3 MB (2311693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e36fbb81eb4a33ce5bfce27a827062a0b8d553c1d9ca2e76dc9b865f51041ac`  
		Last Modified: Fri, 16 Jan 2026 00:23:19 GMT  
		Size: 17.9 KB (17946 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:fb537cf0d57937a57eac33efd079ae5b36a1d35437dc1eba1ecb8800a352b62a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:2e03ae8e0b59c4a7b060238e4246b8a003c7b429019bdce39c024b1d5b056afb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81890627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:926890384ff7b559be8bac4f1e03f0d4ee3ca31ece6f2d938f483b97131ce363`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Thu, 11 Dec 2025 21:21:44 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 11 Dec 2025 21:21:45 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Thu, 11 Dec 2025 21:21:45 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 11 Dec 2025 21:21:45 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Thu, 11 Dec 2025 21:21:47 GMT
ENV INFLUXDB_VERSION=2.8.0
# Thu, 11 Dec 2025 21:21:47 GMT
ENV INFLUXDB_PR=-2
# Thu, 11 Dec 2025 21:21:47 GMT
ENV INFLUXDB_PV=2.8.0-2
# Thu, 11 Dec 2025 21:21:47 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 11 Dec 2025 21:21:47 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Thu, 11 Dec 2025 21:21:48 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 11 Dec 2025 21:21:48 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 11 Dec 2025 21:21:48 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Dec 2025 21:21:48 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 11 Dec 2025 21:21:48 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Dec 2025 21:21:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Dec 2025 21:21:48 GMT
CMD ["influxd"]
# Thu, 11 Dec 2025 21:21:48 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Dec 2025 21:21:48 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Dec 2025 21:21:48 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Dec 2025 21:21:48 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Dec 2025 21:21:48 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Sun, 07 Dec 2025 13:55:07 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10f7056aa72ef8463a31e6afa1dec61d746d3cec587e13de9bcf28396caa037`  
		Last Modified: Thu, 11 Dec 2025 21:22:07 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d56024c76d43582ac2f12311746a23ad83f148c5b42da7c957da34b6cdac498`  
		Last Modified: Thu, 11 Dec 2025 21:21:58 GMT  
		Size: 9.9 MB (9862216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71475ef0f8f2c5f8c394cdda52333392709fc87e769397a0389fb1bb743d399b`  
		Last Modified: Thu, 11 Dec 2025 21:21:58 GMT  
		Size: 6.2 MB (6156990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a315475c1c17f7a223ea2b8a1d9a1985ce438a3bae2dae153555a5d457b051c1`  
		Last Modified: Thu, 11 Dec 2025 21:21:58 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75bc9021d0ef61725243ae72546a2a75243c5424fa7d0fc53f20c469d377cba3`  
		Last Modified: Thu, 11 Dec 2025 21:22:13 GMT  
		Size: 50.4 MB (50447116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c548f8f09a0ce506a8c2e69d75de76926e996dfe9a46448c756d6647e8a04c`  
		Last Modified: Thu, 11 Dec 2025 21:22:00 GMT  
		Size: 11.8 MB (11773781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e504a5513a054282de4e3d4006c910c7003f8804e45058cf073a0422f0212d1`  
		Last Modified: Thu, 11 Dec 2025 21:22:07 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d818200c6c4e7df4884a358b6f80bca9c959914eced87214ae2c44e58fd35b`  
		Last Modified: Thu, 11 Dec 2025 21:22:00 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d217bc1e57c2c30506373ba1fe825b2fe61e5f1ae8585753f0ea1989f9c9f31f`  
		Last Modified: Thu, 11 Dec 2025 21:22:07 GMT  
		Size: 6.3 KB (6282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:fd0843ea7d0b590a344252c4735a3b5c3259175326169b796c7863dc7e9409fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **946.7 KB (946733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25347cf7627bd9599b9ab13a522f86bc1aeca3a4ebde0a65a1049914e53760c1`

```dockerfile
```

-	Layers:
	-	`sha256:94e7f5d4397e9c4d837b19c5727041c7f199d84bee573cb60c1f76fbfe39e3f0`  
		Last Modified: Fri, 12 Dec 2025 00:20:41 GMT  
		Size: 915.9 KB (915886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0679192f4161cc8a9733b5905a2517d3b39a4d0813431aae1e63606bfccd37e1`  
		Last Modified: Fri, 12 Dec 2025 00:20:42 GMT  
		Size: 30.8 KB (30847 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:2b5c1683b2644bc0f3962b069552a6ee4e299162cce72dc8a18758ded5d40771
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78942570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c8d9f31ecd07666432029fe547d3ee536ca6cb4dc83bd8ff55264e2f368cc8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Thu, 11 Dec 2025 21:21:24 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Thu, 11 Dec 2025 21:21:26 GMT
RUN apk add --no-cache       bash       ca-certificates       curl       gnupg       run-parts       su-exec       tzdata &&     update-ca-certificates # buildkit
# Thu, 11 Dec 2025 21:21:26 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Thu, 11 Dec 2025 21:21:26 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb # buildkit
# Thu, 11 Dec 2025 21:21:28 GMT
ENV INFLUXDB_VERSION=2.8.0
# Thu, 11 Dec 2025 21:21:28 GMT
ENV INFLUXDB_PR=-2
# Thu, 11 Dec 2025 21:21:28 GMT
ENV INFLUXDB_PV=2.8.0-2
# Thu, 11 Dec 2025 21:21:28 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&    curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Thu, 11 Dec 2025 21:21:28 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Thu, 11 Dec 2025 21:21:29 GMT
RUN case "$(apk --print-arch)" in       x86_64)  arch=amd64 ;;       aarch64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Thu, 11 Dec 2025 21:21:30 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Thu, 11 Dec 2025 21:21:30 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 11 Dec 2025 21:21:30 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Thu, 11 Dec 2025 21:21:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Dec 2025 21:21:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Dec 2025 21:21:30 GMT
CMD ["influxd"]
# Thu, 11 Dec 2025 21:21:30 GMT
EXPOSE map[8086/tcp:{}]
# Thu, 11 Dec 2025 21:21:30 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 11 Dec 2025 21:21:30 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 11 Dec 2025 21:21:30 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 11 Dec 2025 21:21:30 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 12:04:23 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce46991d2c4c48fd52d13891e1b5eb0777120c6d83d07fcc82f06c4340cfb6ba`  
		Last Modified: Thu, 11 Dec 2025 21:21:39 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af32475cc26ad10355d0ebd8d9c80f88c7f6c44bcf28115edc647d31b95f9884`  
		Last Modified: Thu, 11 Dec 2025 21:21:40 GMT  
		Size: 9.8 MB (9822470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaafcce51f3333786fe19ee810e7107ca5c17a1a11e4b278b34d6d8989811de7`  
		Last Modified: Thu, 11 Dec 2025 21:21:40 GMT  
		Size: 5.8 MB (5790439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519b70514028425c28cf39d8baef11c310457123a628d37c437bd6661fbaad6e`  
		Last Modified: Thu, 11 Dec 2025 21:21:40 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840f20cada75ad84d27130c93e200a873f7b2f5078d5a2049be4894b3a568aa4`  
		Last Modified: Thu, 11 Dec 2025 21:22:10 GMT  
		Size: 48.2 MB (48229359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea275cc0d43ac8b796329c90b2d0397003fdf129d2fa4b0c407b9ffb957177b`  
		Last Modified: Thu, 11 Dec 2025 21:21:41 GMT  
		Size: 11.1 MB (11099994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f18f15a6ac7b5a0a7673d362af6cd43b52cfe07914127acffa738249bb566cd`  
		Last Modified: Thu, 11 Dec 2025 21:21:41 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de188f5486eb8567f178074e890509083cc993bcfb3a37457dd2300060ec14ff`  
		Last Modified: Thu, 11 Dec 2025 21:21:41 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abede7ea0d56bd3a18f4443dc825494ff3d4993f87fee95b61f6d3153eb3f702`  
		Last Modified: Thu, 11 Dec 2025 21:21:42 GMT  
		Size: 6.3 KB (6281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:e77a7505f9f1c8c8b7b80194b833dd81001c9138a0903c7724960f3ba8ab3144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **946.2 KB (946176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbeb577948dfa768d82764b6865eefb8962787cd5730e3e137fed9cf5446383c`

```dockerfile
```

-	Layers:
	-	`sha256:cde75b715d9b30d5cfecd23a0bdfb9e19b4e7fa446afe27e1057910a31641dfe`  
		Last Modified: Fri, 12 Dec 2025 00:20:46 GMT  
		Size: 915.1 KB (915137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7b4d294b1204d82261147c85c10da7d18f3fff5439e60155204f31729b2b191`  
		Last Modified: Fri, 12 Dec 2025 00:20:46 GMT  
		Size: 31.0 KB (31039 bytes)  
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
		Last Modified: Tue, 13 Jan 2026 07:03:32 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb421340cf49eb838ba5a93e97c5a79263668d6c63b6e2bdec9f12f9cb2bbe70`  
		Last Modified: Thu, 15 Jan 2026 22:30:00 GMT  
		Size: 6.7 MB (6666455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c5db002efd1716598d0b566d19a173dfe7126f0914b12e1fdc180f8a7a14e2`  
		Last Modified: Thu, 15 Jan 2026 22:29:50 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6bfc81f68fb579269742625ae883af1e68a469bdc3e47f9cb250ea7d67ceeb1`  
		Last Modified: Thu, 15 Jan 2026 22:30:07 GMT  
		Size: 82.9 MB (82914588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e85a99980b8d4fa689879cdc5ef70054bed61905df3549de46260caf0e47d7b`  
		Last Modified: Thu, 15 Jan 2026 22:29:59 GMT  
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
		Last Modified: Fri, 16 Jan 2026 00:23:05 GMT  
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
		Last Modified: Fri, 16 Jan 2026 00:23:11 GMT  
		Size: 2.3 MB (2311645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50900617900957d671f02b3d04cb4b737068c8a4c247e6954ab2762edcfedfae`  
		Last Modified: Fri, 16 Jan 2026 00:23:12 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:09:06 GMT  
		Size: 24.0 MB (24036867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66c83e9d2d95ae7bb8cae9f8b46bff3d99ebbbdce310b651807fcd051a37ba0`  
		Last Modified: Tue, 13 Jan 2026 04:02:15 GMT  
		Size: 42.3 MB (42319809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485ded8552cc8df9c3417e10f8333c7f5f414f71250ce6145d55fc4b15698edd`  
		Last Modified: Tue, 13 Jan 2026 04:02:12 GMT  
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
		Last Modified: Tue, 13 Jan 2026 06:22:06 GMT  
		Size: 14.1 KB (14077 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:data-alpine`

```console
$ docker pull influxdb@sha256:ce2ffe52a626e318a7eb9a37591b2dab8918b4b9a2db82d40376d10f49ec655c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:data-alpine` - linux; amd64

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
		Last Modified: Sun, 07 Dec 2025 13:55:07 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a3788b43dae292831ae0448a5ed504046ffa71fe7a9f09db40713951fbf944`  
		Last Modified: Wed, 08 Oct 2025 23:09:51 GMT  
		Size: 1.2 MB (1225329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e0170f82fea093122d3570e0d358e936d1db98ed05a0d6a48d33037501b351`  
		Last Modified: Tue, 09 Dec 2025 22:33:31 GMT  
		Size: 42.3 MB (42254311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b0661d8dbfc3b43d49ec386e18c197ae353dd5d5c77c548207da941ba2ee68`  
		Last Modified: Wed, 08 Oct 2025 23:09:51 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39225506d3b8f10fd5e6623059b8c1e0d7efadec626f71dcf9da78fee4f7e2a`  
		Last Modified: Wed, 08 Oct 2025 23:09:51 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d72d987f87daa2925154010870639046590c11fa247eb8c38fdd2ea9c6094b`  
		Last Modified: Wed, 08 Oct 2025 23:09:52 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:data-alpine` - unknown; unknown

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
		Last Modified: Mon, 15 Dec 2025 19:34:05 GMT  
		Size: 775.8 KB (775810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f65ff52ae85ef9fa76b501b5f6ab0974038c20801b32cc1c20d90c94d731471`  
		Last Modified: Wed, 08 Oct 2025 23:09:51 GMT  
		Size: 15.2 KB (15191 bytes)  
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
		Last Modified: Tue, 13 Jan 2026 07:03:32 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d80b8916ac9be25ca39f63d725fbecdb5221cc992a8f8edc501e20aa7f6cdd`  
		Last Modified: Thu, 15 Jan 2026 22:30:24 GMT  
		Size: 6.7 MB (6666466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86baf47ce3b1fa8c7b1d7b1ba023420e80d040d1a773b90f1a3f1444d5398b8`  
		Last Modified: Thu, 15 Jan 2026 22:30:14 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75782d754446062a195fd74ec4f45355abd9b48844b421553b76d0d92c2e9e6`  
		Last Modified: Thu, 15 Jan 2026 22:30:32 GMT  
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
		Last Modified: Fri, 16 Jan 2026 00:23:14 GMT  
		Size: 2.3 MB (2310611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf90cea5e6b638571c01c3c00fe6a8b6e65cbff58a178ba08a0c4a0f3c9fc4d5`  
		Last Modified: Fri, 16 Jan 2026 00:23:14 GMT  
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
		Last Modified: Thu, 15 Jan 2026 22:32:25 GMT  
		Size: 6.7 MB (6678021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a2eb424397e2fd233b9e3e45d8e2e2ff184ac156d640257caac83c500bd03b`  
		Last Modified: Thu, 15 Jan 2026 22:32:24 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c9c7ab39edbfbc219f93a01abd342c7aa9ae427a6e3c461e19bc610c55633c`  
		Last Modified: Thu, 15 Jan 2026 22:32:19 GMT  
		Size: 82.7 MB (82698149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124f15f88b8a4272c18117de13ad2ba7f3853d372748c6fea818c9336b9023fb`  
		Last Modified: Thu, 15 Jan 2026 22:32:24 GMT  
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
		Last Modified: Fri, 16 Jan 2026 00:23:18 GMT  
		Size: 2.3 MB (2311693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e36fbb81eb4a33ce5bfce27a827062a0b8d553c1d9ca2e76dc9b865f51041ac`  
		Last Modified: Fri, 16 Jan 2026 00:23:19 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:27:42 GMT  
		Size: 9.8 MB (9797566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69611437006e7e5d57518505b16149f02d6de08bb4fd641a35b57ff9538e7019`  
		Last Modified: Tue, 13 Jan 2026 02:27:31 GMT  
		Size: 6.2 MB (6156960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c709ee61b6d0aa5181b6f1bd280d67fb9c9c47f750adaeb54071159645ed361`  
		Last Modified: Tue, 13 Jan 2026 02:27:39 GMT  
		Size: 3.2 KB (3222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac01bb46173c8f94318c49396692514d025f567953e9c10e9861bcd55cbaae7`  
		Last Modified: Tue, 13 Jan 2026 02:27:40 GMT  
		Size: 811.5 KB (811477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7f5e8c960d80d311f115d887a80722c31f9018ba0067431f173e26de26051e`  
		Last Modified: Tue, 13 Jan 2026 02:27:55 GMT  
		Size: 50.5 MB (50451829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99ba881f7de4d8bf0add7733db05bf697e3ace7f5cffc314be099705f02ea79`  
		Last Modified: Tue, 13 Jan 2026 02:27:41 GMT  
		Size: 11.8 MB (11775880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeac49fa47842b0d7d0dc90119df9ea3676af835768d021a2069c65930300b22`  
		Last Modified: Tue, 13 Jan 2026 02:27:40 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:09 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff72e9f0d8c78a6aaa8d48cd6cbe9ae48d8da7536f200e4be1224b028abec803`  
		Last Modified: Tue, 13 Jan 2026 02:30:22 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:31:10 GMT  
		Size: 766.4 KB (766370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53a3a9efe7fd59838f76f744fc33e7b7848a8077bf8e265caf35bf5d731caa4`  
		Last Modified: Tue, 13 Jan 2026 02:31:05 GMT  
		Size: 48.2 MB (48229552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68b008dfe291566d50ddf5c7020299a3060b1d20c79012275b130b78a36b807`  
		Last Modified: Tue, 13 Jan 2026 02:31:12 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:09:06 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:02:06 GMT  
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
$ docker pull influxdb@sha256:811acdf4664b52af3f6d703e48787e2b4606ae470747606bfa84ebf6e3395179
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:meta-alpine` - linux; amd64

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
		Last Modified: Sun, 07 Dec 2025 13:55:07 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1506a520a1ca51f516d5068e753e243431efab0ef69c7b1634e53985ce44a2`  
		Last Modified: Wed, 08 Oct 2025 23:09:52 GMT  
		Size: 1.2 MB (1225337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8df8f8e418a27917114426b3d245a3728772fe30be9e1b0b609e79b9ccb3b1d`  
		Last Modified: Wed, 08 Oct 2025 23:09:52 GMT  
		Size: 18.7 MB (18722501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96fdeefb85b445c179f78bb53968e8210d7aaa4a30cccb4d6452d9ac4a7b000`  
		Last Modified: Wed, 08 Oct 2025 23:09:51 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5817ad78e6b46e06d7f07b733f09a0eddd15b789d78398b86fe406d8cd2fdf7`  
		Last Modified: Wed, 08 Oct 2025 23:09:52 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:meta-alpine` - unknown; unknown

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
		Last Modified: Mon, 15 Dec 2025 20:39:37 GMT  
		Size: 681.8 KB (681759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e71c697656e9ce6a76bcb04d0f78aff32c9bc6715c511aa163637cbd6c96a2ac`  
		Last Modified: Mon, 15 Dec 2025 20:39:37 GMT  
		Size: 13.6 KB (13577 bytes)  
		MIME: application/vnd.in-toto+json
