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
-	[`influxdb:1.12.3`](#influxdb1123)
-	[`influxdb:1.12.3-alpine`](#influxdb1123-alpine)
-	[`influxdb:1.12.3-data`](#influxdb1123-data)
-	[`influxdb:1.12.3-data-alpine`](#influxdb1123-data-alpine)
-	[`influxdb:1.12.3-meta`](#influxdb1123-meta)
-	[`influxdb:1.12.3-meta-alpine`](#influxdb1123-meta-alpine)
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
-	[`influxdb:3.9.0-core`](#influxdb390-core)
-	[`influxdb:3.9.0-enterprise`](#influxdb390-enterprise)
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
$ docker pull influxdb@sha256:14d1ff0b2100a23c6d41f0f9f682886cb8f2877ebb9c132aeb85a79f34d82871
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11` - linux; amd64

```console
$ docker pull influxdb@sha256:0764d142983621452fe51d204b68d6d8b9caa652f0154b81b9be761c8a549321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116185816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b14af512fbfe3fbeacf73be90e0cfc67a6f7b3ad8b917376c4b7dd90b1301a2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:37:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:29:37 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Mon, 16 Mar 2026 23:29:45 GMT
ARG INFLUXDB_VERSION=1.11.8
# Mon, 16 Mar 2026 23:29:45 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:29:45 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Mon, 16 Mar 2026 23:29:45 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 16 Mar 2026 23:29:45 GMT
VOLUME [/var/lib/influxdb]
# Mon, 16 Mar 2026 23:29:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 23:29:45 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Mon, 16 Mar 2026 23:29:45 GMT
USER influxdb
# Mon, 16 Mar 2026 23:29:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 23:29:45 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fa3468d221545a43d2151f3977695a31857f9342ba842627d03c9fa1b2ae02`  
		Last Modified: Mon, 16 Mar 2026 22:37:09 GMT  
		Size: 24.0 MB (24038304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e0a9a9cacb78ff932d27937ccb59b96a3ca7f5a8bfedc1373985cf0eea2368`  
		Last Modified: Mon, 16 Mar 2026 23:29:59 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f742a65bcd9d11529f74d530ef24f95304fe36dff935450266d21d97a86f0416`  
		Last Modified: Mon, 16 Mar 2026 23:30:00 GMT  
		Size: 43.7 MB (43656023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a833d5323a9ee64d2e0b5cf720e61df3334eb589d7f2e54e4834f5818c252a8`  
		Last Modified: Mon, 16 Mar 2026 23:29:59 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6217d6ad620ec7dde19664dec713b15fdd415a0c76ea9dab40cf4e26bd9fb47`  
		Last Modified: Mon, 16 Mar 2026 23:29:59 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6187c4c6f00a8856ab98ec0251a70275f9e437bcc9ee44cfa107e67c90675b47`  
		Last Modified: Mon, 16 Mar 2026 23:30:00 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11` - unknown; unknown

```console
$ docker pull influxdb@sha256:bc49d8d906b174e1fae64d0aa65b3eb9c49026047ae93ba16eb444c57db87b90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c30b8bae552f0f2883deb5dd0d68101a618b3ea155cfccf10e7aa8f0df61ee`

```dockerfile
```

-	Layers:
	-	`sha256:d9ca9a1c6123a86f9ed6860b66527b5d7c5122fc0efd46050539f585016dbe4a`  
		Last Modified: Mon, 16 Mar 2026 23:29:59 GMT  
		Size: 5.1 MB (5079263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28d842dd2fc582442789735967a9c1890fab031fb6a508002354976c2095b5bf`  
		Last Modified: Mon, 16 Mar 2026 23:29:59 GMT  
		Size: 15.5 KB (15486 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:b3cc11c08b8b5d48052648b1ee461bb872d5909c893c648e2ab104aadecea5de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113103469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e392d640ee2d9100c33c9c3caf53ce313aefd46422083e790078cb128395789`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:39:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:34:31 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Mon, 16 Mar 2026 23:35:07 GMT
ARG INFLUXDB_VERSION=1.11.8
# Mon, 16 Mar 2026 23:35:07 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:35:07 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Mon, 16 Mar 2026 23:35:07 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 16 Mar 2026 23:35:07 GMT
VOLUME [/var/lib/influxdb]
# Mon, 16 Mar 2026 23:35:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 23:35:07 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Mon, 16 Mar 2026 23:35:07 GMT
USER influxdb
# Mon, 16 Mar 2026 23:35:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 23:35:07 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:2ea98bb5eec9d02a0d7b59638c683db4e1e749f998a317bc731e9506f8480b12`  
		Last Modified: Mon, 16 Mar 2026 21:52:02 GMT  
		Size: 48.4 MB (48373032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbce225727d69d170353500d8834770da849cbdcea48de37e492fe14ef880d0`  
		Last Modified: Mon, 16 Mar 2026 22:39:28 GMT  
		Size: 23.6 MB (23604701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d78bf6e36546eff745de95e5852f7513fec76ebdee9d03dabaa69c9af8105b`  
		Last Modified: Mon, 16 Mar 2026 23:34:51 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f008d80f4fa231b7f0c4bd06533d4cff8242ffba670185d227c027a42f991bcf`  
		Last Modified: Mon, 16 Mar 2026 23:35:19 GMT  
		Size: 41.1 MB (41122830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dccee64b7323af800050ae6e618085474476e1f9beaf4340b55ae81ef530264`  
		Last Modified: Mon, 16 Mar 2026 23:35:18 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d928edbb9424108ee755e108493c696e5512fd6cfba4007ef2f7641f655cbbc`  
		Last Modified: Mon, 16 Mar 2026 23:35:18 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b6fb5fbd6677e812bacad26461c62eda327b648d11b9a3c29a1f45c9f8e55b2`  
		Last Modified: Mon, 16 Mar 2026 23:35:18 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11` - unknown; unknown

```console
$ docker pull influxdb@sha256:ca0c857ac78b2faca616180abaec17b6b3482ecec43dd3f1082ca3ae4de720f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d69c4f3c8cce1e2576c0b08d2bf710afe52eaaf63de13d9d7047e9af3d51fab`

```dockerfile
```

-	Layers:
	-	`sha256:ab18befc14a2a743505cff517c03bb696b946b2b7cd88b251ef761c584505436`  
		Last Modified: Mon, 16 Mar 2026 23:35:19 GMT  
		Size: 5.1 MB (5078728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5864067a7a5c7b031077295ed5229cf72c3f0e75b049dcbecff589878f391a43`  
		Last Modified: Mon, 16 Mar 2026 23:35:18 GMT  
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
$ docker pull influxdb@sha256:18adc0912903e151289cd091e4e94f04018749cbf747821aa83796139e3bae5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-data` - linux; amd64

```console
$ docker pull influxdb@sha256:dd93493dc185f596ca3c6f10400ff01cf20dcc6cc96774544cdcc551003b6b34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114699455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c1fe362238abbbb4a5e88ffc671d28009b4dc239847e5432bd88506a647e436`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:37:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:29:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 16 Mar 2026 23:29:50 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Mon, 16 Mar 2026 23:29:50 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Mon, 16 Mar 2026 23:29:50 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Mon, 16 Mar 2026 23:29:50 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 16 Mar 2026 23:29:50 GMT
VOLUME [/var/lib/influxdb]
# Mon, 16 Mar 2026 23:29:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 23:29:50 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Mon, 16 Mar 2026 23:29:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 23:29:50 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fa3468d221545a43d2151f3977695a31857f9342ba842627d03c9fa1b2ae02`  
		Last Modified: Mon, 16 Mar 2026 22:37:09 GMT  
		Size: 24.0 MB (24038304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab60dbbb6b4dab1f29660c41db2f367ba15bd51cdc95d2f66534f56ea9b7d529`  
		Last Modified: Mon, 16 Mar 2026 23:30:02 GMT  
		Size: 5.1 KB (5055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e2ee73be5569eacce89d676c21f10dd0f010e8f77d43cdd1139e4fd4f74548`  
		Last Modified: Mon, 16 Mar 2026 23:30:03 GMT  
		Size: 42.2 MB (42165738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4174300deb61071f7b1a781a0894a0d3c0d2d219268ad26f124f2ad8c647cffd`  
		Last Modified: Mon, 16 Mar 2026 23:30:02 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6af2851f0a012cf1571e7448d3f0ade1ede9802d40d370e5e944d907fa45171`  
		Last Modified: Mon, 16 Mar 2026 23:30:02 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2653c1f9ba3c4c12f8e06aaa62a27f5f883fd50765540a7d129affc755f59bb`  
		Last Modified: Mon, 16 Mar 2026 23:30:03 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:33167c6b059f0681eb40e3416a11a01a5ebf92bdaed0dc5c4d463b0c7461f1bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4699070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c5e563b9a42a725e8575663be7a8be816e1f25ac2bf08688693be7d42470e31`

```dockerfile
```

-	Layers:
	-	`sha256:65e5e22a9acc1a73fa4ffeb8f488c39fca60d254c1afa421cbe6bb4d91f5a9a4`  
		Last Modified: Mon, 16 Mar 2026 23:30:02 GMT  
		Size: 4.7 MB (4684406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:042256e03c41932c3eece7b85044f27f3b45fa25df405193a1620b428111b88a`  
		Last Modified: Mon, 16 Mar 2026 23:30:02 GMT  
		Size: 14.7 KB (14664 bytes)  
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
$ docker pull influxdb@sha256:5f4fed01c8add37aef6530d85a92eee61c624d1029cc0e455398180894c48308
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:634d943fb8081244df8fc7e8c8978cf7da351eae84bbc5c27c4db61cc4df734e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91128658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e39c01a12b802f02997f3eac6f3ba4de3c5ee55951c7b1714a735246a225b8c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:37:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:29:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 16 Mar 2026 23:29:43 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Mon, 16 Mar 2026 23:29:43 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Mon, 16 Mar 2026 23:29:43 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Mon, 16 Mar 2026 23:29:43 GMT
EXPOSE map[8091/tcp:{}]
# Mon, 16 Mar 2026 23:29:43 GMT
VOLUME [/var/lib/influxdb]
# Mon, 16 Mar 2026 23:29:43 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 23:29:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 23:29:43 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fa3468d221545a43d2151f3977695a31857f9342ba842627d03c9fa1b2ae02`  
		Last Modified: Mon, 16 Mar 2026 22:37:09 GMT  
		Size: 24.0 MB (24038304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df9bbebe44575c63e2f70a92de1ffeb564c648162fb8937b5f6694a466799fe`  
		Last Modified: Mon, 16 Mar 2026 23:29:51 GMT  
		Size: 5.1 KB (5060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca587a13abf721e627eb580cc04d444e7e0165772f1227d09bf8357c65655b77`  
		Last Modified: Mon, 16 Mar 2026 23:29:52 GMT  
		Size: 18.6 MB (18596148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd404110a023556a399bf876f1d8bd016851a11bf0e8367cc85c84e852511f1a`  
		Last Modified: Mon, 16 Mar 2026 23:29:52 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f08adc75e3c47006f90dbd7301668b7b369fbb74f6307c697b0e0029f00db1`  
		Last Modified: Mon, 16 Mar 2026 23:29:52 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:5e120b4b6cefb84a761617df3fb7b5a9b2f1bf16bb9c796dcd21de155ee60a3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4604273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee4903a150daf8b1758a105826a33ea90410ba37498d7771348ab9e1d3641e2b`

```dockerfile
```

-	Layers:
	-	`sha256:7fc5b4dbe10ac632f24ad6b7ad7e73ac48e8fdeaeac389bfe822161d3bdd559d`  
		Last Modified: Mon, 16 Mar 2026 23:29:52 GMT  
		Size: 4.6 MB (4591249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c433f6c875c5d8a5f7cc7132c3990a48733ec5cc57c0577cbc43f2f7cf7024f`  
		Last Modified: Mon, 16 Mar 2026 23:29:51 GMT  
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
$ docker pull influxdb@sha256:14d1ff0b2100a23c6d41f0f9f682886cb8f2877ebb9c132aeb85a79f34d82871
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.11.8` - linux; amd64

```console
$ docker pull influxdb@sha256:0764d142983621452fe51d204b68d6d8b9caa652f0154b81b9be761c8a549321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116185816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b14af512fbfe3fbeacf73be90e0cfc67a6f7b3ad8b917376c4b7dd90b1301a2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:37:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:29:37 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Mon, 16 Mar 2026 23:29:45 GMT
ARG INFLUXDB_VERSION=1.11.8
# Mon, 16 Mar 2026 23:29:45 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:29:45 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Mon, 16 Mar 2026 23:29:45 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 16 Mar 2026 23:29:45 GMT
VOLUME [/var/lib/influxdb]
# Mon, 16 Mar 2026 23:29:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 23:29:45 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Mon, 16 Mar 2026 23:29:45 GMT
USER influxdb
# Mon, 16 Mar 2026 23:29:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 23:29:45 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fa3468d221545a43d2151f3977695a31857f9342ba842627d03c9fa1b2ae02`  
		Last Modified: Mon, 16 Mar 2026 22:37:09 GMT  
		Size: 24.0 MB (24038304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e0a9a9cacb78ff932d27937ccb59b96a3ca7f5a8bfedc1373985cf0eea2368`  
		Last Modified: Mon, 16 Mar 2026 23:29:59 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f742a65bcd9d11529f74d530ef24f95304fe36dff935450266d21d97a86f0416`  
		Last Modified: Mon, 16 Mar 2026 23:30:00 GMT  
		Size: 43.7 MB (43656023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a833d5323a9ee64d2e0b5cf720e61df3334eb589d7f2e54e4834f5818c252a8`  
		Last Modified: Mon, 16 Mar 2026 23:29:59 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6217d6ad620ec7dde19664dec713b15fdd415a0c76ea9dab40cf4e26bd9fb47`  
		Last Modified: Mon, 16 Mar 2026 23:29:59 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6187c4c6f00a8856ab98ec0251a70275f9e437bcc9ee44cfa107e67c90675b47`  
		Last Modified: Mon, 16 Mar 2026 23:30:00 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:bc49d8d906b174e1fae64d0aa65b3eb9c49026047ae93ba16eb444c57db87b90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c30b8bae552f0f2883deb5dd0d68101a618b3ea155cfccf10e7aa8f0df61ee`

```dockerfile
```

-	Layers:
	-	`sha256:d9ca9a1c6123a86f9ed6860b66527b5d7c5122fc0efd46050539f585016dbe4a`  
		Last Modified: Mon, 16 Mar 2026 23:29:59 GMT  
		Size: 5.1 MB (5079263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28d842dd2fc582442789735967a9c1890fab031fb6a508002354976c2095b5bf`  
		Last Modified: Mon, 16 Mar 2026 23:29:59 GMT  
		Size: 15.5 KB (15486 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.11.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:b3cc11c08b8b5d48052648b1ee461bb872d5909c893c648e2ab104aadecea5de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113103469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e392d640ee2d9100c33c9c3caf53ce313aefd46422083e790078cb128395789`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:39:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:34:31 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Mon, 16 Mar 2026 23:35:07 GMT
ARG INFLUXDB_VERSION=1.11.8
# Mon, 16 Mar 2026 23:35:07 GMT
# ARGS: INFLUXDB_VERSION=1.11.8
RUN gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     case "$(dpkg --print-architecture)" in       *amd64) ARCH=amd64 ;;       *arm64) ARCH=arm64 ;;       *) exit 1 ;;     esac &&     export INFLUXDB_DEB=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb &&     export INFLUXDB_ASC=influxdb-${INFLUXDB_VERSION}-${ARCH}.deb.asc &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_DEB}" &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/${INFLUXDB_ASC}" &&     gpg --batch --verify "${INFLUXDB_ASC}" "${INFLUXDB_DEB}" &&     apt-get install -y "./${INFLUXDB_DEB}" &&     rm -rf "${INFLUXDB_DEB}"            "${INFLUXDB_ASC}" 	   /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:35:07 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Mon, 16 Mar 2026 23:35:07 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 16 Mar 2026 23:35:07 GMT
VOLUME [/var/lib/influxdb]
# Mon, 16 Mar 2026 23:35:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 23:35:07 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Mon, 16 Mar 2026 23:35:07 GMT
USER influxdb
# Mon, 16 Mar 2026 23:35:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 23:35:07 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:2ea98bb5eec9d02a0d7b59638c683db4e1e749f998a317bc731e9506f8480b12`  
		Last Modified: Mon, 16 Mar 2026 21:52:02 GMT  
		Size: 48.4 MB (48373032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbce225727d69d170353500d8834770da849cbdcea48de37e492fe14ef880d0`  
		Last Modified: Mon, 16 Mar 2026 22:39:28 GMT  
		Size: 23.6 MB (23604701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d78bf6e36546eff745de95e5852f7513fec76ebdee9d03dabaa69c9af8105b`  
		Last Modified: Mon, 16 Mar 2026 23:34:51 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f008d80f4fa231b7f0c4bd06533d4cff8242ffba670185d227c027a42f991bcf`  
		Last Modified: Mon, 16 Mar 2026 23:35:19 GMT  
		Size: 41.1 MB (41122830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dccee64b7323af800050ae6e618085474476e1f9beaf4340b55ae81ef530264`  
		Last Modified: Mon, 16 Mar 2026 23:35:18 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d928edbb9424108ee755e108493c696e5512fd6cfba4007ef2f7641f655cbbc`  
		Last Modified: Mon, 16 Mar 2026 23:35:18 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b6fb5fbd6677e812bacad26461c62eda327b648d11b9a3c29a1f45c9f8e55b2`  
		Last Modified: Mon, 16 Mar 2026 23:35:18 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:ca0c857ac78b2faca616180abaec17b6b3482ecec43dd3f1082ca3ae4de720f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d69c4f3c8cce1e2576c0b08d2bf710afe52eaaf63de13d9d7047e9af3d51fab`

```dockerfile
```

-	Layers:
	-	`sha256:ab18befc14a2a743505cff517c03bb696b946b2b7cd88b251ef761c584505436`  
		Last Modified: Mon, 16 Mar 2026 23:35:19 GMT  
		Size: 5.1 MB (5078728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5864067a7a5c7b031077295ed5229cf72c3f0e75b049dcbecff589878f391a43`  
		Last Modified: Mon, 16 Mar 2026 23:35:18 GMT  
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
$ docker pull influxdb@sha256:18adc0912903e151289cd091e4e94f04018749cbf747821aa83796139e3bae5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.9-data` - linux; amd64

```console
$ docker pull influxdb@sha256:dd93493dc185f596ca3c6f10400ff01cf20dcc6cc96774544cdcc551003b6b34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114699455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c1fe362238abbbb4a5e88ffc671d28009b4dc239847e5432bd88506a647e436`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:37:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:29:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 16 Mar 2026 23:29:50 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Mon, 16 Mar 2026 23:29:50 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-data_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Mon, 16 Mar 2026 23:29:50 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Mon, 16 Mar 2026 23:29:50 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 16 Mar 2026 23:29:50 GMT
VOLUME [/var/lib/influxdb]
# Mon, 16 Mar 2026 23:29:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 23:29:50 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Mon, 16 Mar 2026 23:29:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 23:29:50 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fa3468d221545a43d2151f3977695a31857f9342ba842627d03c9fa1b2ae02`  
		Last Modified: Mon, 16 Mar 2026 22:37:09 GMT  
		Size: 24.0 MB (24038304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab60dbbb6b4dab1f29660c41db2f367ba15bd51cdc95d2f66534f56ea9b7d529`  
		Last Modified: Mon, 16 Mar 2026 23:30:02 GMT  
		Size: 5.1 KB (5055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e2ee73be5569eacce89d676c21f10dd0f010e8f77d43cdd1139e4fd4f74548`  
		Last Modified: Mon, 16 Mar 2026 23:30:03 GMT  
		Size: 42.2 MB (42165738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4174300deb61071f7b1a781a0894a0d3c0d2d219268ad26f124f2ad8c647cffd`  
		Last Modified: Mon, 16 Mar 2026 23:30:02 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6af2851f0a012cf1571e7448d3f0ade1ede9802d40d370e5e944d907fa45171`  
		Last Modified: Mon, 16 Mar 2026 23:30:02 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2653c1f9ba3c4c12f8e06aaa62a27f5f883fd50765540a7d129affc755f59bb`  
		Last Modified: Mon, 16 Mar 2026 23:30:03 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.9-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:33167c6b059f0681eb40e3416a11a01a5ebf92bdaed0dc5c4d463b0c7461f1bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4699070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c5e563b9a42a725e8575663be7a8be816e1f25ac2bf08688693be7d42470e31`

```dockerfile
```

-	Layers:
	-	`sha256:65e5e22a9acc1a73fa4ffeb8f488c39fca60d254c1afa421cbe6bb4d91f5a9a4`  
		Last Modified: Mon, 16 Mar 2026 23:30:02 GMT  
		Size: 4.7 MB (4684406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:042256e03c41932c3eece7b85044f27f3b45fa25df405193a1620b428111b88a`  
		Last Modified: Mon, 16 Mar 2026 23:30:02 GMT  
		Size: 14.7 KB (14664 bytes)  
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
$ docker pull influxdb@sha256:5f4fed01c8add37aef6530d85a92eee61c624d1029cc0e455398180894c48308
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.11.9-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:634d943fb8081244df8fc7e8c8978cf7da351eae84bbc5c27c4db61cc4df734e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91128658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e39c01a12b802f02997f3eac6f3ba4de3c5ee55951c7b1714a735246a225b8c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:37:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:29:42 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 16 Mar 2026 23:29:43 GMT
ENV INFLUXDB_VERSION=1.11.9-c1.11.9
# Mon, 16 Mar 2026 23:29:43 GMT
RUN wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     gpg --batch --verify influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb.asc influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     dpkg -i influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb &&     rm -f influxdb-meta_${INFLUXDB_VERSION}-1_amd64.deb* # buildkit
# Mon, 16 Mar 2026 23:29:43 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Mon, 16 Mar 2026 23:29:43 GMT
EXPOSE map[8091/tcp:{}]
# Mon, 16 Mar 2026 23:29:43 GMT
VOLUME [/var/lib/influxdb]
# Mon, 16 Mar 2026 23:29:43 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 23:29:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 23:29:43 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fa3468d221545a43d2151f3977695a31857f9342ba842627d03c9fa1b2ae02`  
		Last Modified: Mon, 16 Mar 2026 22:37:09 GMT  
		Size: 24.0 MB (24038304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df9bbebe44575c63e2f70a92de1ffeb564c648162fb8937b5f6694a466799fe`  
		Last Modified: Mon, 16 Mar 2026 23:29:51 GMT  
		Size: 5.1 KB (5060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca587a13abf721e627eb580cc04d444e7e0165772f1227d09bf8357c65655b77`  
		Last Modified: Mon, 16 Mar 2026 23:29:52 GMT  
		Size: 18.6 MB (18596148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd404110a023556a399bf876f1d8bd016851a11bf0e8367cc85c84e852511f1a`  
		Last Modified: Mon, 16 Mar 2026 23:29:52 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f08adc75e3c47006f90dbd7301668b7b369fbb74f6307c697b0e0029f00db1`  
		Last Modified: Mon, 16 Mar 2026 23:29:52 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.11.9-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:5e120b4b6cefb84a761617df3fb7b5a9b2f1bf16bb9c796dcd21de155ee60a3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4604273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee4903a150daf8b1758a105826a33ea90410ba37498d7771348ab9e1d3641e2b`

```dockerfile
```

-	Layers:
	-	`sha256:7fc5b4dbe10ac632f24ad6b7ad7e73ac48e8fdeaeac389bfe822161d3bdd559d`  
		Last Modified: Mon, 16 Mar 2026 23:29:52 GMT  
		Size: 4.6 MB (4591249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c433f6c875c5d8a5f7cc7132c3990a48733ec5cc57c0577cbc43f2f7cf7024f`  
		Last Modified: Mon, 16 Mar 2026 23:29:51 GMT  
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
$ docker pull influxdb@sha256:35e9976120a18fff82fefcc06d631de7585f33e7b096e9128465e6c15a9233fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.12` - linux; amd64

```console
$ docker pull influxdb@sha256:c9e597f49f562e9c7df34bbac4a78480f8ef698869c8b78b7a3c5047cceef260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114650223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e71c51e68940d034f29b79f7dddebb1655e799af27271908e7bf9696b9b0691`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:37:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:29:17 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Mon, 16 Mar 2026 23:29:22 GMT
ENV INFLUXDB_VERSION=1.12.3
# Mon, 16 Mar 2026 23:29:22 GMT
ENV INFLUXDB_PR=-1
# Mon, 16 Mar 2026 23:29:22 GMT
ENV INFLUXDB_PV=1.12.3-1
# Mon, 16 Mar 2026 23:29:22 GMT
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_PV}_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:29:22 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Mon, 16 Mar 2026 23:29:22 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 16 Mar 2026 23:29:22 GMT
VOLUME [/var/lib/influxdb]
# Mon, 16 Mar 2026 23:29:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 23:29:22 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Mon, 16 Mar 2026 23:29:22 GMT
USER influxdb
# Mon, 16 Mar 2026 23:29:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 23:29:22 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fa3468d221545a43d2151f3977695a31857f9342ba842627d03c9fa1b2ae02`  
		Last Modified: Mon, 16 Mar 2026 22:37:09 GMT  
		Size: 24.0 MB (24038304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd7119093d434a9fa04f25028fbd19bf2716d55d191499b2d61a54cc95360c8`  
		Last Modified: Mon, 16 Mar 2026 23:29:34 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d102e94ddf2c19cc83c1f3d220ee65d963953d94b131051cfe6b9b3ee3a30a9`  
		Last Modified: Mon, 16 Mar 2026 23:29:35 GMT  
		Size: 42.1 MB (42120427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc314ad1b5299a15d15d2f9299ed17bbdd4a75159d34124533507b70848b8ea`  
		Last Modified: Mon, 16 Mar 2026 23:29:34 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e1bc2342aa73e48db00f8114136fd1d561a9c084dc6d3991149fedc6e373d6f`  
		Last Modified: Mon, 16 Mar 2026 23:29:34 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086324ee441d159cb3ca0d202b451aa69133e8fd7bf917248f1c1e478972b560`  
		Last Modified: Mon, 16 Mar 2026 23:29:35 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:ed9a628d0c83c23e2be0e9597ae8ea2a80b8aec67b11aab4c67c39118b207290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8781a658e9b0554cd70e0252107078333e6a0239b5216e110f75173dbc7643b`

```dockerfile
```

-	Layers:
	-	`sha256:64c00324047c5e8a2021abe693d8480b5425de6ae2079e591c42b5e99c5b6daf`  
		Last Modified: Mon, 16 Mar 2026 23:29:34 GMT  
		Size: 4.7 MB (4678097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffe074c50ff1a6cba65108a8ce4812ea57707b4d97279831c123ab7f860aa698`  
		Last Modified: Mon, 16 Mar 2026 23:29:34 GMT  
		Size: 16.5 KB (16529 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.12` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:cfe8881ba4d9c7aa7e4a93b01fe01ace82a03d57e9bafe8d414f50c5bed3833e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110737402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9797509dee498f83efb331eaf0b99085b5a1225cdf5f8547d7c2733f1598584`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:39:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:34:31 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Mon, 16 Mar 2026 23:34:37 GMT
ENV INFLUXDB_VERSION=1.12.3
# Mon, 16 Mar 2026 23:34:37 GMT
ENV INFLUXDB_PR=-1
# Mon, 16 Mar 2026 23:34:37 GMT
ENV INFLUXDB_PV=1.12.3-1
# Mon, 16 Mar 2026 23:34:37 GMT
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_PV}_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:34:37 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Mon, 16 Mar 2026 23:34:37 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 16 Mar 2026 23:34:37 GMT
VOLUME [/var/lib/influxdb]
# Mon, 16 Mar 2026 23:34:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 23:34:37 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Mon, 16 Mar 2026 23:34:37 GMT
USER influxdb
# Mon, 16 Mar 2026 23:34:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 23:34:37 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:2ea98bb5eec9d02a0d7b59638c683db4e1e749f998a317bc731e9506f8480b12`  
		Last Modified: Mon, 16 Mar 2026 21:52:02 GMT  
		Size: 48.4 MB (48373032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbce225727d69d170353500d8834770da849cbdcea48de37e492fe14ef880d0`  
		Last Modified: Mon, 16 Mar 2026 22:39:28 GMT  
		Size: 23.6 MB (23604701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d78bf6e36546eff745de95e5852f7513fec76ebdee9d03dabaa69c9af8105b`  
		Last Modified: Mon, 16 Mar 2026 23:34:51 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4db02c63d32db4f73ac09c414cc204c9fe5791539bd4bb5b248606840733186`  
		Last Modified: Mon, 16 Mar 2026 23:34:53 GMT  
		Size: 38.8 MB (38756760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f323f977038beee36d06dd4a30a66db0a7ea609811af7220abe6219d3840ad0f`  
		Last Modified: Mon, 16 Mar 2026 23:34:51 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e9f2b533e9ee81622be4447dbad4712be9e98a438f7bec7d5394c989c389d1`  
		Last Modified: Mon, 16 Mar 2026 23:34:51 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf61bec0f23ebbac2be7097a1232fbb9f978c2735becf050dd545a14cec1ddb0`  
		Last Modified: Mon, 16 Mar 2026 23:34:52 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:88812c3c05516e08c102e14543b32450b07687c4a9ea8b0645a7db6ccecb8fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:161a7aaa88c6184d07532e2bfc50b12235f5e6318b0798bce37cf424d695ffc7`

```dockerfile
```

-	Layers:
	-	`sha256:653f7b11139f7df8ec78d65ba6cd5a1b88ef7cfba6dc0f074e15a5090d56d59e`  
		Last Modified: Mon, 16 Mar 2026 23:34:52 GMT  
		Size: 4.7 MB (4677553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17f2e1276497bdfb3cb925fabb9c1a14baf589edf05c80b54b3d1eaf1d7b1a06`  
		Last Modified: Mon, 16 Mar 2026 23:34:51 GMT  
		Size: 16.6 KB (16623 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12-alpine`

```console
$ docker pull influxdb@sha256:f3052725d772bbfa8c88aa6a10200bf7fe11f07c058240405267ca9373116083
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.12-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:df982cd40ae41733b33162b394252380d3560c36f1dee7a7b33c405cdc5acd52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46927344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:675557d60d9d209532aad2095fe5adf43607d614c0a05f20bd2603d43b35728e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Sat, 14 Mar 2026 00:10:16 GMT
RUN apk add --no-cache bash ca-certificates tzdata &&     update-ca-certificates # buildkit
# Sat, 14 Mar 2026 00:10:20 GMT
ENV INFLUXDB_VERSION=1.12.3
# Sat, 14 Mar 2026 00:10:20 GMT
ENV INFLUXDB_PR=
# Sat, 14 Mar 2026 00:10:20 GMT
ENV INFLUXDB_PV=1.12.3
# Sat, 14 Mar 2026 00:10:20 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     case "$(apk --print-arch)" in         x86_64)  ARCH=amd64 ;;         aarch64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz.asc"         "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz" &&     tar -xvf "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz"         -C /usr/bin --strip-components 1 --wildcards             'influxdb-*/influx'             'influxdb-*/influx_inspect'             'influxdb-*/influxd' &&     rm "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz.asc"        "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz" &&     apk del .build-deps # buildkit
# Sat, 14 Mar 2026 00:10:20 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Sat, 14 Mar 2026 00:10:20 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Sat, 14 Mar 2026 00:10:20 GMT
EXPOSE map[8086/tcp:{}]
# Sat, 14 Mar 2026 00:10:20 GMT
VOLUME [/var/lib/influxdb]
# Sat, 14 Mar 2026 00:10:20 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Mar 2026 00:10:20 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Sat, 14 Mar 2026 00:10:20 GMT
USER influxdb
# Sat, 14 Mar 2026 00:10:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Mar 2026 00:10:20 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f482f1508793ea4777082b8425fb6b01d6634650cfd2c038c9b0b26cc575864a`  
		Last Modified: Sat, 14 Mar 2026 00:10:30 GMT  
		Size: 1.2 MB (1225266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7baa989da2162dcdf28b32c05fedef9b9abf55f72f06e3bb8a2fd1523436382`  
		Last Modified: Sat, 14 Mar 2026 00:10:31 GMT  
		Size: 42.1 MB (42055628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c1de1ce37f873d14f73464929dac4a71bc371438bb2f0d0781a0908aa88f47`  
		Last Modified: Sat, 14 Mar 2026 00:10:30 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18c99f2a41de6c75053f9c647768c20ff60bd95bfffc232f0735466f77a7ebf5`  
		Last Modified: Sat, 14 Mar 2026 00:10:30 GMT  
		Size: 993.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3aacd57433aa6bae5e5fb5ff79657c0a259649122869ff77244eeb4653708c0`  
		Last Modified: Sat, 14 Mar 2026 00:10:31 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1532caeca3ccabc0e55f84dd36dacdfdbbf0e413b62a2675e9587676835e1fc1`  
		Last Modified: Sat, 14 Mar 2026 00:10:31 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:104de23ce7498faae7d0191c2820485f223caba1d142dfcc15de4f82325bbbb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **780.6 KB (780592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb7f95a0e7da8ac14ba56037b7702db4165b4ef7412ffb3b533f293345a3d599`

```dockerfile
```

-	Layers:
	-	`sha256:8c4ef410c415a897a5211f6923160f4325d0e0839a19c1b9842281a28da999ee`  
		Last Modified: Sat, 14 Mar 2026 00:10:30 GMT  
		Size: 761.9 KB (761875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00c50eadb6eeb1faa8ddf7a3d2b514fcbe26e4c96931782244948aaab65df22a`  
		Last Modified: Sat, 14 Mar 2026 00:10:30 GMT  
		Size: 18.7 KB (18717 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.12-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:f4a2998e6a905ad0246287c4ac134aba1d236c99b537c88c3bfd7995259af91b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (43962970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a94f2d5e7eae84557dca447264489b2a84c4e1a4e6b6b5a2d1078f701c0254c2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:07 GMT
ADD alpine-minirootfs-3.21.6-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:07 GMT
CMD ["/bin/sh"]
# Sat, 14 Mar 2026 00:10:07 GMT
RUN apk add --no-cache bash ca-certificates tzdata &&     update-ca-certificates # buildkit
# Sat, 14 Mar 2026 00:10:12 GMT
ENV INFLUXDB_VERSION=1.12.3
# Sat, 14 Mar 2026 00:10:12 GMT
ENV INFLUXDB_PR=
# Sat, 14 Mar 2026 00:10:12 GMT
ENV INFLUXDB_PV=1.12.3
# Sat, 14 Mar 2026 00:10:12 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     case "$(apk --print-arch)" in         x86_64)  ARCH=amd64 ;;         aarch64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz.asc"         "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz" &&     tar -xvf "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz"         -C /usr/bin --strip-components 1 --wildcards             'influxdb-*/influx'             'influxdb-*/influx_inspect'             'influxdb-*/influxd' &&     rm "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz.asc"        "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz" &&     apk del .build-deps # buildkit
# Sat, 14 Mar 2026 00:10:12 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Sat, 14 Mar 2026 00:10:12 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Sat, 14 Mar 2026 00:10:12 GMT
EXPOSE map[8086/tcp:{}]
# Sat, 14 Mar 2026 00:10:12 GMT
VOLUME [/var/lib/influxdb]
# Sat, 14 Mar 2026 00:10:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Mar 2026 00:10:12 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Sat, 14 Mar 2026 00:10:12 GMT
USER influxdb
# Sat, 14 Mar 2026 00:10:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Mar 2026 00:10:12 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:a447a5de8f4eb4a987d81c0afa14d459cc714599c020c08f45fafa9c6c904b30`  
		Last Modified: Wed, 28 Jan 2026 01:18:13 GMT  
		Size: 4.0 MB (3992880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3dc67bddedcd0508208cf35538b222a926fb8a23e97b61d648a4f0917b498a`  
		Last Modified: Sat, 14 Mar 2026 00:10:21 GMT  
		Size: 1.3 MB (1290526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3117cf870c831fbfb1bb5cfc1f3ccfcbe515dd27cd624137b5aa9eb9734257`  
		Last Modified: Sat, 14 Mar 2026 00:10:22 GMT  
		Size: 38.7 MB (38676853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e62c7a473cbc47bba11c41ae3ff3836d458431074d3ad411b786754ec8ab07b`  
		Last Modified: Sat, 14 Mar 2026 00:10:21 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764cfd58375dd6b5826aa6dcfcac5317bb383a7262098553c2f73547204389d6`  
		Last Modified: Sat, 14 Mar 2026 00:10:21 GMT  
		Size: 995.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab0d39d4f370b5f35a879f733f8a1d746308a46b774e392987db734cf8f442a`  
		Last Modified: Sat, 14 Mar 2026 00:10:22 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69472bece26f459c702c9346b579efb20a5b8fa067b0b40bdb4ab9d82fd6605b`  
		Last Modified: Sat, 14 Mar 2026 00:10:23 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:119a974f59510618c572597e00b3364c1d361e184c2148c72c1cb048f99c722d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **779.9 KB (779930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b196ec37e7ecec56d1a07f47a3bdf8b96fe5a195776492dcdbd16f35030f34ec`

```dockerfile
```

-	Layers:
	-	`sha256:573b9a721b46c12e523b2a640182304f154060769f76511acc6765eba794a687`  
		Last Modified: Sat, 14 Mar 2026 00:10:21 GMT  
		Size: 761.1 KB (761102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0886a9c54a0b4543591b17fd4606ae8ec03cfbd98c98427ddd905a484f83f36b`  
		Last Modified: Sat, 14 Mar 2026 00:10:21 GMT  
		Size: 18.8 KB (18828 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12-data`

```console
$ docker pull influxdb@sha256:4f5d4e87b639278d39a7c06e32cba7e62f1de8c8f1fde4b8db4f053d53df4e62
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12-data` - linux; amd64

```console
$ docker pull influxdb@sha256:d21e4988d37a6c1faa8baab25d27def33c754eb350a9b32279e180096f599646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115719726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c31a2127ab5486fbc8d5f74bf1f91ea58319df988e3a4fc8bcc9fb9a085b298`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:37:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:29:22 GMT
ENV INFLUXDB_VERSION=1.12.3-c1.12.3
# Mon, 16 Mar 2026 23:29:22 GMT
ENV INFLUXDB_PR=
# Mon, 16 Mar 2026 23:29:22 GMT
ENV INFLUXDB_PV=1.12.3-c1.12.3
# Mon, 16 Mar 2026 23:29:22 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"         "influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     rm -r "influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"           "influxdb-data_${INFLUXDB_PV}_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:29:22 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Mon, 16 Mar 2026 23:29:22 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 16 Mar 2026 23:29:22 GMT
VOLUME [/var/lib/influxdb]
# Mon, 16 Mar 2026 23:29:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 23:29:22 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Mon, 16 Mar 2026 23:29:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 23:29:22 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fa3468d221545a43d2151f3977695a31857f9342ba842627d03c9fa1b2ae02`  
		Last Modified: Mon, 16 Mar 2026 22:37:09 GMT  
		Size: 24.0 MB (24038304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11793f1b301015b6075c375d2ba0bb8a3b2156f963042752aebaef61a814ab21`  
		Last Modified: Mon, 16 Mar 2026 23:29:35 GMT  
		Size: 43.2 MB (43191068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976aed466c219d17ff192121e29a61c61b4b07b3af73e05e3f8122b9745cf77e`  
		Last Modified: Mon, 16 Mar 2026 23:29:33 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7721a85c674598c3887f132a5849c923eb1a39d9fc59d7db014f335e282f009`  
		Last Modified: Mon, 16 Mar 2026 23:29:33 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f6a089499d992dcda33b7b222b0cee38c4e8142d980d933eba3dff115db4de`  
		Last Modified: Mon, 16 Mar 2026 23:29:33 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:1a36418d9366f8b3788d664ae9f2d6f908e613ba59a7a64a578bb7d4c141b9a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4707287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5574c09e06bdf3267b7dfd8a4b171badb6693dd4bfab7e44f630c20c60a1fff2`

```dockerfile
```

-	Layers:
	-	`sha256:417470ac9dfeac0c0842a7adc8f790420dc1145c0c1e60e4dcb2a1d01afa31aa`  
		Last Modified: Mon, 16 Mar 2026 23:29:34 GMT  
		Size: 4.7 MB (4693133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de8488ad860255ff7afdefbdd4e259397ab7bd5b900efa6d4c4fa45a2449a040`  
		Last Modified: Mon, 16 Mar 2026 23:29:33 GMT  
		Size: 14.2 KB (14154 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12-data-alpine`

```console
$ docker pull influxdb@sha256:b00b5baa2231b78e2d7f36eb1a10e2d977f347b9881dbb417b29b6bdf5830a46
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:81a969bc16b9858dda59761bd5f64a9e845ca937d25c79bf19a7c2e5ef57d5d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47996785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0349bbaf083804873fbb03e5d51d6762630274c9fddcd6d18d97809096a67f24`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Sat, 14 Mar 2026 00:10:26 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Sat, 14 Mar 2026 00:10:31 GMT
ENV INFLUXDB_VERSION=1.12.3-c1.12.3
# Sat, 14 Mar 2026 00:10:31 GMT
ENV INFLUXDB_PR=
# Sat, 14 Mar 2026 00:10:31 GMT
ENV INFLUXDB_PV=1.12.3-c1.12.3
# Sat, 14 Mar 2026 00:10:31 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"         "influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     tar -xvf "influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz"         -C /usr/bin --strip-components 1 --wildcards             'influxdb-*/influx'             'influxdb-*/influx_inspect'             'influxdb-*/influxd' &&     rm "influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"        "influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     apk del .build-deps # buildkit
# Sat, 14 Mar 2026 00:10:31 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Sat, 14 Mar 2026 00:10:31 GMT
EXPOSE map[8086/tcp:{}]
# Sat, 14 Mar 2026 00:10:31 GMT
VOLUME [/var/lib/influxdb]
# Sat, 14 Mar 2026 00:10:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Mar 2026 00:10:32 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Sat, 14 Mar 2026 00:10:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Mar 2026 00:10:32 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68716dcc58a5f148c91121671bed51872ee14024f52511f4f27a30f76dce7229`  
		Last Modified: Sat, 14 Mar 2026 00:10:42 GMT  
		Size: 1.2 MB (1225267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a883869ba3b1cd65a45af9359b43f47d6fac6db9e734ab17670747476688a74`  
		Last Modified: Sat, 14 Mar 2026 00:10:43 GMT  
		Size: 43.1 MB (43126004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea75516ea6f5fc6e704f8a153c5006c341c6d15af305805fe5621cc87017a79`  
		Last Modified: Sat, 14 Mar 2026 00:10:42 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23204e84777414408f116926340ada07e4e53fd479fe293933fd5917377c5ef3`  
		Last Modified: Sat, 14 Mar 2026 00:10:42 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6db343d538c0cd30d0b117de9d02ef0c9964c7ddacb94c1d1548cd2251e8b6`  
		Last Modified: Sat, 14 Mar 2026 00:10:43 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:3cf5b433c5da545ad77ef2c05fbb248e11328258f17be899658ebe11101f2074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **796.7 KB (796739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89d8831c93eb5116260d6aa262a99b5340b8e251edae29efa3ffb935fd035cb7`

```dockerfile
```

-	Layers:
	-	`sha256:54c781f8f3995af817107aeefcc043140f26364ae6ce15fa46f4f2bfdfcbca44`  
		Last Modified: Sat, 14 Mar 2026 00:10:42 GMT  
		Size: 781.2 KB (781229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45e179ee50e5cfb1d3f337ad7930775e5df7f00e5978d5acd75cd3102bd71f6b`  
		Last Modified: Sat, 14 Mar 2026 00:10:42 GMT  
		Size: 15.5 KB (15510 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12-meta`

```console
$ docker pull influxdb@sha256:d619226068a33387766eff93fa2815efadcb0c64ee36d4fdf7f2afa85e5584b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:105f922f373e05fe5be8b3bf03636011fb5eba13b6233319283e68f0f5b771ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91912637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68476159aed012d339094890fe575caf708d10faa17d07b80bd9febfafd4ba49`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:37:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:29:41 GMT
ENV INFLUXDB_VERSION=1.12.3-c1.12.3
# Mon, 16 Mar 2026 23:29:41 GMT
ENV INFLUXDB_PR=
# Mon, 16 Mar 2026 23:29:41 GMT
ENV INFLUXDB_PV=1.12.3-c1.12.3
# Mon, 16 Mar 2026 23:29:41 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"         "influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     rm -r "influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"           "influxdb-meta_${INFLUXDB_PV}_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:29:41 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Mon, 16 Mar 2026 23:29:41 GMT
EXPOSE map[8091/tcp:{}]
# Mon, 16 Mar 2026 23:29:41 GMT
VOLUME [/var/lib/influxdb]
# Mon, 16 Mar 2026 23:29:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 23:29:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 23:29:41 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fa3468d221545a43d2151f3977695a31857f9342ba842627d03c9fa1b2ae02`  
		Last Modified: Mon, 16 Mar 2026 22:37:09 GMT  
		Size: 24.0 MB (24038304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4cf91a29498481bcb2774753d32b947d34c8a875b4d0cc26467895c334f1dd`  
		Last Modified: Mon, 16 Mar 2026 23:29:51 GMT  
		Size: 19.4 MB (19385181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde80dcc1dfd5fc45df6e534c3d90d980adef9abe7e69f7d2aafb14bb57e17cb`  
		Last Modified: Mon, 16 Mar 2026 23:29:50 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07757a4b1133059e10be557710b3424182053781435a85154828461509909d2`  
		Last Modified: Mon, 16 Mar 2026 23:29:50 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:f6a096dcce18046c5b1651cd32ce175e5d9e06a6e3e3ff33cda518466c9231b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4605864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb53755f9f14c374e8e9def0c1f29d32cb98a7b920013ab90ca8cfed126a079e`

```dockerfile
```

-	Layers:
	-	`sha256:e3a4f4e37f0311efd3bc8e767984bd395128ab2484afddf5178d01159451a3d1`  
		Last Modified: Mon, 16 Mar 2026 23:29:50 GMT  
		Size: 4.6 MB (4593201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd9ce7dc3b27548f4a7c880147b540cd89bc6f24c0d36169433b8c194da686ad`  
		Last Modified: Mon, 16 Mar 2026 23:29:50 GMT  
		Size: 12.7 KB (12663 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12-meta-alpine`

```console
$ docker pull influxdb@sha256:0a051eaf780ce5a4e1d0bc51e7c16424b82219208822536392a61d77f4c527cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:5d3f5bc09690d58108cd11b610d1a4190f786a7bc800ae17751ced7c530ea4f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.2 MB (24200738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ba49e476e65f5ea7acf3c9b2e0c08890594b6e04c2dd7f2f369dd925062925`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Sat, 14 Mar 2026 00:11:06 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Sat, 14 Mar 2026 00:11:09 GMT
ENV INFLUXDB_VERSION=1.12.3-c1.12.3
# Sat, 14 Mar 2026 00:11:09 GMT
ENV INFLUXDB_PR=
# Sat, 14 Mar 2026 00:11:09 GMT
ENV INFLUXDB_PV=1.12.3-c1.12.3
# Sat, 14 Mar 2026 00:11:09 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"         "influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     tar -xvf "influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz"         -C /usr/bin --strip-components 1 --wildcards             'influxdb-*/influxd-ctl'             'influxdb-*/influxd-meta' &&     rm "influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"        "influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     apk del .build-deps # buildkit
# Sat, 14 Mar 2026 00:11:09 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Sat, 14 Mar 2026 00:11:09 GMT
EXPOSE map[8091/tcp:{}]
# Sat, 14 Mar 2026 00:11:09 GMT
VOLUME [/var/lib/influxdb]
# Sat, 14 Mar 2026 00:11:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Mar 2026 00:11:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Mar 2026 00:11:09 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff222b2bc1735ef5ae68fbb3cd2555d5c9d167db3009d6ac7b76ffc0b64c953`  
		Last Modified: Sat, 14 Mar 2026 00:11:17 GMT  
		Size: 1.2 MB (1225264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84706419752f10f867a78117779b8e666144cfae465ae3bff03fead1a3d3aaf1`  
		Last Modified: Sat, 14 Mar 2026 00:11:17 GMT  
		Size: 19.3 MB (19331168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd86dc70a190dd7b913375552975c2652ab94591f2b2c476e3c95f5f7937b84d`  
		Last Modified: Sat, 14 Mar 2026 00:11:17 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00fac50404b2e130d37d058e96747807965ead40c44ecc2c3e0c6f11923cdae`  
		Last Modified: Sat, 14 Mar 2026 00:11:17 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:547d60bfe06fa90ad6260c650a3774b3cc5a2e27f910aa0005926649448c72ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **696.0 KB (696015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:806c305f946ee74f2ee15815575ec4bf4caec2d242c42971eb8ee400298717a8`

```dockerfile
```

-	Layers:
	-	`sha256:bd2b90af63566b3d6c84fee2b1d16ffdab0305dcad16b98c31a186f832c7791e`  
		Last Modified: Sat, 14 Mar 2026 00:11:17 GMT  
		Size: 682.1 KB (682083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cac48257e4722c8ccb0f5993024e0cf6e88f5fccb58612457bd007afb71bd55`  
		Last Modified: Sat, 14 Mar 2026 00:11:17 GMT  
		Size: 13.9 KB (13932 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12.3`

```console
$ docker pull influxdb@sha256:35e9976120a18fff82fefcc06d631de7585f33e7b096e9128465e6c15a9233fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.12.3` - linux; amd64

```console
$ docker pull influxdb@sha256:c9e597f49f562e9c7df34bbac4a78480f8ef698869c8b78b7a3c5047cceef260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114650223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e71c51e68940d034f29b79f7dddebb1655e799af27271908e7bf9696b9b0691`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:37:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:29:17 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Mon, 16 Mar 2026 23:29:22 GMT
ENV INFLUXDB_VERSION=1.12.3
# Mon, 16 Mar 2026 23:29:22 GMT
ENV INFLUXDB_PR=-1
# Mon, 16 Mar 2026 23:29:22 GMT
ENV INFLUXDB_PV=1.12.3-1
# Mon, 16 Mar 2026 23:29:22 GMT
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_PV}_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:29:22 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Mon, 16 Mar 2026 23:29:22 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 16 Mar 2026 23:29:22 GMT
VOLUME [/var/lib/influxdb]
# Mon, 16 Mar 2026 23:29:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 23:29:22 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Mon, 16 Mar 2026 23:29:22 GMT
USER influxdb
# Mon, 16 Mar 2026 23:29:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 23:29:22 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fa3468d221545a43d2151f3977695a31857f9342ba842627d03c9fa1b2ae02`  
		Last Modified: Mon, 16 Mar 2026 22:37:09 GMT  
		Size: 24.0 MB (24038304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd7119093d434a9fa04f25028fbd19bf2716d55d191499b2d61a54cc95360c8`  
		Last Modified: Mon, 16 Mar 2026 23:29:34 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d102e94ddf2c19cc83c1f3d220ee65d963953d94b131051cfe6b9b3ee3a30a9`  
		Last Modified: Mon, 16 Mar 2026 23:29:35 GMT  
		Size: 42.1 MB (42120427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc314ad1b5299a15d15d2f9299ed17bbdd4a75159d34124533507b70848b8ea`  
		Last Modified: Mon, 16 Mar 2026 23:29:34 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e1bc2342aa73e48db00f8114136fd1d561a9c084dc6d3991149fedc6e373d6f`  
		Last Modified: Mon, 16 Mar 2026 23:29:34 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086324ee441d159cb3ca0d202b451aa69133e8fd7bf917248f1c1e478972b560`  
		Last Modified: Mon, 16 Mar 2026 23:29:35 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.3` - unknown; unknown

```console
$ docker pull influxdb@sha256:ed9a628d0c83c23e2be0e9597ae8ea2a80b8aec67b11aab4c67c39118b207290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8781a658e9b0554cd70e0252107078333e6a0239b5216e110f75173dbc7643b`

```dockerfile
```

-	Layers:
	-	`sha256:64c00324047c5e8a2021abe693d8480b5425de6ae2079e591c42b5e99c5b6daf`  
		Last Modified: Mon, 16 Mar 2026 23:29:34 GMT  
		Size: 4.7 MB (4678097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffe074c50ff1a6cba65108a8ce4812ea57707b4d97279831c123ab7f860aa698`  
		Last Modified: Mon, 16 Mar 2026 23:29:34 GMT  
		Size: 16.5 KB (16529 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.12.3` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:cfe8881ba4d9c7aa7e4a93b01fe01ace82a03d57e9bafe8d414f50c5bed3833e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110737402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9797509dee498f83efb331eaf0b99085b5a1225cdf5f8547d7c2733f1598584`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:39:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:34:31 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb # buildkit
# Mon, 16 Mar 2026 23:34:37 GMT
ENV INFLUXDB_VERSION=1.12.3
# Mon, 16 Mar 2026 23:34:37 GMT
ENV INFLUXDB_PR=-1
# Mon, 16 Mar 2026 23:34:37 GMT
ENV INFLUXDB_PV=1.12.3-1
# Mon, 16 Mar 2026 23:34:37 GMT
RUN set -x &&     case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"         "influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb_${INFLUXDB_PV}_${ARCH}.deb" &&     rm -r "influxdb_${INFLUXDB_PV}_${ARCH}.deb.asc"           "influxdb_${INFLUXDB_PV}_${ARCH}.deb"           /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:34:37 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Mon, 16 Mar 2026 23:34:37 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 16 Mar 2026 23:34:37 GMT
VOLUME [/var/lib/influxdb]
# Mon, 16 Mar 2026 23:34:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 23:34:37 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Mon, 16 Mar 2026 23:34:37 GMT
USER influxdb
# Mon, 16 Mar 2026 23:34:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 23:34:37 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:2ea98bb5eec9d02a0d7b59638c683db4e1e749f998a317bc731e9506f8480b12`  
		Last Modified: Mon, 16 Mar 2026 21:52:02 GMT  
		Size: 48.4 MB (48373032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbce225727d69d170353500d8834770da849cbdcea48de37e492fe14ef880d0`  
		Last Modified: Mon, 16 Mar 2026 22:39:28 GMT  
		Size: 23.6 MB (23604701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d78bf6e36546eff745de95e5852f7513fec76ebdee9d03dabaa69c9af8105b`  
		Last Modified: Mon, 16 Mar 2026 23:34:51 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4db02c63d32db4f73ac09c414cc204c9fe5791539bd4bb5b248606840733186`  
		Last Modified: Mon, 16 Mar 2026 23:34:53 GMT  
		Size: 38.8 MB (38756760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f323f977038beee36d06dd4a30a66db0a7ea609811af7220abe6219d3840ad0f`  
		Last Modified: Mon, 16 Mar 2026 23:34:51 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e9f2b533e9ee81622be4447dbad4712be9e98a438f7bec7d5394c989c389d1`  
		Last Modified: Mon, 16 Mar 2026 23:34:51 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf61bec0f23ebbac2be7097a1232fbb9f978c2735becf050dd545a14cec1ddb0`  
		Last Modified: Mon, 16 Mar 2026 23:34:52 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.3` - unknown; unknown

```console
$ docker pull influxdb@sha256:88812c3c05516e08c102e14543b32450b07687c4a9ea8b0645a7db6ccecb8fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4694176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:161a7aaa88c6184d07532e2bfc50b12235f5e6318b0798bce37cf424d695ffc7`

```dockerfile
```

-	Layers:
	-	`sha256:653f7b11139f7df8ec78d65ba6cd5a1b88ef7cfba6dc0f074e15a5090d56d59e`  
		Last Modified: Mon, 16 Mar 2026 23:34:52 GMT  
		Size: 4.7 MB (4677553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17f2e1276497bdfb3cb925fabb9c1a14baf589edf05c80b54b3d1eaf1d7b1a06`  
		Last Modified: Mon, 16 Mar 2026 23:34:51 GMT  
		Size: 16.6 KB (16623 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12.3-alpine`

```console
$ docker pull influxdb@sha256:f3052725d772bbfa8c88aa6a10200bf7fe11f07c058240405267ca9373116083
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:1.12.3-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:df982cd40ae41733b33162b394252380d3560c36f1dee7a7b33c405cdc5acd52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46927344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:675557d60d9d209532aad2095fe5adf43607d614c0a05f20bd2603d43b35728e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Sat, 14 Mar 2026 00:10:16 GMT
RUN apk add --no-cache bash ca-certificates tzdata &&     update-ca-certificates # buildkit
# Sat, 14 Mar 2026 00:10:20 GMT
ENV INFLUXDB_VERSION=1.12.3
# Sat, 14 Mar 2026 00:10:20 GMT
ENV INFLUXDB_PR=
# Sat, 14 Mar 2026 00:10:20 GMT
ENV INFLUXDB_PV=1.12.3
# Sat, 14 Mar 2026 00:10:20 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     case "$(apk --print-arch)" in         x86_64)  ARCH=amd64 ;;         aarch64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz.asc"         "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz" &&     tar -xvf "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz"         -C /usr/bin --strip-components 1 --wildcards             'influxdb-*/influx'             'influxdb-*/influx_inspect'             'influxdb-*/influxd' &&     rm "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz.asc"        "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz" &&     apk del .build-deps # buildkit
# Sat, 14 Mar 2026 00:10:20 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Sat, 14 Mar 2026 00:10:20 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Sat, 14 Mar 2026 00:10:20 GMT
EXPOSE map[8086/tcp:{}]
# Sat, 14 Mar 2026 00:10:20 GMT
VOLUME [/var/lib/influxdb]
# Sat, 14 Mar 2026 00:10:20 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Mar 2026 00:10:20 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Sat, 14 Mar 2026 00:10:20 GMT
USER influxdb
# Sat, 14 Mar 2026 00:10:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Mar 2026 00:10:20 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f482f1508793ea4777082b8425fb6b01d6634650cfd2c038c9b0b26cc575864a`  
		Last Modified: Sat, 14 Mar 2026 00:10:30 GMT  
		Size: 1.2 MB (1225266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7baa989da2162dcdf28b32c05fedef9b9abf55f72f06e3bb8a2fd1523436382`  
		Last Modified: Sat, 14 Mar 2026 00:10:31 GMT  
		Size: 42.1 MB (42055628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c1de1ce37f873d14f73464929dac4a71bc371438bb2f0d0781a0908aa88f47`  
		Last Modified: Sat, 14 Mar 2026 00:10:30 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18c99f2a41de6c75053f9c647768c20ff60bd95bfffc232f0735466f77a7ebf5`  
		Last Modified: Sat, 14 Mar 2026 00:10:30 GMT  
		Size: 993.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3aacd57433aa6bae5e5fb5ff79657c0a259649122869ff77244eeb4653708c0`  
		Last Modified: Sat, 14 Mar 2026 00:10:31 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1532caeca3ccabc0e55f84dd36dacdfdbbf0e413b62a2675e9587676835e1fc1`  
		Last Modified: Sat, 14 Mar 2026 00:10:31 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.3-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:104de23ce7498faae7d0191c2820485f223caba1d142dfcc15de4f82325bbbb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **780.6 KB (780592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb7f95a0e7da8ac14ba56037b7702db4165b4ef7412ffb3b533f293345a3d599`

```dockerfile
```

-	Layers:
	-	`sha256:8c4ef410c415a897a5211f6923160f4325d0e0839a19c1b9842281a28da999ee`  
		Last Modified: Sat, 14 Mar 2026 00:10:30 GMT  
		Size: 761.9 KB (761875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00c50eadb6eeb1faa8ddf7a3d2b514fcbe26e4c96931782244948aaab65df22a`  
		Last Modified: Sat, 14 Mar 2026 00:10:30 GMT  
		Size: 18.7 KB (18717 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:1.12.3-alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:f4a2998e6a905ad0246287c4ac134aba1d236c99b537c88c3bfd7995259af91b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (43962970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a94f2d5e7eae84557dca447264489b2a84c4e1a4e6b6b5a2d1078f701c0254c2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:07 GMT
ADD alpine-minirootfs-3.21.6-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:07 GMT
CMD ["/bin/sh"]
# Sat, 14 Mar 2026 00:10:07 GMT
RUN apk add --no-cache bash ca-certificates tzdata &&     update-ca-certificates # buildkit
# Sat, 14 Mar 2026 00:10:12 GMT
ENV INFLUXDB_VERSION=1.12.3
# Sat, 14 Mar 2026 00:10:12 GMT
ENV INFLUXDB_PR=
# Sat, 14 Mar 2026 00:10:12 GMT
ENV INFLUXDB_PV=1.12.3
# Sat, 14 Mar 2026 00:10:12 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     case "$(apk --print-arch)" in         x86_64)  ARCH=amd64 ;;         aarch64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz.asc"         "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz" &&     tar -xvf "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz"         -C /usr/bin --strip-components 1 --wildcards             'influxdb-*/influx'             'influxdb-*/influx_inspect'             'influxdb-*/influxd' &&     rm "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz.asc"        "influxdb-${INFLUXDB_PV}_linux_${ARCH}.tar.gz" &&     apk del .build-deps # buildkit
# Sat, 14 Mar 2026 00:10:12 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Sat, 14 Mar 2026 00:10:12 GMT
RUN addgroup --system --gid 1500 influxdb &&     adduser --system --uid 1500 --ingroup influxdb --home /var/lib/influxdb --shell /bin/false influxdb &&     mkdir -p /var/lib/influxdb &&     mkdir -p /var/log/influxdb &&     chown influxdb:influxdb /var/lib/influxdb &&     chown influxdb:influxdb /var/log/influxdb &&     chmod 0750 /var/lib/influxdb &&     chmod 0750 /var/log/influxdb # buildkit
# Sat, 14 Mar 2026 00:10:12 GMT
EXPOSE map[8086/tcp:{}]
# Sat, 14 Mar 2026 00:10:12 GMT
VOLUME [/var/lib/influxdb]
# Sat, 14 Mar 2026 00:10:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Mar 2026 00:10:12 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Sat, 14 Mar 2026 00:10:12 GMT
USER influxdb
# Sat, 14 Mar 2026 00:10:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Mar 2026 00:10:12 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:a447a5de8f4eb4a987d81c0afa14d459cc714599c020c08f45fafa9c6c904b30`  
		Last Modified: Wed, 28 Jan 2026 01:18:13 GMT  
		Size: 4.0 MB (3992880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3dc67bddedcd0508208cf35538b222a926fb8a23e97b61d648a4f0917b498a`  
		Last Modified: Sat, 14 Mar 2026 00:10:21 GMT  
		Size: 1.3 MB (1290526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3117cf870c831fbfb1bb5cfc1f3ccfcbe515dd27cd624137b5aa9eb9734257`  
		Last Modified: Sat, 14 Mar 2026 00:10:22 GMT  
		Size: 38.7 MB (38676853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e62c7a473cbc47bba11c41ae3ff3836d458431074d3ad411b786754ec8ab07b`  
		Last Modified: Sat, 14 Mar 2026 00:10:21 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764cfd58375dd6b5826aa6dcfcac5317bb383a7262098553c2f73547204389d6`  
		Last Modified: Sat, 14 Mar 2026 00:10:21 GMT  
		Size: 995.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab0d39d4f370b5f35a879f733f8a1d746308a46b774e392987db734cf8f442a`  
		Last Modified: Sat, 14 Mar 2026 00:10:22 GMT  
		Size: 212.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69472bece26f459c702c9346b579efb20a5b8fa067b0b40bdb4ab9d82fd6605b`  
		Last Modified: Sat, 14 Mar 2026 00:10:23 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.3-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:119a974f59510618c572597e00b3364c1d361e184c2148c72c1cb048f99c722d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **779.9 KB (779930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b196ec37e7ecec56d1a07f47a3bdf8b96fe5a195776492dcdbd16f35030f34ec`

```dockerfile
```

-	Layers:
	-	`sha256:573b9a721b46c12e523b2a640182304f154060769f76511acc6765eba794a687`  
		Last Modified: Sat, 14 Mar 2026 00:10:21 GMT  
		Size: 761.1 KB (761102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0886a9c54a0b4543591b17fd4606ae8ec03cfbd98c98427ddd905a484f83f36b`  
		Last Modified: Sat, 14 Mar 2026 00:10:21 GMT  
		Size: 18.8 KB (18828 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12.3-data`

```console
$ docker pull influxdb@sha256:4f5d4e87b639278d39a7c06e32cba7e62f1de8c8f1fde4b8db4f053d53df4e62
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12.3-data` - linux; amd64

```console
$ docker pull influxdb@sha256:d21e4988d37a6c1faa8baab25d27def33c754eb350a9b32279e180096f599646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115719726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c31a2127ab5486fbc8d5f74bf1f91ea58319df988e3a4fc8bcc9fb9a085b298`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:37:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:29:22 GMT
ENV INFLUXDB_VERSION=1.12.3-c1.12.3
# Mon, 16 Mar 2026 23:29:22 GMT
ENV INFLUXDB_PR=
# Mon, 16 Mar 2026 23:29:22 GMT
ENV INFLUXDB_PV=1.12.3-c1.12.3
# Mon, 16 Mar 2026 23:29:22 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"         "influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     rm -r "influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"           "influxdb-data_${INFLUXDB_PV}_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:29:22 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Mon, 16 Mar 2026 23:29:22 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 16 Mar 2026 23:29:22 GMT
VOLUME [/var/lib/influxdb]
# Mon, 16 Mar 2026 23:29:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 23:29:22 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Mon, 16 Mar 2026 23:29:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 23:29:22 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fa3468d221545a43d2151f3977695a31857f9342ba842627d03c9fa1b2ae02`  
		Last Modified: Mon, 16 Mar 2026 22:37:09 GMT  
		Size: 24.0 MB (24038304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11793f1b301015b6075c375d2ba0bb8a3b2156f963042752aebaef61a814ab21`  
		Last Modified: Mon, 16 Mar 2026 23:29:35 GMT  
		Size: 43.2 MB (43191068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976aed466c219d17ff192121e29a61c61b4b07b3af73e05e3f8122b9745cf77e`  
		Last Modified: Mon, 16 Mar 2026 23:29:33 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7721a85c674598c3887f132a5849c923eb1a39d9fc59d7db014f335e282f009`  
		Last Modified: Mon, 16 Mar 2026 23:29:33 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f6a089499d992dcda33b7b222b0cee38c4e8142d980d933eba3dff115db4de`  
		Last Modified: Mon, 16 Mar 2026 23:29:33 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.3-data` - unknown; unknown

```console
$ docker pull influxdb@sha256:1a36418d9366f8b3788d664ae9f2d6f908e613ba59a7a64a578bb7d4c141b9a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4707287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5574c09e06bdf3267b7dfd8a4b171badb6693dd4bfab7e44f630c20c60a1fff2`

```dockerfile
```

-	Layers:
	-	`sha256:417470ac9dfeac0c0842a7adc8f790420dc1145c0c1e60e4dcb2a1d01afa31aa`  
		Last Modified: Mon, 16 Mar 2026 23:29:34 GMT  
		Size: 4.7 MB (4693133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de8488ad860255ff7afdefbdd4e259397ab7bd5b900efa6d4c4fa45a2449a040`  
		Last Modified: Mon, 16 Mar 2026 23:29:33 GMT  
		Size: 14.2 KB (14154 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12.3-data-alpine`

```console
$ docker pull influxdb@sha256:b00b5baa2231b78e2d7f36eb1a10e2d977f347b9881dbb417b29b6bdf5830a46
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12.3-data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:81a969bc16b9858dda59761bd5f64a9e845ca937d25c79bf19a7c2e5ef57d5d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47996785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0349bbaf083804873fbb03e5d51d6762630274c9fddcd6d18d97809096a67f24`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Sat, 14 Mar 2026 00:10:26 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Sat, 14 Mar 2026 00:10:31 GMT
ENV INFLUXDB_VERSION=1.12.3-c1.12.3
# Sat, 14 Mar 2026 00:10:31 GMT
ENV INFLUXDB_PR=
# Sat, 14 Mar 2026 00:10:31 GMT
ENV INFLUXDB_PV=1.12.3-c1.12.3
# Sat, 14 Mar 2026 00:10:31 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"         "influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     tar -xvf "influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz"         -C /usr/bin --strip-components 1 --wildcards             'influxdb-*/influx'             'influxdb-*/influx_inspect'             'influxdb-*/influxd' &&     rm "influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"        "influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     apk del .build-deps # buildkit
# Sat, 14 Mar 2026 00:10:31 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Sat, 14 Mar 2026 00:10:31 GMT
EXPOSE map[8086/tcp:{}]
# Sat, 14 Mar 2026 00:10:31 GMT
VOLUME [/var/lib/influxdb]
# Sat, 14 Mar 2026 00:10:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Mar 2026 00:10:32 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Sat, 14 Mar 2026 00:10:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Mar 2026 00:10:32 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68716dcc58a5f148c91121671bed51872ee14024f52511f4f27a30f76dce7229`  
		Last Modified: Sat, 14 Mar 2026 00:10:42 GMT  
		Size: 1.2 MB (1225267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a883869ba3b1cd65a45af9359b43f47d6fac6db9e734ab17670747476688a74`  
		Last Modified: Sat, 14 Mar 2026 00:10:43 GMT  
		Size: 43.1 MB (43126004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea75516ea6f5fc6e704f8a153c5006c341c6d15af305805fe5621cc87017a79`  
		Last Modified: Sat, 14 Mar 2026 00:10:42 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23204e84777414408f116926340ada07e4e53fd479fe293933fd5917377c5ef3`  
		Last Modified: Sat, 14 Mar 2026 00:10:42 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6db343d538c0cd30d0b117de9d02ef0c9964c7ddacb94c1d1548cd2251e8b6`  
		Last Modified: Sat, 14 Mar 2026 00:10:43 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.3-data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:3cf5b433c5da545ad77ef2c05fbb248e11328258f17be899658ebe11101f2074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **796.7 KB (796739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89d8831c93eb5116260d6aa262a99b5340b8e251edae29efa3ffb935fd035cb7`

```dockerfile
```

-	Layers:
	-	`sha256:54c781f8f3995af817107aeefcc043140f26364ae6ce15fa46f4f2bfdfcbca44`  
		Last Modified: Sat, 14 Mar 2026 00:10:42 GMT  
		Size: 781.2 KB (781229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45e179ee50e5cfb1d3f337ad7930775e5df7f00e5978d5acd75cd3102bd71f6b`  
		Last Modified: Sat, 14 Mar 2026 00:10:42 GMT  
		Size: 15.5 KB (15510 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12.3-meta`

```console
$ docker pull influxdb@sha256:d619226068a33387766eff93fa2815efadcb0c64ee36d4fdf7f2afa85e5584b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12.3-meta` - linux; amd64

```console
$ docker pull influxdb@sha256:105f922f373e05fe5be8b3bf03636011fb5eba13b6233319283e68f0f5b771ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91912637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68476159aed012d339094890fe575caf708d10faa17d07b80bd9febfafd4ba49`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:37:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:29:41 GMT
ENV INFLUXDB_VERSION=1.12.3-c1.12.3
# Mon, 16 Mar 2026 23:29:41 GMT
ENV INFLUXDB_PR=
# Mon, 16 Mar 2026 23:29:41 GMT
ENV INFLUXDB_PV=1.12.3-c1.12.3
# Mon, 16 Mar 2026 23:29:41 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"         "influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     rm -r "influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"           "influxdb-meta_${INFLUXDB_PV}_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:29:41 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Mon, 16 Mar 2026 23:29:41 GMT
EXPOSE map[8091/tcp:{}]
# Mon, 16 Mar 2026 23:29:41 GMT
VOLUME [/var/lib/influxdb]
# Mon, 16 Mar 2026 23:29:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 23:29:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 23:29:41 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fa3468d221545a43d2151f3977695a31857f9342ba842627d03c9fa1b2ae02`  
		Last Modified: Mon, 16 Mar 2026 22:37:09 GMT  
		Size: 24.0 MB (24038304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4cf91a29498481bcb2774753d32b947d34c8a875b4d0cc26467895c334f1dd`  
		Last Modified: Mon, 16 Mar 2026 23:29:51 GMT  
		Size: 19.4 MB (19385181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde80dcc1dfd5fc45df6e534c3d90d980adef9abe7e69f7d2aafb14bb57e17cb`  
		Last Modified: Mon, 16 Mar 2026 23:29:50 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07757a4b1133059e10be557710b3424182053781435a85154828461509909d2`  
		Last Modified: Mon, 16 Mar 2026 23:29:50 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.3-meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:f6a096dcce18046c5b1651cd32ce175e5d9e06a6e3e3ff33cda518466c9231b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4605864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb53755f9f14c374e8e9def0c1f29d32cb98a7b920013ab90ca8cfed126a079e`

```dockerfile
```

-	Layers:
	-	`sha256:e3a4f4e37f0311efd3bc8e767984bd395128ab2484afddf5178d01159451a3d1`  
		Last Modified: Mon, 16 Mar 2026 23:29:50 GMT  
		Size: 4.6 MB (4593201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd9ce7dc3b27548f4a7c880147b540cd89bc6f24c0d36169433b8c194da686ad`  
		Last Modified: Mon, 16 Mar 2026 23:29:50 GMT  
		Size: 12.7 KB (12663 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:1.12.3-meta-alpine`

```console
$ docker pull influxdb@sha256:0a051eaf780ce5a4e1d0bc51e7c16424b82219208822536392a61d77f4c527cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:1.12.3-meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:5d3f5bc09690d58108cd11b610d1a4190f786a7bc800ae17751ced7c530ea4f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.2 MB (24200738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ba49e476e65f5ea7acf3c9b2e0c08890594b6e04c2dd7f2f369dd925062925`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Sat, 14 Mar 2026 00:11:06 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Sat, 14 Mar 2026 00:11:09 GMT
ENV INFLUXDB_VERSION=1.12.3-c1.12.3
# Sat, 14 Mar 2026 00:11:09 GMT
ENV INFLUXDB_PR=
# Sat, 14 Mar 2026 00:11:09 GMT
ENV INFLUXDB_PV=1.12.3-c1.12.3
# Sat, 14 Mar 2026 00:11:09 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"         "influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     tar -xvf "influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz"         -C /usr/bin --strip-components 1 --wildcards             'influxdb-*/influxd-ctl'             'influxdb-*/influxd-meta' &&     rm "influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"        "influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     apk del .build-deps # buildkit
# Sat, 14 Mar 2026 00:11:09 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Sat, 14 Mar 2026 00:11:09 GMT
EXPOSE map[8091/tcp:{}]
# Sat, 14 Mar 2026 00:11:09 GMT
VOLUME [/var/lib/influxdb]
# Sat, 14 Mar 2026 00:11:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Mar 2026 00:11:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Mar 2026 00:11:09 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff222b2bc1735ef5ae68fbb3cd2555d5c9d167db3009d6ac7b76ffc0b64c953`  
		Last Modified: Sat, 14 Mar 2026 00:11:17 GMT  
		Size: 1.2 MB (1225264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84706419752f10f867a78117779b8e666144cfae465ae3bff03fead1a3d3aaf1`  
		Last Modified: Sat, 14 Mar 2026 00:11:17 GMT  
		Size: 19.3 MB (19331168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd86dc70a190dd7b913375552975c2652ab94591f2b2c476e3c95f5f7937b84d`  
		Last Modified: Sat, 14 Mar 2026 00:11:17 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00fac50404b2e130d37d058e96747807965ead40c44ecc2c3e0c6f11923cdae`  
		Last Modified: Sat, 14 Mar 2026 00:11:17 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:1.12.3-meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:547d60bfe06fa90ad6260c650a3774b3cc5a2e27f910aa0005926649448c72ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **696.0 KB (696015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:806c305f946ee74f2ee15815575ec4bf4caec2d242c42971eb8ee400298717a8`

```dockerfile
```

-	Layers:
	-	`sha256:bd2b90af63566b3d6c84fee2b1d16ffdab0305dcad16b98c31a186f832c7791e`  
		Last Modified: Sat, 14 Mar 2026 00:11:17 GMT  
		Size: 682.1 KB (682083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cac48257e4722c8ccb0f5993024e0cf6e88f5fccb58612457bd007afb71bd55`  
		Last Modified: Sat, 14 Mar 2026 00:11:17 GMT  
		Size: 13.9 KB (13932 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:2`

```console
$ docker pull influxdb@sha256:7500f5825d4cdda41befbafca3582ae606b984d33aa1aaf8ae22675dd12d8457
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2` - linux; amd64

```console
$ docker pull influxdb@sha256:51f3627309df65b6d8614512df251c1a3b801de5ed0f1639b74dcaba5167ae86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107240564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1db8a8da9a075b06012bfe43abb0516f9fd5a243a9529acb5fbf0adc047e5706`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:41:32 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:41:33 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 16 Mar 2026 22:41:33 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Mon, 16 Mar 2026 22:42:05 GMT
ENV GOSU_VER=1.19
# Mon, 16 Mar 2026 22:42:05 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Mon, 16 Mar 2026 22:42:05 GMT
ENV INFLUXDB_VERSION=2.8.0
# Mon, 16 Mar 2026 22:42:05 GMT
ENV INFLUXDB_PR=-2
# Mon, 16 Mar 2026 22:42:05 GMT
ENV INFLUXDB_PV=2.8.0-2
# Mon, 16 Mar 2026 22:42:08 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 16 Mar 2026 22:42:08 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 16 Mar 2026 22:42:08 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 16 Mar 2026 22:42:09 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 16 Mar 2026 22:42:09 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 16 Mar 2026 22:42:09 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 16 Mar 2026 22:42:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 22:42:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 22:42:09 GMT
CMD ["influxd"]
# Mon, 16 Mar 2026 22:42:09 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 16 Mar 2026 22:42:09 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 16 Mar 2026 22:42:09 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 16 Mar 2026 22:42:09 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 16 Mar 2026 22:42:09 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df5fe2f66ea80fb2a2904ca93537ac51968560c5437a710e4a2dbf9c6eb7577`  
		Last Modified: Mon, 16 Mar 2026 22:41:54 GMT  
		Size: 9.8 MB (9798253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67415bd2cacb12eefe1400623e7905284a37a8af821b4eb631092ca45e2df0f4`  
		Last Modified: Mon, 16 Mar 2026 22:41:54 GMT  
		Size: 6.2 MB (6156982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3655afae3b0a2802422d8c883d738f92fd775ebb1f500faff27aab0e7340849f`  
		Last Modified: Mon, 16 Mar 2026 22:41:54 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9325aa6fcb1cc238376ef01f3a219658720af41ae657788508a613f7a7a7a77c`  
		Last Modified: Mon, 16 Mar 2026 22:42:19 GMT  
		Size: 811.5 KB (811474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9cd1ff3a1e20994f2652d352e1bd2c61bbaed4601c4aeb0e0f30efa50873e6a`  
		Last Modified: Mon, 16 Mar 2026 22:42:21 GMT  
		Size: 50.5 MB (50451818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ca28afa0e9f842e0bc2ee9d275d2ded12eb174358e33a23a3807d42eaa7a89`  
		Last Modified: Mon, 16 Mar 2026 22:42:20 GMT  
		Size: 11.8 MB (11775857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e5068d62cc59afe0d0c9e8ddf71cd64282ca6623f9bf9676fea89b79e506bc`  
		Last Modified: Mon, 16 Mar 2026 22:42:19 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f8645d360e4540fcc478073a5ed2390b01563ca6b28faf4fef20310627f5dd`  
		Last Modified: Mon, 16 Mar 2026 22:42:20 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd7ac48b4a1dd229ee92f630b36400f7931dc9d788b82f9e807b01d6102c64c`  
		Last Modified: Mon, 16 Mar 2026 22:42:20 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:494269a08b389ddc2b1f2492fbf4b390bff9651c2277953ef1bd6c986907cbcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0fb69034a80b413147e9d25c385d3371a1de9f9fb9afe74658d1fb69070c1cc`

```dockerfile
```

-	Layers:
	-	`sha256:cba10e6f7b4c27e5ef10053adb4892794bc8cd3fb4c2c6f68cfb84dd2c1f797b`  
		Last Modified: Mon, 16 Mar 2026 22:42:19 GMT  
		Size: 2.9 MB (2934237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb8023ab021ed7474ff326bb8e15ba5f2ec39b0b1405d4bed281f484cfe977e5`  
		Last Modified: Mon, 16 Mar 2026 22:42:19 GMT  
		Size: 33.6 KB (33619 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:03aed0dc19b956f0e99b20abced161b88711c5aee5a5674f736bb8e501b601e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103639567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f0119106920d2e2ddb3b92de00996cb93773333bc44a0a76abe7c1ab5518b12`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:43:32 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:43:33 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 16 Mar 2026 22:43:33 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Mon, 16 Mar 2026 22:44:05 GMT
ENV GOSU_VER=1.19
# Mon, 16 Mar 2026 22:44:05 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Mon, 16 Mar 2026 22:44:05 GMT
ENV INFLUXDB_VERSION=2.8.0
# Mon, 16 Mar 2026 22:44:05 GMT
ENV INFLUXDB_PR=-2
# Mon, 16 Mar 2026 22:44:05 GMT
ENV INFLUXDB_PV=2.8.0-2
# Mon, 16 Mar 2026 22:44:08 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 16 Mar 2026 22:44:08 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 16 Mar 2026 22:44:09 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 16 Mar 2026 22:44:09 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 16 Mar 2026 22:44:09 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 16 Mar 2026 22:44:09 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 16 Mar 2026 22:44:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 22:44:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 22:44:09 GMT
CMD ["influxd"]
# Mon, 16 Mar 2026 22:44:09 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 16 Mar 2026 22:44:09 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 16 Mar 2026 22:44:09 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 16 Mar 2026 22:44:09 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 16 Mar 2026 22:44:09 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8bc38a8ddd1b644c33c76658fc21da215f939ed706cf9758ecff41c7fa766fd`  
		Last Modified: Mon, 16 Mar 2026 22:43:54 GMT  
		Size: 9.6 MB (9626825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85aef8ec230715cef2dfb5ab2f9d156911cc7e29a1aa3ce7570d7ccf30dc09d6`  
		Last Modified: Mon, 16 Mar 2026 22:43:54 GMT  
		Size: 5.8 MB (5790426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96446248fc0ab026e9db2728cbbe0c168ecfaf223b7253b5653ebe8590bb829c`  
		Last Modified: Mon, 16 Mar 2026 22:43:54 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbdd5dab386f405de61904714e628f34d6c839314755f61bd0ae62533ed300d`  
		Last Modified: Mon, 16 Mar 2026 22:44:19 GMT  
		Size: 766.4 KB (766373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43a4e1a3f57fc3b933998f99b1ddfbfbce740345b5676fcf938b36dbc69d68e`  
		Last Modified: Mon, 16 Mar 2026 22:44:21 GMT  
		Size: 48.2 MB (48229520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7aeaee757e728fb309c098b8808f34cc0740ee723f01c9ff01bf6923c565587`  
		Last Modified: Mon, 16 Mar 2026 22:44:20 GMT  
		Size: 11.1 MB (11100406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1b35bbe459cc568dffacf1b5ba0d18eca3847c48b1de232ee08a337b85d907`  
		Last Modified: Mon, 16 Mar 2026 22:44:19 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d86454bcba2acfb4eaa197367d866b3b7ddbfde85ab7de66fbe8f264a3dc00`  
		Last Modified: Mon, 16 Mar 2026 22:44:21 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939d5a79753c407ac035243984ba4f00cf508b96e906f6f22e05b2312f294936`  
		Last Modified: Mon, 16 Mar 2026 22:44:21 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2` - unknown; unknown

```console
$ docker pull influxdb@sha256:a97a089cc73e56e7ed298f2da153f9507a717aced7f64b9276f4fd211484ba3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6439137c2c566d8b0f8f91636ff4299f7ac662a77417ce70694f3a1bd9367b7a`

```dockerfile
```

-	Layers:
	-	`sha256:489ffdb6f86c2603567f3ced9380add2b2e47c467d83a243fd27c88a95ece61d`  
		Last Modified: Mon, 16 Mar 2026 22:44:20 GMT  
		Size: 2.9 MB (2933717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cce9d0d3799e339d314382a0a5840b2814e7b2eed13987b113cf402fcf30ac5`  
		Last Modified: Mon, 16 Mar 2026 22:44:19 GMT  
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
$ docker pull influxdb@sha256:5355c90249dac331bbcd1fdf3c31c7782400cd0ec5225145fc50b9aa026e9342
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7` - linux; amd64

```console
$ docker pull influxdb@sha256:9af9d913b26d597f8ce544811415775da360818250a89346fd55a2538f365ce1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157235498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd9c50454c5d5f8bf1898bc647738f9630d83b92d184e924b0afea98265dfdf6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:41:32 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:41:33 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 16 Mar 2026 22:41:33 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Mon, 16 Mar 2026 22:41:35 GMT
ENV GOSU_VER=1.16
# Mon, 16 Mar 2026 22:41:35 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Mon, 16 Mar 2026 22:41:35 GMT
ENV INFLUXDB_VERSION=2.7.12
# Mon, 16 Mar 2026 22:41:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Mon, 16 Mar 2026 22:41:38 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 16 Mar 2026 22:41:39 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 16 Mar 2026 22:41:39 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 16 Mar 2026 22:41:39 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 16 Mar 2026 22:41:39 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 16 Mar 2026 22:41:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 22:41:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 22:41:39 GMT
CMD ["influxd"]
# Mon, 16 Mar 2026 22:41:39 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 16 Mar 2026 22:41:39 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 16 Mar 2026 22:41:39 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 16 Mar 2026 22:41:39 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 16 Mar 2026 22:41:39 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df5fe2f66ea80fb2a2904ca93537ac51968560c5437a710e4a2dbf9c6eb7577`  
		Last Modified: Mon, 16 Mar 2026 22:41:54 GMT  
		Size: 9.8 MB (9798253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67415bd2cacb12eefe1400623e7905284a37a8af821b4eb631092ca45e2df0f4`  
		Last Modified: Mon, 16 Mar 2026 22:41:54 GMT  
		Size: 6.2 MB (6156982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3655afae3b0a2802422d8c883d738f92fd775ebb1f500faff27aab0e7340849f`  
		Last Modified: Mon, 16 Mar 2026 22:41:54 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e99c43b7ddd40a5da1fe9e7a2f831ed4b0325eebe1d1dbddc16aa790b3cee4cc`  
		Last Modified: Mon, 16 Mar 2026 22:41:54 GMT  
		Size: 1.0 MB (1012038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d8332b04e3975953f0c9a96e4c857748372a8f07efad7d2beed749195ce1d3`  
		Last Modified: Mon, 16 Mar 2026 22:41:57 GMT  
		Size: 100.2 MB (100246168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4184ff9cbff011b66ad3ae608b67530779f893367a86b1aeff2352fc9807abb`  
		Last Modified: Mon, 16 Mar 2026 22:41:56 GMT  
		Size: 11.8 MB (11775881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d563cfbbc4143b63a1539ebae9d106dfcc5c93094724c5bd706d5e8bc4aff2`  
		Last Modified: Mon, 16 Mar 2026 22:41:56 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738d59e728839eb94b3d728023766cf4fa5c5e8adc9858d262b2c0297ca08875`  
		Last Modified: Mon, 16 Mar 2026 22:41:56 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958f45fbade674b4845a3048d7b72a0a2e2850d77b763c084e14869f5a7aec04`  
		Last Modified: Mon, 16 Mar 2026 22:41:57 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:e84f6bce11f560efa489e89e605a338eceaa8cb8c3c538c2d051ddccfe81845c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3014385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66af3c61dcbae236cd5f416c0926fda745fcd07b8f1b582b7bac73943c16683d`

```dockerfile
```

-	Layers:
	-	`sha256:4c20377a85d33e7114a774d1fd68de2d61ccaba31fdc270e1ba3216863aba9dd`  
		Last Modified: Mon, 16 Mar 2026 22:41:54 GMT  
		Size: 3.0 MB (2981484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a54b97257a6fd9d5e0a5afa89892f8c3937404e3d82487db6833eeff80733a36`  
		Last Modified: Mon, 16 Mar 2026 22:41:54 GMT  
		Size: 32.9 KB (32901 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:efaf3e0af6aea2e5f933b43797d8fcbef7a1ebb84535696b328b5cfcd2ae485e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151624252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90e083fbe8447a156641878f2c3f3984cfede66c83e48e840b5ed42b59b0385`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:43:32 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:43:33 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 16 Mar 2026 22:43:33 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Mon, 16 Mar 2026 22:43:35 GMT
ENV GOSU_VER=1.16
# Mon, 16 Mar 2026 22:43:35 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Mon, 16 Mar 2026 22:43:35 GMT
ENV INFLUXDB_VERSION=2.7.12
# Mon, 16 Mar 2026 22:43:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Mon, 16 Mar 2026 22:43:38 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 16 Mar 2026 22:43:39 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 16 Mar 2026 22:43:40 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 16 Mar 2026 22:43:40 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 16 Mar 2026 22:43:40 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 16 Mar 2026 22:43:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 22:43:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 22:43:40 GMT
CMD ["influxd"]
# Mon, 16 Mar 2026 22:43:40 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 16 Mar 2026 22:43:40 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 16 Mar 2026 22:43:40 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 16 Mar 2026 22:43:40 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 16 Mar 2026 22:43:40 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8bc38a8ddd1b644c33c76658fc21da215f939ed706cf9758ecff41c7fa766fd`  
		Last Modified: Mon, 16 Mar 2026 22:43:54 GMT  
		Size: 9.6 MB (9626825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85aef8ec230715cef2dfb5ab2f9d156911cc7e29a1aa3ce7570d7ccf30dc09d6`  
		Last Modified: Mon, 16 Mar 2026 22:43:54 GMT  
		Size: 5.8 MB (5790426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96446248fc0ab026e9db2728cbbe0c168ecfaf223b7253b5653ebe8590bb829c`  
		Last Modified: Mon, 16 Mar 2026 22:43:54 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db737f08527b7b841c170fe08b0d5b2c139bbc6ddc7c8d0c6dfabe204730f37`  
		Last Modified: Mon, 16 Mar 2026 22:43:54 GMT  
		Size: 938.9 KB (938874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0f0a9bc278706c136c276377f477b7ef012668423ec21ce629639185d1ed0f`  
		Last Modified: Mon, 16 Mar 2026 22:43:57 GMT  
		Size: 96.0 MB (96041718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe8c5fabfcc2bc1d23cecb6eb6973f884b3812563feb9031a8b60bdd75b1e4b`  
		Last Modified: Mon, 16 Mar 2026 22:43:56 GMT  
		Size: 11.1 MB (11100392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53884d9d9fddbd38cdc0d3f1cc5394888151f9ca818e00f56b7ec2db2446bcbd`  
		Last Modified: Mon, 16 Mar 2026 22:43:55 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b29025c0a8169b874b0e10eaec1a17e1e5f2ce2be9ae210b69bd76be6ee16f`  
		Last Modified: Mon, 16 Mar 2026 22:43:56 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be5c656a85233a9f5d75ad774bbbcbf903810824389d408e9b5c41b2046adeb`  
		Last Modified: Mon, 16 Mar 2026 22:43:57 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7` - unknown; unknown

```console
$ docker pull influxdb@sha256:dedea37ea636ae016c76ec22e5d309138687f95e526136c584500e5d8c81e24d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3013748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c23149120bd6b70d105d63c8a4bde8379905dc64cd46fc87cfe465f7abffd98`

```dockerfile
```

-	Layers:
	-	`sha256:1af5f9eca8447a2f3e192c30933e737cf6f2f831e514240af4e05d98dd3366ba`  
		Last Modified: Mon, 16 Mar 2026 22:43:54 GMT  
		Size: 3.0 MB (2980688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3aa420290d3ed96494e08da0d15dada6146e5bf60079f26feffbfa75c084ae03`  
		Last Modified: Mon, 16 Mar 2026 22:43:54 GMT  
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
$ docker pull influxdb@sha256:5355c90249dac331bbcd1fdf3c31c7782400cd0ec5225145fc50b9aa026e9342
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.7.12` - linux; amd64

```console
$ docker pull influxdb@sha256:9af9d913b26d597f8ce544811415775da360818250a89346fd55a2538f365ce1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157235498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd9c50454c5d5f8bf1898bc647738f9630d83b92d184e924b0afea98265dfdf6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:41:32 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:41:33 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 16 Mar 2026 22:41:33 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Mon, 16 Mar 2026 22:41:35 GMT
ENV GOSU_VER=1.16
# Mon, 16 Mar 2026 22:41:35 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Mon, 16 Mar 2026 22:41:35 GMT
ENV INFLUXDB_VERSION=2.7.12
# Mon, 16 Mar 2026 22:41:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Mon, 16 Mar 2026 22:41:38 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 16 Mar 2026 22:41:39 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 16 Mar 2026 22:41:39 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 16 Mar 2026 22:41:39 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 16 Mar 2026 22:41:39 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 16 Mar 2026 22:41:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 22:41:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 22:41:39 GMT
CMD ["influxd"]
# Mon, 16 Mar 2026 22:41:39 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 16 Mar 2026 22:41:39 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 16 Mar 2026 22:41:39 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 16 Mar 2026 22:41:39 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 16 Mar 2026 22:41:39 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df5fe2f66ea80fb2a2904ca93537ac51968560c5437a710e4a2dbf9c6eb7577`  
		Last Modified: Mon, 16 Mar 2026 22:41:54 GMT  
		Size: 9.8 MB (9798253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67415bd2cacb12eefe1400623e7905284a37a8af821b4eb631092ca45e2df0f4`  
		Last Modified: Mon, 16 Mar 2026 22:41:54 GMT  
		Size: 6.2 MB (6156982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3655afae3b0a2802422d8c883d738f92fd775ebb1f500faff27aab0e7340849f`  
		Last Modified: Mon, 16 Mar 2026 22:41:54 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e99c43b7ddd40a5da1fe9e7a2f831ed4b0325eebe1d1dbddc16aa790b3cee4cc`  
		Last Modified: Mon, 16 Mar 2026 22:41:54 GMT  
		Size: 1.0 MB (1012038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d8332b04e3975953f0c9a96e4c857748372a8f07efad7d2beed749195ce1d3`  
		Last Modified: Mon, 16 Mar 2026 22:41:57 GMT  
		Size: 100.2 MB (100246168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4184ff9cbff011b66ad3ae608b67530779f893367a86b1aeff2352fc9807abb`  
		Last Modified: Mon, 16 Mar 2026 22:41:56 GMT  
		Size: 11.8 MB (11775881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d563cfbbc4143b63a1539ebae9d106dfcc5c93094724c5bd706d5e8bc4aff2`  
		Last Modified: Mon, 16 Mar 2026 22:41:56 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738d59e728839eb94b3d728023766cf4fa5c5e8adc9858d262b2c0297ca08875`  
		Last Modified: Mon, 16 Mar 2026 22:41:56 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958f45fbade674b4845a3048d7b72a0a2e2850d77b763c084e14869f5a7aec04`  
		Last Modified: Mon, 16 Mar 2026 22:41:57 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:e84f6bce11f560efa489e89e605a338eceaa8cb8c3c538c2d051ddccfe81845c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3014385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66af3c61dcbae236cd5f416c0926fda745fcd07b8f1b582b7bac73943c16683d`

```dockerfile
```

-	Layers:
	-	`sha256:4c20377a85d33e7114a774d1fd68de2d61ccaba31fdc270e1ba3216863aba9dd`  
		Last Modified: Mon, 16 Mar 2026 22:41:54 GMT  
		Size: 3.0 MB (2981484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a54b97257a6fd9d5e0a5afa89892f8c3937404e3d82487db6833eeff80733a36`  
		Last Modified: Mon, 16 Mar 2026 22:41:54 GMT  
		Size: 32.9 KB (32901 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.7.12` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:efaf3e0af6aea2e5f933b43797d8fcbef7a1ebb84535696b328b5cfcd2ae485e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151624252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90e083fbe8447a156641878f2c3f3984cfede66c83e48e840b5ed42b59b0385`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:43:32 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:43:33 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 16 Mar 2026 22:43:33 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Mon, 16 Mar 2026 22:43:35 GMT
ENV GOSU_VER=1.16
# Mon, 16 Mar 2026 22:43:35 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Mon, 16 Mar 2026 22:43:35 GMT
ENV INFLUXDB_VERSION=2.7.12
# Mon, 16 Mar 2026 22:43:38 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_VERSION}_linux_${arch}.tar.gz.asc"            "influxdb2_linux_${arch}" &&     influxd version # buildkit
# Mon, 16 Mar 2026 22:43:38 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 16 Mar 2026 22:43:39 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 16 Mar 2026 22:43:40 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 16 Mar 2026 22:43:40 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 16 Mar 2026 22:43:40 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 16 Mar 2026 22:43:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 22:43:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 22:43:40 GMT
CMD ["influxd"]
# Mon, 16 Mar 2026 22:43:40 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 16 Mar 2026 22:43:40 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 16 Mar 2026 22:43:40 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 16 Mar 2026 22:43:40 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 16 Mar 2026 22:43:40 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8bc38a8ddd1b644c33c76658fc21da215f939ed706cf9758ecff41c7fa766fd`  
		Last Modified: Mon, 16 Mar 2026 22:43:54 GMT  
		Size: 9.6 MB (9626825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85aef8ec230715cef2dfb5ab2f9d156911cc7e29a1aa3ce7570d7ccf30dc09d6`  
		Last Modified: Mon, 16 Mar 2026 22:43:54 GMT  
		Size: 5.8 MB (5790426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96446248fc0ab026e9db2728cbbe0c168ecfaf223b7253b5653ebe8590bb829c`  
		Last Modified: Mon, 16 Mar 2026 22:43:54 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db737f08527b7b841c170fe08b0d5b2c139bbc6ddc7c8d0c6dfabe204730f37`  
		Last Modified: Mon, 16 Mar 2026 22:43:54 GMT  
		Size: 938.9 KB (938874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0f0a9bc278706c136c276377f477b7ef012668423ec21ce629639185d1ed0f`  
		Last Modified: Mon, 16 Mar 2026 22:43:57 GMT  
		Size: 96.0 MB (96041718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe8c5fabfcc2bc1d23cecb6eb6973f884b3812563feb9031a8b60bdd75b1e4b`  
		Last Modified: Mon, 16 Mar 2026 22:43:56 GMT  
		Size: 11.1 MB (11100392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53884d9d9fddbd38cdc0d3f1cc5394888151f9ca818e00f56b7ec2db2446bcbd`  
		Last Modified: Mon, 16 Mar 2026 22:43:55 GMT  
		Size: 208.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b29025c0a8169b874b0e10eaec1a17e1e5f2ce2be9ae210b69bd76be6ee16f`  
		Last Modified: Mon, 16 Mar 2026 22:43:56 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be5c656a85233a9f5d75ad774bbbcbf903810824389d408e9b5c41b2046adeb`  
		Last Modified: Mon, 16 Mar 2026 22:43:57 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.7.12` - unknown; unknown

```console
$ docker pull influxdb@sha256:dedea37ea636ae016c76ec22e5d309138687f95e526136c584500e5d8c81e24d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3013748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c23149120bd6b70d105d63c8a4bde8379905dc64cd46fc87cfe465f7abffd98`

```dockerfile
```

-	Layers:
	-	`sha256:1af5f9eca8447a2f3e192c30933e737cf6f2f831e514240af4e05d98dd3366ba`  
		Last Modified: Mon, 16 Mar 2026 22:43:54 GMT  
		Size: 3.0 MB (2980688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3aa420290d3ed96494e08da0d15dada6146e5bf60079f26feffbfa75c084ae03`  
		Last Modified: Mon, 16 Mar 2026 22:43:54 GMT  
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
$ docker pull influxdb@sha256:7500f5825d4cdda41befbafca3582ae606b984d33aa1aaf8ae22675dd12d8457
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.8` - linux; amd64

```console
$ docker pull influxdb@sha256:51f3627309df65b6d8614512df251c1a3b801de5ed0f1639b74dcaba5167ae86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107240564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1db8a8da9a075b06012bfe43abb0516f9fd5a243a9529acb5fbf0adc047e5706`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:41:32 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:41:33 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 16 Mar 2026 22:41:33 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Mon, 16 Mar 2026 22:42:05 GMT
ENV GOSU_VER=1.19
# Mon, 16 Mar 2026 22:42:05 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Mon, 16 Mar 2026 22:42:05 GMT
ENV INFLUXDB_VERSION=2.8.0
# Mon, 16 Mar 2026 22:42:05 GMT
ENV INFLUXDB_PR=-2
# Mon, 16 Mar 2026 22:42:05 GMT
ENV INFLUXDB_PV=2.8.0-2
# Mon, 16 Mar 2026 22:42:08 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 16 Mar 2026 22:42:08 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 16 Mar 2026 22:42:08 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 16 Mar 2026 22:42:09 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 16 Mar 2026 22:42:09 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 16 Mar 2026 22:42:09 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 16 Mar 2026 22:42:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 22:42:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 22:42:09 GMT
CMD ["influxd"]
# Mon, 16 Mar 2026 22:42:09 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 16 Mar 2026 22:42:09 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 16 Mar 2026 22:42:09 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 16 Mar 2026 22:42:09 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 16 Mar 2026 22:42:09 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df5fe2f66ea80fb2a2904ca93537ac51968560c5437a710e4a2dbf9c6eb7577`  
		Last Modified: Mon, 16 Mar 2026 22:41:54 GMT  
		Size: 9.8 MB (9798253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67415bd2cacb12eefe1400623e7905284a37a8af821b4eb631092ca45e2df0f4`  
		Last Modified: Mon, 16 Mar 2026 22:41:54 GMT  
		Size: 6.2 MB (6156982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3655afae3b0a2802422d8c883d738f92fd775ebb1f500faff27aab0e7340849f`  
		Last Modified: Mon, 16 Mar 2026 22:41:54 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9325aa6fcb1cc238376ef01f3a219658720af41ae657788508a613f7a7a7a77c`  
		Last Modified: Mon, 16 Mar 2026 22:42:19 GMT  
		Size: 811.5 KB (811474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9cd1ff3a1e20994f2652d352e1bd2c61bbaed4601c4aeb0e0f30efa50873e6a`  
		Last Modified: Mon, 16 Mar 2026 22:42:21 GMT  
		Size: 50.5 MB (50451818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ca28afa0e9f842e0bc2ee9d275d2ded12eb174358e33a23a3807d42eaa7a89`  
		Last Modified: Mon, 16 Mar 2026 22:42:20 GMT  
		Size: 11.8 MB (11775857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e5068d62cc59afe0d0c9e8ddf71cd64282ca6623f9bf9676fea89b79e506bc`  
		Last Modified: Mon, 16 Mar 2026 22:42:19 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f8645d360e4540fcc478073a5ed2390b01563ca6b28faf4fef20310627f5dd`  
		Last Modified: Mon, 16 Mar 2026 22:42:20 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd7ac48b4a1dd229ee92f630b36400f7931dc9d788b82f9e807b01d6102c64c`  
		Last Modified: Mon, 16 Mar 2026 22:42:20 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:494269a08b389ddc2b1f2492fbf4b390bff9651c2277953ef1bd6c986907cbcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0fb69034a80b413147e9d25c385d3371a1de9f9fb9afe74658d1fb69070c1cc`

```dockerfile
```

-	Layers:
	-	`sha256:cba10e6f7b4c27e5ef10053adb4892794bc8cd3fb4c2c6f68cfb84dd2c1f797b`  
		Last Modified: Mon, 16 Mar 2026 22:42:19 GMT  
		Size: 2.9 MB (2934237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb8023ab021ed7474ff326bb8e15ba5f2ec39b0b1405d4bed281f484cfe977e5`  
		Last Modified: Mon, 16 Mar 2026 22:42:19 GMT  
		Size: 33.6 KB (33619 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.8` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:03aed0dc19b956f0e99b20abced161b88711c5aee5a5674f736bb8e501b601e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103639567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f0119106920d2e2ddb3b92de00996cb93773333bc44a0a76abe7c1ab5518b12`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:43:32 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:43:33 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 16 Mar 2026 22:43:33 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Mon, 16 Mar 2026 22:44:05 GMT
ENV GOSU_VER=1.19
# Mon, 16 Mar 2026 22:44:05 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Mon, 16 Mar 2026 22:44:05 GMT
ENV INFLUXDB_VERSION=2.8.0
# Mon, 16 Mar 2026 22:44:05 GMT
ENV INFLUXDB_PR=-2
# Mon, 16 Mar 2026 22:44:05 GMT
ENV INFLUXDB_PV=2.8.0-2
# Mon, 16 Mar 2026 22:44:08 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 16 Mar 2026 22:44:08 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 16 Mar 2026 22:44:09 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 16 Mar 2026 22:44:09 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 16 Mar 2026 22:44:09 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 16 Mar 2026 22:44:09 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 16 Mar 2026 22:44:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 22:44:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 22:44:09 GMT
CMD ["influxd"]
# Mon, 16 Mar 2026 22:44:09 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 16 Mar 2026 22:44:09 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 16 Mar 2026 22:44:09 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 16 Mar 2026 22:44:09 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 16 Mar 2026 22:44:09 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8bc38a8ddd1b644c33c76658fc21da215f939ed706cf9758ecff41c7fa766fd`  
		Last Modified: Mon, 16 Mar 2026 22:43:54 GMT  
		Size: 9.6 MB (9626825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85aef8ec230715cef2dfb5ab2f9d156911cc7e29a1aa3ce7570d7ccf30dc09d6`  
		Last Modified: Mon, 16 Mar 2026 22:43:54 GMT  
		Size: 5.8 MB (5790426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96446248fc0ab026e9db2728cbbe0c168ecfaf223b7253b5653ebe8590bb829c`  
		Last Modified: Mon, 16 Mar 2026 22:43:54 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbdd5dab386f405de61904714e628f34d6c839314755f61bd0ae62533ed300d`  
		Last Modified: Mon, 16 Mar 2026 22:44:19 GMT  
		Size: 766.4 KB (766373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43a4e1a3f57fc3b933998f99b1ddfbfbce740345b5676fcf938b36dbc69d68e`  
		Last Modified: Mon, 16 Mar 2026 22:44:21 GMT  
		Size: 48.2 MB (48229520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7aeaee757e728fb309c098b8808f34cc0740ee723f01c9ff01bf6923c565587`  
		Last Modified: Mon, 16 Mar 2026 22:44:20 GMT  
		Size: 11.1 MB (11100406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1b35bbe459cc568dffacf1b5ba0d18eca3847c48b1de232ee08a337b85d907`  
		Last Modified: Mon, 16 Mar 2026 22:44:19 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d86454bcba2acfb4eaa197367d866b3b7ddbfde85ab7de66fbe8f264a3dc00`  
		Last Modified: Mon, 16 Mar 2026 22:44:21 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939d5a79753c407ac035243984ba4f00cf508b96e906f6f22e05b2312f294936`  
		Last Modified: Mon, 16 Mar 2026 22:44:21 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8` - unknown; unknown

```console
$ docker pull influxdb@sha256:a97a089cc73e56e7ed298f2da153f9507a717aced7f64b9276f4fd211484ba3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6439137c2c566d8b0f8f91636ff4299f7ac662a77417ce70694f3a1bd9367b7a`

```dockerfile
```

-	Layers:
	-	`sha256:489ffdb6f86c2603567f3ced9380add2b2e47c467d83a243fd27c88a95ece61d`  
		Last Modified: Mon, 16 Mar 2026 22:44:20 GMT  
		Size: 2.9 MB (2933717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cce9d0d3799e339d314382a0a5840b2814e7b2eed13987b113cf402fcf30ac5`  
		Last Modified: Mon, 16 Mar 2026 22:44:19 GMT  
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
$ docker pull influxdb@sha256:7500f5825d4cdda41befbafca3582ae606b984d33aa1aaf8ae22675dd12d8457
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:2.8.0` - linux; amd64

```console
$ docker pull influxdb@sha256:51f3627309df65b6d8614512df251c1a3b801de5ed0f1639b74dcaba5167ae86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107240564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1db8a8da9a075b06012bfe43abb0516f9fd5a243a9529acb5fbf0adc047e5706`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:41:32 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:41:33 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 16 Mar 2026 22:41:33 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Mon, 16 Mar 2026 22:42:05 GMT
ENV GOSU_VER=1.19
# Mon, 16 Mar 2026 22:42:05 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Mon, 16 Mar 2026 22:42:05 GMT
ENV INFLUXDB_VERSION=2.8.0
# Mon, 16 Mar 2026 22:42:05 GMT
ENV INFLUXDB_PR=-2
# Mon, 16 Mar 2026 22:42:05 GMT
ENV INFLUXDB_PV=2.8.0-2
# Mon, 16 Mar 2026 22:42:08 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 16 Mar 2026 22:42:08 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 16 Mar 2026 22:42:08 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 16 Mar 2026 22:42:09 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 16 Mar 2026 22:42:09 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 16 Mar 2026 22:42:09 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 16 Mar 2026 22:42:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 22:42:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 22:42:09 GMT
CMD ["influxd"]
# Mon, 16 Mar 2026 22:42:09 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 16 Mar 2026 22:42:09 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 16 Mar 2026 22:42:09 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 16 Mar 2026 22:42:09 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 16 Mar 2026 22:42:09 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df5fe2f66ea80fb2a2904ca93537ac51968560c5437a710e4a2dbf9c6eb7577`  
		Last Modified: Mon, 16 Mar 2026 22:41:54 GMT  
		Size: 9.8 MB (9798253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67415bd2cacb12eefe1400623e7905284a37a8af821b4eb631092ca45e2df0f4`  
		Last Modified: Mon, 16 Mar 2026 22:41:54 GMT  
		Size: 6.2 MB (6156982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3655afae3b0a2802422d8c883d738f92fd775ebb1f500faff27aab0e7340849f`  
		Last Modified: Mon, 16 Mar 2026 22:41:54 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9325aa6fcb1cc238376ef01f3a219658720af41ae657788508a613f7a7a7a77c`  
		Last Modified: Mon, 16 Mar 2026 22:42:19 GMT  
		Size: 811.5 KB (811474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9cd1ff3a1e20994f2652d352e1bd2c61bbaed4601c4aeb0e0f30efa50873e6a`  
		Last Modified: Mon, 16 Mar 2026 22:42:21 GMT  
		Size: 50.5 MB (50451818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ca28afa0e9f842e0bc2ee9d275d2ded12eb174358e33a23a3807d42eaa7a89`  
		Last Modified: Mon, 16 Mar 2026 22:42:20 GMT  
		Size: 11.8 MB (11775857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e5068d62cc59afe0d0c9e8ddf71cd64282ca6623f9bf9676fea89b79e506bc`  
		Last Modified: Mon, 16 Mar 2026 22:42:19 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f8645d360e4540fcc478073a5ed2390b01563ca6b28faf4fef20310627f5dd`  
		Last Modified: Mon, 16 Mar 2026 22:42:20 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd7ac48b4a1dd229ee92f630b36400f7931dc9d788b82f9e807b01d6102c64c`  
		Last Modified: Mon, 16 Mar 2026 22:42:20 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8.0` - unknown; unknown

```console
$ docker pull influxdb@sha256:494269a08b389ddc2b1f2492fbf4b390bff9651c2277953ef1bd6c986907cbcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0fb69034a80b413147e9d25c385d3371a1de9f9fb9afe74658d1fb69070c1cc`

```dockerfile
```

-	Layers:
	-	`sha256:cba10e6f7b4c27e5ef10053adb4892794bc8cd3fb4c2c6f68cfb84dd2c1f797b`  
		Last Modified: Mon, 16 Mar 2026 22:42:19 GMT  
		Size: 2.9 MB (2934237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb8023ab021ed7474ff326bb8e15ba5f2ec39b0b1405d4bed281f484cfe977e5`  
		Last Modified: Mon, 16 Mar 2026 22:42:19 GMT  
		Size: 33.6 KB (33619 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:2.8.0` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:03aed0dc19b956f0e99b20abced161b88711c5aee5a5674f736bb8e501b601e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103639567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f0119106920d2e2ddb3b92de00996cb93773333bc44a0a76abe7c1ab5518b12`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:43:32 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:43:33 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 16 Mar 2026 22:43:33 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Mon, 16 Mar 2026 22:44:05 GMT
ENV GOSU_VER=1.19
# Mon, 16 Mar 2026 22:44:05 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Mon, 16 Mar 2026 22:44:05 GMT
ENV INFLUXDB_VERSION=2.8.0
# Mon, 16 Mar 2026 22:44:05 GMT
ENV INFLUXDB_PR=-2
# Mon, 16 Mar 2026 22:44:05 GMT
ENV INFLUXDB_PV=2.8.0-2
# Mon, 16 Mar 2026 22:44:08 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 16 Mar 2026 22:44:08 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 16 Mar 2026 22:44:09 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 16 Mar 2026 22:44:09 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 16 Mar 2026 22:44:09 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 16 Mar 2026 22:44:09 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 16 Mar 2026 22:44:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 22:44:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 22:44:09 GMT
CMD ["influxd"]
# Mon, 16 Mar 2026 22:44:09 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 16 Mar 2026 22:44:09 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 16 Mar 2026 22:44:09 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 16 Mar 2026 22:44:09 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 16 Mar 2026 22:44:09 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8bc38a8ddd1b644c33c76658fc21da215f939ed706cf9758ecff41c7fa766fd`  
		Last Modified: Mon, 16 Mar 2026 22:43:54 GMT  
		Size: 9.6 MB (9626825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85aef8ec230715cef2dfb5ab2f9d156911cc7e29a1aa3ce7570d7ccf30dc09d6`  
		Last Modified: Mon, 16 Mar 2026 22:43:54 GMT  
		Size: 5.8 MB (5790426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96446248fc0ab026e9db2728cbbe0c168ecfaf223b7253b5653ebe8590bb829c`  
		Last Modified: Mon, 16 Mar 2026 22:43:54 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbdd5dab386f405de61904714e628f34d6c839314755f61bd0ae62533ed300d`  
		Last Modified: Mon, 16 Mar 2026 22:44:19 GMT  
		Size: 766.4 KB (766373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43a4e1a3f57fc3b933998f99b1ddfbfbce740345b5676fcf938b36dbc69d68e`  
		Last Modified: Mon, 16 Mar 2026 22:44:21 GMT  
		Size: 48.2 MB (48229520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7aeaee757e728fb309c098b8808f34cc0740ee723f01c9ff01bf6923c565587`  
		Last Modified: Mon, 16 Mar 2026 22:44:20 GMT  
		Size: 11.1 MB (11100406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1b35bbe459cc568dffacf1b5ba0d18eca3847c48b1de232ee08a337b85d907`  
		Last Modified: Mon, 16 Mar 2026 22:44:19 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d86454bcba2acfb4eaa197367d866b3b7ddbfde85ab7de66fbe8f264a3dc00`  
		Last Modified: Mon, 16 Mar 2026 22:44:21 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939d5a79753c407ac035243984ba4f00cf508b96e906f6f22e05b2312f294936`  
		Last Modified: Mon, 16 Mar 2026 22:44:21 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:2.8.0` - unknown; unknown

```console
$ docker pull influxdb@sha256:a97a089cc73e56e7ed298f2da153f9507a717aced7f64b9276f4fd211484ba3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6439137c2c566d8b0f8f91636ff4299f7ac662a77417ce70694f3a1bd9367b7a`

```dockerfile
```

-	Layers:
	-	`sha256:489ffdb6f86c2603567f3ced9380add2b2e47c467d83a243fd27c88a95ece61d`  
		Last Modified: Mon, 16 Mar 2026 22:44:20 GMT  
		Size: 2.9 MB (2933717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cce9d0d3799e339d314382a0a5840b2814e7b2eed13987b113cf402fcf30ac5`  
		Last Modified: Mon, 16 Mar 2026 22:44:19 GMT  
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
$ docker pull influxdb@sha256:609ebd662ae250de2979a14ebadb5fdabb638f36164291afbcd250689ce33012
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-core` - linux; amd64

```console
$ docker pull influxdb@sha256:485d207b488d55aeea7a5d3a3cc7840bb4f913d68672805dceae570a1d73bec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.3 MB (119332263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b859ca5ad155b3cc763d332fd2f72fe2a18dd7085b4caac8e1ff738126813e6`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:39:17 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 17 Mar 2026 01:39:17 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 17 Mar 2026 01:39:21 GMT
ENV INFLUXDB_VERSION=3.8.3
# Tue, 17 Mar 2026 01:39:21 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 17 Mar 2026 01:39:22 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:39:22 GMT
USER influxdb3
# Tue, 17 Mar 2026 01:39:22 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 17 Mar 2026 01:39:22 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 17 Mar 2026 01:39:22 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 17 Mar 2026 01:39:22 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Tue, 17 Mar 2026 01:39:22 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 17 Mar 2026 01:39:22 GMT
ENV LOG_FILTER=info
# Tue, 17 Mar 2026 01:39:22 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 17 Mar 2026 01:39:22 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 17 Mar 2026 01:39:22 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af5e6398084a9d4e75bb30b6c2aca56200184633c1cd8f7332ca9b42a2c10c0`  
		Last Modified: Tue, 17 Mar 2026 01:39:37 GMT  
		Size: 6.7 MB (6671609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61664b8c9e70a8f737b8374de8a43c17a6e7ed951ea3405ae356ff8ac1504c2c`  
		Last Modified: Tue, 17 Mar 2026 01:39:37 GMT  
		Size: 3.6 KB (3650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb71f3ada84e0f969a23bc644cab325a901dea08254a55b58a3f4482f903b7ce`  
		Last Modified: Tue, 17 Mar 2026 01:39:39 GMT  
		Size: 82.9 MB (82924340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e231aea6c4f3bb50ae34666ed3ac19cad4ff24461b6c1c79fd9296e47a65b3f1`  
		Last Modified: Tue, 17 Mar 2026 01:39:37 GMT  
		Size: 522.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1674f81369428f8c3e8ba40eb95877924aec2b43c2a40c127c1372a2227bb5c`  
		Last Modified: Tue, 17 Mar 2026 01:39:38 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:016e7be995c4b2e644e24cd8f6c53ddb00c9031c358699427d10bac41fcdc22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df3a93850dd92cce14a5c095cabdac43aa4c2f8ebf5a2c52103d5e948c83f29a`

```dockerfile
```

-	Layers:
	-	`sha256:ad8d87fd71b8ca4613fb1aad11ecda70df15c75210e19ff5983e58fa9770a33c`  
		Last Modified: Tue, 17 Mar 2026 01:39:37 GMT  
		Size: 2.3 MB (2310587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94a0435bb1d6c40bfe6d6b5b90d7c15528dddc8ecc3b5a7efbe1a909f8bc727d`  
		Last Modified: Tue, 17 Mar 2026 01:39:36 GMT  
		Size: 17.6 KB (17617 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:63ea1e59b44f904a50bb2ca5c7fb9f9a8bb22a3c7a5c0587fbc707f7a2971db7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110135104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:341d195bbed7114c685d729af960d2fa3d95a56c3b8e8e702db8f68942e96dc8`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:40:06 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 17 Mar 2026 01:40:06 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 17 Mar 2026 01:40:13 GMT
ENV INFLUXDB_VERSION=3.8.3
# Tue, 17 Mar 2026 01:40:13 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 17 Mar 2026 01:40:13 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:40:13 GMT
USER influxdb3
# Tue, 17 Mar 2026 01:40:13 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 17 Mar 2026 01:40:13 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 17 Mar 2026 01:40:13 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 17 Mar 2026 01:40:13 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Tue, 17 Mar 2026 01:40:13 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 17 Mar 2026 01:40:13 GMT
ENV LOG_FILTER=info
# Tue, 17 Mar 2026 01:40:13 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 17 Mar 2026 01:40:13 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 17 Mar 2026 01:40:13 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a5ff7761a3de3cfdfbde6b4aa7e485e10238103213ecb9db9c4609293d2faa6`  
		Last Modified: Tue, 17 Mar 2026 01:40:27 GMT  
		Size: 6.7 MB (6681856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1264b241981cfe9581d0ba6c743ec3b73bdbb1944e9081b0a022d4f407b473`  
		Last Modified: Tue, 17 Mar 2026 01:40:26 GMT  
		Size: 3.6 KB (3650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56a20c20f06dbbda1dd6a4ab1be0c7c77ea648b3965aba21c4e04af2c1a15a7`  
		Last Modified: Tue, 17 Mar 2026 01:40:28 GMT  
		Size: 74.6 MB (74579220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f703f18e65af6ac7ed5a6c75e70bd0a9e394f226f5ffc0e615d313f1202888`  
		Last Modified: Tue, 17 Mar 2026 01:40:26 GMT  
		Size: 520.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bbf9139ff50f89c76e18e8bd41cee3acb6e075925aa770b2ee60cc389321918`  
		Last Modified: Tue, 17 Mar 2026 01:40:28 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-core` - unknown; unknown

```console
$ docker pull influxdb@sha256:1aef9353b9015c5a38b910cffd2e48a199f9e96fcfdbf0bc40720e45c446f06e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df5730ad5f074116ae5eeafb6c90c912b8313fa502d86022540499653d7c2192`

```dockerfile
```

-	Layers:
	-	`sha256:8f0d054fc2be50c07051760fae65549046134b8a7433c570118936bbf76288b5`  
		Last Modified: Tue, 17 Mar 2026 01:40:26 GMT  
		Size: 2.3 MB (2311669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee9350556a6e72b07053ccdedca25c80c0a30574bf73055e22981b7a17094266`  
		Last Modified: Tue, 17 Mar 2026 01:40:26 GMT  
		Size: 17.8 KB (17766 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3-enterprise`

```console
$ docker pull influxdb@sha256:659da4d6af9a37902819986a2fd489b0f6f2ed454e6822ebb7937ca99f2dbf56
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:3-enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:0068439a849d0a8a75d5bf31109518822189e0a91205428cc4dabbe07adbecad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128390942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e95f3a3854771047f8c42216606eedeede2dd0e6bd68ff406622594620b048`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:39:16 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 17 Mar 2026 01:39:17 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 17 Mar 2026 01:39:24 GMT
ENV INFLUXDB_VERSION=3.8.4
# Tue, 17 Mar 2026 01:39:24 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 17 Mar 2026 01:39:24 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:39:24 GMT
USER influxdb3
# Tue, 17 Mar 2026 01:39:24 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 17 Mar 2026 01:39:24 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 17 Mar 2026 01:39:24 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 17 Mar 2026 01:39:24 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Tue, 17 Mar 2026 01:39:24 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 17 Mar 2026 01:39:24 GMT
ENV LOG_FILTER=info
# Tue, 17 Mar 2026 01:39:24 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 17 Mar 2026 01:39:24 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 17 Mar 2026 01:39:24 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896f80de69282718f797c732aadcb5ad7cb525eba98ad4a175031054cf4c4e18`  
		Last Modified: Tue, 17 Mar 2026 01:39:40 GMT  
		Size: 6.7 MB (6671643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61664b8c9e70a8f737b8374de8a43c17a6e7ed951ea3405ae356ff8ac1504c2c`  
		Last Modified: Tue, 17 Mar 2026 01:39:37 GMT  
		Size: 3.6 KB (3650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1361daea27f76c6bf56c08ba7564ae65156ecb8e251185ccf018f686904d8a`  
		Last Modified: Tue, 17 Mar 2026 01:39:42 GMT  
		Size: 92.0 MB (91982987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4bd0ef6e31704dc021b0a98036ab976fb486d924c03223094882b49fc16927c`  
		Last Modified: Tue, 17 Mar 2026 01:39:40 GMT  
		Size: 521.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933f1bceff72da4ddca28a5cd3c12dfb8fcedcb2836202ab2c5ed2c96f3f2ed8`  
		Last Modified: Tue, 17 Mar 2026 01:39:40 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:1ea34b829420e68babbc9e10a485b40864a22cf629cca20295def1c06bc64d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf42083b11801171ad943480cd34dc1cefdae0725c8038f3efa8bfec30dcdf30`

```dockerfile
```

-	Layers:
	-	`sha256:26b0a0947e306cff33e0baf6ef78e411ba1dc193e9b5199f2a4c37878542d860`  
		Last Modified: Tue, 17 Mar 2026 01:39:40 GMT  
		Size: 2.3 MB (2310635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec22d992ae8949247335d9458549ad1e329d7740a6448e282ca6d1882ab71ab0`  
		Last Modified: Tue, 17 Mar 2026 01:39:40 GMT  
		Size: 17.8 KB (17797 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:3-enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:e71c1877459a80a96b782a6700ab975468ed7c160f8b8aba45d54011f06c2bbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (119034746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f99105f51447acc10566cad4da5c9dd93e87600aea5786c58c1b91b2deba254`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:40:28 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 17 Mar 2026 01:40:28 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 17 Mar 2026 01:40:35 GMT
ENV INFLUXDB_VERSION=3.8.4
# Tue, 17 Mar 2026 01:40:35 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 17 Mar 2026 01:40:35 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:40:35 GMT
USER influxdb3
# Tue, 17 Mar 2026 01:40:35 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 17 Mar 2026 01:40:35 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 17 Mar 2026 01:40:35 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 17 Mar 2026 01:40:35 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Tue, 17 Mar 2026 01:40:35 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 17 Mar 2026 01:40:35 GMT
ENV LOG_FILTER=info
# Tue, 17 Mar 2026 01:40:35 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 17 Mar 2026 01:40:35 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 17 Mar 2026 01:40:35 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c9b202493abf56134337b459be8acb07328c6f25892605d440c7f265df6a7b`  
		Last Modified: Tue, 17 Mar 2026 01:40:49 GMT  
		Size: 6.7 MB (6681738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4286e69af75bf4ff096601e07ac6fe12af7d7bccaa18225bb29036d2f2503c53`  
		Last Modified: Tue, 17 Mar 2026 01:40:49 GMT  
		Size: 3.7 KB (3653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35fff946bce4cefe39db32464b13a52437398b2f8c8bbe74de3121fc2127f368`  
		Last Modified: Tue, 17 Mar 2026 01:40:51 GMT  
		Size: 83.5 MB (83478973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c48ae972e761f8f9851eeed70d099301714e48a925d5b45dd64fbe150592c6`  
		Last Modified: Tue, 17 Mar 2026 01:40:49 GMT  
		Size: 523.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db91e6bd4f3aac338c3aab1210b06acfb137b4ae2fbf6ef74298b77b4d43a83`  
		Last Modified: Tue, 17 Mar 2026 01:40:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:3-enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:5606f14d9173824d7f4dc14323f0db97097ef4ec2f886c3399be7055a68782bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a41e5b6195df8732b06f84032c50c76d3ee58f41e79e1fd31787622cbbefdd`

```dockerfile
```

-	Layers:
	-	`sha256:c2ef077fcbcf2aa087d7b258518807849f8bc051379a75b23bfb92e88b51d361`  
		Last Modified: Tue, 17 Mar 2026 01:40:49 GMT  
		Size: 2.3 MB (2311717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0071489710411d8fa4dd7b44c485227d6ceac8e7c15cd9cb0ac28ad1b57f52cb`  
		Last Modified: Tue, 17 Mar 2026 01:40:49 GMT  
		Size: 17.9 KB (17946 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:3.9-core`

**does not exist** (yet?)

## `influxdb:3.9-enterprise`

**does not exist** (yet?)

## `influxdb:3.9.0-core`

**does not exist** (yet?)

## `influxdb:3.9.0-enterprise`

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
$ docker pull influxdb@sha256:609ebd662ae250de2979a14ebadb5fdabb638f36164291afbcd250689ce33012
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:core` - linux; amd64

```console
$ docker pull influxdb@sha256:485d207b488d55aeea7a5d3a3cc7840bb4f913d68672805dceae570a1d73bec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.3 MB (119332263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b859ca5ad155b3cc763d332fd2f72fe2a18dd7085b4caac8e1ff738126813e6`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:39:17 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 17 Mar 2026 01:39:17 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 17 Mar 2026 01:39:21 GMT
ENV INFLUXDB_VERSION=3.8.3
# Tue, 17 Mar 2026 01:39:21 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 17 Mar 2026 01:39:22 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:39:22 GMT
USER influxdb3
# Tue, 17 Mar 2026 01:39:22 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 17 Mar 2026 01:39:22 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 17 Mar 2026 01:39:22 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 17 Mar 2026 01:39:22 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Tue, 17 Mar 2026 01:39:22 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 17 Mar 2026 01:39:22 GMT
ENV LOG_FILTER=info
# Tue, 17 Mar 2026 01:39:22 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 17 Mar 2026 01:39:22 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 17 Mar 2026 01:39:22 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af5e6398084a9d4e75bb30b6c2aca56200184633c1cd8f7332ca9b42a2c10c0`  
		Last Modified: Tue, 17 Mar 2026 01:39:37 GMT  
		Size: 6.7 MB (6671609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61664b8c9e70a8f737b8374de8a43c17a6e7ed951ea3405ae356ff8ac1504c2c`  
		Last Modified: Tue, 17 Mar 2026 01:39:37 GMT  
		Size: 3.6 KB (3650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb71f3ada84e0f969a23bc644cab325a901dea08254a55b58a3f4482f903b7ce`  
		Last Modified: Tue, 17 Mar 2026 01:39:39 GMT  
		Size: 82.9 MB (82924340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e231aea6c4f3bb50ae34666ed3ac19cad4ff24461b6c1c79fd9296e47a65b3f1`  
		Last Modified: Tue, 17 Mar 2026 01:39:37 GMT  
		Size: 522.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1674f81369428f8c3e8ba40eb95877924aec2b43c2a40c127c1372a2227bb5c`  
		Last Modified: Tue, 17 Mar 2026 01:39:38 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:016e7be995c4b2e644e24cd8f6c53ddb00c9031c358699427d10bac41fcdc22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df3a93850dd92cce14a5c095cabdac43aa4c2f8ebf5a2c52103d5e948c83f29a`

```dockerfile
```

-	Layers:
	-	`sha256:ad8d87fd71b8ca4613fb1aad11ecda70df15c75210e19ff5983e58fa9770a33c`  
		Last Modified: Tue, 17 Mar 2026 01:39:37 GMT  
		Size: 2.3 MB (2310587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94a0435bb1d6c40bfe6d6b5b90d7c15528dddc8ecc3b5a7efbe1a909f8bc727d`  
		Last Modified: Tue, 17 Mar 2026 01:39:36 GMT  
		Size: 17.6 KB (17617 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:core` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:63ea1e59b44f904a50bb2ca5c7fb9f9a8bb22a3c7a5c0587fbc707f7a2971db7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110135104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:341d195bbed7114c685d729af960d2fa3d95a56c3b8e8e702db8f68942e96dc8`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:40:06 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 17 Mar 2026 01:40:06 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 17 Mar 2026 01:40:13 GMT
ENV INFLUXDB_VERSION=3.8.3
# Tue, 17 Mar 2026 01:40:13 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-core-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 17 Mar 2026 01:40:13 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:40:13 GMT
USER influxdb3
# Tue, 17 Mar 2026 01:40:13 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 17 Mar 2026 01:40:13 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 17 Mar 2026 01:40:13 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 17 Mar 2026 01:40:13 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Tue, 17 Mar 2026 01:40:13 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 17 Mar 2026 01:40:13 GMT
ENV LOG_FILTER=info
# Tue, 17 Mar 2026 01:40:13 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 17 Mar 2026 01:40:13 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 17 Mar 2026 01:40:13 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a5ff7761a3de3cfdfbde6b4aa7e485e10238103213ecb9db9c4609293d2faa6`  
		Last Modified: Tue, 17 Mar 2026 01:40:27 GMT  
		Size: 6.7 MB (6681856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1264b241981cfe9581d0ba6c743ec3b73bdbb1944e9081b0a022d4f407b473`  
		Last Modified: Tue, 17 Mar 2026 01:40:26 GMT  
		Size: 3.6 KB (3650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56a20c20f06dbbda1dd6a4ab1be0c7c77ea648b3965aba21c4e04af2c1a15a7`  
		Last Modified: Tue, 17 Mar 2026 01:40:28 GMT  
		Size: 74.6 MB (74579220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f703f18e65af6ac7ed5a6c75e70bd0a9e394f226f5ffc0e615d313f1202888`  
		Last Modified: Tue, 17 Mar 2026 01:40:26 GMT  
		Size: 520.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bbf9139ff50f89c76e18e8bd41cee3acb6e075925aa770b2ee60cc389321918`  
		Last Modified: Tue, 17 Mar 2026 01:40:28 GMT  
		Size: 149.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:core` - unknown; unknown

```console
$ docker pull influxdb@sha256:1aef9353b9015c5a38b910cffd2e48a199f9e96fcfdbf0bc40720e45c446f06e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df5730ad5f074116ae5eeafb6c90c912b8313fa502d86022540499653d7c2192`

```dockerfile
```

-	Layers:
	-	`sha256:8f0d054fc2be50c07051760fae65549046134b8a7433c570118936bbf76288b5`  
		Last Modified: Tue, 17 Mar 2026 01:40:26 GMT  
		Size: 2.3 MB (2311669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee9350556a6e72b07053ccdedca25c80c0a30574bf73055e22981b7a17094266`  
		Last Modified: Tue, 17 Mar 2026 01:40:26 GMT  
		Size: 17.8 KB (17766 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:data`

```console
$ docker pull influxdb@sha256:4f5d4e87b639278d39a7c06e32cba7e62f1de8c8f1fde4b8db4f053d53df4e62
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:data` - linux; amd64

```console
$ docker pull influxdb@sha256:d21e4988d37a6c1faa8baab25d27def33c754eb350a9b32279e180096f599646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115719726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c31a2127ab5486fbc8d5f74bf1f91ea58319df988e3a4fc8bcc9fb9a085b298`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:37:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:29:22 GMT
ENV INFLUXDB_VERSION=1.12.3-c1.12.3
# Mon, 16 Mar 2026 23:29:22 GMT
ENV INFLUXDB_PR=
# Mon, 16 Mar 2026 23:29:22 GMT
ENV INFLUXDB_PV=1.12.3-c1.12.3
# Mon, 16 Mar 2026 23:29:22 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"         "influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-data_${INFLUXDB_PV}_amd64.deb" &&     rm -r "influxdb-data_${INFLUXDB_PV}_amd64.deb.asc"           "influxdb-data_${INFLUXDB_PV}_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:29:22 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Mon, 16 Mar 2026 23:29:22 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 16 Mar 2026 23:29:22 GMT
VOLUME [/var/lib/influxdb]
# Mon, 16 Mar 2026 23:29:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 23:29:22 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Mon, 16 Mar 2026 23:29:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 23:29:22 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fa3468d221545a43d2151f3977695a31857f9342ba842627d03c9fa1b2ae02`  
		Last Modified: Mon, 16 Mar 2026 22:37:09 GMT  
		Size: 24.0 MB (24038304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11793f1b301015b6075c375d2ba0bb8a3b2156f963042752aebaef61a814ab21`  
		Last Modified: Mon, 16 Mar 2026 23:29:35 GMT  
		Size: 43.2 MB (43191068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976aed466c219d17ff192121e29a61c61b4b07b3af73e05e3f8122b9745cf77e`  
		Last Modified: Mon, 16 Mar 2026 23:29:33 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7721a85c674598c3887f132a5849c923eb1a39d9fc59d7db014f335e282f009`  
		Last Modified: Mon, 16 Mar 2026 23:29:33 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f6a089499d992dcda33b7b222b0cee38c4e8142d980d933eba3dff115db4de`  
		Last Modified: Mon, 16 Mar 2026 23:29:33 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:data` - unknown; unknown

```console
$ docker pull influxdb@sha256:1a36418d9366f8b3788d664ae9f2d6f908e613ba59a7a64a578bb7d4c141b9a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4707287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5574c09e06bdf3267b7dfd8a4b171badb6693dd4bfab7e44f630c20c60a1fff2`

```dockerfile
```

-	Layers:
	-	`sha256:417470ac9dfeac0c0842a7adc8f790420dc1145c0c1e60e4dcb2a1d01afa31aa`  
		Last Modified: Mon, 16 Mar 2026 23:29:34 GMT  
		Size: 4.7 MB (4693133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de8488ad860255ff7afdefbdd4e259397ab7bd5b900efa6d4c4fa45a2449a040`  
		Last Modified: Mon, 16 Mar 2026 23:29:33 GMT  
		Size: 14.2 KB (14154 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:data-alpine`

```console
$ docker pull influxdb@sha256:b00b5baa2231b78e2d7f36eb1a10e2d977f347b9881dbb417b29b6bdf5830a46
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:data-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:81a969bc16b9858dda59761bd5f64a9e845ca937d25c79bf19a7c2e5ef57d5d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47996785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0349bbaf083804873fbb03e5d51d6762630274c9fddcd6d18d97809096a67f24`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Sat, 14 Mar 2026 00:10:26 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Sat, 14 Mar 2026 00:10:31 GMT
ENV INFLUXDB_VERSION=1.12.3-c1.12.3
# Sat, 14 Mar 2026 00:10:31 GMT
ENV INFLUXDB_PR=
# Sat, 14 Mar 2026 00:10:31 GMT
ENV INFLUXDB_PV=1.12.3-c1.12.3
# Sat, 14 Mar 2026 00:10:31 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"         "influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     tar -xvf "influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz"         -C /usr/bin --strip-components 1 --wildcards             'influxdb-*/influx'             'influxdb-*/influx_inspect'             'influxdb-*/influxd' &&     rm "influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"        "influxdb-data-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     apk del .build-deps # buildkit
# Sat, 14 Mar 2026 00:10:31 GMT
COPY influxdb.conf /etc/influxdb/influxdb.conf # buildkit
# Sat, 14 Mar 2026 00:10:31 GMT
EXPOSE map[8086/tcp:{}]
# Sat, 14 Mar 2026 00:10:31 GMT
VOLUME [/var/lib/influxdb]
# Sat, 14 Mar 2026 00:10:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Mar 2026 00:10:32 GMT
COPY init-influxdb.sh /init-influxdb.sh # buildkit
# Sat, 14 Mar 2026 00:10:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Mar 2026 00:10:32 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68716dcc58a5f148c91121671bed51872ee14024f52511f4f27a30f76dce7229`  
		Last Modified: Sat, 14 Mar 2026 00:10:42 GMT  
		Size: 1.2 MB (1225267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a883869ba3b1cd65a45af9359b43f47d6fac6db9e734ab17670747476688a74`  
		Last Modified: Sat, 14 Mar 2026 00:10:43 GMT  
		Size: 43.1 MB (43126004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea75516ea6f5fc6e704f8a153c5006c341c6d15af305805fe5621cc87017a79`  
		Last Modified: Sat, 14 Mar 2026 00:10:42 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23204e84777414408f116926340ada07e4e53fd479fe293933fd5917377c5ef3`  
		Last Modified: Sat, 14 Mar 2026 00:10:42 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6db343d538c0cd30d0b117de9d02ef0c9964c7ddacb94c1d1548cd2251e8b6`  
		Last Modified: Sat, 14 Mar 2026 00:10:43 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:data-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:3cf5b433c5da545ad77ef2c05fbb248e11328258f17be899658ebe11101f2074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **796.7 KB (796739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89d8831c93eb5116260d6aa262a99b5340b8e251edae29efa3ffb935fd035cb7`

```dockerfile
```

-	Layers:
	-	`sha256:54c781f8f3995af817107aeefcc043140f26364ae6ce15fa46f4f2bfdfcbca44`  
		Last Modified: Sat, 14 Mar 2026 00:10:42 GMT  
		Size: 781.2 KB (781229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45e179ee50e5cfb1d3f337ad7930775e5df7f00e5978d5acd75cd3102bd71f6b`  
		Last Modified: Sat, 14 Mar 2026 00:10:42 GMT  
		Size: 15.5 KB (15510 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:enterprise`

```console
$ docker pull influxdb@sha256:659da4d6af9a37902819986a2fd489b0f6f2ed454e6822ebb7937ca99f2dbf56
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:enterprise` - linux; amd64

```console
$ docker pull influxdb@sha256:0068439a849d0a8a75d5bf31109518822189e0a91205428cc4dabbe07adbecad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128390942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e95f3a3854771047f8c42216606eedeede2dd0e6bd68ff406622594620b048`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:39:16 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 17 Mar 2026 01:39:17 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 17 Mar 2026 01:39:24 GMT
ENV INFLUXDB_VERSION=3.8.4
# Tue, 17 Mar 2026 01:39:24 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 17 Mar 2026 01:39:24 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:39:24 GMT
USER influxdb3
# Tue, 17 Mar 2026 01:39:24 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 17 Mar 2026 01:39:24 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 17 Mar 2026 01:39:24 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 17 Mar 2026 01:39:24 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Tue, 17 Mar 2026 01:39:24 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 17 Mar 2026 01:39:24 GMT
ENV LOG_FILTER=info
# Tue, 17 Mar 2026 01:39:24 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 17 Mar 2026 01:39:24 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 17 Mar 2026 01:39:24 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896f80de69282718f797c732aadcb5ad7cb525eba98ad4a175031054cf4c4e18`  
		Last Modified: Tue, 17 Mar 2026 01:39:40 GMT  
		Size: 6.7 MB (6671643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61664b8c9e70a8f737b8374de8a43c17a6e7ed951ea3405ae356ff8ac1504c2c`  
		Last Modified: Tue, 17 Mar 2026 01:39:37 GMT  
		Size: 3.6 KB (3650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1361daea27f76c6bf56c08ba7564ae65156ecb8e251185ccf018f686904d8a`  
		Last Modified: Tue, 17 Mar 2026 01:39:42 GMT  
		Size: 92.0 MB (91982987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4bd0ef6e31704dc021b0a98036ab976fb486d924c03223094882b49fc16927c`  
		Last Modified: Tue, 17 Mar 2026 01:39:40 GMT  
		Size: 521.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933f1bceff72da4ddca28a5cd3c12dfb8fcedcb2836202ab2c5ed2c96f3f2ed8`  
		Last Modified: Tue, 17 Mar 2026 01:39:40 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:1ea34b829420e68babbc9e10a485b40864a22cf629cca20295def1c06bc64d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2328432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf42083b11801171ad943480cd34dc1cefdae0725c8038f3efa8bfec30dcdf30`

```dockerfile
```

-	Layers:
	-	`sha256:26b0a0947e306cff33e0baf6ef78e411ba1dc193e9b5199f2a4c37878542d860`  
		Last Modified: Tue, 17 Mar 2026 01:39:40 GMT  
		Size: 2.3 MB (2310635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec22d992ae8949247335d9458549ad1e329d7740a6448e282ca6d1882ab71ab0`  
		Last Modified: Tue, 17 Mar 2026 01:39:40 GMT  
		Size: 17.8 KB (17797 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:enterprise` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:e71c1877459a80a96b782a6700ab975468ed7c160f8b8aba45d54011f06c2bbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (119034746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f99105f51447acc10566cad4da5c9dd93e87600aea5786c58c1b91b2deba254`
-	Entrypoint: `["\/usr\/bin\/entrypoint.sh"]`
-	Default Command: `["influxdb3","serve"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:40:28 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         ca-certificates         curl         gettext-base         gnupg         libssl3 &&     rm -rf /var/lib/apt/lists* # buildkit
# Tue, 17 Mar 2026 01:40:28 GMT
RUN groupadd --gid 1500 influxdb3 &&     useradd  --uid 1500 --gid influxdb3 --shell /bin/bash --create-home influxdb3 &&     mkdir -p /var/lib/influxdb3              /usr/lib/influxdb3              /plugins # buildkit
# Tue, 17 Mar 2026 01:40:35 GMT
ENV INFLUXDB_VERSION=3.8.4
# Tue, 17 Mar 2026 01:40:35 GMT
RUN case "$(dpkg --print-architecture)" in         amd64) ARCH=amd64 ;;         arm64) ARCH=arm64 ;;         *) echo 'Unsupported Architecture' ; exit 1 ;;     esac &&     curl -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"          -fsSLO "https://dl.influxdata.com/influxdb/releases/influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     tar --strip-components 1 -C /usr/lib/influxdb3 -xvf "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" &&     mv /usr/lib/influxdb3/influxdb3 /usr/bin/influxdb3 &&     chown -R influxdb3:influxdb3 /var/lib/influxdb3 /plugins &&     chown -R root:root /usr/lib/influxdb3 &&     rm  "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz.asc"         "influxdb3-enterprise-${INFLUXDB_VERSION}_linux_${ARCH}.tar.gz" # buildkit
# Tue, 17 Mar 2026 01:40:35 GMT
COPY entrypoint.sh /usr/bin/entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:40:35 GMT
USER influxdb3
# Tue, 17 Mar 2026 01:40:35 GMT
RUN mkdir ~/.influxdb3 # buildkit
# Tue, 17 Mar 2026 01:40:35 GMT
ENV INFLUXDB3_PLUGIN_DIR=/plugins
# Tue, 17 Mar 2026 01:40:35 GMT
ENV INFLUXDB3_DATA_DIR=/home/influxdb3/.influxdb3
# Tue, 17 Mar 2026 01:40:35 GMT
ENV INFLUXDB3_SERVE_INVOCATION_METHOD=docker-hub
# Tue, 17 Mar 2026 01:40:35 GMT
ENV INFLUXDB_IOX_DB_DIR=/var/lib/influxdb3
# Tue, 17 Mar 2026 01:40:35 GMT
ENV LOG_FILTER=info
# Tue, 17 Mar 2026 01:40:35 GMT
EXPOSE map[8181/tcp:{}]
# Tue, 17 Mar 2026 01:40:35 GMT
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
# Tue, 17 Mar 2026 01:40:35 GMT
CMD ["influxdb3" "serve"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c9b202493abf56134337b459be8acb07328c6f25892605d440c7f265df6a7b`  
		Last Modified: Tue, 17 Mar 2026 01:40:49 GMT  
		Size: 6.7 MB (6681738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4286e69af75bf4ff096601e07ac6fe12af7d7bccaa18225bb29036d2f2503c53`  
		Last Modified: Tue, 17 Mar 2026 01:40:49 GMT  
		Size: 3.7 KB (3653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35fff946bce4cefe39db32464b13a52437398b2f8c8bbe74de3121fc2127f368`  
		Last Modified: Tue, 17 Mar 2026 01:40:51 GMT  
		Size: 83.5 MB (83478973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c48ae972e761f8f9851eeed70d099301714e48a925d5b45dd64fbe150592c6`  
		Last Modified: Tue, 17 Mar 2026 01:40:49 GMT  
		Size: 523.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db91e6bd4f3aac338c3aab1210b06acfb137b4ae2fbf6ef74298b77b4d43a83`  
		Last Modified: Tue, 17 Mar 2026 01:40:50 GMT  
		Size: 150.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:enterprise` - unknown; unknown

```console
$ docker pull influxdb@sha256:5606f14d9173824d7f4dc14323f0db97097ef4ec2f886c3399be7055a68782bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a41e5b6195df8732b06f84032c50c76d3ee58f41e79e1fd31787622cbbefdd`

```dockerfile
```

-	Layers:
	-	`sha256:c2ef077fcbcf2aa087d7b258518807849f8bc051379a75b23bfb92e88b51d361`  
		Last Modified: Tue, 17 Mar 2026 01:40:49 GMT  
		Size: 2.3 MB (2311717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0071489710411d8fa4dd7b44c485227d6ceac8e7c15cd9cb0ac28ad1b57f52cb`  
		Last Modified: Tue, 17 Mar 2026 01:40:49 GMT  
		Size: 17.9 KB (17946 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:latest`

```console
$ docker pull influxdb@sha256:7500f5825d4cdda41befbafca3582ae606b984d33aa1aaf8ae22675dd12d8457
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:51f3627309df65b6d8614512df251c1a3b801de5ed0f1639b74dcaba5167ae86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107240564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1db8a8da9a075b06012bfe43abb0516f9fd5a243a9529acb5fbf0adc047e5706`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:41:32 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:41:33 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 16 Mar 2026 22:41:33 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Mon, 16 Mar 2026 22:42:05 GMT
ENV GOSU_VER=1.19
# Mon, 16 Mar 2026 22:42:05 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Mon, 16 Mar 2026 22:42:05 GMT
ENV INFLUXDB_VERSION=2.8.0
# Mon, 16 Mar 2026 22:42:05 GMT
ENV INFLUXDB_PR=-2
# Mon, 16 Mar 2026 22:42:05 GMT
ENV INFLUXDB_PV=2.8.0-2
# Mon, 16 Mar 2026 22:42:08 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 16 Mar 2026 22:42:08 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 16 Mar 2026 22:42:08 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 16 Mar 2026 22:42:09 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 16 Mar 2026 22:42:09 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 16 Mar 2026 22:42:09 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 16 Mar 2026 22:42:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 22:42:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 22:42:09 GMT
CMD ["influxd"]
# Mon, 16 Mar 2026 22:42:09 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 16 Mar 2026 22:42:09 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 16 Mar 2026 22:42:09 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 16 Mar 2026 22:42:09 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 16 Mar 2026 22:42:09 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df5fe2f66ea80fb2a2904ca93537ac51968560c5437a710e4a2dbf9c6eb7577`  
		Last Modified: Mon, 16 Mar 2026 22:41:54 GMT  
		Size: 9.8 MB (9798253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67415bd2cacb12eefe1400623e7905284a37a8af821b4eb631092ca45e2df0f4`  
		Last Modified: Mon, 16 Mar 2026 22:41:54 GMT  
		Size: 6.2 MB (6156982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3655afae3b0a2802422d8c883d738f92fd775ebb1f500faff27aab0e7340849f`  
		Last Modified: Mon, 16 Mar 2026 22:41:54 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9325aa6fcb1cc238376ef01f3a219658720af41ae657788508a613f7a7a7a77c`  
		Last Modified: Mon, 16 Mar 2026 22:42:19 GMT  
		Size: 811.5 KB (811474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9cd1ff3a1e20994f2652d352e1bd2c61bbaed4601c4aeb0e0f30efa50873e6a`  
		Last Modified: Mon, 16 Mar 2026 22:42:21 GMT  
		Size: 50.5 MB (50451818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ca28afa0e9f842e0bc2ee9d275d2ded12eb174358e33a23a3807d42eaa7a89`  
		Last Modified: Mon, 16 Mar 2026 22:42:20 GMT  
		Size: 11.8 MB (11775857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e5068d62cc59afe0d0c9e8ddf71cd64282ca6623f9bf9676fea89b79e506bc`  
		Last Modified: Mon, 16 Mar 2026 22:42:19 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f8645d360e4540fcc478073a5ed2390b01563ca6b28faf4fef20310627f5dd`  
		Last Modified: Mon, 16 Mar 2026 22:42:20 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd7ac48b4a1dd229ee92f630b36400f7931dc9d788b82f9e807b01d6102c64c`  
		Last Modified: Mon, 16 Mar 2026 22:42:20 GMT  
		Size: 6.3 KB (6287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:494269a08b389ddc2b1f2492fbf4b390bff9651c2277953ef1bd6c986907cbcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0fb69034a80b413147e9d25c385d3371a1de9f9fb9afe74658d1fb69070c1cc`

```dockerfile
```

-	Layers:
	-	`sha256:cba10e6f7b4c27e5ef10053adb4892794bc8cd3fb4c2c6f68cfb84dd2c1f797b`  
		Last Modified: Mon, 16 Mar 2026 22:42:19 GMT  
		Size: 2.9 MB (2934237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb8023ab021ed7474ff326bb8e15ba5f2ec39b0b1405d4bed281f484cfe977e5`  
		Last Modified: Mon, 16 Mar 2026 22:42:19 GMT  
		Size: 33.6 KB (33619 bytes)  
		MIME: application/vnd.in-toto+json

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:03aed0dc19b956f0e99b20abced161b88711c5aee5a5674f736bb8e501b601e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103639567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f0119106920d2e2ddb3b92de00996cb93773333bc44a0a76abe7c1ab5518b12`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:43:32 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&     apt-get update -y &&     apt-get install -y --no-install-recommends       ca-certificates       curl       gnupg &&     apt-get clean &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:43:33 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     curl -fL "https://github.com/TomWright/dasel/releases/download/v2.8.1/dasel_linux_${arch}.gz" | gzip -d > /usr/local/bin/dasel &&     case ${arch} in       amd64) echo '21fda0a4dc3c779c42737eca4b37e4f187d7ab91ba6301eed97b801af84a9ea2  /usr/local/bin/dasel' ;;       arm64) echo '2c75e63f9884c37578f48788819dda5a5a5c32ec6c4a663eefc19839f44d6291  /usr/local/bin/dasel' ;;     esac | sha256sum -c - &&     chmod +x /usr/local/bin/dasel &&     dasel --version # buildkit
# Mon, 16 Mar 2026 22:43:33 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --create-home --home-dir=/home/influxdb --shell=/bin/bash influxdb # buildkit
# Mon, 16 Mar 2026 22:44:05 GMT
ENV GOSU_VER=1.19
# Mon, 16 Mar 2026 22:44:05 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       B42F6819007F00F88E364FD4036A9C25BF357DD4 &&     curl -fLo /usr/local/bin/gosu     "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}"          -fLo /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-${arch}.asc" &&     gpg --batch --verify /usr/local/bin/gosu.asc                          /usr/local/bin/gosu &&     rm -rf /usr/local/bin/gosu.asc &&     chmod +x /usr/local/bin/gosu &&     gosu --version &&     gosu nobody true # buildkit
# Mon, 16 Mar 2026 22:44:05 GMT
ENV INFLUXDB_VERSION=2.8.0
# Mon, 16 Mar 2026 22:44:05 GMT
ENV INFLUXDB_PR=-2
# Mon, 16 Mar 2026 22:44:05 GMT
ENV INFLUXDB_PV=2.8.0-2
# Mon, 16 Mar 2026 22:44:08 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/v${INFLUXDB_VERSION}/influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"                          "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     tar xzf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz" &&     cp "influxdb2-${INFLUXDB_VERSION}/usr/bin/influxd" /usr/local/bin/influxd &&     rm -rf "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz"            "influxdb2-${INFLUXDB_PV}_linux_${arch}.tar.gz.asc"            "influxdb2-${INFLUXDB_VERSION}" &&     influxd version # buildkit
# Mon, 16 Mar 2026 22:44:08 GMT
ENV INFLUX_CLI_VERSION=2.7.5
# Mon, 16 Mar 2026 22:44:09 GMT
RUN case "$(dpkg --print-architecture)" in       *amd64) arch=amd64 ;;       *arm64) arch=arm64 ;;       *) echo 'Unsupported architecture' && exit 1 ;;     esac &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys       24C975CBA61A024EE1B631787C3D57159FC2F927 &&     curl -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"          -fLO "https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     gpg --batch --verify "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc"                          "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" &&     tar xzf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz" -C /usr/local/bin ./influx &&     rm -rf "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz"            "influxdb2-client-${INFLUX_CLI_VERSION}-linux-${arch}.tar.gz.asc" &&     influx version # buildkit
# Mon, 16 Mar 2026 22:44:09 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2 # buildkit
# Mon, 16 Mar 2026 22:44:09 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 16 Mar 2026 22:44:09 GMT
COPY default-config.yml /etc/defaults/influxdb2/config.yml # buildkit
# Mon, 16 Mar 2026 22:44:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 22:44:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 22:44:09 GMT
CMD ["influxd"]
# Mon, 16 Mar 2026 22:44:09 GMT
EXPOSE map[8086/tcp:{}]
# Mon, 16 Mar 2026 22:44:09 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 16 Mar 2026 22:44:09 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 16 Mar 2026 22:44:09 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 16 Mar 2026 22:44:09 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8bc38a8ddd1b644c33c76658fc21da215f939ed706cf9758ecff41c7fa766fd`  
		Last Modified: Mon, 16 Mar 2026 22:43:54 GMT  
		Size: 9.6 MB (9626825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85aef8ec230715cef2dfb5ab2f9d156911cc7e29a1aa3ce7570d7ccf30dc09d6`  
		Last Modified: Mon, 16 Mar 2026 22:43:54 GMT  
		Size: 5.8 MB (5790426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96446248fc0ab026e9db2728cbbe0c168ecfaf223b7253b5653ebe8590bb829c`  
		Last Modified: Mon, 16 Mar 2026 22:43:54 GMT  
		Size: 3.2 KB (3225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbdd5dab386f405de61904714e628f34d6c839314755f61bd0ae62533ed300d`  
		Last Modified: Mon, 16 Mar 2026 22:44:19 GMT  
		Size: 766.4 KB (766373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43a4e1a3f57fc3b933998f99b1ddfbfbce740345b5676fcf938b36dbc69d68e`  
		Last Modified: Mon, 16 Mar 2026 22:44:21 GMT  
		Size: 48.2 MB (48229520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7aeaee757e728fb309c098b8808f34cc0740ee723f01c9ff01bf6923c565587`  
		Last Modified: Mon, 16 Mar 2026 22:44:20 GMT  
		Size: 11.1 MB (11100406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1b35bbe459cc568dffacf1b5ba0d18eca3847c48b1de232ee08a337b85d907`  
		Last Modified: Mon, 16 Mar 2026 22:44:19 GMT  
		Size: 209.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d86454bcba2acfb4eaa197367d866b3b7ddbfde85ab7de66fbe8f264a3dc00`  
		Last Modified: Mon, 16 Mar 2026 22:44:21 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939d5a79753c407ac035243984ba4f00cf508b96e906f6f22e05b2312f294936`  
		Last Modified: Mon, 16 Mar 2026 22:44:21 GMT  
		Size: 6.3 KB (6285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:latest` - unknown; unknown

```console
$ docker pull influxdb@sha256:a97a089cc73e56e7ed298f2da153f9507a717aced7f64b9276f4fd211484ba3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2967532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6439137c2c566d8b0f8f91636ff4299f7ac662a77417ce70694f3a1bd9367b7a`

```dockerfile
```

-	Layers:
	-	`sha256:489ffdb6f86c2603567f3ced9380add2b2e47c467d83a243fd27c88a95ece61d`  
		Last Modified: Mon, 16 Mar 2026 22:44:20 GMT  
		Size: 2.9 MB (2933717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cce9d0d3799e339d314382a0a5840b2814e7b2eed13987b113cf402fcf30ac5`  
		Last Modified: Mon, 16 Mar 2026 22:44:19 GMT  
		Size: 33.8 KB (33815 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:meta`

```console
$ docker pull influxdb@sha256:d619226068a33387766eff93fa2815efadcb0c64ee36d4fdf7f2afa85e5584b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:meta` - linux; amd64

```console
$ docker pull influxdb@sha256:105f922f373e05fe5be8b3bf03636011fb5eba13b6233319283e68f0f5b771ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91912637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68476159aed012d339094890fe575caf708d10faa17d07b80bd9febfafd4ba49`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:37:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:29:41 GMT
ENV INFLUXDB_VERSION=1.12.3-c1.12.3
# Mon, 16 Mar 2026 23:29:41 GMT
ENV INFLUXDB_PR=
# Mon, 16 Mar 2026 23:29:41 GMT
ENV INFLUXDB_PV=1.12.3-c1.12.3
# Mon, 16 Mar 2026 23:29:41 GMT
RUN curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"         "influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     export DEBIAN_FRONTEND=noninteractive &&     apt-get update &&     apt-get install --no-install-recommends -y         "/influxdb-meta_${INFLUXDB_PV}_amd64.deb" &&     rm -r "influxdb-meta_${INFLUXDB_PV}_amd64.deb.asc"           "influxdb-meta_${INFLUXDB_PV}_amd64.deb"           /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:29:41 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Mon, 16 Mar 2026 23:29:41 GMT
EXPOSE map[8091/tcp:{}]
# Mon, 16 Mar 2026 23:29:41 GMT
VOLUME [/var/lib/influxdb]
# Mon, 16 Mar 2026 23:29:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 16 Mar 2026 23:29:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Mar 2026 23:29:41 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fa3468d221545a43d2151f3977695a31857f9342ba842627d03c9fa1b2ae02`  
		Last Modified: Mon, 16 Mar 2026 22:37:09 GMT  
		Size: 24.0 MB (24038304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4cf91a29498481bcb2774753d32b947d34c8a875b4d0cc26467895c334f1dd`  
		Last Modified: Mon, 16 Mar 2026 23:29:51 GMT  
		Size: 19.4 MB (19385181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde80dcc1dfd5fc45df6e534c3d90d980adef9abe7e69f7d2aafb14bb57e17cb`  
		Last Modified: Mon, 16 Mar 2026 23:29:50 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07757a4b1133059e10be557710b3424182053781435a85154828461509909d2`  
		Last Modified: Mon, 16 Mar 2026 23:29:50 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:meta` - unknown; unknown

```console
$ docker pull influxdb@sha256:f6a096dcce18046c5b1651cd32ce175e5d9e06a6e3e3ff33cda518466c9231b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4605864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb53755f9f14c374e8e9def0c1f29d32cb98a7b920013ab90ca8cfed126a079e`

```dockerfile
```

-	Layers:
	-	`sha256:e3a4f4e37f0311efd3bc8e767984bd395128ab2484afddf5178d01159451a3d1`  
		Last Modified: Mon, 16 Mar 2026 23:29:50 GMT  
		Size: 4.6 MB (4593201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd9ce7dc3b27548f4a7c880147b540cd89bc6f24c0d36169433b8c194da686ad`  
		Last Modified: Mon, 16 Mar 2026 23:29:50 GMT  
		Size: 12.7 KB (12663 bytes)  
		MIME: application/vnd.in-toto+json

## `influxdb:meta-alpine`

```console
$ docker pull influxdb@sha256:0a051eaf780ce5a4e1d0bc51e7c16424b82219208822536392a61d77f4c527cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `influxdb:meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:5d3f5bc09690d58108cd11b610d1a4190f786a7bc800ae17751ced7c530ea4f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.2 MB (24200738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ba49e476e65f5ea7acf3c9b2e0c08890594b6e04c2dd7f2f369dd925062925`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Sat, 14 Mar 2026 00:11:06 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates # buildkit
# Sat, 14 Mar 2026 00:11:09 GMT
ENV INFLUXDB_VERSION=1.12.3-c1.12.3
# Sat, 14 Mar 2026 00:11:09 GMT
ENV INFLUXDB_PR=
# Sat, 14 Mar 2026 00:11:09 GMT
ENV INFLUXDB_PV=1.12.3-c1.12.3
# Sat, 14 Mar 2026 00:11:09 GMT
RUN apk add --no-cache --virtual .build-deps curl gnupg tar &&     curl -fsSLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"          -fssLO "https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys         24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify         "influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"         "influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     tar -xvf "influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz"         -C /usr/bin --strip-components 1 --wildcards             'influxdb-*/influxd-ctl'             'influxdb-*/influxd-meta' &&     rm "influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz.asc"        "influxdb-meta-${INFLUXDB_PV}_linux_amd64.tar.gz" &&     apk del .build-deps # buildkit
# Sat, 14 Mar 2026 00:11:09 GMT
COPY influxdb-meta.conf /etc/influxdb/influxdb-meta.conf # buildkit
# Sat, 14 Mar 2026 00:11:09 GMT
EXPOSE map[8091/tcp:{}]
# Sat, 14 Mar 2026 00:11:09 GMT
VOLUME [/var/lib/influxdb]
# Sat, 14 Mar 2026 00:11:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sat, 14 Mar 2026 00:11:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Mar 2026 00:11:09 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff222b2bc1735ef5ae68fbb3cd2555d5c9d167db3009d6ac7b76ffc0b64c953`  
		Last Modified: Sat, 14 Mar 2026 00:11:17 GMT  
		Size: 1.2 MB (1225264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84706419752f10f867a78117779b8e666144cfae465ae3bff03fead1a3d3aaf1`  
		Last Modified: Sat, 14 Mar 2026 00:11:17 GMT  
		Size: 19.3 MB (19331168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd86dc70a190dd7b913375552975c2652ab94591f2b2c476e3c95f5f7937b84d`  
		Last Modified: Sat, 14 Mar 2026 00:11:17 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00fac50404b2e130d37d058e96747807965ead40c44ecc2c3e0c6f11923cdae`  
		Last Modified: Sat, 14 Mar 2026 00:11:17 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `influxdb:meta-alpine` - unknown; unknown

```console
$ docker pull influxdb@sha256:547d60bfe06fa90ad6260c650a3774b3cc5a2e27f910aa0005926649448c72ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **696.0 KB (696015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:806c305f946ee74f2ee15815575ec4bf4caec2d242c42971eb8ee400298717a8`

```dockerfile
```

-	Layers:
	-	`sha256:bd2b90af63566b3d6c84fee2b1d16ffdab0305dcad16b98c31a186f832c7791e`  
		Last Modified: Sat, 14 Mar 2026 00:11:17 GMT  
		Size: 682.1 KB (682083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cac48257e4722c8ccb0f5993024e0cf6e88f5fccb58612457bd007afb71bd55`  
		Last Modified: Sat, 14 Mar 2026 00:11:17 GMT  
		Size: 13.9 KB (13932 bytes)  
		MIME: application/vnd.in-toto+json
