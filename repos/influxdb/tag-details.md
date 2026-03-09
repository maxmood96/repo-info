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
-	[`influxdb:3.8.3-core`](#influxdb383-core)
-	[`influxdb:3.8.4-enterprise`](#influxdb384-enterprise)
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
$ docker pull influxdb@sha256:ae2f7de7f60138e168f822a8d0d9ca3c7f188efc22340397d9e995dff1b204aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11` - linux; amd64

```console
$ docker pull influxdb@sha256:b454e42547c3db4198bc1a767c65dae4e35c12faad41e710b815c6f74eb75ffd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116186164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad8dacf02178045c191230a548cf18419a42f1a1bd81a3a72369981ac10322c2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:08:03 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 24 Feb 2026 20:08:12 GMT
ARG INFLUXDB_VERSION=1.11.8
# Tue, 24 Feb 2026 20:08:12 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:08:12 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 24 Feb 2026 20:08:12 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 24 Feb 2026 20:08:12 GMT
VOLUME [/var/lib/influxdb]
# Tue, 24 Feb 2026 20:08:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Feb 2026 20:08:12 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 24 Feb 2026 20:08:12 GMT
USER influxdb
# Tue, 24 Feb 2026 20:08:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 20:08:12 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab3b37e4807fe48145826511e16a527bbc4695222ceb966669a4d16729b3b94`  
		Last Modified: Tue, 24 Feb 2026 19:18:52 GMT  
		Size: 24.0 MB (24038450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea933ba36b372f3d09eb79b52541b8d38b26a7bac6be12bae3539aeb4b4998c3`  
		Last Modified: Tue, 24 Feb 2026 20:08:28 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69118c12c342928657dd021082c902bfaba26a47b279ff6f461c1fd2293cc6bc`  
		Last Modified: Tue, 24 Feb 2026 20:08:30 GMT  
		Size: 43.7 MB (43656026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a40664c9d9796cd74b7fca6a2e9b121d00562ae90d1623e8d0c611415922a65`  
		Last Modified: Tue, 24 Feb 2026 20:08:28 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d290ec38dddd962d9ae00b0fd15b8ca16ac3960030ad465388cba60d308d82b8`  
		Last Modified: Tue, 24 Feb 2026 20:08:28 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd62f917df407da0e4a8c22ef9208f5f108712c219d44016ac1998975e308ead`  
		Last Modified: Tue, 24 Feb 2026 20:08:29 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11` - unknown; unknown

```console
$ docker pull influxdb@sha256:40f7d37b4981341cdc76f53dd1f53448bf390f9b8d7a2001330c1cf27647c516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e0ca81923ec630d22081742e997d96c1f051510412a7dd523dd9f6499cc6cd`

```dockerfile
```

-	Layers:
	-	`sha256:ace4dde07fce1491b9eb8e69f405fbc1959c5736921b79debad4697ca022d46b`  
		Last Modified: Tue, 24 Feb 2026 20:08:28 GMT  
		Size: 5.1 MB (5079263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c7fa836051d8fd07485c098d1b5b52046176c33448b1ad7e6a88e6f535ccd0b`  
		Last Modified: Tue, 24 Feb 2026 20:08:28 GMT  
		Size: 15.5 KB (15486 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:d0bacb8c92eeccf60ebff76276cff5e388a99276549f4be22112919edb200063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113103673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff71a0455bef658dc65df7b18c2a4401870b7de47118ddf4a4c92c2b1db1bfb7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:24:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:18:42 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 24 Feb 2026 20:18:50 GMT
ARG INFLUXDB_VERSION=1.11.8
# Tue, 24 Feb 2026 20:18:50 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:18:50 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 24 Feb 2026 20:18:50 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 24 Feb 2026 20:18:50 GMT
VOLUME [/var/lib/influxdb]
# Tue, 24 Feb 2026 20:18:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Feb 2026 20:18:50 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 24 Feb 2026 20:18:50 GMT
USER influxdb
# Tue, 24 Feb 2026 20:18:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 20:18:50 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443d4217b87aad21c6acb58313c9038eb24571a4e9f81de2463aaf19d403a640`  
		Last Modified: Tue, 24 Feb 2026 19:24:13 GMT  
		Size: 23.6 MB (23604736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f277c4a9423fec44b999869bd2d7dbd978044732beb14c7e74556406612de82f`  
		Last Modified: Tue, 24 Feb 2026 20:19:00 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2eb97318c8c624d74d74ee1de7c4a7e7959fc091e8671b50a1ab23bb9a7954`  
		Last Modified: Tue, 24 Feb 2026 20:19:03 GMT  
		Size: 41.1 MB (41122814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51edf24dfa55da51c9058dcb7004cf7fb9959d32cd83101df950423d52626510`  
		Last Modified: Tue, 24 Feb 2026 20:19:02 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d5f1b44697e5e5cc8b9af08721a1a53cadca9a64e3125fa4a9db5ecfb87769`  
		Last Modified: Tue, 24 Feb 2026 20:19:02 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427b7cb3192e715b2b4dac5163e2c0b2bd2182e22ad02a79fccfb18ca646489d`  
		Last Modified: Tue, 24 Feb 2026 20:19:02 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11` - unknown; unknown

```console
$ docker pull influxdb@sha256:686ea774876a3690a547b2d6d1d7e0363a2b7129c3d304886394071ef3ea0af1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:101a5dc134f24a58434f44bfbe5dda796b16a3189e045686119d48a975cebf3c`

```dockerfile
```

-	Layers:
	-	`sha256:de751047819248c9f9fe3c3467a5c3fd7152329e7941d4a82b0039299573ea84`  
		Last Modified: Tue, 24 Feb 2026 20:19:02 GMT  
		Size: 5.1 MB (5078728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81128d27b85b990120b08f653d85897a87c45ac46656ddb659133c864b787489`  
		Last Modified: Tue, 24 Feb 2026 20:19:02 GMT  
		Size: 15.6 KB (15580 bytes)  
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
$ docker pull influxdb@sha256:d8b51fa9fb59edf94d707db487eaf11255581a24866d4965384381a10b33e283
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data` - linux; amd64

```console
$ docker pull influxdb@sha256:3e0d0c44caafce47757a69571d9a49dc562c51a9b566531b3f51025cd30e335e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114699812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd31cb4bd060b5c7aa0d5345dce14081bf952c4c8d4f682cc1ef075cfdb1ee20`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:08:17 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 24 Feb 2026 20:08:20 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Tue, 24 Feb 2026 20:08:20 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 24 Feb 2026 20:08:20 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 24 Feb 2026 20:08:20 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 24 Feb 2026 20:08:20 GMT
VOLUME [/var/lib/influxdb]
# Tue, 24 Feb 2026 20:08:20 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Feb 2026 20:08:20 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 24 Feb 2026 20:08:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 20:08:20 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab3b37e4807fe48145826511e16a527bbc4695222ceb966669a4d16729b3b94`  
		Last Modified: Tue, 24 Feb 2026 19:18:52 GMT  
		Size: 24.0 MB (24038450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc5cb90670ebc74fde718188aa469c885bb10cc33c5c99df988035c827e0091`  
		Last Modified: Tue, 24 Feb 2026 20:08:31 GMT  
		Size: 5.1 KB (5069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e66c095f9c253c4b8a635965e42952c3434b9ab671281d9da387bea6f373fc1`  
		Last Modified: Tue, 24 Feb 2026 20:08:32 GMT  
		Size: 42.2 MB (42165740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:989e50b78a8cd2f21a0f122fcace1d73c8f7e4a8bdb084521f5a120ae2ea5f4e`  
		Last Modified: Tue, 24 Feb 2026 20:08:31 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56213ef67ff2879b23604ed3cd9d78d020f8ded006cca27d0a12cc451a1c5c0`  
		Last Modified: Tue, 24 Feb 2026 20:08:31 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3198c88332e3b53e6956280803477d80aea6560ad87ff8f60ff88a989af119`  
		Last Modified: Tue, 24 Feb 2026 20:08:32 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:c33796a59a4e4ae13bae4b39c249d66249bacaba7df39050ab0a0fee3af084f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4699071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f328b91982ac245769eed7f42569f148f64c084dc2912c24c6f0d2047e4b69fb`

```dockerfile
```

-	Layers:
	-	`sha256:672efa04e921ac40ff0eb60e405d6ccd8610ca5584e329b00fc54ebc875b390f`  
		Last Modified: Tue, 24 Feb 2026 20:08:31 GMT  
		Size: 4.7 MB (4684406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc5a9259dc8a13fb961ea7776c2b28c6392bb5d5b20cbaf53753af49fedf8240`  
		Last Modified: Tue, 24 Feb 2026 20:08:31 GMT  
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
$ docker pull influxdb@sha256:3e14f6ce5a70a6bd0c4595bcc1c4598fef4728085d7b01d69832905127f686d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:d216c08a2141c85f2dc3a6908b550c5f14ea49d6c220ec15c59f67bfa58698ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91129003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0dec76e6b72e8188ad337ee677ff0750b09a3c8b9a0ddcbfffafade61a156af`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:08:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 24 Feb 2026 20:08:19 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Tue, 24 Feb 2026 20:08:19 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 24 Feb 2026 20:08:19 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 24 Feb 2026 20:08:19 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 24 Feb 2026 20:08:19 GMT
VOLUME [/var/lib/influxdb]
# Tue, 24 Feb 2026 20:08:19 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Feb 2026 20:08:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 20:08:19 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab3b37e4807fe48145826511e16a527bbc4695222ceb966669a4d16729b3b94`  
		Last Modified: Tue, 24 Feb 2026 19:18:52 GMT  
		Size: 24.0 MB (24038450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3532fb7b5a878a399c22cfd5eaf01899d40df24f559aa0c9455b0281b7928f`  
		Last Modified: Tue, 24 Feb 2026 20:08:28 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adff68aa719159f054bb67a1fe92fce6f3ca4342483a856bf8cc2e711911609c`  
		Last Modified: Tue, 24 Feb 2026 20:08:29 GMT  
		Size: 18.6 MB (18596141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db11e9ac6dd745b94836c69fcacfee544de585ff508bd108d2bfd81bc4033200`  
		Last Modified: Tue, 24 Feb 2026 20:08:27 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e59752c26f83c26016de3b65e274e6a52fb12cc0d45b8bd61f61b46cbe815d7`  
		Last Modified: Tue, 24 Feb 2026 20:08:28 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:18a7ba8a49a0233368a6716cbac26bc3515bd536e82746c50dcc66a2f309deb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4604273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:170766f6dcc5225a6f32adf250082efbccc1b72fb04874e4d5f6a6313ed1ced4`

```dockerfile
```

-	Layers:
	-	`sha256:3d7ddaf787b100ec11ca2c4b22ab3aad86f0f677580657874fd240de1badd477`  
		Last Modified: Tue, 24 Feb 2026 20:08:28 GMT  
		Size: 4.6 MB (4591249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:629403330a558052ee488c7ab7655799581762c673bba07af3b1e12036873a9b`  
		Last Modified: Tue, 24 Feb 2026 20:08:27 GMT  
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
$ docker pull influxdb@sha256:ae2f7de7f60138e168f822a8d0d9ca3c7f188efc22340397d9e995dff1b204aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11.8` - linux; amd64

```console
$ docker pull influxdb@sha256:b454e42547c3db4198bc1a767c65dae4e35c12faad41e710b815c6f74eb75ffd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116186164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad8dacf02178045c191230a548cf18419a42f1a1bd81a3a72369981ac10322c2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:08:03 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 24 Feb 2026 20:08:12 GMT
ARG INFLUXDB_VERSION=1.11.8
# Tue, 24 Feb 2026 20:08:12 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:08:12 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 24 Feb 2026 20:08:12 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 24 Feb 2026 20:08:12 GMT
VOLUME [/var/lib/influxdb]
# Tue, 24 Feb 2026 20:08:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Feb 2026 20:08:12 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 24 Feb 2026 20:08:12 GMT
USER influxdb
# Tue, 24 Feb 2026 20:08:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 20:08:12 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab3b37e4807fe48145826511e16a527bbc4695222ceb966669a4d16729b3b94`  
		Last Modified: Tue, 24 Feb 2026 19:18:52 GMT  
		Size: 24.0 MB (24038450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea933ba36b372f3d09eb79b52541b8d38b26a7bac6be12bae3539aeb4b4998c3`  
		Last Modified: Tue, 24 Feb 2026 20:08:28 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69118c12c342928657dd021082c902bfaba26a47b279ff6f461c1fd2293cc6bc`  
		Last Modified: Tue, 24 Feb 2026 20:08:30 GMT  
		Size: 43.7 MB (43656026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a40664c9d9796cd74b7fca6a2e9b121d00562ae90d1623e8d0c611415922a65`  
		Last Modified: Tue, 24 Feb 2026 20:08:28 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d290ec38dddd962d9ae00b0fd15b8ca16ac3960030ad465388cba60d308d82b8`  
		Last Modified: Tue, 24 Feb 2026 20:08:28 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd62f917df407da0e4a8c22ef9208f5f108712c219d44016ac1998975e308ead`  
		Last Modified: Tue, 24 Feb 2026 20:08:29 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:40f7d37b4981341cdc76f53dd1f53448bf390f9b8d7a2001330c1cf27647c516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e0ca81923ec630d22081742e997d96c1f051510412a7dd523dd9f6499cc6cd`

```dockerfile
```

-	Layers:
	-	`sha256:ace4dde07fce1491b9eb8e69f405fbc1959c5736921b79debad4697ca022d46b`  
		Last Modified: Tue, 24 Feb 2026 20:08:28 GMT  
		Size: 5.1 MB (5079263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c7fa836051d8fd07485c098d1b5b52046176c33448b1ad7e6a88e6f535ccd0b`  
		Last Modified: Tue, 24 Feb 2026 20:08:28 GMT  
		Size: 15.5 KB (15486 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:d0bacb8c92eeccf60ebff76276cff5e388a99276549f4be22112919edb200063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113103673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff71a0455bef658dc65df7b18c2a4401870b7de47118ddf4a4c92c2b1db1bfb7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:24:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:18:42 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 24 Feb 2026 20:18:50 GMT
ARG INFLUXDB_VERSION=1.11.8
# Tue, 24 Feb 2026 20:18:50 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:18:50 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 24 Feb 2026 20:18:50 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 24 Feb 2026 20:18:50 GMT
VOLUME [/var/lib/influxdb]
# Tue, 24 Feb 2026 20:18:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Feb 2026 20:18:50 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 24 Feb 2026 20:18:50 GMT
USER influxdb
# Tue, 24 Feb 2026 20:18:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 20:18:50 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443d4217b87aad21c6acb58313c9038eb24571a4e9f81de2463aaf19d403a640`  
		Last Modified: Tue, 24 Feb 2026 19:24:13 GMT  
		Size: 23.6 MB (23604736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f277c4a9423fec44b999869bd2d7dbd978044732beb14c7e74556406612de82f`  
		Last Modified: Tue, 24 Feb 2026 20:19:00 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2eb97318c8c624d74d74ee1de7c4a7e7959fc091e8671b50a1ab23bb9a7954`  
		Last Modified: Tue, 24 Feb 2026 20:19:03 GMT  
		Size: 41.1 MB (41122814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51edf24dfa55da51c9058dcb7004cf7fb9959d32cd83101df950423d52626510`  
		Last Modified: Tue, 24 Feb 2026 20:19:02 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d5f1b44697e5e5cc8b9af08721a1a53cadca9a64e3125fa4a9db5ecfb87769`  
		Last Modified: Tue, 24 Feb 2026 20:19:02 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427b7cb3192e715b2b4dac5163e2c0b2bd2182e22ad02a79fccfb18ca646489d`  
		Last Modified: Tue, 24 Feb 2026 20:19:02 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:686ea774876a3690a547b2d6d1d7e0363a2b7129c3d304886394071ef3ea0af1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:101a5dc134f24a58434f44bfbe5dda796b16a3189e045686119d48a975cebf3c`

```dockerfile
```

-	Layers:
	-	`sha256:de751047819248c9f9fe3c3467a5c3fd7152329e7941d4a82b0039299573ea84`  
		Last Modified: Tue, 24 Feb 2026 20:19:02 GMT  
		Size: 5.1 MB (5078728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81128d27b85b990120b08f653d85897a87c45ac46656ddb659133c864b787489`  
		Last Modified: Tue, 24 Feb 2026 20:19:02 GMT  
		Size: 15.6 KB (15580 bytes)  
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
$ docker pull influxdb@sha256:d8b51fa9fb59edf94d707db487eaf11255581a24866d4965384381a10b33e283
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.9-data` - linux; amd64

```console
$ docker pull influxdb@sha256:3e0d0c44caafce47757a69571d9a49dc562c51a9b566531b3f51025cd30e335e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114699812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd31cb4bd060b5c7aa0d5345dce14081bf952c4c8d4f682cc1ef075cfdb1ee20`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:08:17 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 24 Feb 2026 20:08:20 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Tue, 24 Feb 2026 20:08:20 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 24 Feb 2026 20:08:20 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 24 Feb 2026 20:08:20 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 24 Feb 2026 20:08:20 GMT
VOLUME [/var/lib/influxdb]
# Tue, 24 Feb 2026 20:08:20 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Feb 2026 20:08:20 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 24 Feb 2026 20:08:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 20:08:20 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab3b37e4807fe48145826511e16a527bbc4695222ceb966669a4d16729b3b94`  
		Last Modified: Tue, 24 Feb 2026 19:18:52 GMT  
		Size: 24.0 MB (24038450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc5cb90670ebc74fde718188aa469c885bb10cc33c5c99df988035c827e0091`  
		Last Modified: Tue, 24 Feb 2026 20:08:31 GMT  
		Size: 5.1 KB (5069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e66c095f9c253c4b8a635965e42952c3434b9ab671281d9da387bea6f373fc1`  
		Last Modified: Tue, 24 Feb 2026 20:08:32 GMT  
		Size: 42.2 MB (42165740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:989e50b78a8cd2f21a0f122fcace1d73c8f7e4a8bdb084521f5a120ae2ea5f4e`  
		Last Modified: Tue, 24 Feb 2026 20:08:31 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56213ef67ff2879b23604ed3cd9d78d020f8ded006cca27d0a12cc451a1c5c0`  
		Last Modified: Tue, 24 Feb 2026 20:08:31 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3198c88332e3b53e6956280803477d80aea6560ad87ff8f60ff88a989af119`  
		Last Modified: Tue, 24 Feb 2026 20:08:32 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.9-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:c33796a59a4e4ae13bae4b39c249d66249bacaba7df39050ab0a0fee3af084f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4699071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f328b91982ac245769eed7f42569f148f64c084dc2912c24c6f0d2047e4b69fb`

```dockerfile
```

-	Layers:
	-	`sha256:672efa04e921ac40ff0eb60e405d6ccd8610ca5584e329b00fc54ebc875b390f`  
		Last Modified: Tue, 24 Feb 2026 20:08:31 GMT  
		Size: 4.7 MB (4684406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc5a9259dc8a13fb961ea7776c2b28c6392bb5d5b20cbaf53753af49fedf8240`  
		Last Modified: Tue, 24 Feb 2026 20:08:31 GMT  
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
$ docker pull influxdb@sha256:3e14f6ce5a70a6bd0c4595bcc1c4598fef4728085d7b01d69832905127f686d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.9-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:d216c08a2141c85f2dc3a6908b550c5f14ea49d6c220ec15c59f67bfa58698ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91129003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0dec76e6b72e8188ad337ee677ff0750b09a3c8b9a0ddcbfffafade61a156af`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:08:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 24 Feb 2026 20:08:19 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Tue, 24 Feb 2026 20:08:19 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Tue, 24 Feb 2026 20:08:19 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 24 Feb 2026 20:08:19 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 24 Feb 2026 20:08:19 GMT
VOLUME [/var/lib/influxdb]
# Tue, 24 Feb 2026 20:08:19 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Feb 2026 20:08:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 20:08:19 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab3b37e4807fe48145826511e16a527bbc4695222ceb966669a4d16729b3b94`  
		Last Modified: Tue, 24 Feb 2026 19:18:52 GMT  
		Size: 24.0 MB (24038450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3532fb7b5a878a399c22cfd5eaf01899d40df24f559aa0c9455b0281b7928f`  
		Last Modified: Tue, 24 Feb 2026 20:08:28 GMT  
		Size: 5.1 KB (5070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adff68aa719159f054bb67a1fe92fce6f3ca4342483a856bf8cc2e711911609c`  
		Last Modified: Tue, 24 Feb 2026 20:08:29 GMT  
		Size: 18.6 MB (18596141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db11e9ac6dd745b94836c69fcacfee544de585ff508bd108d2bfd81bc4033200`  
		Last Modified: Tue, 24 Feb 2026 20:08:27 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e59752c26f83c26016de3b65e274e6a52fb12cc0d45b8bd61f61b46cbe815d7`  
		Last Modified: Tue, 24 Feb 2026 20:08:28 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.9-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:18a7ba8a49a0233368a6716cbac26bc3515bd536e82746c50dcc66a2f309deb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4604273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:170766f6dcc5225a6f32adf250082efbccc1b72fb04874e4d5f6a6313ed1ced4`

```dockerfile
```

-	Layers:
	-	`sha256:3d7ddaf787b100ec11ca2c4b22ab3aad86f0f677580657874fd240de1badd477`  
		Last Modified: Tue, 24 Feb 2026 20:08:28 GMT  
		Size: 4.6 MB (4591249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:629403330a558052ee488c7ab7655799581762c673bba07af3b1e12036873a9b`  
		Last Modified: Tue, 24 Feb 2026 20:08:27 GMT  
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
$ docker pull influxdb@sha256:f313b61c0ddb391344f89f0b0f1d2ea521bd405a8961506c3218b4efc01bd2bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.12` - linux; amd64

```console
$ docker pull influxdb@sha256:807748eb423abc9342c1d5c114519be24b520d5d9dd4fe4628ae99d211a4702b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.9 MB (113863290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b300c081c09c58972bd5fb5bb28d946741561fe8dcd445f9749b78147815a88`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:07:51 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 24 Feb 2026 20:07:57 GMT
ARG INFLUXDB_VERSION=1.12.2
# Tue, 24 Feb 2026 20:07:57 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:07:57 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 24 Feb 2026 20:07:57 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 24 Feb 2026 20:07:57 GMT
VOLUME [/var/lib/influxdb]
# Tue, 24 Feb 2026 20:07:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Feb 2026 20:07:57 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 24 Feb 2026 20:07:57 GMT
USER influxdb
# Tue, 24 Feb 2026 20:07:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 20:07:57 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab3b37e4807fe48145826511e16a527bbc4695222ceb966669a4d16729b3b94`  
		Last Modified: Tue, 24 Feb 2026 19:18:52 GMT  
		Size: 24.0 MB (24038450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b48eeff53e5afbaa7c55c88fca8bd9a1dcb6ffb363a05330431df6c89ccee6d`  
		Last Modified: Tue, 24 Feb 2026 20:08:10 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b08704d5621364bc02003dfc4ab5b532dac9c161192c5b8a469ada610ed91dc`  
		Last Modified: Tue, 24 Feb 2026 20:08:12 GMT  
		Size: 41.3 MB (41333149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e6fac8fed321f66f420ca799838dd7b562d6244a2f5b5f9e2063716758d587`  
		Last Modified: Tue, 24 Feb 2026 20:08:10 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20dc25a1743706f8476d83e05f155c9189de4d5d37fc4220662b35f7c57a65de`  
		Last Modified: Tue, 24 Feb 2026 20:08:11 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c92754d4e6740ebf34cd59c19eed7abc408b426710f71152909424a52f98599`  
		Last Modified: Tue, 24 Feb 2026 20:08:11 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:050a38b91e3165762b60593b7ca3c5a7449131b0ec1bf410baf4919ed0d75f35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4692912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:000ea3042e5fae2e49a430db844e96a6f7762fdf7e7c349d1871cf611a1d77d6`

```dockerfile
```

-	Layers:
	-	`sha256:6b088eb3ad863d9570953bb33f20bfba0b9f80056a85005784e01d4b657828c6`  
		Last Modified: Tue, 24 Feb 2026 20:08:11 GMT  
		Size: 4.7 MB (4676456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7b21caaf201b80fe4247e11ecbd890f61109738000b667a5fe1ff0932caa28c`  
		Last Modified: Tue, 24 Feb 2026 20:08:10 GMT  
		Size: 16.5 KB (16456 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.12` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:44c4eb0e1db2062291c5e8e4b9b713666022f9bb5ee0b6c4b145cbe74feb8fd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110117799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e23712c6c0602c73bd75d7e0a22e71a08492775274143cebbb644791504662c9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:24:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:18:42 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 24 Feb 2026 20:18:48 GMT
ARG INFLUXDB_VERSION=1.12.2
# Tue, 24 Feb 2026 20:18:48 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:18:48 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 24 Feb 2026 20:18:48 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 24 Feb 2026 20:18:48 GMT
VOLUME [/var/lib/influxdb]
# Tue, 24 Feb 2026 20:18:48 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Feb 2026 20:18:48 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 24 Feb 2026 20:18:48 GMT
USER influxdb
# Tue, 24 Feb 2026 20:18:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 20:18:48 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443d4217b87aad21c6acb58313c9038eb24571a4e9f81de2463aaf19d403a640`  
		Last Modified: Tue, 24 Feb 2026 19:24:13 GMT  
		Size: 23.6 MB (23604736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f277c4a9423fec44b999869bd2d7dbd978044732beb14c7e74556406612de82f`  
		Last Modified: Tue, 24 Feb 2026 20:19:00 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf69fdd58cb8e1da1638c67642f95fe7bf6a2373124642a8ebb760ba522674b`  
		Last Modified: Tue, 24 Feb 2026 20:19:01 GMT  
		Size: 38.1 MB (38136941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e3f1ac35a564bd4589cf8b4171bd3b526783a47716dc543b5b22a1f08f88ae`  
		Last Modified: Tue, 24 Feb 2026 20:19:00 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2628d8c8cc26536b0154c12507f80d2d7b24677a9823e1024d2751c9a32f7a`  
		Last Modified: Tue, 24 Feb 2026 20:19:00 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f651210d3043fddb592b6e52043eaf4885582de675da88971aa3700d4be2ad4`  
		Last Modified: Tue, 24 Feb 2026 20:19:01 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:f9d783e4076d78662b74fa335dfd33ca792d2e0ed69ec24e027bed990b051f0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4692464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab7de0094bc70a67f145adef1cca73cf0803091dc912900ffeea231e3c76b843`

```dockerfile
```

-	Layers:
	-	`sha256:57e8243ca4f273d4780bb0c497485b470b657397f763ffcefb3795ecfa14ead1`  
		Last Modified: Tue, 24 Feb 2026 20:19:00 GMT  
		Size: 4.7 MB (4675914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9dff0fe394167e86a12f32cbab26535e25fe72cd3c037f8af4b9cdf7c3a8b17`  
		Last Modified: Tue, 24 Feb 2026 20:19:00 GMT  
		Size: 16.6 KB (16550 bytes)  
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
$ docker pull influxdb@sha256:40a5c206b6f380abae88b69ae0524895c1c2e942dba023a469101f76d2af1d31
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12-data` - linux; amd64

```console
$ docker pull influxdb@sha256:155b636700f0303800c702d9a5399d444553918463a71d7c03e3001e694fbcd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114848805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae63172d05356fc4dd7607ef82abc295d6b12d9e8cb06daa68c35b0aa3508b8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:07:58 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Tue, 24 Feb 2026 20:07:58 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"         "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     rm -r "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"           "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:07:58 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 24 Feb 2026 20:07:58 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 24 Feb 2026 20:07:58 GMT
VOLUME [/var/lib/influxdb]
# Tue, 24 Feb 2026 20:07:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Feb 2026 20:07:58 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 24 Feb 2026 20:07:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 20:07:58 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab3b37e4807fe48145826511e16a527bbc4695222ceb966669a4d16729b3b94`  
		Last Modified: Tue, 24 Feb 2026 19:18:52 GMT  
		Size: 24.0 MB (24038450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097b775cb2b27f1be92722003efb2fdb5d4197757a50a9b95ab6a93b00497d0f`  
		Last Modified: Tue, 24 Feb 2026 20:08:11 GMT  
		Size: 42.3 MB (42319802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f444d666081f71dfd818ed6196fe39d16150c4af02efe1c5aee1553ea30b91`  
		Last Modified: Tue, 24 Feb 2026 20:08:09 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2740311728c56c143f1b5aba87ff0fc892e297fb301843e933c9bbf4deff525f`  
		Last Modified: Tue, 24 Feb 2026 20:08:10 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481ed7b20e0cef23ddc82013da6afb2579b45cf2c248e33227067fc6fe65ead0`  
		Last Modified: Tue, 24 Feb 2026 20:08:09 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:5f0467d4ec768bcb4c700a4dd5f902b2ae1df8f87fe29d6259c92493799e5741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4700469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc8463996ea682da5336ee474467e07c1eb3be4cb528ba88155d7cc5440c2be`

```dockerfile
```

-	Layers:
	-	`sha256:92829c2cf557d9451e1bc187054f75422a5afeb34a4d86305f9d37fa7026f09c`  
		Last Modified: Tue, 24 Feb 2026 20:08:10 GMT  
		Size: 4.7 MB (4686392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d029d29b02f092a4d1ae8cc07df0ffc48d59a2d101c776e333697e726a40f9e`  
		Last Modified: Tue, 24 Feb 2026 20:08:09 GMT  
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
$ docker pull influxdb@sha256:870a545ecc6d7f384d9d95ebdefe94c9f71fc389138fd78d6f8f6ef794339f93
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:3ea08f1dd67708e3f236fcaf2beeb38e3420f7dd148e3ae3557ed2b6e8b42d87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91308642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd0408fdfebdd6d30fca8f1b4b6900ef5b86163779484b8ef51e06649f061a82`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:08:02 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Tue, 24 Feb 2026 20:08:02 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"         "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     rm -r "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"           "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:08:02 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 24 Feb 2026 20:08:02 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 24 Feb 2026 20:08:02 GMT
VOLUME [/var/lib/influxdb]
# Tue, 24 Feb 2026 20:08:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Feb 2026 20:08:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 20:08:02 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab3b37e4807fe48145826511e16a527bbc4695222ceb966669a4d16729b3b94`  
		Last Modified: Tue, 24 Feb 2026 19:18:52 GMT  
		Size: 24.0 MB (24038450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe73a33fbd74774b5656ba240fd4b80929188336a7dbcac04888686d532f9eeb`  
		Last Modified: Tue, 24 Feb 2026 20:08:12 GMT  
		Size: 18.8 MB (18780849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de483592411eb2e58aec7264221b1d7e548bb39f7d27e7e780c38fc0939fa2b2`  
		Last Modified: Tue, 24 Feb 2026 20:08:11 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5e0f613809771fa649a15fd30247095d1435cf09a18b1c419dd23e2fb93f8d`  
		Last Modified: Tue, 24 Feb 2026 20:08:12 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:85f0fef50e41b9b3d7872f7fb04555915c63d0aad3745a0047f21a9816dee3f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4604146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf9900ce74fff1e8d4fb23312927ca743bd936c5f901cadbf0b98bd18656d700`

```dockerfile
```

-	Layers:
	-	`sha256:bc06be1fbb5e04ec1d186c2ce2c60e1de2086cb324856d13f3e3ad44fc2e79cf`  
		Last Modified: Tue, 24 Feb 2026 20:08:12 GMT  
		Size: 4.6 MB (4591555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4bae4f6329aff18224f10f1bedf7f4dbbd3e5200c8d9f6faca06fa57156d287`  
		Last Modified: Tue, 24 Feb 2026 20:08:11 GMT  
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
$ docker pull influxdb@sha256:f313b61c0ddb391344f89f0b0f1d2ea521bd405a8961506c3218b4efc01bd2bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.12.2` - linux; amd64

```console
$ docker pull influxdb@sha256:807748eb423abc9342c1d5c114519be24b520d5d9dd4fe4628ae99d211a4702b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.9 MB (113863290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b300c081c09c58972bd5fb5bb28d946741561fe8dcd445f9749b78147815a88`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:07:51 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 24 Feb 2026 20:07:57 GMT
ARG INFLUXDB_VERSION=1.12.2
# Tue, 24 Feb 2026 20:07:57 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:07:57 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 24 Feb 2026 20:07:57 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 24 Feb 2026 20:07:57 GMT
VOLUME [/var/lib/influxdb]
# Tue, 24 Feb 2026 20:07:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Feb 2026 20:07:57 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 24 Feb 2026 20:07:57 GMT
USER influxdb
# Tue, 24 Feb 2026 20:07:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 20:07:57 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab3b37e4807fe48145826511e16a527bbc4695222ceb966669a4d16729b3b94`  
		Last Modified: Tue, 24 Feb 2026 19:18:52 GMT  
		Size: 24.0 MB (24038450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b48eeff53e5afbaa7c55c88fca8bd9a1dcb6ffb363a05330431df6c89ccee6d`  
		Last Modified: Tue, 24 Feb 2026 20:08:10 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b08704d5621364bc02003dfc4ab5b532dac9c161192c5b8a469ada610ed91dc`  
		Last Modified: Tue, 24 Feb 2026 20:08:12 GMT  
		Size: 41.3 MB (41333149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e6fac8fed321f66f420ca799838dd7b562d6244a2f5b5f9e2063716758d587`  
		Last Modified: Tue, 24 Feb 2026 20:08:10 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20dc25a1743706f8476d83e05f155c9189de4d5d37fc4220662b35f7c57a65de`  
		Last Modified: Tue, 24 Feb 2026 20:08:11 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c92754d4e6740ebf34cd59c19eed7abc408b426710f71152909424a52f98599`  
		Last Modified: Tue, 24 Feb 2026 20:08:11 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2` - unknown; unknown

```console
$ docker pull influxdb@sha256:050a38b91e3165762b60593b7ca3c5a7449131b0ec1bf410baf4919ed0d75f35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4692912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:000ea3042e5fae2e49a430db844e96a6f7762fdf7e7c349d1871cf611a1d77d6`

```dockerfile
```

-	Layers:
	-	`sha256:6b088eb3ad863d9570953bb33f20bfba0b9f80056a85005784e01d4b657828c6`  
		Last Modified: Tue, 24 Feb 2026 20:08:11 GMT  
		Size: 4.7 MB (4676456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7b21caaf201b80fe4247e11ecbd890f61109738000b667a5fe1ff0932caa28c`  
		Last Modified: Tue, 24 Feb 2026 20:08:10 GMT  
		Size: 16.5 KB (16456 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.12.2` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:44c4eb0e1db2062291c5e8e4b9b713666022f9bb5ee0b6c4b145cbe74feb8fd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110117799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e23712c6c0602c73bd75d7e0a22e71a08492775274143cebbb644791504662c9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:24:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:18:42 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Tue, 24 Feb 2026 20:18:48 GMT
ARG INFLUXDB_VERSION=1.12.2
# Tue, 24 Feb 2026 20:18:48 GMT
# ARGS: INFLUXDB_VERSION=1.12.2
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_VERSION}-1_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:18:48 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 24 Feb 2026 20:18:48 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 24 Feb 2026 20:18:48 GMT
VOLUME [/var/lib/influxdb]
# Tue, 24 Feb 2026 20:18:48 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Feb 2026 20:18:48 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 24 Feb 2026 20:18:48 GMT
USER influxdb
# Tue, 24 Feb 2026 20:18:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 20:18:48 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443d4217b87aad21c6acb58313c9038eb24571a4e9f81de2463aaf19d403a640`  
		Last Modified: Tue, 24 Feb 2026 19:24:13 GMT  
		Size: 23.6 MB (23604736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f277c4a9423fec44b999869bd2d7dbd978044732beb14c7e74556406612de82f`  
		Last Modified: Tue, 24 Feb 2026 20:19:00 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf69fdd58cb8e1da1638c67642f95fe7bf6a2373124642a8ebb760ba522674b`  
		Last Modified: Tue, 24 Feb 2026 20:19:01 GMT  
		Size: 38.1 MB (38136941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e3f1ac35a564bd4589cf8b4171bd3b526783a47716dc543b5b22a1f08f88ae`  
		Last Modified: Tue, 24 Feb 2026 20:19:00 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2628d8c8cc26536b0154c12507f80d2d7b24677a9823e1024d2751c9a32f7a`  
		Last Modified: Tue, 24 Feb 2026 20:19:00 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f651210d3043fddb592b6e52043eaf4885582de675da88971aa3700d4be2ad4`  
		Last Modified: Tue, 24 Feb 2026 20:19:01 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2` - unknown; unknown

```console
$ docker pull influxdb@sha256:f9d783e4076d78662b74fa335dfd33ca792d2e0ed69ec24e027bed990b051f0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4692464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab7de0094bc70a67f145adef1cca73cf0803091dc912900ffeea231e3c76b843`

```dockerfile
```

-	Layers:
	-	`sha256:57e8243ca4f273d4780bb0c497485b470b657397f763ffcefb3795ecfa14ead1`  
		Last Modified: Tue, 24 Feb 2026 20:19:00 GMT  
		Size: 4.7 MB (4675914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9dff0fe394167e86a12f32cbab26535e25fe72cd3c037f8af4b9cdf7c3a8b17`  
		Last Modified: Tue, 24 Feb 2026 20:19:00 GMT  
		Size: 16.6 KB (16550 bytes)  
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
$ docker pull influxdb@sha256:40a5c206b6f380abae88b69ae0524895c1c2e942dba023a469101f76d2af1d31
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12.2-data` - linux; amd64

```console
$ docker pull influxdb@sha256:155b636700f0303800c702d9a5399d444553918463a71d7c03e3001e694fbcd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114848805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae63172d05356fc4dd7607ef82abc295d6b12d9e8cb06daa68c35b0aa3508b8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:07:58 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Tue, 24 Feb 2026 20:07:58 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"         "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     rm -r "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"           "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:07:58 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 24 Feb 2026 20:07:58 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 24 Feb 2026 20:07:58 GMT
VOLUME [/var/lib/influxdb]
# Tue, 24 Feb 2026 20:07:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Feb 2026 20:07:58 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 24 Feb 2026 20:07:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 20:07:58 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab3b37e4807fe48145826511e16a527bbc4695222ceb966669a4d16729b3b94`  
		Last Modified: Tue, 24 Feb 2026 19:18:52 GMT  
		Size: 24.0 MB (24038450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097b775cb2b27f1be92722003efb2fdb5d4197757a50a9b95ab6a93b00497d0f`  
		Last Modified: Tue, 24 Feb 2026 20:08:11 GMT  
		Size: 42.3 MB (42319802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f444d666081f71dfd818ed6196fe39d16150c4af02efe1c5aee1553ea30b91`  
		Last Modified: Tue, 24 Feb 2026 20:08:09 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2740311728c56c143f1b5aba87ff0fc892e297fb301843e933c9bbf4deff525f`  
		Last Modified: Tue, 24 Feb 2026 20:08:10 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481ed7b20e0cef23ddc82013da6afb2579b45cf2c248e33227067fc6fe65ead0`  
		Last Modified: Tue, 24 Feb 2026 20:08:09 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:5f0467d4ec768bcb4c700a4dd5f902b2ae1df8f87fe29d6259c92493799e5741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4700469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc8463996ea682da5336ee474467e07c1eb3be4cb528ba88155d7cc5440c2be`

```dockerfile
```

-	Layers:
	-	`sha256:92829c2cf557d9451e1bc187054f75422a5afeb34a4d86305f9d37fa7026f09c`  
		Last Modified: Tue, 24 Feb 2026 20:08:10 GMT  
		Size: 4.7 MB (4686392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d029d29b02f092a4d1ae8cc07df0ffc48d59a2d101c776e333697e726a40f9e`  
		Last Modified: Tue, 24 Feb 2026 20:08:09 GMT  
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
$ docker pull influxdb@sha256:870a545ecc6d7f384d9d95ebdefe94c9f71fc389138fd78d6f8f6ef794339f93
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12.2-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:3ea08f1dd67708e3f236fcaf2beeb38e3420f7dd148e3ae3557ed2b6e8b42d87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91308642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd0408fdfebdd6d30fca8f1b4b6900ef5b86163779484b8ef51e06649f061a82`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:08:02 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Tue, 24 Feb 2026 20:08:02 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"         "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     rm -r "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"           "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:08:02 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 24 Feb 2026 20:08:02 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 24 Feb 2026 20:08:02 GMT
VOLUME [/var/lib/influxdb]
# Tue, 24 Feb 2026 20:08:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Feb 2026 20:08:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 20:08:02 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab3b37e4807fe48145826511e16a527bbc4695222ceb966669a4d16729b3b94`  
		Last Modified: Tue, 24 Feb 2026 19:18:52 GMT  
		Size: 24.0 MB (24038450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe73a33fbd74774b5656ba240fd4b80929188336a7dbcac04888686d532f9eeb`  
		Last Modified: Tue, 24 Feb 2026 20:08:12 GMT  
		Size: 18.8 MB (18780849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de483592411eb2e58aec7264221b1d7e548bb39f7d27e7e780c38fc0939fa2b2`  
		Last Modified: Tue, 24 Feb 2026 20:08:11 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5e0f613809771fa649a15fd30247095d1435cf09a18b1c419dd23e2fb93f8d`  
		Last Modified: Tue, 24 Feb 2026 20:08:12 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.2-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:85f0fef50e41b9b3d7872f7fb04555915c63d0aad3745a0047f21a9816dee3f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4604146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf9900ce74fff1e8d4fb23312927ca743bd936c5f901cadbf0b98bd18656d700`

```dockerfile
```

-	Layers:
	-	`sha256:bc06be1fbb5e04ec1d186c2ce2c60e1de2086cb324856d13f3e3ad44fc2e79cf`  
		Last Modified: Tue, 24 Feb 2026 20:08:12 GMT  
		Size: 4.6 MB (4591555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4bae4f6329aff18224f10f1bedf7f4dbbd3e5200c8d9f6faca06fa57156d287`  
		Last Modified: Tue, 24 Feb 2026 20:08:11 GMT  
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
$ docker pull influxdb@sha256:60676b368409b4ac9664d1ba57b2613c5dec7c1a0f9dcd9405a0be0c375409f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2` - linux; amd64

```console
$ docker pull influxdb@sha256:51f91b302e29e29ce2edc9d6bb455d9aa5817de4454ce05eef4a09e772e01f39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107240632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f3a2343a3671477cd132c7d9f4152a11fa2ee240eaaf42009286cd1766db09a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:24:31 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:24:32 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 24 Feb 2026 19:24:32 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 24 Feb 2026 19:24:33 GMT
ENV GOSU_VER=1.19
# Tue, 24 Feb 2026 19:24:33 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 24 Feb 2026 19:24:33 GMT
ENV INFLUXDB_VERSION=2.8.0
# Tue, 24 Feb 2026 19:24:33 GMT
ENV INFLUXDB_PR=-2
# Tue, 24 Feb 2026 19:24:33 GMT
ENV INFLUXDB_PV=2.8.0-2
# Tue, 24 Feb 2026 19:24:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 24 Feb 2026 19:24:37 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 24 Feb 2026 19:24:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 24 Feb 2026 19:24:38 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 24 Feb 2026 19:24:38 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 24 Feb 2026 19:24:38 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 24 Feb 2026 19:24:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Feb 2026 19:24:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 19:24:38 GMT
CMD ["influxd"]
# Tue, 24 Feb 2026 19:24:38 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 24 Feb 2026 19:24:38 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 24 Feb 2026 19:24:38 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 24 Feb 2026 19:24:38 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 24 Feb 2026 19:24:38 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29a72782dae8e2d0c2dd676903f07119956ff0ddbee522e846ca64f5d673ea3`  
		Last Modified: Tue, 24 Feb 2026 19:24:50 GMT  
		Size: 9.8 MB (9798239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e187256dc8671a9ea7ee2754ad32915bdf6e9351237d33cec709ef4a3b6690`  
		Last Modified: Tue, 24 Feb 2026 19:24:50 GMT  
		Size: 6.2 MB (6156985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754b7251cdd173cc2ed22540b88f024b57e2946a7d215fd66a6d5d569a5c7bc9`  
		Last Modified: Tue, 24 Feb 2026 19:24:49 GMT  
		Size: 3.2 KB (3223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2810d4ff70b30298726c86e4942b59ad3704e8afa238c27782a742d9f9f493f0`  
		Last Modified: Tue, 24 Feb 2026 19:24:49 GMT  
		Size: 811.5 KB (811476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:162f11ba0bc175e0762579610de84c1bf80b617956f2aca92c14352395489990`  
		Last Modified: Tue, 24 Feb 2026 19:24:52 GMT  
		Size: 50.5 MB (50451821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6589bf91aad0c6e9fac3002eecc32cb153e7a67fa0a8c13777b9a9572bd461`  
		Last Modified: Tue, 24 Feb 2026 19:24:51 GMT  
		Size: 11.8 MB (11775878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab4b0b785b1a6d9a356adbc43855407bb1895b8d8aae5e7315b2a2374eb7223`  
		Last Modified: Tue, 24 Feb 2026 19:24:51 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea8c9e5957a972ad576d0742f682159bfc40c965d0cc0ebfa57b2fd6216e32e`  
		Last Modified: Tue, 24 Feb 2026 19:24:51 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce1d9cfee12e80e9f4b7d7d4aeed9bcb4b69a0d170a990cb536a60401c5c538`  
		Last Modified: Tue, 24 Feb 2026 19:24:52 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:88ecbd1360961d9f6eb9da320021355e22fd4aa94850f617fc4a114492b6306d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2c1c3f01da9c818d49a617a327c5b682db93addcab90d1e5b434f6f61251b31`

```dockerfile
```

-	Layers:
	-	`sha256:09f8c63961fd2025d17ba710188931974d23034eca0c9c32e95d4f238fe3b448`  
		Last Modified: Tue, 24 Feb 2026 19:24:50 GMT  
		Size: 2.9 MB (2934237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63a982fec1badfad4e243a1da8cd71d94383a37e58b6300e8fd79a6e5d38520d`  
		Last Modified: Tue, 24 Feb 2026 19:24:49 GMT  
		Size: 33.6 KB (33621 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ebd1ad4130df82ab4f633f9614ad1078df41c200a3054e5993228e4ba72e0b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103639647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b175a581af2a7af62bc8bbbada2a5107c0cc1adbde00775b335d8f113d66b09`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:29:09 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:29:09 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 24 Feb 2026 19:29:09 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 24 Feb 2026 19:29:11 GMT
ENV GOSU_VER=1.19
# Tue, 24 Feb 2026 19:29:11 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 24 Feb 2026 19:29:11 GMT
ENV INFLUXDB_VERSION=2.8.0
# Tue, 24 Feb 2026 19:29:11 GMT
ENV INFLUXDB_PR=-2
# Tue, 24 Feb 2026 19:29:11 GMT
ENV INFLUXDB_PV=2.8.0-2
# Tue, 24 Feb 2026 19:29:15 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 24 Feb 2026 19:29:15 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 24 Feb 2026 19:29:16 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 24 Feb 2026 19:29:16 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 24 Feb 2026 19:29:16 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 24 Feb 2026 19:29:16 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 24 Feb 2026 19:29:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Feb 2026 19:29:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 19:29:16 GMT
CMD ["influxd"]
# Tue, 24 Feb 2026 19:29:16 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 24 Feb 2026 19:29:16 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 24 Feb 2026 19:29:16 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 24 Feb 2026 19:29:16 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 24 Feb 2026 19:29:16 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0972f022d79a6181cce6188986c7899054c4374abffea6fb9207121bb45c80d9`  
		Last Modified: Tue, 24 Feb 2026 19:29:28 GMT  
		Size: 9.6 MB (9626871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e14b6090329229da5fd6f4042c8cdb0b06710efc78f68d31e344861b7b0e2a`  
		Last Modified: Tue, 24 Feb 2026 19:29:27 GMT  
		Size: 5.8 MB (5790414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7773d217697f39b64fd0eb3704baf907e6d6e52e2ecdd1fef3bd4917ec118597`  
		Last Modified: Tue, 24 Feb 2026 19:29:27 GMT  
		Size: 3.2 KB (3228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c43a53e1b3108d2b67b3ea5c71d60d9c9b2e0a80573fcf4dfdb0da4b0f986a8b`  
		Last Modified: Tue, 24 Feb 2026 19:29:27 GMT  
		Size: 766.4 KB (766373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6198a91ebeffd09d491d5b6faa9c006923cfedf1420e59e1c07687a30a0b50`  
		Last Modified: Tue, 24 Feb 2026 19:29:30 GMT  
		Size: 48.2 MB (48229560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ee346ad7d6a8f3f20a9e0e764accda51fc4c423404d1edc7c35072f9d2890e`  
		Last Modified: Tue, 24 Feb 2026 19:29:28 GMT  
		Size: 11.1 MB (11100389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1bda9b68d1668c1ea61f245e536c240787680a21bfab2a4226f3cb806a12fe2`  
		Last Modified: Tue, 24 Feb 2026 19:29:28 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b917881adf30187773219c9f82f321beb1e65fc183140c007a1f00113900982`  
		Last Modified: Tue, 24 Feb 2026 19:29:29 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ba8c8eb7f196b123dfa17207a68bab975b39d9f792b615c7f3226193377d0f`  
		Last Modified: Tue, 24 Feb 2026 19:29:29 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:b4c95f6c1e881ee21dbfc3608222b824dff7221141f8f7f0e63bb50382a864d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ad0a394ffb79894431b79112075fa33a8da4b9af83d4558efb4e3b633c3bfbb`

```dockerfile
```

-	Layers:
	-	`sha256:0b1cd26abacc2d2c4d46b117a2d163ebde6b332ad8005d816af61c700e4360d8`  
		Last Modified: Tue, 24 Feb 2026 19:29:27 GMT  
		Size: 2.9 MB (2933717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29e07eaf66c27e08b1e26f8744e41143741c5682f0a31dded582b8047d9ac96b`  
		Last Modified: Tue, 24 Feb 2026 19:29:26 GMT  
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
$ docker pull influxdb@sha256:3de4b6d4a18415d3d0e3b1c6409be46630bf6e5a01fcab3000b00c5c809128df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7` - linux; amd64

```console
$ docker pull influxdb@sha256:ec12488ce07ddaf61ea169dc4dc76163a7c46140f16af4e9264b273f1645aeec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157235478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f56c6cc0917f3ecc2eba4149dba82838da42669a417b70e4516c1101ca108042`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:24:25 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:24:26 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 24 Feb 2026 19:24:26 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 24 Feb 2026 19:24:28 GMT
ENV GOSU_VER=1.16
# Tue, 24 Feb 2026 19:24:28 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 24 Feb 2026 19:24:28 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 24 Feb 2026 19:24:34 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 24 Feb 2026 19:24:34 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 24 Feb 2026 19:24:35 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 24 Feb 2026 19:24:35 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 24 Feb 2026 19:24:35 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 24 Feb 2026 19:24:35 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 24 Feb 2026 19:24:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Feb 2026 19:24:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 19:24:35 GMT
CMD ["influxd"]
# Tue, 24 Feb 2026 19:24:35 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 24 Feb 2026 19:24:35 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 24 Feb 2026 19:24:35 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 24 Feb 2026 19:24:35 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 24 Feb 2026 19:24:35 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5a143e10bfd98170f9dca317000471838042167177e9fe677a92462ba8d146`  
		Last Modified: Tue, 24 Feb 2026 19:24:51 GMT  
		Size: 9.8 MB (9798163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c2bf2b65c983b695b5f95f181e3fb71873aef1f6f81b306e5e9704d57c8372`  
		Last Modified: Tue, 24 Feb 2026 19:24:51 GMT  
		Size: 6.2 MB (6156975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4379b954f3ac7e69e5d83bef1e24b0c5d2e83bc25ba5e1c16201bdb78094969`  
		Last Modified: Tue, 24 Feb 2026 19:24:50 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2504a115f2449a421c2a2d257ce4ef8bed8e77eede2087209e377922db6be7`  
		Last Modified: Tue, 24 Feb 2026 19:24:51 GMT  
		Size: 1.0 MB (1012038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a8092ff745e800731aa0b0a1432d06b0790b2c8d7ed6fdaf7de962a3ea96bf`  
		Last Modified: Tue, 24 Feb 2026 19:24:54 GMT  
		Size: 100.2 MB (100246193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51694c418db853b8f7beffab22a11803c404bd41511742667b620c0129f6993d`  
		Last Modified: Tue, 24 Feb 2026 19:24:52 GMT  
		Size: 11.8 MB (11775878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84fb109de12af035c3a5e39820713502a300c95f02908e4fec66cccfdd4d2ec5`  
		Last Modified: Tue, 24 Feb 2026 19:24:52 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b79ac3ed5ab1cf39e2f9dcd79a1ff02a6689a65c156348e59e46c8459f70b2d`  
		Last Modified: Tue, 24 Feb 2026 19:24:52 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f820162616c6ad673556e831e72573d0b3598a1ef28693b2ddc712f86cb1354c`  
		Last Modified: Tue, 24 Feb 2026 19:24:53 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:41d95953a40a6e38b95288af14c826db44dbc6e14010f2090fda4c94dda83b0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3014385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02abf0a96de10852d4c48430022af5d00aaa0963b435fe127fd25d21ec298e1a`

```dockerfile
```

-	Layers:
	-	`sha256:701df7ef9a92b087b6094bf472b21241ac9c492065ef48b4440621d5386224b6`  
		Last Modified: Tue, 24 Feb 2026 19:24:50 GMT  
		Size: 3.0 MB (2981484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76b4abdf4c5d0090a9f3888822c92f0338fa73413b78e97569c15bb7b83a88bb`  
		Last Modified: Tue, 24 Feb 2026 19:24:50 GMT  
		Size: 32.9 KB (32901 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:c931adc11093f73935463f6326361aff9cf75a0ad9ef91bc41a03410adf2ca8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151624405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f313fd19e073344d3ec8c3d27398ac6bad7c35ecd4e58f7bee986f3a4566fdf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:29:05 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:29:06 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 24 Feb 2026 19:29:06 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 24 Feb 2026 19:29:08 GMT
ENV GOSU_VER=1.16
# Tue, 24 Feb 2026 19:29:08 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 24 Feb 2026 19:29:08 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 24 Feb 2026 19:29:12 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 24 Feb 2026 19:29:12 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 24 Feb 2026 19:29:14 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 24 Feb 2026 19:29:14 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 24 Feb 2026 19:29:14 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 24 Feb 2026 19:29:14 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 24 Feb 2026 19:29:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Feb 2026 19:29:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 19:29:14 GMT
CMD ["influxd"]
# Tue, 24 Feb 2026 19:29:14 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 24 Feb 2026 19:29:14 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 24 Feb 2026 19:29:14 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 24 Feb 2026 19:29:14 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 24 Feb 2026 19:29:14 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb163bcac26aa90914db6535d0492ec186fbd239fb1d234830e363715ccb1bb2`  
		Last Modified: Tue, 24 Feb 2026 19:29:29 GMT  
		Size: 9.6 MB (9626946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b0ad9575074e2855f93d020747f19ff4cfb63791a05be74eb385cf41f31a91`  
		Last Modified: Tue, 24 Feb 2026 19:29:29 GMT  
		Size: 5.8 MB (5790427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ba4af1e47ee64c31687a5a2e9ff5354c21edff471348c5381037749a20e93b`  
		Last Modified: Tue, 24 Feb 2026 19:29:29 GMT  
		Size: 3.2 KB (3227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba7713ae6563053b4230f076429777572bbe067819edad6cb13aacf30b25481`  
		Last Modified: Tue, 24 Feb 2026 19:29:29 GMT  
		Size: 938.9 KB (938879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d885cf694b6a9c321a1f629d85c5bfedcbd1e1cc0eb161897f9efe5f608dc67`  
		Last Modified: Tue, 24 Feb 2026 19:29:32 GMT  
		Size: 96.0 MB (96041722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e1cf622fbc96d1d1ca76eedb92c569debb0798d23e0b173f5688077d48f1e9`  
		Last Modified: Tue, 24 Feb 2026 19:29:31 GMT  
		Size: 11.1 MB (11100393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736ef4e6a715ee0fb87d2088210812d67c34d1e4d88c2cb180936e7e00a68aeb`  
		Last Modified: Tue, 24 Feb 2026 19:29:30 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855f97ca9ed6060171a808dde739db53cb0bb5509e49fd603b0d94b29fad7d7c`  
		Last Modified: Tue, 24 Feb 2026 19:29:31 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f7877cb875e18455ec089b0f9fc4513f20dfdf56f176058b0f6c7c00b52461`  
		Last Modified: Tue, 24 Feb 2026 19:29:32 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:4f01b77d2298c90309e160b8eaa26a05e9568a1c9d28b60d18bde4c779192bd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3013748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2da6610314f67e5fa21eb721d794e8be2b06b887a9a0fdc2f6a8eb3bf220435`

```dockerfile
```

-	Layers:
	-	`sha256:7a987cb420d9a6ef2daea1f9a69e532c8a3efb9b222b3bd5f57e0941b8d39823`  
		Last Modified: Tue, 24 Feb 2026 19:29:29 GMT  
		Size: 3.0 MB (2980688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8da46999895cadec32b0650f3d54bc45f359da31515560018fdbb9d99220df13`  
		Last Modified: Tue, 24 Feb 2026 19:29:29 GMT  
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
$ docker pull influxdb@sha256:3de4b6d4a18415d3d0e3b1c6409be46630bf6e5a01fcab3000b00c5c809128df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.12` - linux; amd64

```console
$ docker pull influxdb@sha256:ec12488ce07ddaf61ea169dc4dc76163a7c46140f16af4e9264b273f1645aeec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157235478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f56c6cc0917f3ecc2eba4149dba82838da42669a417b70e4516c1101ca108042`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:24:25 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:24:26 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 24 Feb 2026 19:24:26 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 24 Feb 2026 19:24:28 GMT
ENV GOSU_VER=1.16
# Tue, 24 Feb 2026 19:24:28 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 24 Feb 2026 19:24:28 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 24 Feb 2026 19:24:34 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 24 Feb 2026 19:24:34 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 24 Feb 2026 19:24:35 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 24 Feb 2026 19:24:35 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 24 Feb 2026 19:24:35 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 24 Feb 2026 19:24:35 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 24 Feb 2026 19:24:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Feb 2026 19:24:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 19:24:35 GMT
CMD ["influxd"]
# Tue, 24 Feb 2026 19:24:35 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 24 Feb 2026 19:24:35 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 24 Feb 2026 19:24:35 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 24 Feb 2026 19:24:35 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 24 Feb 2026 19:24:35 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5a143e10bfd98170f9dca317000471838042167177e9fe677a92462ba8d146`  
		Last Modified: Tue, 24 Feb 2026 19:24:51 GMT  
		Size: 9.8 MB (9798163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c2bf2b65c983b695b5f95f181e3fb71873aef1f6f81b306e5e9704d57c8372`  
		Last Modified: Tue, 24 Feb 2026 19:24:51 GMT  
		Size: 6.2 MB (6156975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4379b954f3ac7e69e5d83bef1e24b0c5d2e83bc25ba5e1c16201bdb78094969`  
		Last Modified: Tue, 24 Feb 2026 19:24:50 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2504a115f2449a421c2a2d257ce4ef8bed8e77eede2087209e377922db6be7`  
		Last Modified: Tue, 24 Feb 2026 19:24:51 GMT  
		Size: 1.0 MB (1012038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a8092ff745e800731aa0b0a1432d06b0790b2c8d7ed6fdaf7de962a3ea96bf`  
		Last Modified: Tue, 24 Feb 2026 19:24:54 GMT  
		Size: 100.2 MB (100246193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51694c418db853b8f7beffab22a11803c404bd41511742667b620c0129f6993d`  
		Last Modified: Tue, 24 Feb 2026 19:24:52 GMT  
		Size: 11.8 MB (11775878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84fb109de12af035c3a5e39820713502a300c95f02908e4fec66cccfdd4d2ec5`  
		Last Modified: Tue, 24 Feb 2026 19:24:52 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b79ac3ed5ab1cf39e2f9dcd79a1ff02a6689a65c156348e59e46c8459f70b2d`  
		Last Modified: Tue, 24 Feb 2026 19:24:52 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f820162616c6ad673556e831e72573d0b3598a1ef28693b2ddc712f86cb1354c`  
		Last Modified: Tue, 24 Feb 2026 19:24:53 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:41d95953a40a6e38b95288af14c826db44dbc6e14010f2090fda4c94dda83b0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3014385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02abf0a96de10852d4c48430022af5d00aaa0963b435fe127fd25d21ec298e1a`

```dockerfile
```

-	Layers:
	-	`sha256:701df7ef9a92b087b6094bf472b21241ac9c492065ef48b4440621d5386224b6`  
		Last Modified: Tue, 24 Feb 2026 19:24:50 GMT  
		Size: 3.0 MB (2981484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76b4abdf4c5d0090a9f3888822c92f0338fa73413b78e97569c15bb7b83a88bb`  
		Last Modified: Tue, 24 Feb 2026 19:24:50 GMT  
		Size: 32.9 KB (32901 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7.12` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:c931adc11093f73935463f6326361aff9cf75a0ad9ef91bc41a03410adf2ca8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151624405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f313fd19e073344d3ec8c3d27398ac6bad7c35ecd4e58f7bee986f3a4566fdf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:29:05 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:29:06 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 24 Feb 2026 19:29:06 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 24 Feb 2026 19:29:08 GMT
ENV GOSU_VER=1.16
# Tue, 24 Feb 2026 19:29:08 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 24 Feb 2026 19:29:08 GMT
ENV INFLUXDB_VERSION=2.7.12
# Tue, 24 Feb 2026 19:29:12 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Tue, 24 Feb 2026 19:29:12 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 24 Feb 2026 19:29:14 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 24 Feb 2026 19:29:14 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 24 Feb 2026 19:29:14 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 24 Feb 2026 19:29:14 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 24 Feb 2026 19:29:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Feb 2026 19:29:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 19:29:14 GMT
CMD ["influxd"]
# Tue, 24 Feb 2026 19:29:14 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 24 Feb 2026 19:29:14 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 24 Feb 2026 19:29:14 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 24 Feb 2026 19:29:14 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 24 Feb 2026 19:29:14 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb163bcac26aa90914db6535d0492ec186fbd239fb1d234830e363715ccb1bb2`  
		Last Modified: Tue, 24 Feb 2026 19:29:29 GMT  
		Size: 9.6 MB (9626946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b0ad9575074e2855f93d020747f19ff4cfb63791a05be74eb385cf41f31a91`  
		Last Modified: Tue, 24 Feb 2026 19:29:29 GMT  
		Size: 5.8 MB (5790427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ba4af1e47ee64c31687a5a2e9ff5354c21edff471348c5381037749a20e93b`  
		Last Modified: Tue, 24 Feb 2026 19:29:29 GMT  
		Size: 3.2 KB (3227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba7713ae6563053b4230f076429777572bbe067819edad6cb13aacf30b25481`  
		Last Modified: Tue, 24 Feb 2026 19:29:29 GMT  
		Size: 938.9 KB (938879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d885cf694b6a9c321a1f629d85c5bfedcbd1e1cc0eb161897f9efe5f608dc67`  
		Last Modified: Tue, 24 Feb 2026 19:29:32 GMT  
		Size: 96.0 MB (96041722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e1cf622fbc96d1d1ca76eedb92c569debb0798d23e0b173f5688077d48f1e9`  
		Last Modified: Tue, 24 Feb 2026 19:29:31 GMT  
		Size: 11.1 MB (11100393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736ef4e6a715ee0fb87d2088210812d67c34d1e4d88c2cb180936e7e00a68aeb`  
		Last Modified: Tue, 24 Feb 2026 19:29:30 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855f97ca9ed6060171a808dde739db53cb0bb5509e49fd603b0d94b29fad7d7c`  
		Last Modified: Tue, 24 Feb 2026 19:29:31 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f7877cb875e18455ec089b0f9fc4513f20dfdf56f176058b0f6c7c00b52461`  
		Last Modified: Tue, 24 Feb 2026 19:29:32 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:4f01b77d2298c90309e160b8eaa26a05e9568a1c9d28b60d18bde4c779192bd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3013748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2da6610314f67e5fa21eb721d794e8be2b06b887a9a0fdc2f6a8eb3bf220435`

```dockerfile
```

-	Layers:
	-	`sha256:7a987cb420d9a6ef2daea1f9a69e532c8a3efb9b222b3bd5f57e0941b8d39823`  
		Last Modified: Tue, 24 Feb 2026 19:29:29 GMT  
		Size: 3.0 MB (2980688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8da46999895cadec32b0650f3d54bc45f359da31515560018fdbb9d99220df13`  
		Last Modified: Tue, 24 Feb 2026 19:29:29 GMT  
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
$ docker pull influxdb@sha256:60676b368409b4ac9664d1ba57b2613c5dec7c1a0f9dcd9405a0be0c375409f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.8` - linux; amd64

```console
$ docker pull influxdb@sha256:51f91b302e29e29ce2edc9d6bb455d9aa5817de4454ce05eef4a09e772e01f39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107240632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f3a2343a3671477cd132c7d9f4152a11fa2ee240eaaf42009286cd1766db09a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:24:31 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:24:32 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 24 Feb 2026 19:24:32 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 24 Feb 2026 19:24:33 GMT
ENV GOSU_VER=1.19
# Tue, 24 Feb 2026 19:24:33 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 24 Feb 2026 19:24:33 GMT
ENV INFLUXDB_VERSION=2.8.0
# Tue, 24 Feb 2026 19:24:33 GMT
ENV INFLUXDB_PR=-2
# Tue, 24 Feb 2026 19:24:33 GMT
ENV INFLUXDB_PV=2.8.0-2
# Tue, 24 Feb 2026 19:24:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 24 Feb 2026 19:24:37 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 24 Feb 2026 19:24:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 24 Feb 2026 19:24:38 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 24 Feb 2026 19:24:38 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 24 Feb 2026 19:24:38 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 24 Feb 2026 19:24:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Feb 2026 19:24:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 19:24:38 GMT
CMD ["influxd"]
# Tue, 24 Feb 2026 19:24:38 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 24 Feb 2026 19:24:38 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 24 Feb 2026 19:24:38 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 24 Feb 2026 19:24:38 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 24 Feb 2026 19:24:38 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29a72782dae8e2d0c2dd676903f07119956ff0ddbee522e846ca64f5d673ea3`  
		Last Modified: Tue, 24 Feb 2026 19:24:50 GMT  
		Size: 9.8 MB (9798239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e187256dc8671a9ea7ee2754ad32915bdf6e9351237d33cec709ef4a3b6690`  
		Last Modified: Tue, 24 Feb 2026 19:24:50 GMT  
		Size: 6.2 MB (6156985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754b7251cdd173cc2ed22540b88f024b57e2946a7d215fd66a6d5d569a5c7bc9`  
		Last Modified: Tue, 24 Feb 2026 19:24:49 GMT  
		Size: 3.2 KB (3223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2810d4ff70b30298726c86e4942b59ad3704e8afa238c27782a742d9f9f493f0`  
		Last Modified: Tue, 24 Feb 2026 19:24:49 GMT  
		Size: 811.5 KB (811476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:162f11ba0bc175e0762579610de84c1bf80b617956f2aca92c14352395489990`  
		Last Modified: Tue, 24 Feb 2026 19:24:52 GMT  
		Size: 50.5 MB (50451821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6589bf91aad0c6e9fac3002eecc32cb153e7a67fa0a8c13777b9a9572bd461`  
		Last Modified: Tue, 24 Feb 2026 19:24:51 GMT  
		Size: 11.8 MB (11775878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab4b0b785b1a6d9a356adbc43855407bb1895b8d8aae5e7315b2a2374eb7223`  
		Last Modified: Tue, 24 Feb 2026 19:24:51 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea8c9e5957a972ad576d0742f682159bfc40c965d0cc0ebfa57b2fd6216e32e`  
		Last Modified: Tue, 24 Feb 2026 19:24:51 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce1d9cfee12e80e9f4b7d7d4aeed9bcb4b69a0d170a990cb536a60401c5c538`  
		Last Modified: Tue, 24 Feb 2026 19:24:52 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:88ecbd1360961d9f6eb9da320021355e22fd4aa94850f617fc4a114492b6306d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2c1c3f01da9c818d49a617a327c5b682db93addcab90d1e5b434f6f61251b31`

```dockerfile
```

-	Layers:
	-	`sha256:09f8c63961fd2025d17ba710188931974d23034eca0c9c32e95d4f238fe3b448`  
		Last Modified: Tue, 24 Feb 2026 19:24:50 GMT  
		Size: 2.9 MB (2934237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63a982fec1badfad4e243a1da8cd71d94383a37e58b6300e8fd79a6e5d38520d`  
		Last Modified: Tue, 24 Feb 2026 19:24:49 GMT  
		Size: 33.6 KB (33621 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ebd1ad4130df82ab4f633f9614ad1078df41c200a3054e5993228e4ba72e0b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103639647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b175a581af2a7af62bc8bbbada2a5107c0cc1adbde00775b335d8f113d66b09`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:29:09 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:29:09 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 24 Feb 2026 19:29:09 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 24 Feb 2026 19:29:11 GMT
ENV GOSU_VER=1.19
# Tue, 24 Feb 2026 19:29:11 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 24 Feb 2026 19:29:11 GMT
ENV INFLUXDB_VERSION=2.8.0
# Tue, 24 Feb 2026 19:29:11 GMT
ENV INFLUXDB_PR=-2
# Tue, 24 Feb 2026 19:29:11 GMT
ENV INFLUXDB_PV=2.8.0-2
# Tue, 24 Feb 2026 19:29:15 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 24 Feb 2026 19:29:15 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 24 Feb 2026 19:29:16 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 24 Feb 2026 19:29:16 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 24 Feb 2026 19:29:16 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 24 Feb 2026 19:29:16 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 24 Feb 2026 19:29:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Feb 2026 19:29:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 19:29:16 GMT
CMD ["influxd"]
# Tue, 24 Feb 2026 19:29:16 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 24 Feb 2026 19:29:16 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 24 Feb 2026 19:29:16 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 24 Feb 2026 19:29:16 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 24 Feb 2026 19:29:16 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0972f022d79a6181cce6188986c7899054c4374abffea6fb9207121bb45c80d9`  
		Last Modified: Tue, 24 Feb 2026 19:29:28 GMT  
		Size: 9.6 MB (9626871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e14b6090329229da5fd6f4042c8cdb0b06710efc78f68d31e344861b7b0e2a`  
		Last Modified: Tue, 24 Feb 2026 19:29:27 GMT  
		Size: 5.8 MB (5790414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7773d217697f39b64fd0eb3704baf907e6d6e52e2ecdd1fef3bd4917ec118597`  
		Last Modified: Tue, 24 Feb 2026 19:29:27 GMT  
		Size: 3.2 KB (3228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c43a53e1b3108d2b67b3ea5c71d60d9c9b2e0a80573fcf4dfdb0da4b0f986a8b`  
		Last Modified: Tue, 24 Feb 2026 19:29:27 GMT  
		Size: 766.4 KB (766373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6198a91ebeffd09d491d5b6faa9c006923cfedf1420e59e1c07687a30a0b50`  
		Last Modified: Tue, 24 Feb 2026 19:29:30 GMT  
		Size: 48.2 MB (48229560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ee346ad7d6a8f3f20a9e0e764accda51fc4c423404d1edc7c35072f9d2890e`  
		Last Modified: Tue, 24 Feb 2026 19:29:28 GMT  
		Size: 11.1 MB (11100389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1bda9b68d1668c1ea61f245e536c240787680a21bfab2a4226f3cb806a12fe2`  
		Last Modified: Tue, 24 Feb 2026 19:29:28 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b917881adf30187773219c9f82f321beb1e65fc183140c007a1f00113900982`  
		Last Modified: Tue, 24 Feb 2026 19:29:29 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ba8c8eb7f196b123dfa17207a68bab975b39d9f792b615c7f3226193377d0f`  
		Last Modified: Tue, 24 Feb 2026 19:29:29 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:b4c95f6c1e881ee21dbfc3608222b824dff7221141f8f7f0e63bb50382a864d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ad0a394ffb79894431b79112075fa33a8da4b9af83d4558efb4e3b633c3bfbb`

```dockerfile
```

-	Layers:
	-	`sha256:0b1cd26abacc2d2c4d46b117a2d163ebde6b332ad8005d816af61c700e4360d8`  
		Last Modified: Tue, 24 Feb 2026 19:29:27 GMT  
		Size: 2.9 MB (2933717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29e07eaf66c27e08b1e26f8744e41143741c5682f0a31dded582b8047d9ac96b`  
		Last Modified: Tue, 24 Feb 2026 19:29:26 GMT  
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
$ docker pull influxdb@sha256:60676b368409b4ac9664d1ba57b2613c5dec7c1a0f9dcd9405a0be0c375409f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.8.0` - linux; amd64

```console
$ docker pull influxdb@sha256:51f91b302e29e29ce2edc9d6bb455d9aa5817de4454ce05eef4a09e772e01f39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107240632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f3a2343a3671477cd132c7d9f4152a11fa2ee240eaaf42009286cd1766db09a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:24:31 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:24:32 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 24 Feb 2026 19:24:32 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 24 Feb 2026 19:24:33 GMT
ENV GOSU_VER=1.19
# Tue, 24 Feb 2026 19:24:33 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 24 Feb 2026 19:24:33 GMT
ENV INFLUXDB_VERSION=2.8.0
# Tue, 24 Feb 2026 19:24:33 GMT
ENV INFLUXDB_PR=-2
# Tue, 24 Feb 2026 19:24:33 GMT
ENV INFLUXDB_PV=2.8.0-2
# Tue, 24 Feb 2026 19:24:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 24 Feb 2026 19:24:37 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 24 Feb 2026 19:24:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 24 Feb 2026 19:24:38 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 24 Feb 2026 19:24:38 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 24 Feb 2026 19:24:38 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 24 Feb 2026 19:24:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Feb 2026 19:24:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 19:24:38 GMT
CMD ["influxd"]
# Tue, 24 Feb 2026 19:24:38 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 24 Feb 2026 19:24:38 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 24 Feb 2026 19:24:38 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 24 Feb 2026 19:24:38 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 24 Feb 2026 19:24:38 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29a72782dae8e2d0c2dd676903f07119956ff0ddbee522e846ca64f5d673ea3`  
		Last Modified: Tue, 24 Feb 2026 19:24:50 GMT  
		Size: 9.8 MB (9798239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e187256dc8671a9ea7ee2754ad32915bdf6e9351237d33cec709ef4a3b6690`  
		Last Modified: Tue, 24 Feb 2026 19:24:50 GMT  
		Size: 6.2 MB (6156985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754b7251cdd173cc2ed22540b88f024b57e2946a7d215fd66a6d5d569a5c7bc9`  
		Last Modified: Tue, 24 Feb 2026 19:24:49 GMT  
		Size: 3.2 KB (3223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2810d4ff70b30298726c86e4942b59ad3704e8afa238c27782a742d9f9f493f0`  
		Last Modified: Tue, 24 Feb 2026 19:24:49 GMT  
		Size: 811.5 KB (811476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:162f11ba0bc175e0762579610de84c1bf80b617956f2aca92c14352395489990`  
		Last Modified: Tue, 24 Feb 2026 19:24:52 GMT  
		Size: 50.5 MB (50451821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6589bf91aad0c6e9fac3002eecc32cb153e7a67fa0a8c13777b9a9572bd461`  
		Last Modified: Tue, 24 Feb 2026 19:24:51 GMT  
		Size: 11.8 MB (11775878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab4b0b785b1a6d9a356adbc43855407bb1895b8d8aae5e7315b2a2374eb7223`  
		Last Modified: Tue, 24 Feb 2026 19:24:51 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea8c9e5957a972ad576d0742f682159bfc40c965d0cc0ebfa57b2fd6216e32e`  
		Last Modified: Tue, 24 Feb 2026 19:24:51 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce1d9cfee12e80e9f4b7d7d4aeed9bcb4b69a0d170a990cb536a60401c5c538`  
		Last Modified: Tue, 24 Feb 2026 19:24:52 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8.0` - unknown; unknown

```console
$ docker pull influxdb@sha256:88ecbd1360961d9f6eb9da320021355e22fd4aa94850f617fc4a114492b6306d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2c1c3f01da9c818d49a617a327c5b682db93addcab90d1e5b434f6f61251b31`

```dockerfile
```

-	Layers:
	-	`sha256:09f8c63961fd2025d17ba710188931974d23034eca0c9c32e95d4f238fe3b448`  
		Last Modified: Tue, 24 Feb 2026 19:24:50 GMT  
		Size: 2.9 MB (2934237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63a982fec1badfad4e243a1da8cd71d94383a37e58b6300e8fd79a6e5d38520d`  
		Last Modified: Tue, 24 Feb 2026 19:24:49 GMT  
		Size: 33.6 KB (33621 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.8.0` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ebd1ad4130df82ab4f633f9614ad1078df41c200a3054e5993228e4ba72e0b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103639647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b175a581af2a7af62bc8bbbada2a5107c0cc1adbde00775b335d8f113d66b09`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:29:09 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:29:09 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 24 Feb 2026 19:29:09 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 24 Feb 2026 19:29:11 GMT
ENV GOSU_VER=1.19
# Tue, 24 Feb 2026 19:29:11 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 24 Feb 2026 19:29:11 GMT
ENV INFLUXDB_VERSION=2.8.0
# Tue, 24 Feb 2026 19:29:11 GMT
ENV INFLUXDB_PR=-2
# Tue, 24 Feb 2026 19:29:11 GMT
ENV INFLUXDB_PV=2.8.0-2
# Tue, 24 Feb 2026 19:29:15 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 24 Feb 2026 19:29:15 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 24 Feb 2026 19:29:16 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 24 Feb 2026 19:29:16 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 24 Feb 2026 19:29:16 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 24 Feb 2026 19:29:16 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 24 Feb 2026 19:29:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Feb 2026 19:29:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 19:29:16 GMT
CMD ["influxd"]
# Tue, 24 Feb 2026 19:29:16 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 24 Feb 2026 19:29:16 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 24 Feb 2026 19:29:16 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 24 Feb 2026 19:29:16 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 24 Feb 2026 19:29:16 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0972f022d79a6181cce6188986c7899054c4374abffea6fb9207121bb45c80d9`  
		Last Modified: Tue, 24 Feb 2026 19:29:28 GMT  
		Size: 9.6 MB (9626871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e14b6090329229da5fd6f4042c8cdb0b06710efc78f68d31e344861b7b0e2a`  
		Last Modified: Tue, 24 Feb 2026 19:29:27 GMT  
		Size: 5.8 MB (5790414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7773d217697f39b64fd0eb3704baf907e6d6e52e2ecdd1fef3bd4917ec118597`  
		Last Modified: Tue, 24 Feb 2026 19:29:27 GMT  
		Size: 3.2 KB (3228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c43a53e1b3108d2b67b3ea5c71d60d9c9b2e0a80573fcf4dfdb0da4b0f986a8b`  
		Last Modified: Tue, 24 Feb 2026 19:29:27 GMT  
		Size: 766.4 KB (766373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6198a91ebeffd09d491d5b6faa9c006923cfedf1420e59e1c07687a30a0b50`  
		Last Modified: Tue, 24 Feb 2026 19:29:30 GMT  
		Size: 48.2 MB (48229560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ee346ad7d6a8f3f20a9e0e764accda51fc4c423404d1edc7c35072f9d2890e`  
		Last Modified: Tue, 24 Feb 2026 19:29:28 GMT  
		Size: 11.1 MB (11100389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1bda9b68d1668c1ea61f245e536c240787680a21bfab2a4226f3cb806a12fe2`  
		Last Modified: Tue, 24 Feb 2026 19:29:28 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b917881adf30187773219c9f82f321beb1e65fc183140c007a1f00113900982`  
		Last Modified: Tue, 24 Feb 2026 19:29:29 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ba8c8eb7f196b123dfa17207a68bab975b39d9f792b615c7f3226193377d0f`  
		Last Modified: Tue, 24 Feb 2026 19:29:29 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8.0` - unknown; unknown

```console
$ docker pull influxdb@sha256:b4c95f6c1e881ee21dbfc3608222b824dff7221141f8f7f0e63bb50382a864d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ad0a394ffb79894431b79112075fa33a8da4b9af83d4558efb4e3b633c3bfbb`

```dockerfile
```

-	Layers:
	-	`sha256:0b1cd26abacc2d2c4d46b117a2d163ebde6b332ad8005d816af61c700e4360d8`  
		Last Modified: Tue, 24 Feb 2026 19:29:27 GMT  
		Size: 2.9 MB (2933717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29e07eaf66c27e08b1e26f8744e41143741c5682f0a31dded582b8047d9ac96b`  
		Last Modified: Tue, 24 Feb 2026 19:29:26 GMT  
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
$ docker pull influxdb@sha256:255268d2a5f42b8c38d373864a4ba72956d91e14a3361019706bfad2f7c039ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-core` - linux; amd64

```console
$ docker pull influxdb@sha256:62775f106f8dac81e102b098d65ff85bced00936418c9689ec995c4ae081579a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.3 MB (119327710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:822ae8137edf72418a2e8940ae5d9ee9a540ba42089758cf7f152633aaa9a9a2`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Wed, 25 Feb 2026 17:33:00 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 25 Feb 2026 17:33:00 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 25 Feb 2026 17:33:07 GMT
ENV INFLUXDB_VERSION=3.8.3
# Wed, 25 Feb 2026 17:33:07 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 25 Feb 2026 17:33:07 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 25 Feb 2026 17:33:07 GMT
USER influxdb3
# Wed, 25 Feb 2026 17:33:07 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 25 Feb 2026 17:33:07 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 25 Feb 2026 17:33:07 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 25 Feb 2026 17:33:07 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 25 Feb 2026 17:33:07 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 25 Feb 2026 17:33:07 GMT
ENV LOG_FILTER=info
# Wed, 25 Feb 2026 17:33:07 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 25 Feb 2026 17:33:07 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 25 Feb 2026 17:33:07 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9542c760bea8712a7b1c7320237ab218944b72df43f69ed08641fae1d8c8e62`  
		Last Modified: Wed, 25 Feb 2026 17:33:23 GMT  
		Size: 6.7 MB (6671516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173d8ef7fd2a07ba4c6d17512223b9003f3fb95a0e816d58cfa268a72e52e6d8`  
		Last Modified: Wed, 25 Feb 2026 17:33:22 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e48d156f776b0a2da1758df77ebd46edfd1fad75d9263c2bf8f372f1512b67`  
		Last Modified: Wed, 25 Feb 2026 17:33:25 GMT  
		Size: 82.9 MB (82924266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:983e350c598a24824dc923bbf46cda0ef4bdae4f038af8eff88c8b6e962fd570`  
		Last Modified: Wed, 25 Feb 2026 17:33:22 GMT  
		Size: 517.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd8897b1c30e1f42aea23a38708759ab99d46124513222b00c6d6278b834abc`  
		Last Modified: Wed, 25 Feb 2026 17:33:23 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:39aad74b5cdb36ffcb31ad7ea28355818840cb560280535fa0ed9dba8a68571a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f8912a005531705bde9206c7cfbd729fba8b6021a5f966c0686b7f69a19610`

```dockerfile
```

-	Layers:
	-	`sha256:f7820589c3db8a4e9719fe6e0ee548b36c99b3d514cf136bf12da97fb3735d1c`  
		Last Modified: Wed, 25 Feb 2026 17:33:22 GMT  
		Size: 2.3 MB (2310571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af5e75a1973c652afdc1e55fee67cc715982acaf272ee16200297d6a2a256194`  
		Last Modified: Wed, 25 Feb 2026 17:33:22 GMT  
		Size: 17.6 KB (17617 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:6b45900e2ab53d82ae88dbbfcd757def6fe76ba93369743f2fd317b6a8e17846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110130123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97c5a1135218b678758c5822631868dabc3016114cad2e110d78f5678ae85e98`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Wed, 25 Feb 2026 17:44:14 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 25 Feb 2026 17:44:15 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 25 Feb 2026 17:44:21 GMT
ENV INFLUXDB_VERSION=3.8.3
# Wed, 25 Feb 2026 17:44:21 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 25 Feb 2026 17:44:21 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 25 Feb 2026 17:44:21 GMT
USER influxdb3
# Wed, 25 Feb 2026 17:44:21 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 25 Feb 2026 17:44:21 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 25 Feb 2026 17:44:21 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 25 Feb 2026 17:44:21 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 25 Feb 2026 17:44:21 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 25 Feb 2026 17:44:21 GMT
ENV LOG_FILTER=info
# Wed, 25 Feb 2026 17:44:21 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 25 Feb 2026 17:44:21 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 25 Feb 2026 17:44:21 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1600a9c64eb260873cf108122e4cdf204f8272ba853903f05a1c8ce4928cc9b`  
		Last Modified: Wed, 25 Feb 2026 17:44:35 GMT  
		Size: 6.7 MB (6681454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a8f741a77a6ec6590221f763db0c06a439f2b3a4f0234d2eeec7b43a90ae1b`  
		Last Modified: Wed, 25 Feb 2026 17:44:34 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc615a32cd32e801400994677df8f107cfa4f9e57facaed86ebf5028095ccde`  
		Last Modified: Wed, 25 Feb 2026 17:44:36 GMT  
		Size: 74.6 MB (74579225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884b5c05caaac19df93120744391be11a6fb6fa2dcc0caa05e0ae634e4aa8bcb`  
		Last Modified: Wed, 25 Feb 2026 17:44:34 GMT  
		Size: 520.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f395b8f9fbee60a71ca0db75d66de3ba21d8c72bc0b8a822efe23579e83020b`  
		Last Modified: Wed, 25 Feb 2026 17:44:36 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:8134d33f6efa7eeb3dd051b4647f98e2707d239233aca84041ba7e3ad027e527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893aff8378f9a605d056fb94eae68f81a8a0bf94be432174cf0acdf9d7631c86`

```dockerfile
```

-	Layers:
	-	`sha256:69b0b59299b0eda121a960ef36b94d23f04a3deb935dafcb63268337c659235c`  
		Last Modified: Wed, 25 Feb 2026 17:44:34 GMT  
		Size: 2.3 MB (2311653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9501d98ec72095cee13f3d9bc289f16f36f85c63d56c997e3930db1d51c228c3`  
		Last Modified: Wed, 25 Feb 2026 17:44:34 GMT  
		Size: 17.8 KB (17764 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3-enterprise`

```console
$ docker pull influxdb@sha256:f392a1a9568870f6f15271b6292b6d95b117d82f2619f8c2b5ea8d54ae8ea628
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:0cc529867fa1f410068d02ce553c6d500ad395163eb5a74753e1ba475cb5d3eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128364098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b65d86e37fdd243fed5f8c89797813cebcc7d38aad80ea32828840d6699abd`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Wed, 25 Feb 2026 17:33:00 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 25 Feb 2026 17:33:00 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 25 Feb 2026 17:33:39 GMT
ENV INFLUXDB_VERSION=3.8.3
# Wed, 25 Feb 2026 17:33:39 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 25 Feb 2026 17:33:39 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 25 Feb 2026 17:33:39 GMT
USER influxdb3
# Wed, 25 Feb 2026 17:33:39 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 25 Feb 2026 17:33:39 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 25 Feb 2026 17:33:39 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 25 Feb 2026 17:33:39 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 25 Feb 2026 17:33:39 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 25 Feb 2026 17:33:39 GMT
ENV LOG_FILTER=info
# Wed, 25 Feb 2026 17:33:39 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 25 Feb 2026 17:33:39 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 25 Feb 2026 17:33:39 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9542c760bea8712a7b1c7320237ab218944b72df43f69ed08641fae1d8c8e62`  
		Last Modified: Wed, 25 Feb 2026 17:33:23 GMT  
		Size: 6.7 MB (6671516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173d8ef7fd2a07ba4c6d17512223b9003f3fb95a0e816d58cfa268a72e52e6d8`  
		Last Modified: Wed, 25 Feb 2026 17:33:22 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3fe89b6d0e71dea3acd1a59241822c25d4f05e78884b8211f97d7df3554c080`  
		Last Modified: Wed, 25 Feb 2026 17:33:57 GMT  
		Size: 92.0 MB (91960651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5735e88aedf81bd71267a38840c016d9a4b8db594299acc493756a02d1b619f2`  
		Last Modified: Wed, 25 Feb 2026 17:33:55 GMT  
		Size: 517.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd4ae8b9ddf57c50ba883b006c6e1ccc720ee5dfe33c3fb4d2bc255dc782ffa`  
		Last Modified: Wed, 25 Feb 2026 17:33:55 GMT  
		Size: 151.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:9918b7f24acf4aa4aee77ed1d7c7dcfafdd4fcfd17bb68ec6c5261bc6a6ba9c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aed0f2e1c167a5ce6e3b62bd9fc2dfa63b411a22b9dd9f94f84dafa143ac65dd`

```dockerfile
```

-	Layers:
	-	`sha256:a5919f172ad357c7bd480ad375d2118fdca042307adf9c07c10faa5ed6ea1336`  
		Last Modified: Wed, 25 Feb 2026 17:33:55 GMT  
		Size: 2.3 MB (2310619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f9822286a39b10571bd9835dc3e4b78a74c6e9eecd9f284b3f28cdace701242`  
		Last Modified: Wed, 25 Feb 2026 17:33:55 GMT  
		Size: 17.8 KB (17797 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:599b86bf46a9d8e9df22b4cb45afab9f2df2e4f0051cbb3c6bb32a7de45845df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (118967689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9282d312b323de847f08819402467b17b58ea8851fe2d6957b0db453fee2e450`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Wed, 25 Feb 2026 17:44:14 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 25 Feb 2026 17:44:15 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 25 Feb 2026 17:44:54 GMT
ENV INFLUXDB_VERSION=3.8.3
# Wed, 25 Feb 2026 17:44:54 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 25 Feb 2026 17:44:54 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 25 Feb 2026 17:44:54 GMT
USER influxdb3
# Wed, 25 Feb 2026 17:44:54 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 25 Feb 2026 17:44:54 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 25 Feb 2026 17:44:54 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 25 Feb 2026 17:44:54 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 25 Feb 2026 17:44:54 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 25 Feb 2026 17:44:54 GMT
ENV LOG_FILTER=info
# Wed, 25 Feb 2026 17:44:54 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 25 Feb 2026 17:44:54 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 25 Feb 2026 17:44:54 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1600a9c64eb260873cf108122e4cdf204f8272ba853903f05a1c8ce4928cc9b`  
		Last Modified: Wed, 25 Feb 2026 17:44:35 GMT  
		Size: 6.7 MB (6681454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a8f741a77a6ec6590221f763db0c06a439f2b3a4f0234d2eeec7b43a90ae1b`  
		Last Modified: Wed, 25 Feb 2026 17:44:34 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd98dae91172a1c1d44d43c624ddf280ec16f253dcdb0a43262c519ddf791bd`  
		Last Modified: Wed, 25 Feb 2026 17:45:10 GMT  
		Size: 83.4 MB (83416791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ed5be20f00166b950a72770bee50ba841f42986961f75925a87b6efc0ffe28`  
		Last Modified: Wed, 25 Feb 2026 17:45:08 GMT  
		Size: 520.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:792a89f12f8ec69ba70c82d56987e1b1a8dae7af9a84d516174ac5f968dc8f32`  
		Last Modified: Wed, 25 Feb 2026 17:45:08 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:e1e6d15a0cc91736906ee54a213ed9d97eb9f5d2497d726bc0adac9809dccdc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e16625a4304b70ceb915254f3a4f4ba276d89f77d521168a0fd43859089b3d5`

```dockerfile
```

-	Layers:
	-	`sha256:18286a9d2f68442ed57ed6beca7243dcbc5ec75c92490e315b4a11a05deb014d`  
		Last Modified: Wed, 25 Feb 2026 17:45:08 GMT  
		Size: 2.3 MB (2311701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd9c2cd867e205e55c2284c3881fff22b9bfc4c1f84da3702e84bb1aea735a4d`  
		Last Modified: Wed, 25 Feb 2026 17:45:08 GMT  
		Size: 17.9 KB (17946 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.8-core`

```console
$ docker pull influxdb@sha256:255268d2a5f42b8c38d373864a4ba72956d91e14a3361019706bfad2f7c039ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.8-core` - linux; amd64

```console
$ docker pull influxdb@sha256:62775f106f8dac81e102b098d65ff85bced00936418c9689ec995c4ae081579a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.3 MB (119327710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:822ae8137edf72418a2e8940ae5d9ee9a540ba42089758cf7f152633aaa9a9a2`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Wed, 25 Feb 2026 17:33:00 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 25 Feb 2026 17:33:00 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 25 Feb 2026 17:33:07 GMT
ENV INFLUXDB_VERSION=3.8.3
# Wed, 25 Feb 2026 17:33:07 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 25 Feb 2026 17:33:07 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 25 Feb 2026 17:33:07 GMT
USER influxdb3
# Wed, 25 Feb 2026 17:33:07 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 25 Feb 2026 17:33:07 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 25 Feb 2026 17:33:07 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 25 Feb 2026 17:33:07 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 25 Feb 2026 17:33:07 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 25 Feb 2026 17:33:07 GMT
ENV LOG_FILTER=info
# Wed, 25 Feb 2026 17:33:07 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 25 Feb 2026 17:33:07 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 25 Feb 2026 17:33:07 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9542c760bea8712a7b1c7320237ab218944b72df43f69ed08641fae1d8c8e62`  
		Last Modified: Wed, 25 Feb 2026 17:33:23 GMT  
		Size: 6.7 MB (6671516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173d8ef7fd2a07ba4c6d17512223b9003f3fb95a0e816d58cfa268a72e52e6d8`  
		Last Modified: Wed, 25 Feb 2026 17:33:22 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e48d156f776b0a2da1758df77ebd46edfd1fad75d9263c2bf8f372f1512b67`  
		Last Modified: Wed, 25 Feb 2026 17:33:25 GMT  
		Size: 82.9 MB (82924266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:983e350c598a24824dc923bbf46cda0ef4bdae4f038af8eff88c8b6e962fd570`  
		Last Modified: Wed, 25 Feb 2026 17:33:22 GMT  
		Size: 517.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd8897b1c30e1f42aea23a38708759ab99d46124513222b00c6d6278b834abc`  
		Last Modified: Wed, 25 Feb 2026 17:33:23 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.8-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:39aad74b5cdb36ffcb31ad7ea28355818840cb560280535fa0ed9dba8a68571a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f8912a005531705bde9206c7cfbd729fba8b6021a5f966c0686b7f69a19610`

```dockerfile
```

-	Layers:
	-	`sha256:f7820589c3db8a4e9719fe6e0ee548b36c99b3d514cf136bf12da97fb3735d1c`  
		Last Modified: Wed, 25 Feb 2026 17:33:22 GMT  
		Size: 2.3 MB (2310571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af5e75a1973c652afdc1e55fee67cc715982acaf272ee16200297d6a2a256194`  
		Last Modified: Wed, 25 Feb 2026 17:33:22 GMT  
		Size: 17.6 KB (17617 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.8-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:6b45900e2ab53d82ae88dbbfcd757def6fe76ba93369743f2fd317b6a8e17846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110130123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97c5a1135218b678758c5822631868dabc3016114cad2e110d78f5678ae85e98`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Wed, 25 Feb 2026 17:44:14 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 25 Feb 2026 17:44:15 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 25 Feb 2026 17:44:21 GMT
ENV INFLUXDB_VERSION=3.8.3
# Wed, 25 Feb 2026 17:44:21 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 25 Feb 2026 17:44:21 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 25 Feb 2026 17:44:21 GMT
USER influxdb3
# Wed, 25 Feb 2026 17:44:21 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 25 Feb 2026 17:44:21 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 25 Feb 2026 17:44:21 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 25 Feb 2026 17:44:21 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 25 Feb 2026 17:44:21 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 25 Feb 2026 17:44:21 GMT
ENV LOG_FILTER=info
# Wed, 25 Feb 2026 17:44:21 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 25 Feb 2026 17:44:21 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 25 Feb 2026 17:44:21 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1600a9c64eb260873cf108122e4cdf204f8272ba853903f05a1c8ce4928cc9b`  
		Last Modified: Wed, 25 Feb 2026 17:44:35 GMT  
		Size: 6.7 MB (6681454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a8f741a77a6ec6590221f763db0c06a439f2b3a4f0234d2eeec7b43a90ae1b`  
		Last Modified: Wed, 25 Feb 2026 17:44:34 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc615a32cd32e801400994677df8f107cfa4f9e57facaed86ebf5028095ccde`  
		Last Modified: Wed, 25 Feb 2026 17:44:36 GMT  
		Size: 74.6 MB (74579225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884b5c05caaac19df93120744391be11a6fb6fa2dcc0caa05e0ae634e4aa8bcb`  
		Last Modified: Wed, 25 Feb 2026 17:44:34 GMT  
		Size: 520.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f395b8f9fbee60a71ca0db75d66de3ba21d8c72bc0b8a822efe23579e83020b`  
		Last Modified: Wed, 25 Feb 2026 17:44:36 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.8-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:8134d33f6efa7eeb3dd051b4647f98e2707d239233aca84041ba7e3ad027e527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893aff8378f9a605d056fb94eae68f81a8a0bf94be432174cf0acdf9d7631c86`

```dockerfile
```

-	Layers:
	-	`sha256:69b0b59299b0eda121a960ef36b94d23f04a3deb935dafcb63268337c659235c`  
		Last Modified: Wed, 25 Feb 2026 17:44:34 GMT  
		Size: 2.3 MB (2311653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9501d98ec72095cee13f3d9bc289f16f36f85c63d56c997e3930db1d51c228c3`  
		Last Modified: Wed, 25 Feb 2026 17:44:34 GMT  
		Size: 17.8 KB (17764 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.8-enterprise`

```console
$ docker pull influxdb@sha256:f392a1a9568870f6f15271b6292b6d95b117d82f2619f8c2b5ea8d54ae8ea628
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.8-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:0cc529867fa1f410068d02ce553c6d500ad395163eb5a74753e1ba475cb5d3eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128364098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b65d86e37fdd243fed5f8c89797813cebcc7d38aad80ea32828840d6699abd`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Wed, 25 Feb 2026 17:33:00 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 25 Feb 2026 17:33:00 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 25 Feb 2026 17:33:39 GMT
ENV INFLUXDB_VERSION=3.8.3
# Wed, 25 Feb 2026 17:33:39 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 25 Feb 2026 17:33:39 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 25 Feb 2026 17:33:39 GMT
USER influxdb3
# Wed, 25 Feb 2026 17:33:39 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 25 Feb 2026 17:33:39 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 25 Feb 2026 17:33:39 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 25 Feb 2026 17:33:39 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 25 Feb 2026 17:33:39 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 25 Feb 2026 17:33:39 GMT
ENV LOG_FILTER=info
# Wed, 25 Feb 2026 17:33:39 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 25 Feb 2026 17:33:39 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 25 Feb 2026 17:33:39 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9542c760bea8712a7b1c7320237ab218944b72df43f69ed08641fae1d8c8e62`  
		Last Modified: Wed, 25 Feb 2026 17:33:23 GMT  
		Size: 6.7 MB (6671516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173d8ef7fd2a07ba4c6d17512223b9003f3fb95a0e816d58cfa268a72e52e6d8`  
		Last Modified: Wed, 25 Feb 2026 17:33:22 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3fe89b6d0e71dea3acd1a59241822c25d4f05e78884b8211f97d7df3554c080`  
		Last Modified: Wed, 25 Feb 2026 17:33:57 GMT  
		Size: 92.0 MB (91960651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5735e88aedf81bd71267a38840c016d9a4b8db594299acc493756a02d1b619f2`  
		Last Modified: Wed, 25 Feb 2026 17:33:55 GMT  
		Size: 517.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd4ae8b9ddf57c50ba883b006c6e1ccc720ee5dfe33c3fb4d2bc255dc782ffa`  
		Last Modified: Wed, 25 Feb 2026 17:33:55 GMT  
		Size: 151.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.8-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:9918b7f24acf4aa4aee77ed1d7c7dcfafdd4fcfd17bb68ec6c5261bc6a6ba9c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aed0f2e1c167a5ce6e3b62bd9fc2dfa63b411a22b9dd9f94f84dafa143ac65dd`

```dockerfile
```

-	Layers:
	-	`sha256:a5919f172ad357c7bd480ad375d2118fdca042307adf9c07c10faa5ed6ea1336`  
		Last Modified: Wed, 25 Feb 2026 17:33:55 GMT  
		Size: 2.3 MB (2310619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f9822286a39b10571bd9835dc3e4b78a74c6e9eecd9f284b3f28cdace701242`  
		Last Modified: Wed, 25 Feb 2026 17:33:55 GMT  
		Size: 17.8 KB (17797 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.8-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:599b86bf46a9d8e9df22b4cb45afab9f2df2e4f0051cbb3c6bb32a7de45845df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (118967689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9282d312b323de847f08819402467b17b58ea8851fe2d6957b0db453fee2e450`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Wed, 25 Feb 2026 17:44:14 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 25 Feb 2026 17:44:15 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 25 Feb 2026 17:44:54 GMT
ENV INFLUXDB_VERSION=3.8.3
# Wed, 25 Feb 2026 17:44:54 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 25 Feb 2026 17:44:54 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 25 Feb 2026 17:44:54 GMT
USER influxdb3
# Wed, 25 Feb 2026 17:44:54 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 25 Feb 2026 17:44:54 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 25 Feb 2026 17:44:54 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 25 Feb 2026 17:44:54 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 25 Feb 2026 17:44:54 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 25 Feb 2026 17:44:54 GMT
ENV LOG_FILTER=info
# Wed, 25 Feb 2026 17:44:54 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 25 Feb 2026 17:44:54 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 25 Feb 2026 17:44:54 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1600a9c64eb260873cf108122e4cdf204f8272ba853903f05a1c8ce4928cc9b`  
		Last Modified: Wed, 25 Feb 2026 17:44:35 GMT  
		Size: 6.7 MB (6681454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a8f741a77a6ec6590221f763db0c06a439f2b3a4f0234d2eeec7b43a90ae1b`  
		Last Modified: Wed, 25 Feb 2026 17:44:34 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd98dae91172a1c1d44d43c624ddf280ec16f253dcdb0a43262c519ddf791bd`  
		Last Modified: Wed, 25 Feb 2026 17:45:10 GMT  
		Size: 83.4 MB (83416791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ed5be20f00166b950a72770bee50ba841f42986961f75925a87b6efc0ffe28`  
		Last Modified: Wed, 25 Feb 2026 17:45:08 GMT  
		Size: 520.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:792a89f12f8ec69ba70c82d56987e1b1a8dae7af9a84d516174ac5f968dc8f32`  
		Last Modified: Wed, 25 Feb 2026 17:45:08 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.8-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:e1e6d15a0cc91736906ee54a213ed9d97eb9f5d2497d726bc0adac9809dccdc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e16625a4304b70ceb915254f3a4f4ba276d89f77d521168a0fd43859089b3d5`

```dockerfile
```

-	Layers:
	-	`sha256:18286a9d2f68442ed57ed6beca7243dcbc5ec75c92490e315b4a11a05deb014d`  
		Last Modified: Wed, 25 Feb 2026 17:45:08 GMT  
		Size: 2.3 MB (2311701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd9c2cd867e205e55c2284c3881fff22b9bfc4c1f84da3702e84bb1aea735a4d`  
		Last Modified: Wed, 25 Feb 2026 17:45:08 GMT  
		Size: 17.9 KB (17946 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.8.3-core`

```console
$ docker pull influxdb@sha256:255268d2a5f42b8c38d373864a4ba72956d91e14a3361019706bfad2f7c039ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3.8.3-core` - linux; amd64

```console
$ docker pull influxdb@sha256:62775f106f8dac81e102b098d65ff85bced00936418c9689ec995c4ae081579a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.3 MB (119327710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:822ae8137edf72418a2e8940ae5d9ee9a540ba42089758cf7f152633aaa9a9a2`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Wed, 25 Feb 2026 17:33:00 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 25 Feb 2026 17:33:00 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 25 Feb 2026 17:33:07 GMT
ENV INFLUXDB_VERSION=3.8.3
# Wed, 25 Feb 2026 17:33:07 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 25 Feb 2026 17:33:07 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 25 Feb 2026 17:33:07 GMT
USER influxdb3
# Wed, 25 Feb 2026 17:33:07 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 25 Feb 2026 17:33:07 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 25 Feb 2026 17:33:07 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 25 Feb 2026 17:33:07 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 25 Feb 2026 17:33:07 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 25 Feb 2026 17:33:07 GMT
ENV LOG_FILTER=info
# Wed, 25 Feb 2026 17:33:07 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 25 Feb 2026 17:33:07 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 25 Feb 2026 17:33:07 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9542c760bea8712a7b1c7320237ab218944b72df43f69ed08641fae1d8c8e62`  
		Last Modified: Wed, 25 Feb 2026 17:33:23 GMT  
		Size: 6.7 MB (6671516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173d8ef7fd2a07ba4c6d17512223b9003f3fb95a0e816d58cfa268a72e52e6d8`  
		Last Modified: Wed, 25 Feb 2026 17:33:22 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e48d156f776b0a2da1758df77ebd46edfd1fad75d9263c2bf8f372f1512b67`  
		Last Modified: Wed, 25 Feb 2026 17:33:25 GMT  
		Size: 82.9 MB (82924266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:983e350c598a24824dc923bbf46cda0ef4bdae4f038af8eff88c8b6e962fd570`  
		Last Modified: Wed, 25 Feb 2026 17:33:22 GMT  
		Size: 517.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd8897b1c30e1f42aea23a38708759ab99d46124513222b00c6d6278b834abc`  
		Last Modified: Wed, 25 Feb 2026 17:33:23 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.8.3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:39aad74b5cdb36ffcb31ad7ea28355818840cb560280535fa0ed9dba8a68571a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f8912a005531705bde9206c7cfbd729fba8b6021a5f966c0686b7f69a19610`

```dockerfile
```

-	Layers:
	-	`sha256:f7820589c3db8a4e9719fe6e0ee548b36c99b3d514cf136bf12da97fb3735d1c`  
		Last Modified: Wed, 25 Feb 2026 17:33:22 GMT  
		Size: 2.3 MB (2310571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af5e75a1973c652afdc1e55fee67cc715982acaf272ee16200297d6a2a256194`  
		Last Modified: Wed, 25 Feb 2026 17:33:22 GMT  
		Size: 17.6 KB (17617 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3.8.3-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:6b45900e2ab53d82ae88dbbfcd757def6fe76ba93369743f2fd317b6a8e17846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110130123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97c5a1135218b678758c5822631868dabc3016114cad2e110d78f5678ae85e98`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Wed, 25 Feb 2026 17:44:14 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 25 Feb 2026 17:44:15 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 25 Feb 2026 17:44:21 GMT
ENV INFLUXDB_VERSION=3.8.3
# Wed, 25 Feb 2026 17:44:21 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 25 Feb 2026 17:44:21 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 25 Feb 2026 17:44:21 GMT
USER influxdb3
# Wed, 25 Feb 2026 17:44:21 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 25 Feb 2026 17:44:21 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 25 Feb 2026 17:44:21 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 25 Feb 2026 17:44:21 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 25 Feb 2026 17:44:21 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 25 Feb 2026 17:44:21 GMT
ENV LOG_FILTER=info
# Wed, 25 Feb 2026 17:44:21 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 25 Feb 2026 17:44:21 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 25 Feb 2026 17:44:21 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1600a9c64eb260873cf108122e4cdf204f8272ba853903f05a1c8ce4928cc9b`  
		Last Modified: Wed, 25 Feb 2026 17:44:35 GMT  
		Size: 6.7 MB (6681454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a8f741a77a6ec6590221f763db0c06a439f2b3a4f0234d2eeec7b43a90ae1b`  
		Last Modified: Wed, 25 Feb 2026 17:44:34 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc615a32cd32e801400994677df8f107cfa4f9e57facaed86ebf5028095ccde`  
		Last Modified: Wed, 25 Feb 2026 17:44:36 GMT  
		Size: 74.6 MB (74579225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884b5c05caaac19df93120744391be11a6fb6fa2dcc0caa05e0ae634e4aa8bcb`  
		Last Modified: Wed, 25 Feb 2026 17:44:34 GMT  
		Size: 520.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f395b8f9fbee60a71ca0db75d66de3ba21d8c72bc0b8a822efe23579e83020b`  
		Last Modified: Wed, 25 Feb 2026 17:44:36 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3.8.3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:8134d33f6efa7eeb3dd051b4647f98e2707d239233aca84041ba7e3ad027e527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893aff8378f9a605d056fb94eae68f81a8a0bf94be432174cf0acdf9d7631c86`

```dockerfile
```

-	Layers:
	-	`sha256:69b0b59299b0eda121a960ef36b94d23f04a3deb935dafcb63268337c659235c`  
		Last Modified: Wed, 25 Feb 2026 17:44:34 GMT  
		Size: 2.3 MB (2311653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9501d98ec72095cee13f3d9bc289f16f36f85c63d56c997e3930db1d51c228c3`  
		Last Modified: Wed, 25 Feb 2026 17:44:34 GMT  
		Size: 17.8 KB (17764 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.8.4-enterprise`

**does not exist** (yet?)

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
$ docker pull influxdb@sha256:255268d2a5f42b8c38d373864a4ba72956d91e14a3361019706bfad2f7c039ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:core` - linux; amd64

```console
$ docker pull influxdb@sha256:62775f106f8dac81e102b098d65ff85bced00936418c9689ec995c4ae081579a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.3 MB (119327710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:822ae8137edf72418a2e8940ae5d9ee9a540ba42089758cf7f152633aaa9a9a2`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Wed, 25 Feb 2026 17:33:00 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 25 Feb 2026 17:33:00 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 25 Feb 2026 17:33:07 GMT
ENV INFLUXDB_VERSION=3.8.3
# Wed, 25 Feb 2026 17:33:07 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 25 Feb 2026 17:33:07 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 25 Feb 2026 17:33:07 GMT
USER influxdb3
# Wed, 25 Feb 2026 17:33:07 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 25 Feb 2026 17:33:07 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 25 Feb 2026 17:33:07 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 25 Feb 2026 17:33:07 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 25 Feb 2026 17:33:07 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 25 Feb 2026 17:33:07 GMT
ENV LOG_FILTER=info
# Wed, 25 Feb 2026 17:33:07 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 25 Feb 2026 17:33:07 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 25 Feb 2026 17:33:07 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9542c760bea8712a7b1c7320237ab218944b72df43f69ed08641fae1d8c8e62`  
		Last Modified: Wed, 25 Feb 2026 17:33:23 GMT  
		Size: 6.7 MB (6671516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173d8ef7fd2a07ba4c6d17512223b9003f3fb95a0e816d58cfa268a72e52e6d8`  
		Last Modified: Wed, 25 Feb 2026 17:33:22 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e48d156f776b0a2da1758df77ebd46edfd1fad75d9263c2bf8f372f1512b67`  
		Last Modified: Wed, 25 Feb 2026 17:33:25 GMT  
		Size: 82.9 MB (82924266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:983e350c598a24824dc923bbf46cda0ef4bdae4f038af8eff88c8b6e962fd570`  
		Last Modified: Wed, 25 Feb 2026 17:33:22 GMT  
		Size: 517.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd8897b1c30e1f42aea23a38708759ab99d46124513222b00c6d6278b834abc`  
		Last Modified: Wed, 25 Feb 2026 17:33:23 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:39aad74b5cdb36ffcb31ad7ea28355818840cb560280535fa0ed9dba8a68571a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f8912a005531705bde9206c7cfbd729fba8b6021a5f966c0686b7f69a19610`

```dockerfile
```

-	Layers:
	-	`sha256:f7820589c3db8a4e9719fe6e0ee548b36c99b3d514cf136bf12da97fb3735d1c`  
		Last Modified: Wed, 25 Feb 2026 17:33:22 GMT  
		Size: 2.3 MB (2310571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af5e75a1973c652afdc1e55fee67cc715982acaf272ee16200297d6a2a256194`  
		Last Modified: Wed, 25 Feb 2026 17:33:22 GMT  
		Size: 17.6 KB (17617 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:6b45900e2ab53d82ae88dbbfcd757def6fe76ba93369743f2fd317b6a8e17846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110130123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97c5a1135218b678758c5822631868dabc3016114cad2e110d78f5678ae85e98`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Wed, 25 Feb 2026 17:44:14 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 25 Feb 2026 17:44:15 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 25 Feb 2026 17:44:21 GMT
ENV INFLUXDB_VERSION=3.8.3
# Wed, 25 Feb 2026 17:44:21 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 25 Feb 2026 17:44:21 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 25 Feb 2026 17:44:21 GMT
USER influxdb3
# Wed, 25 Feb 2026 17:44:21 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 25 Feb 2026 17:44:21 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 25 Feb 2026 17:44:21 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 25 Feb 2026 17:44:21 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 25 Feb 2026 17:44:21 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 25 Feb 2026 17:44:21 GMT
ENV LOG_FILTER=info
# Wed, 25 Feb 2026 17:44:21 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 25 Feb 2026 17:44:21 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 25 Feb 2026 17:44:21 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1600a9c64eb260873cf108122e4cdf204f8272ba853903f05a1c8ce4928cc9b`  
		Last Modified: Wed, 25 Feb 2026 17:44:35 GMT  
		Size: 6.7 MB (6681454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a8f741a77a6ec6590221f763db0c06a439f2b3a4f0234d2eeec7b43a90ae1b`  
		Last Modified: Wed, 25 Feb 2026 17:44:34 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc615a32cd32e801400994677df8f107cfa4f9e57facaed86ebf5028095ccde`  
		Last Modified: Wed, 25 Feb 2026 17:44:36 GMT  
		Size: 74.6 MB (74579225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884b5c05caaac19df93120744391be11a6fb6fa2dcc0caa05e0ae634e4aa8bcb`  
		Last Modified: Wed, 25 Feb 2026 17:44:34 GMT  
		Size: 520.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f395b8f9fbee60a71ca0db75d66de3ba21d8c72bc0b8a822efe23579e83020b`  
		Last Modified: Wed, 25 Feb 2026 17:44:36 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:8134d33f6efa7eeb3dd051b4647f98e2707d239233aca84041ba7e3ad027e527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893aff8378f9a605d056fb94eae68f81a8a0bf94be432174cf0acdf9d7631c86`

```dockerfile
```

-	Layers:
	-	`sha256:69b0b59299b0eda121a960ef36b94d23f04a3deb935dafcb63268337c659235c`  
		Last Modified: Wed, 25 Feb 2026 17:44:34 GMT  
		Size: 2.3 MB (2311653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9501d98ec72095cee13f3d9bc289f16f36f85c63d56c997e3930db1d51c228c3`  
		Last Modified: Wed, 25 Feb 2026 17:44:34 GMT  
		Size: 17.8 KB (17764 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:data`

```console
$ docker pull influxdb@sha256:40a5c206b6f380abae88b69ae0524895c1c2e942dba023a469101f76d2af1d31
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:data` - linux; amd64

```console
$ docker pull influxdb@sha256:155b636700f0303800c702d9a5399d444553918463a71d7c03e3001e694fbcd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114848805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae63172d05356fc4dd7607ef82abc295d6b12d9e8cb06daa68c35b0aa3508b8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:07:58 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Tue, 24 Feb 2026 20:07:58 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"         "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb" &&     rm -r "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc"           "influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:07:58 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Tue, 24 Feb 2026 20:07:58 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 24 Feb 2026 20:07:58 GMT
VOLUME [/var/lib/influxdb]
# Tue, 24 Feb 2026 20:07:58 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Feb 2026 20:07:58 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Tue, 24 Feb 2026 20:07:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 20:07:58 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab3b37e4807fe48145826511e16a527bbc4695222ceb966669a4d16729b3b94`  
		Last Modified: Tue, 24 Feb 2026 19:18:52 GMT  
		Size: 24.0 MB (24038450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097b775cb2b27f1be92722003efb2fdb5d4197757a50a9b95ab6a93b00497d0f`  
		Last Modified: Tue, 24 Feb 2026 20:08:11 GMT  
		Size: 42.3 MB (42319802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f444d666081f71dfd818ed6196fe39d16150c4af02efe1c5aee1553ea30b91`  
		Last Modified: Tue, 24 Feb 2026 20:08:09 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2740311728c56c143f1b5aba87ff0fc892e297fb301843e933c9bbf4deff525f`  
		Last Modified: Tue, 24 Feb 2026 20:08:10 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481ed7b20e0cef23ddc82013da6afb2579b45cf2c248e33227067fc6fe65ead0`  
		Last Modified: Tue, 24 Feb 2026 20:08:09 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:data` - unknown; unknown

```console
$ docker pull influxdb@sha256:5f0467d4ec768bcb4c700a4dd5f902b2ae1df8f87fe29d6259c92493799e5741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4700469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc8463996ea682da5336ee474467e07c1eb3be4cb528ba88155d7cc5440c2be`

```dockerfile
```

-	Layers:
	-	`sha256:92829c2cf557d9451e1bc187054f75422a5afeb34a4d86305f9d37fa7026f09c`  
		Last Modified: Tue, 24 Feb 2026 20:08:10 GMT  
		Size: 4.7 MB (4686392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d029d29b02f092a4d1ae8cc07df0ffc48d59a2d101c776e333697e726a40f9e`  
		Last Modified: Tue, 24 Feb 2026 20:08:09 GMT  
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
$ docker pull influxdb@sha256:f392a1a9568870f6f15271b6292b6d95b117d82f2619f8c2b5ea8d54ae8ea628
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:0cc529867fa1f410068d02ce553c6d500ad395163eb5a74753e1ba475cb5d3eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128364098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b65d86e37fdd243fed5f8c89797813cebcc7d38aad80ea32828840d6699abd`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Wed, 25 Feb 2026 17:33:00 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 25 Feb 2026 17:33:00 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 25 Feb 2026 17:33:39 GMT
ENV INFLUXDB_VERSION=3.8.3
# Wed, 25 Feb 2026 17:33:39 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 25 Feb 2026 17:33:39 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 25 Feb 2026 17:33:39 GMT
USER influxdb3
# Wed, 25 Feb 2026 17:33:39 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 25 Feb 2026 17:33:39 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 25 Feb 2026 17:33:39 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 25 Feb 2026 17:33:39 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 25 Feb 2026 17:33:39 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 25 Feb 2026 17:33:39 GMT
ENV LOG_FILTER=info
# Wed, 25 Feb 2026 17:33:39 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 25 Feb 2026 17:33:39 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 25 Feb 2026 17:33:39 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9542c760bea8712a7b1c7320237ab218944b72df43f69ed08641fae1d8c8e62`  
		Last Modified: Wed, 25 Feb 2026 17:33:23 GMT  
		Size: 6.7 MB (6671516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173d8ef7fd2a07ba4c6d17512223b9003f3fb95a0e816d58cfa268a72e52e6d8`  
		Last Modified: Wed, 25 Feb 2026 17:33:22 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3fe89b6d0e71dea3acd1a59241822c25d4f05e78884b8211f97d7df3554c080`  
		Last Modified: Wed, 25 Feb 2026 17:33:57 GMT  
		Size: 92.0 MB (91960651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5735e88aedf81bd71267a38840c016d9a4b8db594299acc493756a02d1b619f2`  
		Last Modified: Wed, 25 Feb 2026 17:33:55 GMT  
		Size: 517.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd4ae8b9ddf57c50ba883b006c6e1ccc720ee5dfe33c3fb4d2bc255dc782ffa`  
		Last Modified: Wed, 25 Feb 2026 17:33:55 GMT  
		Size: 151.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:9918b7f24acf4aa4aee77ed1d7c7dcfafdd4fcfd17bb68ec6c5261bc6a6ba9c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aed0f2e1c167a5ce6e3b62bd9fc2dfa63b411a22b9dd9f94f84dafa143ac65dd`

```dockerfile
```

-	Layers:
	-	`sha256:a5919f172ad357c7bd480ad375d2118fdca042307adf9c07c10faa5ed6ea1336`  
		Last Modified: Wed, 25 Feb 2026 17:33:55 GMT  
		Size: 2.3 MB (2310619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f9822286a39b10571bd9835dc3e4b78a74c6e9eecd9f284b3f28cdace701242`  
		Last Modified: Wed, 25 Feb 2026 17:33:55 GMT  
		Size: 17.8 KB (17797 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:599b86bf46a9d8e9df22b4cb45afab9f2df2e4f0051cbb3c6bb32a7de45845df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (118967689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9282d312b323de847f08819402467b17b58ea8851fe2d6957b0db453fee2e450`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Wed, 25 Feb 2026 17:44:14 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Wed, 25 Feb 2026 17:44:15 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Wed, 25 Feb 2026 17:44:54 GMT
ENV INFLUXDB_VERSION=3.8.3
# Wed, 25 Feb 2026 17:44:54 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Wed, 25 Feb 2026 17:44:54 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Wed, 25 Feb 2026 17:44:54 GMT
USER influxdb3
# Wed, 25 Feb 2026 17:44:54 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Wed, 25 Feb 2026 17:44:54 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Wed, 25 Feb 2026 17:44:54 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Wed, 25 Feb 2026 17:44:54 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Wed, 25 Feb 2026 17:44:54 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Wed, 25 Feb 2026 17:44:54 GMT
ENV LOG_FILTER=info
# Wed, 25 Feb 2026 17:44:54 GMT
EXPOSE map[8181/tcp:{}]
# Wed, 25 Feb 2026 17:44:54 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Wed, 25 Feb 2026 17:44:54 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1600a9c64eb260873cf108122e4cdf204f8272ba853903f05a1c8ce4928cc9b`  
		Last Modified: Wed, 25 Feb 2026 17:44:35 GMT  
		Size: 6.7 MB (6681454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a8f741a77a6ec6590221f763db0c06a439f2b3a4f0234d2eeec7b43a90ae1b`  
		Last Modified: Wed, 25 Feb 2026 17:44:34 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd98dae91172a1c1d44d43c624ddf280ec16f253dcdb0a43262c519ddf791bd`  
		Last Modified: Wed, 25 Feb 2026 17:45:10 GMT  
		Size: 83.4 MB (83416791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ed5be20f00166b950a72770bee50ba841f42986961f75925a87b6efc0ffe28`  
		Last Modified: Wed, 25 Feb 2026 17:45:08 GMT  
		Size: 520.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:792a89f12f8ec69ba70c82d56987e1b1a8dae7af9a84d516174ac5f968dc8f32`  
		Last Modified: Wed, 25 Feb 2026 17:45:08 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:e1e6d15a0cc91736906ee54a213ed9d97eb9f5d2497d726bc0adac9809dccdc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e16625a4304b70ceb915254f3a4f4ba276d89f77d521168a0fd43859089b3d5`

```dockerfile
```

-	Layers:
	-	`sha256:18286a9d2f68442ed57ed6beca7243dcbc5ec75c92490e315b4a11a05deb014d`  
		Last Modified: Wed, 25 Feb 2026 17:45:08 GMT  
		Size: 2.3 MB (2311701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd9c2cd867e205e55c2284c3881fff22b9bfc4c1f84da3702e84bb1aea735a4d`  
		Last Modified: Wed, 25 Feb 2026 17:45:08 GMT  
		Size: 17.9 KB (17946 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:latest`

```console
$ docker pull influxdb@sha256:60676b368409b4ac9664d1ba57b2613c5dec7c1a0f9dcd9405a0be0c375409f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:51f91b302e29e29ce2edc9d6bb455d9aa5817de4454ce05eef4a09e772e01f39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107240632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f3a2343a3671477cd132c7d9f4152a11fa2ee240eaaf42009286cd1766db09a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:24:31 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:24:32 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 24 Feb 2026 19:24:32 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 24 Feb 2026 19:24:33 GMT
ENV GOSU_VER=1.19
# Tue, 24 Feb 2026 19:24:33 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 24 Feb 2026 19:24:33 GMT
ENV INFLUXDB_VERSION=2.8.0
# Tue, 24 Feb 2026 19:24:33 GMT
ENV INFLUXDB_PR=-2
# Tue, 24 Feb 2026 19:24:33 GMT
ENV INFLUXDB_PV=2.8.0-2
# Tue, 24 Feb 2026 19:24:37 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 24 Feb 2026 19:24:37 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 24 Feb 2026 19:24:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 24 Feb 2026 19:24:38 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 24 Feb 2026 19:24:38 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 24 Feb 2026 19:24:38 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 24 Feb 2026 19:24:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Feb 2026 19:24:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 19:24:38 GMT
CMD ["influxd"]
# Tue, 24 Feb 2026 19:24:38 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 24 Feb 2026 19:24:38 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 24 Feb 2026 19:24:38 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 24 Feb 2026 19:24:38 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 24 Feb 2026 19:24:38 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29a72782dae8e2d0c2dd676903f07119956ff0ddbee522e846ca64f5d673ea3`  
		Last Modified: Tue, 24 Feb 2026 19:24:50 GMT  
		Size: 9.8 MB (9798239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e187256dc8671a9ea7ee2754ad32915bdf6e9351237d33cec709ef4a3b6690`  
		Last Modified: Tue, 24 Feb 2026 19:24:50 GMT  
		Size: 6.2 MB (6156985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754b7251cdd173cc2ed22540b88f024b57e2946a7d215fd66a6d5d569a5c7bc9`  
		Last Modified: Tue, 24 Feb 2026 19:24:49 GMT  
		Size: 3.2 KB (3223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2810d4ff70b30298726c86e4942b59ad3704e8afa238c27782a742d9f9f493f0`  
		Last Modified: Tue, 24 Feb 2026 19:24:49 GMT  
		Size: 811.5 KB (811476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:162f11ba0bc175e0762579610de84c1bf80b617956f2aca92c14352395489990`  
		Last Modified: Tue, 24 Feb 2026 19:24:52 GMT  
		Size: 50.5 MB (50451821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6589bf91aad0c6e9fac3002eecc32cb153e7a67fa0a8c13777b9a9572bd461`  
		Last Modified: Tue, 24 Feb 2026 19:24:51 GMT  
		Size: 11.8 MB (11775878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab4b0b785b1a6d9a356adbc43855407bb1895b8d8aae5e7315b2a2374eb7223`  
		Last Modified: Tue, 24 Feb 2026 19:24:51 GMT  
		Size: 211.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea8c9e5957a972ad576d0742f682159bfc40c965d0cc0ebfa57b2fd6216e32e`  
		Last Modified: Tue, 24 Feb 2026 19:24:51 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce1d9cfee12e80e9f4b7d7d4aeed9bcb4b69a0d170a990cb536a60401c5c538`  
		Last Modified: Tue, 24 Feb 2026 19:24:52 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:88ecbd1360961d9f6eb9da320021355e22fd4aa94850f617fc4a114492b6306d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2c1c3f01da9c818d49a617a327c5b682db93addcab90d1e5b434f6f61251b31`

```dockerfile
```

-	Layers:
	-	`sha256:09f8c63961fd2025d17ba710188931974d23034eca0c9c32e95d4f238fe3b448`  
		Last Modified: Tue, 24 Feb 2026 19:24:50 GMT  
		Size: 2.9 MB (2934237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63a982fec1badfad4e243a1da8cd71d94383a37e58b6300e8fd79a6e5d38520d`  
		Last Modified: Tue, 24 Feb 2026 19:24:49 GMT  
		Size: 33.6 KB (33621 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:ebd1ad4130df82ab4f633f9614ad1078df41c200a3054e5993228e4ba72e0b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103639647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b175a581af2a7af62bc8bbbada2a5107c0cc1adbde00775b335d8f113d66b09`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:29:09 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:29:09 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Tue, 24 Feb 2026 19:29:09 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Tue, 24 Feb 2026 19:29:11 GMT
ENV GOSU_VER=1.19
# Tue, 24 Feb 2026 19:29:11 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Tue, 24 Feb 2026 19:29:11 GMT
ENV INFLUXDB_VERSION=2.8.0
# Tue, 24 Feb 2026 19:29:11 GMT
ENV INFLUXDB_PR=-2
# Tue, 24 Feb 2026 19:29:11 GMT
ENV INFLUXDB_PV=2.8.0-2
# Tue, 24 Feb 2026 19:29:15 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Tue, 24 Feb 2026 19:29:15 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Tue, 24 Feb 2026 19:29:16 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Tue, 24 Feb 2026 19:29:16 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Tue, 24 Feb 2026 19:29:16 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 24 Feb 2026 19:29:16 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Tue, 24 Feb 2026 19:29:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Feb 2026 19:29:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 19:29:16 GMT
CMD ["influxd"]
# Tue, 24 Feb 2026 19:29:16 GMT
EXPOSE map[8086/tcp:{}]
# Tue, 24 Feb 2026 19:29:16 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 24 Feb 2026 19:29:16 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 24 Feb 2026 19:29:16 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 24 Feb 2026 19:29:16 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0972f022d79a6181cce6188986c7899054c4374abffea6fb9207121bb45c80d9`  
		Last Modified: Tue, 24 Feb 2026 19:29:28 GMT  
		Size: 9.6 MB (9626871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e14b6090329229da5fd6f4042c8cdb0b06710efc78f68d31e344861b7b0e2a`  
		Last Modified: Tue, 24 Feb 2026 19:29:27 GMT  
		Size: 5.8 MB (5790414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7773d217697f39b64fd0eb3704baf907e6d6e52e2ecdd1fef3bd4917ec118597`  
		Last Modified: Tue, 24 Feb 2026 19:29:27 GMT  
		Size: 3.2 KB (3228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c43a53e1b3108d2b67b3ea5c71d60d9c9b2e0a80573fcf4dfdb0da4b0f986a8b`  
		Last Modified: Tue, 24 Feb 2026 19:29:27 GMT  
		Size: 766.4 KB (766373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6198a91ebeffd09d491d5b6faa9c006923cfedf1420e59e1c07687a30a0b50`  
		Last Modified: Tue, 24 Feb 2026 19:29:30 GMT  
		Size: 48.2 MB (48229560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ee346ad7d6a8f3f20a9e0e764accda51fc4c423404d1edc7c35072f9d2890e`  
		Last Modified: Tue, 24 Feb 2026 19:29:28 GMT  
		Size: 11.1 MB (11100389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1bda9b68d1668c1ea61f245e536c240787680a21bfab2a4226f3cb806a12fe2`  
		Last Modified: Tue, 24 Feb 2026 19:29:28 GMT  
		Size: 210.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b917881adf30187773219c9f82f321beb1e65fc183140c007a1f00113900982`  
		Last Modified: Tue, 24 Feb 2026 19:29:29 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ba8c8eb7f196b123dfa17207a68bab975b39d9f792b615c7f3226193377d0f`  
		Last Modified: Tue, 24 Feb 2026 19:29:29 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:b4c95f6c1e881ee21dbfc3608222b824dff7221141f8f7f0e63bb50382a864d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ad0a394ffb79894431b79112075fa33a8da4b9af83d4558efb4e3b633c3bfbb`

```dockerfile
```

-	Layers:
	-	`sha256:0b1cd26abacc2d2c4d46b117a2d163ebde6b332ad8005d816af61c700e4360d8`  
		Last Modified: Tue, 24 Feb 2026 19:29:27 GMT  
		Size: 2.9 MB (2933717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29e07eaf66c27e08b1e26f8744e41143741c5682f0a31dded582b8047d9ac96b`  
		Last Modified: Tue, 24 Feb 2026 19:29:26 GMT  
		Size: 33.8 KB (33815 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:meta`

```console
$ docker pull influxdb@sha256:870a545ecc6d7f384d9d95ebdefe94c9f71fc389138fd78d6f8f6ef794339f93
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:meta` - linux; amd64

```console
$ docker pull influxdb@sha256:3ea08f1dd67708e3f236fcaf2beeb38e3420f7dd148e3ae3557ed2b6e8b42d87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91308642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd0408fdfebdd6d30fca8f1b4b6900ef5b86163779484b8ef51e06649f061a82`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:08:02 GMT
ENV INFLUXDB_VERSION=1.12.2-c1.12.2
# Tue, 24 Feb 2026 20:08:02 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"         "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb" &&     rm -r "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc"           "influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:08:02 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Tue, 24 Feb 2026 20:08:02 GMT
EXPOSE map[8091/tcp:{}]
# Tue, 24 Feb 2026 20:08:02 GMT
VOLUME [/var/lib/influxdb]
# Tue, 24 Feb 2026 20:08:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 24 Feb 2026 20:08:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Feb 2026 20:08:02 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab3b37e4807fe48145826511e16a527bbc4695222ceb966669a4d16729b3b94`  
		Last Modified: Tue, 24 Feb 2026 19:18:52 GMT  
		Size: 24.0 MB (24038450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe73a33fbd74774b5656ba240fd4b80929188336a7dbcac04888686d532f9eeb`  
		Last Modified: Tue, 24 Feb 2026 20:08:12 GMT  
		Size: 18.8 MB (18780849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de483592411eb2e58aec7264221b1d7e548bb39f7d27e7e780c38fc0939fa2b2`  
		Last Modified: Tue, 24 Feb 2026 20:08:11 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5e0f613809771fa649a15fd30247095d1435cf09a18b1c419dd23e2fb93f8d`  
		Last Modified: Tue, 24 Feb 2026 20:08:12 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:85f0fef50e41b9b3d7872f7fb04555915c63d0aad3745a0047f21a9816dee3f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4604146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf9900ce74fff1e8d4fb23312927ca743bd936c5f901cadbf0b98bd18656d700`

```dockerfile
```

-	Layers:
	-	`sha256:bc06be1fbb5e04ec1d186c2ce2c60e1de2086cb324856d13f3e3ad44fc2e79cf`  
		Last Modified: Tue, 24 Feb 2026 20:08:12 GMT  
		Size: 4.6 MB (4591555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4bae4f6329aff18224f10f1bedf7f4dbbd3e5200c8d9f6faca06fa57156d287`  
		Last Modified: Tue, 24 Feb 2026 20:08:11 GMT  
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
